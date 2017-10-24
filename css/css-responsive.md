# CSS Responsiveness

Media queries and viewport

? look into how to get javascript device-width property!

##### Definitions

* _Hardware pixel_ - physicsl pixel size
* _Device-independent pixel (diip)_ - scaling of hardware pixel to match a uniform _reference pixel_ at normal viewing difference, approximately device/density independent, a mobile will probably be fewer diip than actual device pixels.
* _CSS pixel_ - this is the `px` in CSS styles like `width`. _Scale factor_ is CSS pixel to diip ratio.

## Media Query

* [Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)
* [A pixel is not a pixel is not a pixel](http://www.quirksmode.org/blog/archives/2010/04/a_pixel_is_not.html)

---

`@media` CSS [at-rule]
(https://developer.mozilla.org/en-US/docs/Web/CSS/At-rule)

    @media <media-query-list> {
        <group-rule-body>
    }

A `<media-query>` is composed of a _media type_ and/or a number of _media features_ (CSS3).

Media types can be all, print, screen, or speech.

Media features include

Eg:

    /* iPads (portrait) ----------- */
    @media only screen 
    and (min-device-width : 768px) 
    and (max-device-width : 1024px) 
    and (orientation : portrait) {
    /* Styles */
    }

----

pixels
viewport

## Viewports

Use `<meta name="viewport">` tag or `@viewport` CSS at-rule. If a viewport is not defined a mobile browser will render page at a `fallback width` on the order of 800-1024 CSS pixels.

This is the standard to include everywhere!

    <meta name="viewport" content="width=device-width, initial-scale=1">

It may be ncecssary to also mess with `maximum-scale`

Standard iPhone is 320px and so for a perfect fit do:

    <meta name="viewport" content="width=320, initial-scale=1">

But if you set an initial or maximum scale then the width property is effectively a minimum viewport width. On large screens the viewport will be expanded to fill the screen. If the screen is too small to accomodate your layout then??

##### `<meta name="viewport">` properties

* `width` controls size of viewport, in pixel (w/o units) or `device-width` which is the width of the screen in _CSS pixels_ at a scale of 100%.
* `height` is similar

* `initial-scale` controls zoom level when page is first loaded, user can zoom according to `maximum-scale`, `minimum-scale`, and `user-scalable` properties

* [Configure the Viewport](https://developers.google.com/speed/docs/insights/ConfigureViewport)
* [Using the viewport meta tag to control layout on mobile browsers](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag)
* [A tale of two viewports - part one](http://www.quirksmode.org/mobile/viewports.html) / [part two](http://www.quirksmode.org/mobile/viewports2.html)

See list of [viewport sizes](http://viewportsizes.com/).

Note: if necessary to fill the screen at the requested scale most mobile browsers will expand the viewport width.

    <meta name="viewport" content="width=500, initial-scale=1">
    
## Links

* [Pixel-Perfect UI in the WebView](https://developer.chrome.com/multidevice/webview/pixelperfect) - read this now!
* [Desing and UI @ Google Web Fundamentals](https://developers.google.com/web/fundamentals/design-and-ui/)
* [PageSpeed Insight Rules](https://developers.google.com/speed/docs/insights/rules) great advice from Google on how to develop for mobile. Source for viewport advice above, and also advice on [fonts](https://developers.google.com/speed/docs/insights/rules).


