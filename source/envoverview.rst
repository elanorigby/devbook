A basic Python development environment on Mac 
=============================================


Install Xcode and command line tools because you’ll have to at some point anyway 🤷🏻‍♀️
----------------------------------------------------------------------------------------

In your terminal, check if command line tools installed / install them
::
    $ xcode-select --install

open the appstore and search for xcode. install it.

install extra components / agree to stuff

|

Install Homebrew so you don’t hate your life 🍺
--------------------------------------------------
Homebrew is a package manager for OSX. You want your packages to be managed.

open your terminal, paste this in
::
    $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

..
    Homebrew docs - http://brew.sh/


if permissions need fixing
::
    $ sudo chown -R "$USER":admin /usr/local # or whatever the dir in question is

..
    reference - https://github.com/Homebrew/brew/blob/master/docs/FAQ.md

|

Use Pyenv to keep your sneks in a row 🐍🐍🐍
---------------------------------------------------
::

    $ brew install pyenv

add ``eval "$(pyenv init -)"`` to your bash_profile.

This can be done by running::

    $ echo 'eval "$(pyenv init -)"' >> ~/.bash_profile

resart your shell
::
    $ exec $SHELL

install the python version(s) you want. 
::
    $ pyenv install 3.5.3
    $ pyenv install 3.6.1

set global(default) version of python
::
    $ pyenv global 3.5.3

you can see all available versions with ``pyenv install --list``.

    reference - https://github.com/pyenv/pyenv/blob/master/README.md

|

Make sure you have Pip so Python doesn’t squeeze you to death 💀
-------------------------------------------------------------------
Pip is the offical package manager of PyPi - the Python Package Index. If you want to use a library/package that is not in the standard library (which you will) you need this.

    Pip docs - https://pip.pypa.io/en/stable/

check to see if you already have it (you almost certainly do):
::
    $ pip --version

if not installed, follow directions in docs -
https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py

upgrade it
::
    $ pip install --upgrade pip

..

    reference - https://pip.pypa.io/en/stable/user_guide/#only-if-needed-recursive-upgrade

The other stuff I've written about pip is :doc:`here <pip/pip_over>`.


|

Use Virtualenv because you don't 💩 where you eat
--------------------------------------------------------
This is a tool to make ✨isolated environments✨ so you can keep your projects' dependencies separate and tidy and they don't junk up your system and create version conflicts and general badness and eventual sorrow.
::
    $ pip install virtualenv

..

    reference - http://docs.python-guide.org/en/latest/dev/virtualenvs/ 

|

Cleanse your soul in the waters of Pipenv 🐋
----------------------------------------------
Pipenv is how you're going to interact with virtualenv and pip 99.999% of the time probably. It gives you easy ways to create and manage your virtualenvs and keeps track of the packages you install in them using the shiny new delicousness that is Pipfile.
    
Begin
:: 
    $ pip install pipenv

When you want to create a new pipenv, ``cd`` into the :ref:`directory <directory_ref>` of the project you're starting, then 
::
    $ pipenv install

This will create a virtualenv associated with that project, and automatically create a Pipfile and a Pipfile.lock in that directory. 

When you want to add packages::

    $ pipenv install <package_name>

This will install the package to the virtualenv and also add it to the Pipfile. It's probably a good idea to make a fresh lock every time you add a package becuase you're thinking about it now go ahead and do it. This is how - 
::
    $ pipenv lock

This updates Pipfile.lock which is what pipenv will use to install the packages in your pipfile in a new environment. You, or someone else setting up your project, can copy this pipfile.lock into a directory, run ``pipenv install`` and all the specified packages will be installed into a virtualenv exactly like you have in the original one. 

If you only need a package for development, such as a testing library::

    $ pipenv install --dev pytest

Doing this means that if someone installing this project's dependencies isn't going to be doing dev stuff, they can run ``pipenv install`` and pytest will not be installed. 

To get the development packages as well as the rest, run
::
    $ pipenv install --dev
   

If you don't need a package anymore
::
    $ pipenv uninstall <package_name>

To actually activate the virtualenv
::
    $ pipenv shell

You'll need to activate the pipenv shell when you need to run any of the packages you have installed, such as testing suites, or interface with databases from the command line, and stuff like that.

If you were previously using virtualenvwrapper, here are :doc:`pipenv/pipenv_v_wrapper`.


    Pipenv docs - http://docs.pipenv.org/en/latest/


|

Use Git so that you don’t lose your mind 🗡 get murdered by your co-workers 
----------------------------------------------------------------------------
There are a lot of very nice resources for learning git. Here's one to get you started: https://www.atlassian.com/git

The other stuff I've written about git is :doc:`here <git/git_over>`.

