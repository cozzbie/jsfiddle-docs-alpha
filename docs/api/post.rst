==========================
Display a Fiddle from POST
==========================

There is a way to display a fiddle using the POST query.

Input
=====

URL Structure
--------------

One need to choose the framework using the URL:

URL: ``http://jsfiddle.net/api/post/{framework}/{version}/``

Use ``library/pure`` for no framework:

URL: ``http://jsfiddle.net/api/post/library/pure/``

There is an option to add dependencies as a comma separated list:

URL: ``http://jsfiddle.net/api/post/{framework}/{version}/dependencies/{dependency_list}/``

**framework**
   the desired framework name. Which framework should be loaded with the 
   fiddle.

**version**
   substring of the framework version - the last passing will be used. If 1.3 
   will be given, jsFiddle will use the latest search result. it will favorize 
   1.3.2 over 1.3.1 and 1.3
    
**dependency_list**
   comma separated list of dependency substrings. It would mark any dependency 
   containing the substring.

POST Variables
--------------

All fields are optional. New fiddle setting will be used if no data provided.

**html,js,css**
   code for specific panels

**panel_[html/js/css]**
   choose language for specific panel
   
   * ``panel_html`` accepts only ``0``
   * ``panel_js`` 
     * ``0`` - JavaScript
     * ``1`` - CoffeeScript
     * ``2`` - JavaScript 1.7
   * ``panel_css`` 
     * ``0`` - CSS
     * ``1`` - SCSS

**resources**
   a comma separated list of external resources

**title**
   title of the fiddle

**description**
   description of the fiddle

**normalize_css**
   yes or no - should normalize.css be loaded before any CSS
   declarations?

**dtd**
   substring of the chosen DTD (i.e. "html 4")

**wrap**
   set the JS code wrap:

   * *l* - onLoad
   * *d* - domReady
   * *h* - no wrap - in <head>
   * *b* - no wrap - in <body>  
  

Example
=======

http://jsfiddle.net/zalun/sthmj/embedded/result/

