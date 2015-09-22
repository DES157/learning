XML
===


Links
-----

- [XML Home Page](http://www.w3.org/XML)
- [XML Technology](http://www.w3.org/standards/xml)
- [The XML FAQ](http://xml.silmaril.ie)
- [Official Markup Validator](https://validator.w3.org)
- [XML - Managing Data Exchange @Wikibooks](https://en.wikibooks.org/wiki/XML_-_Managing_Data_Exchange)


Basics
------

> An xml _document_ contains one or more _elements_, which are delimited by start and end _tags_.
> The first element in every xml document is called the _root_ element.
> Elements can have _attributes_, which are name-value pairs. Attribute values must be quoted. You may use either single or double quotes. The ordering of the attributes is not significant.
> Putting a / character in the start tag is shorthand for writing _empty_ elements.
>
> XML elements can be declared in different namespaces `<ELEMENT xmlns='http://...'>`. The namespace declaration affects the element where it’s declared, plus all child elements. 
> You can also use an xmlns:prefix declaration to define a namespace and associate it with a prefix `<NAMESPACE:ELEMENT xmlns:NAMESPACE='http://...'>`. Then each element in that namespace must be explicitly declared with the prefix.
> XML documents can contain character encoding information on the first line, before the root element `<?xml version='1.0' encoding='utf-8'?>`.

> -- from [A 5-Minute Crash Course in XML](http://www.diveintopython3.net/xml.html#xml-intro)



Schema
------


Bindings
--------

### [Python](https://wiki.python.org/moin/PythonXml)

Working with [XML in Python](http://www.diveintopython3.net/xml.html).

- [`untangle`](https://github.com/stchris/untangle)
- [`xmltodict`](https://github.com/martinblech/xmltodict)
- `lxml`
- `PyXML` (appears deprecated)

MiniDom and ElementTree are in standard library but prefer newer pythonic packages.

### R

- [`XML`](http://cran.r-project.org/web/packages/XML)
