# JSON

JSON (JavaScript Object Notation) is a nice [alternative to XML](http://www.json.org/xml.html).

JSON is specified by [RFC 7159](https://tools.ietf.org/html/rfc7159.html) and [ECMA-404](https://www.ecma-international.org/publications/standards/Ecma-404.htm).

JSON is a data exchange format derived from (and subset of) JavaScript object notation.

MIME type "application/json".

## JSON Basics

See http://www.json.org for concise and readable specs, but summarized here.

JSON is build on:

1. collection of name/value pairs (*object*)
2. an ordered list of values (*array*)

Note that in JSON a *string* (name) must be (double) quoted strings (unlike in JS object literal notation where the quotes may be optional and which also allows numbers and identifiers to be used).

A *value* may be one of:

* *string* (double quoted)
* *number*
* *object*
* *array*
* `true`
* `false`
* `null`

Note that JavaScript also allows values to be functions, date, or undefined [[ref](https://www.w3schools.com/js/js_json_syntax.asp)].

#### JavaScript Object Literals

JavaScript **object literal notation** are comma-separeted lists of colon-separated property names and values wrapped in curly braces.

> An object literal is a list of zero or more pairs of property names and associated values of an object, enclosed in curly braces (`{}`). Additionally, you can use a numeric or string literal for the name of a property or nest an object inside another. Object property names can be any string, including the empty string. If the property name would not be a valid JavaScript identifier or number, it must be enclosed in quotes. Property names that are not valid identifiers also cannot be accessed as a dot (.) property, but can be accessed and set with the array-like notation("[]"). [[ref](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Object_literals)]

* [What is the difference between JSON and Object Literal Notation?](http://stackoverflow.com/q/2904131/)

## JSON Tools

* [jq](https://stedolan.github.io/jq/) - command-line json processor; play with it in the browser [here](https://jqplay.org/).

#### JSON Tools in Python

* [json](https://docs.python.org/3/library/json.html) module in the Python Standard Library
* [simplejson](https://github.com/simplejson/simplejson)

## JSON References

* [An Introduction to JavaScript Object Notation (JSON) in JavaScript and .NET](https://msdn.microsoft.com/en-us/library/bb299886.aspx)

