# JavaScript Objects

* [Working with objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
* [Introducing JavaScript objects](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects) including working with JSON

How to declare objects?

what about constructors?

Note that everything in JS is an object and objects inherit from other objects, not classes. So there are no classes per se, but ES6 does introduce `class` syntax.

one way is to define a class as a function, and use this, along the lines of

    function myClass(x, y) {
      this.x = x;
      this.y = y;
      this.display = function() {};
    }
    
    var thing = new myClass(1, 2);

Note that it is probablly better to declare methods as

    myClass.prototype.display = function() {};

You can also declare as object literals, but this creates a singleton (does not allow you to create instances):

    var thing = {
      x: 1,
      y: 2,
      display: function() {}
    }

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes
https://www.sitepoint.com/object-oriented-javascript-deep-dive-es6-classes/
https://scotch.io/tutorials/better-javascript-with-es6-pt-ii-a-deep-dive-into-classes

https://www.phpied.com/3-ways-to-define-a-javascript-class/



## Global Objects

Objects in the global scope (vs the *global object* returned by `this`, which in browsers is `window`).

* [Standard built-in objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects)

* Array
