# JavaScript Functions

## Defining Functions

* function declaration (function statement)
* function expression (incl. named function expressions and anonymous function expressions)
* arrow function expression (`=>`) --- ES6; doe not bind `this`!

I thought I'd written about these elsewhere but can't find it!


#### Function Declaration

A [function declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function) creates a `Function` object. Is hoisted.

    function name([param,[, param,[..., param]]]) {
      [statements]
    }



#### Function Expression

A [function expression](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function) can be stored in a variable. Use named function expression e.g. if you need recursion. Not hoisted.

    var myFunction = function [name]([param1[, param2[, ..., paramN]]]) {
      statements
    };


## Function Basics

function scope...

## Closures

Note `var that = this;` hack, and how to get around it using arrow functions! [ref](https://stackoverflow.com/q/4886632/2762964)

## Callbacks

Is there a difference of using anonymous functions or named functions? In terms of scope/closure?

## Questions

How does scope/closure apply to 
What if you define a callback in another function? Firebase vs html callbacks?
