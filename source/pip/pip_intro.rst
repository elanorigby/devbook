Use pip so Python doesn’t squeeze you to death
================================================
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

You'll need :doc:`pip_commands` to survive.
