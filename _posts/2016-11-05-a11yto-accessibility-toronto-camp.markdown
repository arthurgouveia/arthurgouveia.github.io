---
layout: post
title: '#a11yTO 2016 – Accessibility Toronto Camp notes'
tweet: '#a11yTO 2016 – Accessibility Toronto Camp notes'
description: 'Some notes I took from the talks I attended at #a11yTO'
keywords: 'accessibility, a11y, a11yTO'
tags: [a11y]
image: 'posts/a11y-to.jpg'
---

On November 5th, 2016, I attended to a super cool event full of brilliant people in Toronto: "#a11yTO - Accessibility Toronto Camp". Was super enlightening and at the same time great for validating some ideas and practices I've been acquiring/doing through my time working with accessibility. I figured that dumping the notes I got there would be a good thing for further reference, so here it is.

### Opening notes
- Focusing on getting value out of people participating.
  - Create evangelists - spread the word.
- a11yTO - largest a11y camp in the world
- There will be a conference on 2017
- Camp will be happening as usual, yearly, around the same time
- Next year, the meet-ups will be sort of made with a curriculum. Walk people through a11y through the year
- Conferences will be specially focused on training folks
- a11y is not only the right thing, not only legal obligation, is a force for positive change, source of new ideas and catalyst for innovation
- Government is highly interested into making an effort for a better a11y.
  - PM appointed the first "minister of a11y" and is personally involved on the efforts
- [Johnny Taylor](http://ajohnnytaylor.org/) - presented using a text reader. Interested to see he's using a MacBook.
  - Almost cried here. Big heart punch
  - Locked-in syndrome
  - a11y can be the difference between life and death in some cases
  - Maybe check for a11y testing availability, remote if that's the case

### Mobilizing Web Accessibility - [Seth Holladay](http://www.seth-holladay.com/)

- Packed. Not enough seats
- [sitecues](http://www.sitecues.com) - Bought by the JAWS company, apparently
- Wrong understanding that people with disabilities use Desktop over Mobile
- "Variation between device and OS is massive"
  - Slows the development process very much due to the lack of standards
- Operating environment plays a huge part on Accessibility. Glare on the screen, noisy metro, etc.
- "Assistive tech is VoiceOver or TalkBack, not JAWS or ZoomText"
  - VoiceOver is great at reading out the screen
  - Not as many people are familiar with the Android tools
  - Could not get why he stated that JAWS is not assistive tech but VoiceOver and TalkBack are
- Reactions to problems
  - 2/3 of people will use the website less or not at all if they find it hard to use
  - 1/3 will look for another competitor
- Over 90% of general public faces challenges with mobile websites
 - 66% occasionally
 - 23% regularly
 - 3% most of the time
- Difficulty to perform activities on the web
  - 47% of the people interviewed have trouble filling out a form
  - 34% clicking buttons/link
  - 27% reading a page
  - 26% finding info on websites
  - 21% completing a transaction
- Reasons for website challenges on smartphones
  - 40% Screen too small
  - 33% Controls not working
  - 28% Glare

### You Can’t Start a Fire Without a Spark! - [Mike Paciello](https://twitter.com/mpaciello)

- People pursue a11y because they are afraid of getting a lawsuit
- Sad truth that it is not about empathy
- Side note: amazing plain language skillz. OMG.
- "Great that there are so many compliance and lawsuits out there. Forces people"
- "Are compliance and lawsuits the big catalyst of attention to a11y?"
- "What if we prioritized people with disabilities when designing our products?"
- Huge issue on accessible employment scenario
- Accessibility should be a norm, a standard, a natural thing. We shouldn't need accessibility experts
- New a11y paradigm: Apple is the first logo there, along with Lainey Feingold, Oslo & Akershus and Teach access
  - Inside-out thinking
  - Teaching a11y "from birth", at universities, Norway
- Teaching Accessibility Initiative
 - Universities CS and degree programs
- There's isn't a lot of ROI into putting effort to a11y, so it's hard to convince people/companies
  - It's more about being inclusive. Being human
  - a11y goes out the window when thinking about revenue
- [An Accessible Design Maturity Continuum](http://uxfor.us/mature-it)
- Design guides are important for the newcomers
- Integrate a11y best practices into culture or development
- Publicly saying you're accessible or pushing towards that adds a lot of attention to the company
  - On the negative side, mostly. Lawsuits will follow
- Don't separate accessibility from usability
- "Disabilities community, blind users and such" is apparently not as divisive as many well known speakers use it comfortably
- Validated some of Shopify efforts on a11y testing of our products

### Technical Accessibility - [Marcy Sutton](http://twitter.com/@MarcySutton)

- axe-core - API, set of tools for a11y
- Build a11y on frameworks so everyone can benefit from it (Angular)
- [Accessible Wins blog](http://a11ywins.tumblr.com)
  - Value the wins. It's easy to trash talk the fails, but we need to encourage people.
- Accessibility code coverage
  - Add JS tests - Unit and Integration
- The New York Times
  - Major accessibility problems
  - Fixed the search form/controls on top bar
- The Globe and Mail
  - They are ok, but can do better
  - Fixed the log in modal

### I Never Knew a Website Could Hurt Somebody - [Karl Groves](http://twitter.com/@karlgroves)

- "A11Y is not only about blind users" - remembering us about this common misconception
- Chronic Pain (Fibromyalgia), the so neglected or misunderstood physical condition
  - "Attempting to interact with a poorly designed and inaccessible website can actually hurt users"
  - The National Pain Foundation old website was a HUGE pain for people without the disability, imagine for those with
- OAW -> Obvious Always Wins
- Interesting thing often neglected: alter the title tag if a form has errors, for instance
- The users' goals is what really matter
- Good design: convergence between creativity and capability

### Accessible & Usable Web Forms. Your How To Guide! - [Rabab Gomaa](https://twitter.com/RubysDo)

- Missed the first 3 minutes. So packed I didn't have good room to right anything although sitting
- Lots of examples on simple forms. Nothing new that we're not doing already on the Shopify Checkout #winning
- Some stuff was relying on semantic tags, which are not a viable solution for all apps. Checkout, for instance, needs to allow people to checkout nicely on IE6, so it's a no no to us at Shopify. The [WAI-ARIA](https://www.w3.org/WAI/intro/aria) stuff helps us get there, in any case

### Some comments I heard from a visually impaired user
- Hatred for JAWS
  - "Costly, old and new versions basically add bell sounds"
- Android - gotta be a freaking ninja to use it
- IOS - best screen reading, but the price makes it non accessible
- Government Sensus (CA) was really awesome
