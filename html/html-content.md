# HTML Content

* [Content Categories @ Mozilla](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories)

See [Kinds of content](https://www.w3.org/TR/html5/dom.html#kinds-of-content) in the HTML5 specs.

"content models"

flow

p/div - block elements by default

span - inline by default, can force display:block

> A span cannot act like a div (regardless of how it is styled) because a span cannot contain flow content as divs can. Spans may only contain phrasing content, even if they have display: block;. –

a

how float?

### Phrasing Content

inline elements ~= phrasing content?

### Flow Content

block elements ~= flow content?

#### Sectioning Content

> Elements belonging to the sectioning content model create a section in the current outline that defines the scope of  `<header>` elements, `<footer>` elements, and heading content.
>
> Elements belonging to this category are `<article>`, `<aside>`, `<nav>` and `<section>`.

#### Heading Content

> Heading content defines the title of a section, whether marked by an explicit sectioning content element or implicitly defined by the heading content itself.
>
>Elements belonging to this category are `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` and `<hgroup>`. 
