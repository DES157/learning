# Fetch API

A better Ajax

* [Fetch API @ MDN](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) is a great overview, tutorial, and reference, including [fetch-examples](https://mdn.github.io/fetch-examples/)
* [Fetch Living Standard @ whatwg](https://fetch.spec.whatwg.org/)
* [Introduction to fetch()](https://developers.google.com/web/updates/2015/03/introduction-to-fetch)
* [This API is so Fetching!](https://hacks.mozilla.org/2015/03/this-api-is-so-fetching/)
* [fetch API](https://davidwalsh.name/fetch)
* [How to Use the JavaScript Fetch API to Get Data @ scotch](https://scotch.io/tutorials/how-to-use-the-javascript-fetch-api-to-get-data)

`cors`, `no-cors`

`opaque` response

## Basic Use

    fetch(url)
    .then(function(response) {
        // handle data
    })
    .catch(function(error) {
        // deal with errors
    });

## Handling the Response

A response can be read and processes using the `text`, `json`, `blob`, `formData`, or `arrayBuffer` methods from `Body`.

These can be used directly or they can be chained since they return a promise.

`response.blob()`

    fetch(url)
    .then(function(response) {
      if(response.ok) {
        return response.blob();
      }
      throw new Error('Network response was not ok.');
    })
    .then(function(myBlob) { 
      var objectURL = URL.createObjectURL(myBlob); 
      myImage.src = objectURL; 
    }).catch(function(error) {
      console.log('There has been a problem with your fetch operation: ' + error.message);
    });

`response.json()` does JSON.parse()


### Error Checking

Review this...

    if(response.ok) {
    }
    
    if (response.status !== 200) {
      console.log('Looks like there was a problem. Status Code: ' +
        response.status);
      return;
    }
    
    .then()

    var contentType = response.headers.get("content-type");
    if(contentType && contentType.includes("application/json")) {
      return response.json();
    }
    throw new TypeError("Oops, we haven't got JSON!");


## Fetch Interfaces

e.g. [Headers](https://developer.mozilla.org/en-US/docs/Web/API/Headers), [Request](https://developer.mozilla.org/en-US/docs/Web/API/Request), and [Response](https://developer.mozilla.org/en-US/docs/Web/API/Response) interfaces, and [Body](https://developer.mozilla.org/en-US/docs/Web/API/Body) mixin, etc.

And fetch involves interaction with other machinery.



