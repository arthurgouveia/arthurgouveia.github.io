---
layout: post
title: 'Setting up your Ruby environment with RVM'
permalink: /2012/06/29/setting-up-your-ruby-environment-with-rvm
tweet: 'Setting up your Ruby environment with RVM'
description: 'A quick look into how you can make your Ruby development process smoother with RVM and manage your projects better'
keywords: 'Ruby on Rails RVM install setup mac os x linux development environment organize rubies gemset'
---

*"Shame on you! Almost two months and no new posts!"*

Yeah, I know. I kept asking myself what to write about and I always thought nobody would be interested in reading so I kept postponing forever and ever.

Well, it ends today (assuming this is somehow useful and interesting). Now let's get down to business.

##RVM: WTF is it and WTH am I going to do with it?

Well, RVM stands for Ruby Version Manager. The name is pretty self explanatory, but it is basically a tool that will allow you to install several Ruby versions on your computer and use different versions for different purposes, at your will. It will allow you to work in different projects that use different Ruby versions easily and also create a set of Gems for each project, preventing you from having one single Ruby install with a ton of gems from your 21857 unfinished pet projects.

*Note: I'm not going to be covering RVM setup on Windows. If you're doing Web Development on Windows, refer to <a href="http://gifsoup.com/webroot/animatedgifs/1057764_o.gif" target="_blank">here</a>, <a href="http://clipservideos.com/files/photos/13349992923642ae_l.gif" target="_blank">here</a> or <a href="http://www.threadbombing.com/data/media/54/000fs937.gif" target="_blank">here</a>. Thanks.*

##Installing RVM

I'll be assuming you're reading this because you already have at least one version of Ruby on your computer and that you have [curl](http://curl.haxx.se/) up and running. You simply run this in your preferred Terminal/Console application:

<code class="prettyprint">curl -L https://get.rvm.io | bash -s stable</code>

This will install the latest stable release of RVM on your computer. If you're not running as root, it should be installed in your home directory ~/.rvm

##Messing up with RVM

Now that you have RVM installed, you need to install Ruby versions. Want **rvm** to **list** the **known** versions? Suppa hard:

<code class="prettyprint">rvm list known</code>

Ask RVM for the requirements to install the version by typing:

<code class="prettyprint">rvm requirements</code>

Install a Ruby version:

<code class="prettyprint">rvm install 1.9.3</code>

Upgrading previously installed Rubies to newest versions:

<code class="prettyprint">rvm upgrade ruby-1.9.3-p120 ruby-1.9.3-p194</code>

Listing the current installed Rubies:

<code class="prettyprint">rvm list</code>

Changing Ruby versions:

<code class="prettyprint">rvm 1.9.3
rvm 1.8.7</code>

##Organizing your environment

Assuming you've been doing some Ruby/Rails work for a while and that some of the projects you've been working on have different Ruby versions and each one has different Gems (& versions) for it to run nicely, we will setup your environment so that when you **cd** into your project, RVM will automatically switch to the desired Ruby version and to a specific Gemset.

###Gemsets & Organization

Gemsets are, well, sets of gems. What it does for you is packing up all the gems you installed in a structure that RVM knows how to manage and switch whenever you need it.

If you have three projects in your computer and each one uses a different gem set but they are all running on the same Ruby version, here's what you should do (Terminal/Console):

<code class="prettyprint">rvm 1.9.3
rvm gemset create socialNetworkFacebookKiller groupBuyingInnovativeIdea yetAnotherBestCMSEva</code>

*Note: you can name your gemsets whatever you want. Does not need to be the name of your project*

Once you did that, you will have three different gemsets to work on your client's *awesome* ideas. Now you want to switch to a specific one because you know what you'll be working with

<code class="prettyprint">cd dev/socialNetworkFacebookKiller
rvm 1.9.3@socialNetworkFacebookKiller</code>

With this you'll be running Ruby **1.9.3** and on the Gemset **socialNetworkFacebookKiller**. Now you can run your *bundle install* and have all your gems installed only for this project. Repeat the procedure for the other projects to keep yourself organized and your environment clean.

To know what Gemset you're using, type:

<code class="prettyprint">rvm gemset name</code>

###Make it simpler with .rvmrc

This is a file that RVM will generate for you if you want and what it does is automagically switching to a Ruby version with a specific Gemset you defined for that directory it was created in!

<code class="prettyprint">cd dev/socialNetworkFacebookKiller
rvm \-\-rvmrc \-\-create 1.9.3@socialNetworkFacebookKiller</code>

Now you **cd** outside of this directory and **cd** inside of it again. You should be prompted if you want to use this rvm. Just answer yes and TADA! You will be running the desired Ruby version with the desired Gemset right after you **cd** on the directory

I hope you guys liked it and that it makes everything a bit easier on a day to day basis.

