# URL and URLSearchParams

* [URL](https://developer.mozilla.org/en-US/docs/Web/API/URL) see [spec](https://url.spec.whatwg.org/)
* [URLSearchParams](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams) is useful for dealing with web services!

##### Tutorials

* [Easy URL Manipulation with URLSearchParams](https://developers.google.com/web/updates/2016/01/urlsearchparams)
* [Get Query String Parameters with JavaScript](https://davidwalsh.name/query-string-javascript)
* https://www.sitepoint.com/get-url-parameters-with-javascript/

## URL

`.href` ~ `.toString()`

`.search` property (undocumented?) appears to just return search string, including `?` --- may be from an old api related to window.location.search?

`.searchParams` returns a URLSearchParams object

`origin` readonly

`hostname`

`pathname`

## URLSearchParams

Inspect using `.toString()`. Can get iterators using `entries()`, `keys()`, and `values()`.

has()

get()/getAll()

set()

append()

delete()

sort()



