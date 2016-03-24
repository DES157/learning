HTML
====


? Canvas
? DOM


Links
-----

##### WHATWG

- [__HTML: The Living Standard (Edition for Web Developers)__](https://developers.whatwg.org/)  
- [HTML Living Standard](https://html.spec.whatwg.org/multipage/) super detailed for browser developers
- [](https://spec.whatwg.org/)

##### WebPlatform

- [__Web Platform Docs__](http://docs.webplatform.org/wiki/Main_Page) - good reference!


##### W3C

###### Standards

- [Web Design and Applications](https://www.w3.org/standards/webdesign/) 
- [HTML5 W3C Standard](https://www.w3.org/TR/html5/) [W3C](https://www.w3.org/) fork of WHATWG

###### Learning

- [W3C Developers](https://www.w3.org/developers/)
    - [W3DevCampus](http://www.w3devcampus.com/)
    - [W3Cx](https://www.edx.org/school/w3cx) Free online courses from The World Wide Web Consortium (W3C)


##### Mozilla

- [HTML @ Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTML) - lots of good guides, references, and tutorials!




HTML Standards
--------------

### HTML




### XHTML

After HTML4, but never really caught on.  HTML5 is the new thing.


### HTML5

`<!DOCTYPE html>`


### Etc.

- Read about [CSS](css.html)


***

HTML Basics
-----------

HTML documents must start with a Document Type Declaration ("doctype"). These declare a Document Type Definition (DTD) to allow for parsing and validation by SGML tools. For HTML 4 (strict version of HTML 4.01) this would be:
`<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`. HTML5 is much simpler: `<!DOCTYPE html>`.


*tags* and *attributes* which are name-value pairs (it's a good idea to quote attribute values). Note that *element* is a more semantic concept and generally refers to a start tag, end tag, and content.

```
<!DOCTYPE html>
<html>
  <head>
    <title>This is a title</title>
  </head>
  <body>
    <p>Hello world!</p>
  </body>
</html>
```

### Headings

6 levels:
`<h1>Heading level 1</h1>`


### Misc

###### line breaks
`<br>`

###### comments
`<!-- This is a comment -->`


***

Quick Answers
-------------

##### coloring text

Set the font [color](http://www.w3schools.com/tags/att_font_color.asp) attribute.
`<font color="color_name|hex_number|rgb_number">`
eg. `<font color="red">This is some text!</font>`

Use CSS syntax in HTML5 since font tag is not supported:
e.g. `<p style="color:red">`
See here to pick colors by [name](http://www.w3schools.com/cssref/css_colornames.asp).



Along the lines of Markdown is also [HAML](http://haml.info/) for generating (X)HTML. It is primarily Ruby, but also has bindings to Python, etc.


HTML Tools
----------

> tidy - validate, correct, and pretty-print HTML files
