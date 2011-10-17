# Easie.js

A plugin for [Ender](http://ender.no.de/) + [Morpheus](https://github.com/ded/morpheus), adapted from [jquery.easie.js](https://github.com/jaukia/easie).

It gives you CSS3 cubic-bezier easing in javascript, so your javascript tweens can look like CSS and vice-versa.

Examples
--------

With the ender bridge:

``` js
$('#content').animate({ left: 911, easing: 'easeInOut', complete: function () {
    console.log('boosh')
  }
})
```

Or not:

``` js
var morpheus = require("morpheus")

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

Easing Shortcuts
----------------

**CSS3 defaults**

    ease
    ease-in
    easeIn
    ease-out
    easeOut
    ease-in-out
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


Thank yous
----------

  * [Janne Aukia](https://github.com/jaukia/)
  * [Dustin Diaz](https://github.com/ded/)
  * [Jacob Thornton](https://github.com/fat/)

