# HTML

[TOC]

? above the fold?

tags

elements

attributes/values / quote all attributes!!!


some think like this is a good idea...

     <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1, user-scalable=no"/>



The meta tag (because it's a *void element*) does not need closing `/` in HTML5. It does, however, in XHTML and earlier versions of HTML, to mark it as *self-closing*.


---


## Box Model

### Display

There are *inline* and *block* elements. Inline elements cannot contain block level elements.

Additionally, `inline-block` creates a rectangular block but does not create newlines.

    display: inline;
    display: block;
    display: inline-block;

#### Inline Elements

As small as possible, and do not create newlines.

Does not have `width` or `height` or vertical `margin`.

`<span>`

#### Blocklevel Elements

Block-level elements define a rectangular region. They try to be as wide as possible and begin and end with new line?

`<div>`

### Etc

and then there's the issue of `float`...



## Elements

[HTML Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)


#### Content *Categories*

HTML elements fall into zero or more categories [[ref](https://w3c.github.io/html/dom.html#kinds-of-content)]:

* Metadata content
* Flow content
* Sectioning content
* Heading content
* Phrasing content
* Embedded content
* Interactive content


* `<main>` / at most one per document

### Sectioning Content

* `<article>` (HTML5)
* `<section>` (HTML5)
* `<nav>` (HTML5)
* `<aside>` (HTML5)


### Global Attributes

[Global Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes)


## HTML5




#### HTML5 Sectioning

[ref](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML_sections_and_outlines)

The `<body>`, `<section>`, `<article>`, `<aside>`, and `<nav>` tags (as well as `<body>` itself) are sectioning. Note `<header>`, `<footer>`, and ...? are not sectioning.

Headings `<h1>`-`<h6>` define *implicit* sections (link to details). Outline determined by structure of sections, but heading rank relative within sections.

Sectioning roots ,`<blockquote>`, `<details>`, `<fieldset>`, `<figure>` and `<td>` can have their own outlines but do not contribute to outline of their ancestors.
Compare that to `<aside>` and `<nav>` which are also outside the main outline.


---


## Load Order


head? inline js? css?

##

Note DOMContentLoaded is on document, where load (.onload) is window.

    // DOMContentLoaded waits for HTML but not images, stylesheets, etc.
    // may wait for external scripts in html
    // here using anonymous function, but any listener (js function or EventListener interface)
    document.addEventListener("DOMContentLoaded", function(event) {});

    // load waits for everything, false optional!?
    window.addEventListener("load", function(event) {}, false);

`window.onload = ` only allows one listener, whereas addEventListener allows multiple listeners. Someplace said rarely used.

Note `attachEvent` is nonstandard for IE5-8 and below, probably not necessary anymore

    window.attachEvent("onload"


## Forms

how to access? document.formname... or 


in a form button defaults typp="submit", but outside a form I don't think so.

