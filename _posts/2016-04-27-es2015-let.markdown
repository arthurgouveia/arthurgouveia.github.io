---
layout: post
title: 'ES2015 tl;dr; - using let'
tweet: 'ES2015 tl;dr; - using let'
description: 'One of the series of short posts on ES2015 usage'
keywords: 'front-end, javascript'
tags: [front-end, javascript]
---

This is the first of a series of short posts on ES2015 (aka ES6). Starting from the basics, we'll explore in a practical and objective manner how to use `let`.

It's been quite some time since I wrote anything on the blog and I'm going to try, again, to get back at writing. The initial goal is not hairy and I'm aiming at 1 post every couple weeks. Hopefully it will become a **combo** and I'll be pushing myself not break the streak.

Off to work.

### DRY - Don't Repeat Yourself

This is for real on `var` vs `let`. It won't allow you to redeclare it and throw an error if that's ever the case.

    var coolBand = 'Bee Gees';
    var coolBand = 'Baha Men';
    // Works and console.log(coolBand) outputs 'Baha Men'

    let theDogsOut = 'woof woof woof';
    let theDogsOut = 'meow meow meow';
    // Dogs don't meow and let won't let (haha) you redeclare a variable on the same scope
    // Throws: Uncaught SyntaxError: Identifier 'theDogsOut' has already been declared

BUT, if you have another scope, you may do so, because `let` will only **hoist** the variable to the closest block:

    let theDogsOut = 'woof woof woof';
    let geneticallyModifiedDogs = true;

    if (geneticallyModifiedDogs) {
      let theDogsOut = 'meow meow meow';
    }

    console.log(theDogsOut);
    // Outputs 'woof woof woof' because let is scoped in the if block
    // If we replaced let for var in all instances, then the dogs would meow

### Don't `let` the `var` hoist

Hoisting, to sum up, is the process of "kickstarting" your variables, moving them to the very top of the declaration block via magical procedures of computer sciences. Check this code:

    function getTearFromHero(hero) {
      if (hero === 'Batman') {
        var dcVillain = 'Dad joke';
        // do something
      } else if (hero === 'SpiderMan') {
        var marvelVillain = 'Famous rice brand';
        // do something
      }
      console.log(dcVillain);
      console.log(marvelVillain);
    }

    getTearFromHero('Batman');
    // Outputs: 'Dad joke' and undefined

    getTearFromHero('SpiderMan');
    // Outputs: undefined and 'Picture of mom'

We get **undefined** logged (instead of a reference error) because those variables were hoisted to the top as if the code was written like this:

    function getTearFromHero(hero) {
      var dcVillain, marvelVillain;
      if (hero === 'Batman') {
        dcVillain = 'Dad joke';
        // do something
      } else if (hero === 'SpiderMan') {
        marvelVillain = 'Famous rice brand';
        // do something
      }
      console.log(dcVillain);
      console.log(marvelVillain);
    }

This is very likely to lead to weird or unnexpected behaviours, and it's easily fixed/assured with `let` (we wanted it to break):

    function getTearFromHero(hero) {
      if (hero === 'Batman') {
        let dcVillain = 'Dad joke';
        // do something
      } else if (hero === 'SpiderMan') {
        let marvelVillain = 'Famous rice brand';
        // do something
      }
      console.log(dcVillain);
      console.log(marvelVillain);
    }

    getTearFromHero('Batman');
    // Breaks: 'Uncaught ReferenceError: dcVillain is not defined'

    getTearFromHero('SpiderMan');
    // Doesn't even run :sad_panda:

Also, don't try to use a variable defined with `let` before defining it. It gets hoisted, but into a so called **Temporal dead zone** before the actual usage/definition, and you'll get a `ReferenceError`.

### Don't `let` it iterate `for` good

Sometimes `for`s can behave weirdly in JavaScript:

    function slowTicketPrinter(listOfNames) {
      for(var i = listOfNames.length - 1; i >= 0; i--) {
        // Just **imagine** printers are not super fast in 2016
        setTimeout(function() {
          console.log('Ticket for ' + listOfNames[i] + ' was printed.');
        }, 1000);
      }
    }

    slowTicketPrinter(['John Snow', 'Ned Stark', 'Arya Stark']);
    // Outputs 'Ticket for undefined was printed.' three times

This will happen because `i` will be hoisted to the very top and every asynced callback will reference it instead of something that belonged solely to that execution block. Using `let` saves us from that:

    ...
    for(let i = listOfNames.length - 1; i >= 0; i--) {
    ...
    slowTicketPrinter(['John Snow', 'Ned Stark', 'Arya Stark']);
    // Outputs 'Ticket for John Snow/Ned Stark/Arya Stark was printed.'

Yeah, we could `.bind` that function with the correct param, but... really?

### Not a global problem

Variables declared with `let` don't populate the global scope:

    var isAvailable = 'YOLO';
    let isNotAvailable = 'SCOPED';

    console.log(this.isAvailable)
    // Outputs 'YOLO'

    console.log(this.isNotAvailable)
    // Outputs undefined

Watcha think? Have you been using `let` for some time now? Got some experiences to share on the topic?
