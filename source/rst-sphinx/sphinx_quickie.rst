Sphinx Reference stuff
=======================

build the build
-----------------
::	
	$ sphinx-build -b html source build

where source is the source directory, and build is the directory in which you want to place the built documentation. The -b option selects a builder; in this example Sphinx will build HTML files.

make the html
::
	$ make html

view the html in ur browzr

unless you add new directories (and files?) you can just keep running make html to update


link to a doc (sphinx only)
---------------------------
:: 
	``:doc:`pip/pip_commands```



http://www.sphinx-doc.org/en/stable/markup/inline.html#

http://www.sphinx-doc.org/en/stable/markup/inline.html#ref-role

https://stackoverflow.com/questions/15394347/adding-a-cross-reference-to-a-subheading-or-anchor-in-another-page

https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html#id4