## The CometD Dojo Bindings Repository

This repository is a copy of the
[CometD Dojo bindings](https://github.com/cometd/cometd/tree/master/cometd-javascript/dojo)
that you can find at the [master CometD repository](https://github.com/cometd/cometd).

While the master CometD repository packages the CometD Dojo bindings
in a format that is appropriate for Maven users and for users that
want to build Java web applications, this repository repackages the
CometD Dojo bindings in a format that is more convenient for non-Maven
users and for users that prefer to consume JavaScript source files,
for example with build tools.

This repository is synchronized with the master repository on every
CometD release.

The code in this repository is available under either the modified
[BSD license](http://trac.dojotoolkit.org/browser/dojo/trunk/LICENSE#L13)
or the [Apache 2 license](http://www.apache.org/licenses/LICENSE-2.0).

### How to use it

Download the CometD Dojo bindings for a specific release, browsing
https://github.com/cometd/cometd-dojo/tags

Unzip the CometD Dojo bindings in your directory structure, where you
have already Dojo (and other libraries), under a directory of your 
choice, for example directory `cometd-dojo/`:

    dojo/
    dijit/
    cometd-dojo/
        cometd/
        org/
        cometd.js

Now you just need to tell Dojo where to find CometD, in this way:

    <html>
        <head>
            <script type="text/javascript" src="dojo/dojo.js"
                data-dojo-config="async: true, paths: { 
                    'dojox/cometd': '../cometd-dojo/cometd' , 
                    'org/cometd': '../cometd-dojo/org/cometd' 
                }"></script>

            <script type="text/javascript">
                require(["dojox/cometd", "dojo/domReady!"], function(cometd) {
                    // Use the cometd object here
               });
           </script>
        </head>
        <body>
        </body>
    </html>

