# jsroot-example

This is simple example how JSROOT can be installed and used from Node.js and bower

To run example, checkout repository and call:

    [shell] npm start

It should start HTTP server at port 3000.

There is three html pages, showing usage of JSROOT:



index.html shows how to use JSROOT.

    <script src="vendor/jsroot/scripts/JSRootCore.js?bower" type="text/javascript"></script>

Here one specifies addditional URL parameter '?bower', which  says JSROOT to reuses scripts like d3.js or three.js from bower installation.



index_require_intern.html shows method to include JSRootCore.js with require.js. 
It is standard method, which uses internal libraries from JSROOT directories.



index_require_extern.html uses package configuration info, which is automatically created when
example repository checked out. There is '.bowerrc' file, which contains post-install command
   "postinstall": "./node_modules/.bin/bower-requirejs -t -c public/config.js"
   
File config.js included into HTML pages and let JSROOT directly reuse bower packages


To install only JSROOT with bower do:

   [shell] bower install jsroot


