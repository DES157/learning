# HTML Styling

* [HTML Styles](http://www.w3schools.com/html/html_styles.asp)

## Style Attributes

    style="property:value;"

The property is a CSS property. The value is a CSS value.

## CSS Properties

* `color`
* `opacity`
* `font-familiy`
* `font-size`
* `text-align`

        text-align: left|right|center|justify|initial|inherit;

##### Backgrounds

See [CSS Backgrounds](http://www.w3schools.com/css/css_background.asp) and [CSS3 Backgrounds](http://www.w3schools.com/css/css3_backgrounds.asp).

The background of an element is the total size of the element, including padding and border (but not the margin). Can apply to elements, including `body`.

Note: you can specify multiple background images!

    background	Sets all the background properties in one declaration (any order)
    background-attachment	Sets whether a background image is fixed or scrolls with the rest of the page
    background-color	Sets the background color of an element
    background-image	Sets the background image for an element
    background-position	Sets the starting position of a background image
    background-repeat	Sets how a background image will be repeated

In the DOM, acess `background` property of the document as `document.body.style.background`, or for an element as `Element.background`. Also e.g. `backgroundColor`, `backgroundPosition`, etc.

* `background-position`

        background-position: value;
        
    Specify value pairs of `left/right/top/bottom`, `%x %y`, or `xpos ypos` (in _CSS units_). If only one specified the other defaults to `center`, `50%`, `50%` respectively. Default is `background-position: 0% 0%` which is top left corner.

* `background-attachment`

        background-attachment: scroll|fixed|local|initial|inherit;
        
        scroll  The background scrolls along with the element. This is default
        fixed   The background is fixed with regard to the viewport
        local   The background scrolls along with the element's contents
        initial Sets this property to its default value. Read about initial
        inherit Inherits this property from its parent element. Read about inherit


    

##### New CSS3 Background Properties
    
    background-clip	Specifies the painting area of the background
    background-origin	Specifies where the background image(s) is/are positioned
    background-size	Specifies the size of the background image(s)
    initial

Note: can now have more than one image.

* `background-size`


        background-size: auto|length|percentage|cover|contain|initial|inherit;

    With `cover` the background image will scale to cover the entire content area, keeps the aspect ratio (some part of the background image may be clipped).
    
##### sort these
    
* `text-decoration`
* `line-height`
* `initial`

##### Layout

See [CSS Box Model](http://www.w3schools.com/css/css_boxmodel.asp).

1. content
2. padding
3. border
4. margin

![box model](http://www.w3schools.com/css/box-model.gif)

* `width` / `max-width` - use `max-width` to adapt to smaller screens! Does not include padding, borders, or margin!

        width: auto|value|initial|inherit;
    
* `height`

* `padding` - white space between element content and border
* `margin` - default 0, size of white space outside the border.

        margin: length|auto|initial|inherit;

##### Visibility

* `display` - `none | inline | block | inline-block | ...`

    1. `none` (hides, does not take up room unlike `visibility: hidden`)
    2. `inline` (default of _inline_ elements)
    3. `block` (default of _block-level_ elements)
    4. `inline-block` elements are like inline elements but they can have a width and a height.

* `visibility` - still affects layout regardless of visibility!


        visibility: visible|hidden|collapse|initial|inherit;

?
* `text-decoration`

##### Floating Layout

The elements after a floating element (e.g. `float: left`) will flow around it, unless you clear (`clear: left`) the following element. Using `display: inline-block` instead of `float: left` is the new way, and does not require a clear for the element after.

* `float` (default `none`)

        float: none|left|right|initial|inherit;
    
    Note: setting e.g. `float: left/right` will implicitely set `display: block`.
    
* `clear`

        clear: none|left|right|both|initial|inherit;

* `overflow` / `overflow-x` / `overflow-y`

##### Borders

* `border` - shorthand for following
    - `border-style`
    - `border-width`
    - `border-color`

##### CSS3

* `border-radius`

##### Outline

Not part of the box model! Unike borders they don't take up space and can be non-rectangular.

> An outline is a line that is drawn around elements (outside the borders) to make the element "stand out".
>
> However, the outline property is different from the border property - The outline is NOT a part of an element's dimensions; the element's total width and height is not affected by the width of the outline.
> 

* `outline`

        outline: outline-color outline-style outline-width|initial|inherit;

    - `outline-color`	Specifies the color of the outline
    - `outline-style`	Specifies the style of the outline
    - `outline-width`	Specifies the width of outline

See [CSS Outline](http://www.w3schools.com/css/css_outline.asp).

##### Positioning

* `position`

        position: static|absolute|fixed|relative|initial|inherit;
    
    Static positioned elements are not affected by the top, bottom, left, and right properties. A "positioned" element is one whose position is anything except static.
    Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position.
    An element with `position: fixed`; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.
    An element with `position: absolute`; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).

However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

        static	Default value. Elements render in order, as they appear in the document flow
        absolute	The element is positioned relative to its first positioned (not static) ancestor element
        fixed	The element is positioned relative to the browser window
        relative	The element is positioned relative to its normal position, so "left:20" adds 20 pixels to the element's LEFT position

    
See [The position Property](http://www.w3schools.com/css/css_positioning.asp) and [CSS position Property](http://www.w3schools.com/cssref/pr_class_position.asp)

* `z-index`

    The z-index property specifies the stack order of an element.
    An element with greater stack order is always in front of an element with a lower stack order.
    Note: z-index only works on positioned elements (position:absolute, position:relative, or position:fixed).

        z-index: auto|number|initial|inherit;

## CSS3
