# cytoscape.js

## Documentation

You can find the documentation in the [wiki](https://github.com/cytoscape/cytoscape.js/wiki).  This readme is mostly for developers of cytoscape.js.


## Acknowledgements

A big thanks goes out to Keith Wood for his jQuery SVG library, which is used
in Cytoscape Web's default SVG renderer implementation.  You can find out more
about his library at [his website](http://keith-wood.name/svg.html).

We would also like to thank Mark Gibson for his work on the jQuery color
library, which is used in our continuous mapper calculations.  You can find out
more about Mark's library at [his website](http://www.adaptavist.com/display/jQuery/Colour+Library).

We used Kevin Lindsey's SVG intersection library to calculate the positioning
of some objects, like edges.  You can find his library at [his website](http://www.kevlindev.com/gui/math/intersection).

We used Brandon Aaron's mouse wheel library for providing easy cross-browser
support for zooming with the mouse wheel in the SVG renderer.  You can find out
more about his library at [his website](http://brandonaaron.net).

Arbor was used in one of Cytoscape Web's included layouts.  We made some
modifications to the library, written by Samizdat Drafting Co., so that it
would work with multiple instances of Cytoscape Web and that it would work
on lesser browsers, like IE.  Information about this library can be found
at the [Arbor website](http://arborjs.org/) and on [GitHub](https://github.com/maxkfranz/arbor) where the original code was forked.


## Build dependencies

You need a number of executables installed on your system to successfully run
`make` to build the project.
	
Their paths are defined in `Makefile`, so you can revise the paths to these
executables and still run `make` successfully.  You should be able to run
`make` without modification on any well configured Unix-like machine, such as
Linux or Mac OS X---Mac needs XCode with command line tools installed to run
`make`.



## Build instructions

Run `make` in the console.  The targets are:

 * `all` : build everything (default)
 * `minify` : build the production minified JS
 * `zip` : minify and make a ZIP file for release
 * `clean` : deletes built files

A note to developers:

For `zip`, make sure to define `VERSION` in `Makefile` if you're making an
actual release ZIP.



## Tests

QUnit tests are found in the [tests directory](https://github.com/cytoscape/cytoscape.js/tree/master/tests).  The tests are automatically
run against different versions of jQuery.

