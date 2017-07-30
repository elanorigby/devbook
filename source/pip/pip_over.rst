===
Pip
===

A longer introduction to using Pip 🍎
======================================
pip is the offical package manager of PyPi - the Python Package Index. 

    https://pip.pypa.io/en/stable/

check to see if you already have it (you almost certainly do):
::

    $ pip --version

if not installed, follow directions in docs -
https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py

upgrade it
::

    $ pip install --upgrade pip

upgrading
    https://pip.pypa.io/en/stable/user_guide/#only-if-needed-recursive-upgrade

NOTE: if you are using pipenv you won't usually need any of the below

to see a list of the packages you have installed
::
    $ pip list

**OR** be a cool guy and use :ref:`pipdeptree <pipdeptree-ref>`

to install a package
::
    $ pip install <package_name>

to install a specific version of a package
::
    $ pip install Flask==0.10.1

to update a package
::
    $ pip install --upgrade <package_name>

to uninstall a package
:: 
    $ pip uninstall <package_name>

|

Some useful pip packages for development 📦
=============================================

.. _pipdeptree-ref: 

pipdeptree: a much more helpful pip list
-----------------------------------------
Shows not only packages installed, but what package installed that package and package requirements and versions

example::

	Flask==0.12
  		- click [required: >=2.0, installed: 6.7]
  		- itsdangerous [required: >=0.21, installed: 0.24]
  		- Jinja2 [required: >=2.4, installed: 2.9.5]
      - MarkupSafe [required: >=0.23, installed: 1.0]
  		- Werkzeug [required: >=0.7, installed: 0.12]
	pip-tools==1.9.0
  		- click [required: >=6, installed: 6.7]
  		- first [required: Any, installed: 2.0.1]
  		- six [required: Any, installed: 1.10.0]
	pipdeptree==0.10.1
  		- pip [required: >=6.0.0, installed: 9.0.1]

to install::

	$ pip install pipdeptree

to use::
	
	$ pipdeptree

OR do yourself a favor and :doc:`alias <../bash/bash_aliasing>` it.
