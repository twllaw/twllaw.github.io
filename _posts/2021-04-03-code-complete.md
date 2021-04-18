---
title: "Code Complete: A Quick Glance"
date: 2021-04-18 00:00:00
category: tech-darts
description: "A quick look at Code Complete"
layout: tech-post
---
<div class="image-container">
    <img src="images/code-complete.jpeg" alt="Code Complete cover">
</div>

Many years ago I had decided to read this book called **Code Complete**. Written by [Steve McConnell](https://en.wikipedia.org/wiki/Steve_McConnell), it was first released in 1993, with a second edition that followed in 2004. This 960 page mammoth is widely considered as one of the best works on the topic of software development, so I thought to give it a shot, and I'm super glad that I did.

Back in the early stages of my career, I would look at the requirements for a task, then start hacking away code without giving it too much thought. As long as I was able to implement a feature or fix a bug, I could pat myself on the back on a job well done. Nothing else really mattered, right?

Code Complete really opened my eyes on the art of software construction. My approach and thought process with regards to coding had improved drastically, thanks to the variety of topics covered in this book. I truly felt that I knew how to write better code after reading, and that it had made me a better developer.

While the code snippets in the book are written in object-oriented languages like C++ and Java, there are many concepts that I feel are useful and very good to know regardless of what your language of choice is. Below are some key points from the book that won't take too much effort to incorporate when you are coding. Perhaps you are already doing some, if not most of these things!

## Routines

**(a.k.a. methods, functions)**

* Creating routines will reduce a program's complexity, improve readability and maintainability

* Code blocks that contain deep nesting are good candidates to be extracted into new routines

* Avoid duplicating code where possible

Ideally you would write a routine and have it called from various other places. Once you do that, any further changes can be updated in just one location, instead of two, or even more. This also helps during debugging sessions. If the logic is incorrect in one place, then you only need to fix it in one place.

* Create a good name for a routine that clearly describes what it does

Sometimes it also helps to further split up routines once they get too big. Abstracting logic away into well-named routines helps to document its purpose.

## Variables

* Initialise each variable close to where it's first used

This is the Principle of Proximity: keep related actions together. You can also be more certain that the variable hasn't been unintentionally modified after it was initialised.

* Declare each variable inside the smallest segment of code that needs it

Take it outside the code block only when it is necessary to expand the scope.

* Use each variable for one purpose only

I've seen JavaScript code where either a string or an object could be assigned to the same variable, and that gave me quite the headache! Just because you can do that, doesn't mean you should. It's better to use two different variables in this instance, as it will improve code clarity.

* Create descriptive variable names

Be as specific as possible. Avoid the likes of `x` and `i`, when you can use `count` or `index` instead.

* For booleans, give names that imply true or false

Putting a simple `is` in front of a boolean helps to make things obvious, e.g. `isValid` instead of `valid`. It is also good to avoid using negative names such as `notFound`, so you don't end up with the likes of `if (!notFound)`. Double negatives make things more complicated than it should be.

## Other stuff

* Avoid magic numbers and strings

Assign them to constants instead, it will make your job easier if those values were to change in the future, because you would then only need to update it in one place rather than several.

* Keep couplings loose

Tightly coupled code can be difficult to maintain, test and refactor, so it is ideal to keep modules loosely coupled instead.

* Make complicated expressions simple

If you have conditionals like the following:

```javascript
if (game.year <= maxYear && game.year >= minYear &&
  game.developer === developer && game.averageScore >= minScore) {
}
```
Consider putting the logic inside a variable, constant or even a routine, then use that instead:

```javascript
const isMatchingGame = game.year <= maxYear &&
  game.year >= minYear &&
  game.developer === developer &&
  game.averageScore >= minScore;

if (isMatchingGame) {
}
```
This will give the person reading the code a better picture of what the conditional is trying to achieve.

* Iterate

After creating a pull request, I like to look through my own changes and try to review objectively. Often times you will realise that certain improvements can be made, and that's even before sending the PR link to your colleagues.

* Refactor

While working on a piece of code, why not try to improve the quality of code while you're in there? Be careful not to go down the rabbit hole though, as major refactors should be worked on separately.

## Wrapping Up

As there are 35 chapters worth of material, what I've covered here is merely the tip of the iceberg. A kiddie pool compared to Code Complete's Mariana Trench, if you will. Other chapters of interest include testing, collaboration and even one's personal character.

As the book is quite old, not everything in here may be as relevant in 2021, though I believe the majority of topics are still useful to learn or revisit. The following is the role of the book as described by the author:

<div class="image-container">
    <img src="images/code-complete-role.png" alt="Role of Code Complete">
</div>

So if you're an engineer/developer/programmer/coder, Code Complete is a book I highly recommend reading.

[McConnell, Steve. Code Complete, Second Edition. Microsoft Press, 2004.](https://www.amazon.com.au/Code-Complete-Developer-Best-Practices-ebook/dp/B00JDMPOSY/ref=tmm_kin_swatch_0?_encoding=UTF8&qid=1618640367&sr=8-1)