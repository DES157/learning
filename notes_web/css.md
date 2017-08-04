# CSS


? lists horizonal? inline-block/inline or 

overflow

[TOC]

---

- [CSS @Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS)

---

standard page widths, retina displays, breakpoints



##### Comments

    /* ... */


## CSS Syntax


A CSS *ruleset* consists of a *selector* and a *declaration block*. The declaration block contains 

    selector {
        property: value;
        ...
    }



Big ideas: display, position



### CSS Selectors

See [Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Selectors)

###### Multiple selectors

``

###### Basic Selectors

Selector | Syntax
---------|-------
Type | `elementname`
Class | `.classname`
ID | `#idname`
Universal | read up on!
Attribute | `[attr=value]`

###### Combinators

* descendant selector (space)
* child selector (>)
* adjacent sibling selector (+)
* general sibling selector (~)



* `:pseudo-class`
* `::pseudo-element`






comma?

    html,
    body {
        margin: 0;
    }



## Box Model

1. content
    * width:, height:, min:/max-width:/height:
2. padding
    * padding: ~ padding-left:/right:/top:/bottom:
3. border
    * border: ~ border-width:, border-style:, border-color:
4. margin
    * margin: ~ margin-top:/bottom:/left:/right:
        * check, but I think to use margin: auto you must set width

###### Properties

* box-sizing / how width and height of elements are calculated
    * content-box / css standard, content only
    * border-box / content+padding+border, exclude margin


## Layout

% sizing is relative to parent, but if parent not sized it's problematic, esp. with height, but width will probably work. setting width/height of html and body will allow setting 100%, but consider vw/vh/vmin/vmax

overflowing? read up on overflow css, and
- inline-block may work?
- wrapper overflow: hidden?


* float: (all elements) take out of flow!
    * none, left, right
* clear: (block-level)
    * none, left, right, both
* visibility:

* width:/height:
    * `<length>` / must have units!
        * relative
            * em
            * ex
            * ch
            * rem
        * viewport
            * vh
            * vw
            * vmin
            * vmax
        * absolute
            * px
            * mm (25.4mm=96px)
            * q
            * cm (2.54cm=96px)
            * in = 96px
            * pt (3pt=4px)
            * pc (6pc=96px)
    * `<percentage>`
    * `auto`
 

## Positioning

note: margin: auto; way of centering does not work with 


* position: (all elements)
    * static
        * default, in flow, can not specify top/bottom/left/right
    * relative ("relatively positioned element")
        * adjust from position in normal flow, leaving space
    * absolute ("absolutely positioned element")
        * take out of flow, specify position relative to closest positioned ancestor 
    * fixed ("absolutely positioned element")
        * take out of flow, position relative to viewport, does not scroll, also technically called absolutely positioned element


position | comments | top/bottom/left/right
---------|----------|----------------------
static   || no
relative || 
absolute | can **not** center by margin: auto; |
fixed    ||


>The top, right, bottom, and left properties specify the position of positioned elements.

>For absolutely positioned elements (those with position: absolute or position: fixed), it specifies the distance between the top margin edge of the element and the top edge of its containing block.

>For relatively positioned elements (those with position: relative), it specifies the amount the element is moved below its normal position.


    div {
        position: ?;
        top:
        bottom:
        left:
        right:
        height:
        width:
        background:
        }

absolute position takes out of flow, so not much sense to use it with display inline-block, absolute positioned elements automatically treated as inline. Note also `display: table`.

review: margins don't make much sense with absolute positioning (and I suppose fixed as well), althought I think they technically have them, also note that they do not collapse with other margins fwiw.


Negative margins: top/left pull element, bottom/right move succeeding elements.


## Text Sizing

`rem`s always relative to `font-size` of root (`<html>`), vs `em`s always relative to that of parent.

The `line-height` property

## CSS Fonts

The original way is with `@font-face` rule `font-family` property.

    @font-face

e.g.

    font: 400 16px/1.5 "Helvetica Neue", Helvetica, Arial, sans-serif;
        font-family: "Helvetica Neue",Helvetica,Arial,sans-serif;
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 1.5;
        font-size-adjust: none;
        font-stretch: normal;
        ...


## CSS Transitions and Animation

...


## Color

opacity normally is inherited by children, but if you want a transparent background with fully opaque children/text now in css3 on the container you can specify alpha with `rgba(r,g,b,a)`, alternatively you can style `thing::before` with rgba (look into how opacity combines with rgba if you use both! it seems that you can reduce either and still get full opacity on at least text.) the before technique may not suffer from inheritance since you are actually placing a child element! (i think should be absolutely positioned)  see https://codepen.io/spencermathews/pen/QdVNqj and some page that links to it.

---

Quirks

width/height

If you wish to set the height of an element which is the child of body then body must have an explictly set height. If you set 

    html, body { height: 100%; }

then things work. If all you want is body to take up full height then it's fine to set `body { min-height: 100%}`, but it seems that would still not allow children to be % positioned.

Another, perhaps preferred alternative, which still suffers from the issue of % positioning children, is:

    body { height: 100vh; }


There may be issues with overflow and scroll bars.

Note that html and body both default to width/height of auto.


From [height @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/height) :

> The percentage is calculated with respect to the height of the generated box's containing block. If the height of the containing block is not specified explicitly (i.e., it depends on content height), and this element is not absolutely positioned, the value computes to auto. A percentage height on the root element is relative to the initial containing block.

What does that last sentence mean?

review viewports and html and body heights!

Read and summarize these:

height: http://stackoverflow.com/q/6654958/2762964
width: http://stackoverflow.com/q/15095833/2762964
https://www.kirupa.com/html5/make_body_take_up_full_browser_height.htm
https://jssnippets.wordpress.com/2016/04/05/tutorial-why-htmlbody-height100-is-required-for-div-height100-to-work/

body { width: auto; } ?

See using min-height on body, and quirks.

Quick that height is treated somewhat differently than width, exp wrt parent element sizing.

body { height: 100vh; } may help expand page? maybe min-height: 100vh?

Note that `position: absolute` can influence whether/how % will work.


background-color

Basically, if you set `background-color` in `body` then it propagates up to `html`, but if you set it also in `html` then there will be a distinction.

Note: `html` is the root element of HTML5.

http://stackoverflow.com/q/10947541/2762964

https://drafts.csswg.org/css-backgrounds-3/#special-backgrounds
