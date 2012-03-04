# ender.easie.js

A plugin for [Ender](http://ender.no.de/) + [Morpheus](https://github.com/ded/morpheus), adapted from [jquery.easie.js](https://github.com/jaukia/easie).

Easie gives you CSS3 cubic-bezier easing in javascript, so your javascript tweens can look like CSS and vice-versa. This adaptation plugs easie's functions into `morpheus.easings`.

## Examples

With the ender bridge:

``` js
$('#content').animate({ left: 911, easing: 'easeInOut', complete: function () {
    console.log('boosh')
  }
})
```

Or standalone morpheus:

``` js
morpheus(elements, {
  // CSS
    left: -50
  , top: 100
  , width: '+=50'
  , height: '-=50px'
  , fontSize: '30px'
  , color: '#f00'
  , transform: 'rotate(30deg) scale(+=3)'
  , "background-color": '#f00'

  // API
  , duration: 500
  , easing: 'easeInOutExpo'
  , bezier: [[100, 200], [200, 100]]
  , complete: function () {
      console.log('done')
    }
})
```

## Easing Shortcuts

Accessable via `morpheus.easings`

**CSS3 defaults**

    ease
    easeIn
    easeOut
    easeInOut

**cubic-bezier curves**

    easeInCirc
    easeOutCirc
    easeInOutCirc
    easeInCubic
    easeOutCubic
    easeInOutCubic
    easeInExpo
    easeInOutExpo
    easeOutExpo
    easeInQuad
    easeInOutQuad
    easeOutQuad
    easeInQuart
    easeInOutQuart
    easeOutQuart
    easeInQuint
    easeInOutQuint
    easeOutQuint
    easeInSine
    easeInOutSine
    easeOutSine

## Thanks

* [Janne Aukia](https://github.com/jaukia/)
* [Dustin Diaz](https://github.com/ded/)
* [Jacob Thornton](https://github.com/fat/)

## License

```
* LICENSE INFORMATION:
*
* Copyright (c) 2011 Janne Aukia (janne.aukia.com),
* Louis-Rémi Babé (public@lrbabe.com).
* Adapted to Ender/Morpheus by Dan Rogers (danro.net)
*
* Dual licensed under the MIT & and GPL Version 2 licenses:
* http://danro.mit-license.org/
* https://raw.github.com/danro/ender-easie/master/GPL-LICENSE
*
* LICENSE INFORMATION FOR DERIVED FUNCTIONS:
*
* Function cubicBezierAtTime is written by Christian Effenberger,
* and corresponds 1:1 to the WebKit project function.
* "WebCore and JavaScriptCore are available under the
* Lesser GNU Public License. WebKit is available under
* a BSD-style license."
```