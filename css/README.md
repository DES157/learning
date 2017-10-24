# CSS

what are sprites?

## Links

* [CSS @ Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS)
* [HTML Styles - CSS @ w3schools](http://www.w3schools.com/html/html_css.asp)
* [CSS Tutorial @ w3schools](http://www.w3schools.com/css/default.asp)
* [CSS Reference](http://tympanus.net/codrops/css_reference/)

#### Tools

* [Sass](http://sass-lang.com/)
* [Compass](http://compass-style.org/)
* [less](http://lesscss.org/)

## Basics

Styling can be added to HTML elements in 3 ways:

1. Inline - using a __style attribute__ in HTML elements
2. Internal - using a `<style>` __element__ in the HTML `<head>` section
3.  External - `<link>` to one or more __external CSS files__

> Use the HTML style attribute for inline styling
Use the HTML `<style>` element to define internal CSS
Use the HTML `<link>` element to refer to an external CSS file
Use the HTML `<head>` element to store `<style>` and `<link>` elements
Use the CSS color property for text colors
Use the CSS font-family property for text fonts
Use the CSS font-size property for text sizes
Use the CSS border property for visible element borders
Use the CSS padding property for space inside the border
Use the CSS margin property for space outside the border

### Internal Styling (Internal CSS)

    <!DOCTYPE html>
    <html>
        <head>
            <style>
                ...
            </style>
        </head>
        <body>
            ...
        </body>
    </html>


### Exernal Styling (External CSS)

    <!DOCTYPE html>
    <html>
        <head>
            <link rel="stylesheet" href="styles.css">
        </head>
        <body>
            ...
        </body>
    </html>

### CSS Fonts

1. `color`
2. `font-family`
3. `font-size`

### CSS Box Model

1. `border`
2. `padding`
3. `margin`

### Targeting Elements

Use `id` to address a single element (`element#id`). Use `class` to address groups of elements (`element.class`).

### CSS Syntax

`selector {property:value;}` e.g. `h1 {color:blue; font-size:12px;}`

## CSS Selectors

## Important Properties

display

position

---

## Other

#### CSS Transformations

* [CSS Transforms](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transforms)
* [Intro to CSS 3D transforms](https://desandro.github.io/3dtransforms/)
* [Tidiv](http://tridiv.com/) web based 3D shape editor for CSS
