# AJAX

[Ajax](https://developer.mozilla.org/en-US/docs/AJAX)

[`XMLHttpRequest`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest)

now can use

[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

Note issues with CORS server-side access control and problems with cross-origin requests! It's the [*same origin policy*](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy)!

https://blog.garstasio.com/you-dont-need-jquery/ajax/

## JSONP

Requires server support!

with jQuery.ajax set dataType to jsonp and maybe crossDomain true

without jquery src in script tag with ?callback=myFunction

https://sacha.me/articles/jsonp-demystified/

https://davidwalsh.name/unwrapping-jsonp

## CORS

Do you have to manually add Origin header?

* [Using CORS](https://www.html5rocks.com/en/tutorials/cors/)
* [An In-depth Look at CORS](https://www.sitepoint.com/an-in-depth-look-at-cors/)


## Overcoming Same Origin Policy

https://jvaneyck.wordpress.com/2014/01/07/cross-domain-requests-in-javascript/

* [JSONProxy](https://jsonp.herokuapp.com/) works!
* [cors-proxy](https://galvanize-cors-proxy.herokuapp.com/)
* [cors-anywhere](https://cors-anywhere.herokuapp.com/)
* [Whatever Origin](http://www.whateverorigin.org/)
* [Any Origin](https://anyorigin.com/)
* [crossorigin.me](https://crossorigin.me/)
* [Cors proxies](https://gist.github.com/jimmywarting/ac1be6ea0297c16c477e17f8fbe51347) list
* Load in iframe?
* * [Yahoo Query Language (YQL)](https://developer.yahoo.com/yql/) see [here](https://developer.yahoo.com/javascript/howto-proxy.html)
* http://www.ajax-cross-origin.com/
