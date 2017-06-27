A basic Python development environment on Mac
=============================================


Install Xcode and command line tools because you’ll have to at some point anyway
--------------------------------------------------------------------------------

In your terminal, check if command line tools installed / install them
::
    $ xcode-select --install

open the appstore and search for xcode. install it.

install extra components / agree to stuff


Install Homebrew so you don’t hate your life
--------------------------------------------
Homebrew is a package manager for OSX. You want your packages to be managed.

open your terminal, paste this in
::
    $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

..
    reference - http://brew.sh/


if permissions need fixing
::
    $ sudo chown -R "$USER":admin /usr/local # or whatever the dir in question is

..
    reference - https://github.com/Homebrew/brew/blob/master/docs/FAQ.md


Install pyenv with Homebrew to manage your python versions
----------------------------------------------------------------------
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

    https://github.com/pyenv/pyenv/blob/master/README.md


make sure you have pip so Python doesn’t squeeze you to death
------------------------------------------------
pip is the offical package manager of PyPi - the Python Package Index. If you want to use a library/package that is not in the standard library (which you will) you need this.

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


Install virtualenv because you don't sh\*t where you eat
---------------------------------------------------------
::

    pip install virtualenv

..

    reference - http://docs.python-guide.org/en/latest/dev/virtualenvs/ 


Cleanse your soul in the waters of pipenv
-------------------------------------------






Use Git so that you don’t lose your mind / get murdered by your co-workers
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
There are a lot of very nice resources for learning git. Here's one to get you started: https://www.atlassian.com/git









