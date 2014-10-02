.. _gist-read:

========================
Display Fiddle from Gist
========================

It is enough to simply prepare and provide a link on the page to have jsFiddle read the demo from 
gist and present it as a fiddle.

Input
=====

It is important to have demo prepared for jsFiddle. 

Gist files
------------------------

  * fiddle.js

  * fiddle.html

  * fiddle.css

  * fiddle.manifest


**fiddle.[js/html/css]**
   contains fiddle code for the specific panel

**fiddle.manifest**
  is a description of the gist written in YAML, structure compatible with MooTools doc

.. code-block:: yaml
   
    name: The Name of the Fiddle
    description: Some description, please keep it in one line
    authors:
      - John Doe
      - Jan Wisniewski
    resources:
      - http://some.url.com/some/file.js
      - http://other.url.com/other_filename.css
    normalize_css: no
    wrap: b
    panel_js: 1
    panel_css: 1

All above fields are optional.

*panel_[html/js/css]*
   choose language for specific panel
   
   * ``panel_html`` accepts only ``0``
   * ``panel_js`` 

     * ``0`` - JavaScript
     * ``1`` - CoffeeScript
     * ``2`` - JavaScript 1.7
   * ``panel_css`` 

     * ``0`` - CSS
     * ``1`` - SCSS

*resources*
   list of external resources

*name*
   title of the fiddle

*description*
   description of the fiddle

*normalize_css*
   yes or no - should normalize.css be loaded before any CSS
   declarations?

*wrap*
   set the JS code wrap:

   * *l* - onLoad
   * *d* - domReady
   * *h* - no wrap - in <head>
   * *b* - no wrap - in <body>  
 


Run in jsFiddle
---------------

One need to choose the framework and the Gist id using the URL:

URL: ``http://jsfiddle.net/gh/gist/{framework}/{version}/{gist_id}/``

Use ``library/pure`` for no framework:

URL: ``http://jsfiddle.net/gh/gist/library/pure/{gist_id}/``

There is an option to add dependencies as a comma separated list:

URL: ``http://jsfiddle.net/gh/gist/{framework}/{version}/dependencies/{dependency_list}/{gist_id}/``

**framework**
   the desired framework name. Which framework should be loaded with the fiddle.

**version**
   substring of the framework version - the last passing will be used. If 1.3 will be given, jsFiddle will use the latest search result. it will favorize 1.3.2 over 1.3.1 and 1.3
    
**dependency_list**
   comma separated list of dependency substrings. It would mark any dependency containing the substring.

**gist_id**
   gist id displayed in url ("http://gist.github.com/{username}/{gist_id}/")

Example
=======

Demo on the github: http://gist.github.com/606699/ 

URL to jsFiddle: http://jsfiddle.net/gh/gist/mootools/1.2/606699/

It will load the fiddle with MooTools framework in version 1.2.5
