# JavaScript


[TOC]

synchronous vs asynch? vs ?


##### Comments

1. single line comments `//`
2. multi-line comments `/* */`


---

Browser objects include `Window`

*hoisting* applies to variable declarations (but not the assignment) and function declarations.


## JS Variables

The `window` object is *global object* and [window](https://developer.mozilla.org/en-US/docs/Web/API/Window/window) property (`window.window`) just points to the object itself, and properties of window object can be reached without having to prefix with `window.`. Global variables are properties of window (`myVar == window.myVar`)

? find citation about referencing ids as global?


review directly accessing id in global namespace!


## JS Functions

See [Named function expressions demystified](https://kangax.github.io/nfe/)

1. *named functions*
2. *function expressions* / can assign to unnamed/anonymous function (or named function expression if you also give function a name)
3. anonymous function - involved in function expressions, also can use as argument
4. as object methods...

Like this:

    // named function, function declaration
    function foo() {}
    
    // function expression or anonymous function definition
    (function() {alert('foo');})();
    var func = function() {}  

    // named function expressions
    var bar = function foo() {stuff;}  


Review how to use the variable method with `:` to define a function to call with dot notation...

closures! esp fact that *inner functions* have implicit access to outer function's scope! the outer function typically returns the inner function, then probably end up doing a function expression providing arguments to the outer function. The new function can then be called, effectively making the inner function accessible from outsider the declaring function.



Explain *execution context* and `this` syntax? why?

    event=function() {bar()}
    function bar() {..}


Look into the array-like `arguments` object associated with functions, as well as `apply()` and i think some other associated function.

Look into the that/why of callback functions (user defined).

*Closures*!

## JS Logic

? trinary, look this up

    x ? y : z


## DOM


Get `html` node by `document.documentElement`

#### HTML DOM Objects


* Document
* Elements
* Attributes
* Events
* Style


* Window `window` / global browser object, root of DOM
    * `window.screen` property = `screen`
    * `window.document` property = `document` is the object to be rendered

can reference html element id's as `window.ID`, `window["ID"]`, etc. also like `document.body.firstChild`, `document.body.children[0]`, ...


##### Document Object (`document`)

Properties...

body ( i.e.`document.body`)

doctype

createElement("some_name), but must must insert with element.appendChild() or element.insertBefore()

getElementById()

getElementsByClassName()

getElementsByName() deprecated vfor getElementsById()?

getElementsByTagName()

querySelector()

querySelectorAll()


### Window

See [Window @ MDN](https://developer.mozilla.org/en-US/docs/Web/API/Window)

* `Window.screenX/screenY`
* `Window.scrollX/scrollY`


##### Element Object

appendChild()

attributes

getElementsByClassName()

getElementsByTagName()

id

innerHTML



#### Element Properties

`scrollLeft/scrollTop`, can read or set, commonly used as `document.body.scrollTop`, compare to `window.scrollX/scrollY`?


---

## Events

https://www.w3.org/TR/DOM-Level-3-Events/#event-flow

listeners

Three possible *event phases* along the *propagation path*:

1. capture phase
2. target phase
3. bubble phase

Note: parameter to addEventListener defaults to `true` meaning listen for event during bubble phase, use `true` to listen on capture. Note `event.stopPropagation()`.

Read about throttle and debounce, especially for scroll and resize events, and see how to do w/o jQuery!

See:

* [Event @ MDN](https://developer.mozilla.org/en-US/docs/Web/Events)
* [Event developer guide @ MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/Events)
* [UIEvent @ MDN](https://developer.mozilla.org/en-US/docs/Web/API/UIEvent)

// these two 
window.onload = myFunction;
window.onload = function() {myFunction()};

// 
window.onscroll
window.onresize


### Mouse Events

See [MouseEvent @ MDN](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent)

Used to be fairly inconsistent across browsers, but mostly converged.

* `mouseover/mouseout` (react to event bubbling), see `onmouseover` property
* `mouseenter/mouseleave` (do not react to event bubbling)


##### Mouse Buttons

* `event.button` $\in\{0, 1, 2\}$
* `event.which` $\in\{1, 2, 3\}$, not on older IE
* `event.buttons` $\in\{0, 1, 2\}$

Possible way to test:
    
    // from http://eloquentjavascript.net/14_event.html
    function buttonPressed(event) {
        if (event.buttons == null)
            return event.which != 0;
        else
            return event.buttons != 0;
    }

Or here's an ides from [here](http://www.unixpapa.com/js/mouse.html):

    if (event.which == null)
        /* IE case */
        button= (event.button < 2) ? "LEFT" :
            ((event.button == 4) ? "MIDDLE" : "RIGHT");
    else
        /* All others */
        button= (event.which < 2) ? "LEFT" :
            ((event.which == 2) ? "MIDDLE" : "RIGHT");

It's a good idea to attach to mouseup


See [1](https://bl.ocks.org/mbostock/5247027)


##### Mouse Position

* `MouseEvent.screenX/screenY` screen coordinates
* `MouseEvent.clientX/clientY` window coordinates, experimental alias `MouseEvent.x/y` has partial support
* `MouseEvent.pageX/pageY` document coordinates

Note that there is also `window.screenX/screenY`

##### Onload Event

Detecting `DOMContentLoaded` event is current best practice to fire when DOM ready:
    

    // from https://developer.mozilla.org/en-US/docs/Web/Events/DOMContentLoaded
    document.addEventListener("DOMContentLoaded", function(event) {
      console.log("DOM fully loaded and parsed");
    });
    // some like to add false to fill in second argument
    // why did above use event?
    document.addEventListener('DOMContentLoaded', function() {
      alert("Ready!");
    }, false);

Note: detecting `load` event will wait for fully loaded page

In JQuery:

    $(document).ready(function() { /* code here */ });
    $(function() { /* code here */ });

Genrally speaking the onload event occurs when and object has been loaded.

Onload can specified in HTML:

    <element onload="myFunction()">

Or in JavaScript:

    object.onload = function(){myFunction()};

Or using addEventListener

It's most often used with the body element to execute a script once a web page and all its content (including images, scripts, css) has loaded. Possible that now bo

See discussion [window.onload vs document.onload](http://stackoverflow.com/q/588040/2762964)!

    body.onload 
    window.onload // all content!, same as document.body.onload?
    document.onload // when DOM is ready


What about `window.addEventListener('load', function() { }, false)`?


[]


## Etc

Coffeescript

TypeScript

Backbone.js/Underscore.js


getComputedStyle()
