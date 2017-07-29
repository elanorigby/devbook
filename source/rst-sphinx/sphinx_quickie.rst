Sphinx Reference stuff
=======================

build the build
----------------
If you used quickstart and have that makefile you can just do
::
	$ make html

view the html in ur browzr

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


adding a logo
--------------
add
::
	``html_logo = 'path-to-image'``
to conf.py
(alabaster says you can add 'logo' to the html_theme_options dictionary, but that didn't work for me for some reason)	

html_logo

    If given, this must be the name of an image file (path relative to the configuration directory) that is the logo of the docs. It is placed at the top of the sidebar; its width should therefore not exceed 200 pixels. Default: None.

    New in version 0.4.1: The image file will be copied to the _static directory of the output HTML, but only if the file does not already exist there.

http://www.sphinx-doc.org/en/stable/config.html



http://www.sphinx-doc.org/en/stable/markup/inline.html#

http://www.sphinx-doc.org/en/stable/markup/inline.html#ref-role

https://stackoverflow.com/questions/15394347/adding-a-cross-reference-to-a-subheading-or-anchor-in-another-page

https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html#id4
