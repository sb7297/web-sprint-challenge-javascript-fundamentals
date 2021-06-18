# Sprint Challenge - JavaScript Fundamentals

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in project. This Sprint explored JavaScript Fundamentals. During this Sprint, you studied array methods, this keyword, prototypes, and class syntax. In your challenge this week, you will demonstrate proficiency by completing a survey of JavaScript problems.

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the sprint challenge. 

_You have **three hours** to complete this challenge. Plan your time accordingly._


## Introduction

The index.js file contains all of your challenges. Please review it in full before answering the questions. If you complete the stretch goals please leave them in your file but commented out so that they do not affect the MVP tasks 

In meeting the minimum viable product (MVP) specifications listed below, you should have all tests passing. You can console.log to check your work and ensure you are submitting the correct results 

### Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your team lead as the evaluate your solution.

## Interview Questions
### (please edit this file and write your answer below each question. In addition, you may also review these questions with your mentor)
Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read.

1. Briefly compare and contrast `.forEach` & `.map` (2-3 sentences max)

Both `.forEach` and `.map` take a callback function which is executed once for
each element of the array. The difference is that `.map` automatically creates
and returns a new array made from the return values of the callback executed on
each element of the array, where `.forEach` does nothing with the callback's
return value and returns nothing.

2. Explain the difference between a callback and a higher order function.

A callback is a function that is passed in as an argument to another function.
A higher order function is a function that receives another function as an
argument or returns a function.
```js
function H(f, g, x) {
    return g(f(x)); 
}
```
In the above, `H` is a higher order function because it takes `f` and `g` as
arguments, and `f` and `g` are callbacks because they are passed in to `H` as
arguments.


3. Can you explain what a closure is and how you used it in the counter function? 

A closure is a function which "closes" over a variable that is in its
surrounding scope.
```js
function counter(initial) {
    let ret = function() {
        initial++;
        return initial;
    }
    return ret;
}

let cnt = counter(0);
console.log(cnt()); // 1
console.log(cnt()); // 2
```
In the above example, we pass in in `0` as `initial` to `counter`. Normally
the binding of `initial` to `0` would vanish after the execution of `counter`
finished, but since in this case we return a function out of `counter`, that
function "closes" over the values in scope when it is created and forces them
to continue existing for as long as it does.
We can see by executing `cnt` that it even preserves the value of the counter
across executions.
I did not use a closure in the sprint challenge, as it wasn't necessary.

4. Describe the four principles of the 'this' keyword.

 - If `this` is used in the global scope the user receives either the window object or the node console object depending on whether the execution environment is the browser or node.
 - If `this` is used inside a function that is called using dot notation, as in `obj.method()`, `this` refers to the object to the left of the dot. In the case of this example, that is `obj`.
 - If `this` is used inside a constructor function (a function intended to be called using `new`), then `this` refers to the new object that is being created by the function.
 - If `this` is used inside a function that is being called using a method such as `.call` or `.apply`, then `this` refers to the object explicitly being passed to `.call` or `.apply`.

5. Why do we need super() in an extended class?

We must explicitly call the constructor of the parent object, because Javascript
won't do it for us. This way the child object retains all the properties of the
parent along with its own particular properties.

This is equivalent to `Parent.call(this, args)` in the constructor in the older
style of object-orientation.

You are expected to be able to answer questions in these areas. Your responses contribute to your Sprint Challenge grade. 

## Instructions

### Task 1: Project Set Up

Follow these steps to set up your project:

1. Fork the repo
2. Clone your forked version of the repo
3. cd into your repo and create a branch with your first and last name
NOTE: Tests will run for the JavaScript portion of this challenge only
4. open the terminal in your vs code and type `npm install`
5. next type `npm run test:watch` in your terminal
6. Complete your work making regular commits, once you have all your tests passing and you are ready to submit your work please see canvas for instructions on how to submit

### Task 2: Project Requirements

Your finished project must include all of the following requirements

#### Task A: Closure

This challenge takes a look at closures as well as scope. 
* [ ] Find this challenge in the index.js file. Read the instructions carefully!

#### Task B: Objects and Arrays

Test your knowledge of advanced array methods and callbacks.
* [ ] Find this challenge in the index.js file. Read the instructions carefully!

#### Task C: Prototypes

Create constructors, bind methods, and create cuboids in this prototypes challenge.
* [ ] Find this challenge in the index.js file. Read the instructions carefully!

#### Task D: Classes

Once you have completed the prototypes challenge, it's time to convert all your hard work into classes.
* Find this challenge in the index.js file. Read the instructions carefully!

In your solutions, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

### Task 3: Stretch Goals 

There are a few stretch problems found throughout the files, don't work on them until you are finished with MVP requirements! Please remember to comment out your stretch goals before you submit 

## Submission format

See Canvas for submission instructions 

