---
layout: post
title: 'prettyCheckable: my first open-source, 7 days later'
permalink: /2012/10/01/prettyCheckable-my-first-open-source
tweet: 'prettyCheckable: my first open-source, 7 days later'
description: 'My experience on creating my first open-source project: prettyCheackble. What was great and why you should do the same'
keywords: 'prettyCheckable, jQuery, plugin, JavaScript, Style checkbox, Style radio, CSS radio checkbox'
---

Last week, on September 24th, I launched my first open-source project and also my first jQuery plugin: <a href="http://arthurgouveia.com/prettyCheckable" target="_blank">prettyCheckable</a>. In a nutshell, it replaces your radios and checkboxes for better looking ones with ease.

Today, seven days later, I'd like to share the experience I had on making it and express why you should do the same.

##The problem

I got this freelance job from a <a href="http://ilustrebob.com.br" target="_blank">friend</a> of mine who happens to be an awesome designer, and when I looked at the PSD, I saw this nicely designed checkbox. I liked it very much but I realized right away that I wouldn't be able to style it with simple CSS.

So I did some JavaScript & CSS and boom: a nice checkbox came to life. Freelance job finished, another one came. A new styled checkbox and also a radio. That's when I realized I should save myself some time and therefore make some more money by adding efficiency to my process. Of course, the cost was: I needed to invest time into building something flexible, maintainable and easily customizable.

##The motivation

As I said before, I knew that if I invested some time into building something more flexible, I could use it for many other situations like those and in the process save money by spending less time on the jobs to come.

And that's when it hit me that I should in fact take this opportunity to make something so nice that not only me, but any other web developer facing the same thing would be able to use without struggling and re-inventing the wheel. 

I also thought that as I had never built anything open-source, would be great to make this the first one and get some feedback from the developer community. 

This would make me see the bugs, code improvements, etc I didn't see at first. This would help me get feedback that would make my plugin a better one and therefore me a better developer by learning from it.

##The coding

As nerdy as it my sound, I **really** liked digging into a new approach to the problem and coding the best I could for the sake of making this plugin as easy, maintaineable and customizable as it could be. As I didn't measure time from the beginning since I was just making a one time thing for the first freelance job, so I'm not 100% sure about how much time I used in the process of making it.

The number that comes to my mind when I think back is around 15~20 hours, divided any random days and times. It was used for:

+ Improving the code I had previously done for replacing the inputs;
+ Researching & fixing problems with overwriting default behavior for HTML elements;
+ Adjusting the original design and creating the new colors;
+ Testing is on many browsers;
+ Making it a plugin with jQuery best practices;
+ Creating unit tests with Jasmine;
+ Creating a landing page.

Once I was done with most these items, I asked for code feedback from two very good developers who I happened to work with: <a href="http://twitter.com/PosAbsolute" target="_blank">Cedric Dugas</a> and <a href="http://twitter.com/cjoudrey" target="_blank">Christian Joudrey</a>. I came to know <a href="http://jqueryboilerplate.com/" target="_blank">jQuery Boilerplate</a> (thanks Cedric!), adjusted the code and got some review/fixes from them.

##The results

To this day, here's the status I have:

+ 1.888 people visited the <a href="http://arthurgouveia.com/prettyCheckable" target="_blank">prettyCheckable website</a>;
+ Twitter plugin reports 51 tweets;
+ Facebook plugin reports 59 likes;
+ <a href="https://github.com/arthurgouveia/prettyCheckable" target="_blank">GitHub Repo</a> got 26 stars, 2 forks and 105 downloads;
+ Got featured in at least 10 different websites jQuery&HTML related;
+ I got some new followers and met awesome people.

Aside from that, what I personally liked the most (besides how excited I was for making my first open-source), was the fact that because I had in mind this code would be seen and used by I lot of people, I forced myself to try to make it as simple as possible to use and as clear as I could to be modified, understood and extended by the open-source community.

##And why you should do the same

Personally, I believe that **feedback is fuel**. Whether is a positive or negative, knowing what you're doing right or wrong will make you a better person/professional.

Practicing your problem solving abilities will help you became a great developer, so why don't you try making it public and allow yourself to get some feedback on the process? The fact that you'll be going open-source might even motivate you to write better, re-analyze your code a bunch times and test like there's no tomorrow.

You'll also get your name out there and will meet great people too.

In my case, the amount of shares, visits, downloads, stars, etc, told me that I did something that people needed, liked and accepted, and that I was in the correct path. The few things I fixed told me that there were flaws that should not have been there, and that I should have tried to foresee problems a bit more.

I hope this gives you some insight, and maybe push you towards starting a new open-source project. I'm 100% sure you'll be thankful for doing so.