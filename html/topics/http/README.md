# HTTP

* [HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
* [HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

> HTTP defines methods (sometimes referred to as verbs) to indicate the desired action to be performed on the identified resource. What this resource represents, whether pre-existing data or data that is generated dynamically, depends on the implementation of the server. Often, the resource corresponds to a file or the output of an executable residing on the server. The HTTP/1.0 specification[12] defined the GET, POST and HEAD methods and the HTTP/1.1 specification[13] added 5 new methods: OPTIONS, PUT, DELETE, TRACE and CONNECT

* [A Beginner’s Guide to HTTP and REST](https://code.tutsplus.com/tutorials/a-beginners-guide-to-http-and-rest--net-16340)

### HTTP 1.1

Request and Response formats. Use [Fiddler](http://www.telerik.com/download/fiddler) or [FiddlerCap](http://www.telerik.com/fiddler/fiddlercap) to inspect.

#### HTTP Request

    <VERB> <URI> <HTTP Version>
    <Request Header>
    <Request Body>

> - `<VERB>` is one of the HTTP methods like GET, PUT, POST, DELETE, OPTIONS, etc
> - `<URI>` is the URI of the resource on which the operation is going to be performed
> - `<HTTP Version>` is the version of HTTP, generally "HTTP v1.1" .
> - `<Request Header>` contains the metadata as a collection of key-value pairs of headers and their values. These settings contain information about the message and its sender like client type, the formats client supports, format type of the message body, cache settings for the response, and a lot more information.
> - `<Request Body>` is the actual message content. In a RESTful service, that's where the representations of resources sit in a message.

Method | Operation performed on server | Quality
-------|-------------------------------|--------
GET | Read a resource. | Safe
PUT | Insert a new resource or update if the resource already exists. | Idempotent
POST | Insert a new resource. Also can be used to update an existing resource. | N/A
DELETE | Delete a resource. | Idempotent
OPTIONS | List the allowed operations on a resource. | Safe
HEAD | Return only the response headers and no response body. | Safe

#### HTTP Response

    <HTTP Version> <Response Code>
    <Response Header>
    <Response Body>

> - The server returns `<Response Code>`, which contains the status of the request. This response code is generally the 3-digit HTTP status code.
> - `<Response Header>` contains the metadata and settings about the response message.
> - `<Response Body>` contains the representation if the request was successful.

### HTTPS

`POST` `GET` ...

## Protocols

### SOAP

### RESTful Web Services

[REST](rest) &rarr;

## Authentication

* [OAuth](http://oauth.net)
