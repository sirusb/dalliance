Biodalliance: fast, embeddable genome visualization
=========================

Dalliance is a genome viewing tool that aims to offer a high
level of interactivity while working entirely within your web
browser. It works with current versions of Chrome, Firefox, and
Safari and (with minor visual glitches) Internet Explorer 11.  It
is also usable with current mobile web browsers.

To try it, visit [http://www.biodalliance.org/human37.html](http://www.biodalliance.org/human37.html).

Development
-----------

You should be able to run Dalliance directly from a git checkout.  You
first need to download a couple of dependencies using:

          git submodule init
          git submodule update

Then point your web browser at the file `test.html`.  Once you've
confirmed this is working, you can customize your display by editing
the block of configuration javascript within the HTML file.

Adding extra data
-----------------

Dalliance loads data via the [DAS](http://biodas.org/) protocol.
There's a button to click that will let you add DAS sources.  If what
you're after is in the registry, you should just be able to select and
add, otherwise you'll need to type a URL.

You can also add data directly from indexed binary files (currently
bigwig, bigbed and BAM, probably other formats in the future).  Binary files
can either be hosted on a web server or loaded from local disk.

However, there is one caveat.  Since Dalliance is a pure Javascript
program running in your web browser, it is normally subject to the
"same origin policy", which only permits Javascript code to access
resources on the same server.  To get round this, DAS servers need to
support the W3C [CORS](http://www.w3.org/TR/cors/) extension.  The
latest versions of Dazzle, Proserver and MyDAS should implement this by
default.

Reporting bugs
--------------

Dalliance is under active development and we welcome your suggestions.
Right now, probably the best place for bug reports or feature requests
is the [Github issue tracker](http://github.com/dasmoth/dalliance).

There is also a [mailing list](https://groups.google.com/forum/#!forum/biodalliance-dev)
where the project can be discussed.