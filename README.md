[jMobile](http://jmobile.isell.com/) - Mobile JavaScript
==================================================

## Introduction

The jMobile library was created as a much lighter and faster jQuery, built specifically for mobile devices. Which means it has a drastically smaller file size (6.8kb minified & gzipped) as compared to jQuery (23kb minified & gzipped).

In addition to core jQuery functionality, jMobile implements [geolocation through HTML5](http://dev.w3.org/geo/api/spec-source.html) as well with full callback support.

## What is included?

Methods marked with * are only partially implemented.

  - [$(selector)](http://api.jquery.com/jQuery/) 
	- $(selector, context), $(element), $(array)

### Methods operating on a `$(selector)`
  
  - add
  - each
  - attr
  - removeAttr
  - get
  - toArray
  - data
  - append
  - appendTo
  - prepend
  - prependTo
  - before
  - insertBefore
  - after
  - insertAfter
  - toggle
  - hide
  - show
  - fadeIn and fadeOut - does so without animation*
  - eq
  - first
  - last
  - indexOf
  - slice
  - find*
  - not*
  - filter*
  - is*
  - remove
  - closest
  - val* - does not do checkbox, select, etc.
  - html
  - text
  - empty
  - addClass
  - removeClass
  - hasClass
  - parent
  - parents
  - parentsUntil
  - next
  - prev
  - nextAll
  - nextUntil
  - prevUntil
  - siblings
  - children
  - contents
  - serializeArray

### static methods off $
  
  - $$ - querySelectorAll or query engine shim
  - $.each 
  - [$._each](http://documentcloud.github.com/underscore/#each) - Underscore's native each
  - [$._indexOf](http://documentcloud.github.com/underscore/#indexOf) - Underscore's indexOf
  - [$._defaults](http://documentcloud.github.com/underscore/#defaults) - Underscore's defaults
  - [$._filter](http://documentcloud.github.com/underscore/#filter) - Underscore's filter
  - $.Expr - :hidden :visible now supported, can plugin other expressions as needed.
  - $.filter
  - $.dir
  - $.nth
  - $.sibling
  - $.grep
  - $.map
  - $.data
  - $.attrs
  - $.trim
  - $.isFunction
  - $.isArray
  - $.isWindow
  - $.isNaN
  - $.merge
  - $.extend
  - $.makeArray
  - $.hasClass
  - $.typeOf - safe type of a variable
  - $.loadScript - (url, callback [, async]) load an external script dynamically
  - $.loadAsync - load js async and call `$(callback)` or `$.scriptsLoaded` when all scripts have been loaded
  - $.scriptsLoaded - register callbacks to be fired when all async scripts have been loaded.
  - $.htmlFrag - creates a document fragment from a html string **(name changed)**
  - $.walk - traveres all childElems including self `(predicateFn, [[, context], results])`
  - $.query - query Engine i.r. doc.querySelector || queryEngine Shim
  - $.attrs - an elements attributes
  - $.unique - return a unique list of elements in document order
  - $.contains - parent element contains sibling

## Contributing

Pull requests are welcome!

Areas of interest are bug testing this library on mobile devices and integrating core browser functionality, most importantly from HTML5.

## Contributors

- [@odmarkj](https://github.com/odmarkj) (Joshua Odmark)

## Core

This library is based of of [jquip](http://github.com/mythz/jquip), which is based off of [jQuery](http://github.com/jquery/jquery).

The main differentiation is converting the main variable into an object so that it may be extended with core functionality, for example, HTML5's geolocation.
