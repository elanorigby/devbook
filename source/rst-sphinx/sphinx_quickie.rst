Sphinx Reference stuff
=======================

build the build
----------------
If you used quickstart and have that makefile you can just do
::
	$ make html

& view the html in ur browzr

if you didn't quickstart
::	
	$ sphinx-build -b html source build

where source is the source directory, and build is the directory in which you want to place the built documentation. The -b option selects a builder; in this example Sphinx will build HTML files.


clean out build
----------------
Delete the build cache before building documents if you make changes in the code by running
::
	$ make clean

if you didn't quickstart for some reason
::
	$ sphinx-build -E

link to a doc 
--------------

:: 
	``:doc:`folder/file```

|

link to arbitray reference point
---------------------------------
Create the reference in the place you want to link to::
	``.. _ref_title:``

if this is placed right before a title it will automatically use that title as the text-to-show, unless other is specified. If the lable isn't before a title, you must include text-to-show when you reference it.

Put this in the place you want the link::
	``:ref:`text-to-show <ref_title>```
	or
	``:ref:`ref_title```

|

adding a logo
--------------
Max width: 200px
Put the logo file in the _static directory and add
::
	``html_logo = 'path-to-image'``

to conf.py

(alabaster says you can add 'logo' to the html_theme_options dictionary, but that didn't work for me for some reason)	

|

WATCH OUT for these ones
-------------------------
 - there must be a blank line or something between the ``::`` of a literal block and the ----/whatever underlining a title for the literal block to work



http://www.sphinx-doc.org/en/stable/config.html

http://www.sphinx-doc.org/en/stable/markup/inline.html#

http://www.sphinx-doc.org/en/stable/markup/inline.html#ref-role

https://stackoverflow.com/questions/15394347/adding-a-cross-reference-to-a-subheading-or-anchor-in-another-page

https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html#id4
