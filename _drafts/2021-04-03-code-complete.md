---
title: "Code Complete untitled"
date: 2021-04-03 00:00:00
category: tech-darts
description: "Code Complete changed my life!"
layout: default
---
Quite some time ago, while I was stuck in a rut at a dead end job, I decided to read a book written by Steve McConnell called **Code Complete**. First released in 1993, with a second edition in 2004, this 960 page mammoth is widely considered as one of the best works on the topic of programming, so I thought to give it a shot...and I'm SO glad that I did. I'm not exaggerating when I say that it changed my life (as a developer)! At the very least it altered my career trajectory for the better.

Back in those days, I used look at requirements, then start hacking away code without giving it much thought. As long as I was able to implement a feature or fix a bug, I could pat myself on the back on a job well done. Nothing else really matters, right?

Code Complete really opened my eyes. My approach and thinking to coding changed drastically.

Easier nowadays with linters

While some concepts in the book are written specificly for object oriented languages, as well as other topics may not be very applicable in 2021, there are certain points that I feel are useful and very good to know, no matter what your language of choice is.

# Routines (a.k.a. methods, functions)

* Creating routines will reduce a program's complexity, improve readability and maintainability
* A good candidate to extract code into a routine is places with deep nesting
* Avoid duplicate code. Migrate common code into its own routine. Modify in one location instead of two or more. When debugging you only need to check one place
* Create a good name for a routine that clearly describes everything it does; Sometimes it helps to break up routines so that they each have stronger purposes and better names to accurately describe them. Abstract logic away into a well-named routine helps to document its purpose
* Simplifies complicated boolean tests

# Variables
* Ideally initialize each variable close to where it's first used, when you are reading code it's a lot easier than having to scroll up
* Declare each variable to be visible to the smallest segment of code that needs it; take it outside the block only when it is necessary
* Use each variable for one purpose; having more can cause confusion
* Create descriptive variable names! Be as specific as possible
* For booleans, give names that imply true or false
* Avoid magic numbers and strings, assign them to constants instead, it makes people's jobs easier if that value is to change in the future

# Other stuff

* Keep couplings loose, it makes it easier to replace entire logic should the need arise
* Make complicated expressions simple, especially for conditionals, put that the logic in a boolean instead
* Forming boolean expressions positively
* Iterate, after creating a PR, I like to look through my own changes and try to 'review' objectively. Often times you realise potential improvements can be made, and that's even before sending the PR link to your colleagues 
* Refactoring, while working on a piece of code, why not try to improve the code while you're there? Be careful not going down the rabbit hole though
* Self documenting code - is everything well-named? does the routine name describe what it does? some parts of a routine could benefit from being put into its own routine. Variables need to have good names too; named constants instead of magic numbers and strings. Minimise nesting. Make sure the code is straight forward, avoid 'cleverness'. When adding comments, make sure it's good information

As there are 35 chapters worth of material, what I've covered here is barely the tip of the iceberg. Other topics of interest include testing, collaboration and personal character. If you haven't read it yet, I highly recommend Code Complete.

McConnell, Steve. Code Complete, Second Edition. Microsoft Press, 2004.