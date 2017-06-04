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


Install pyenv with Homebrew to manage your Python versions
----------------------------------------------------------------------
::

    $ brew install pyenv

add ``eval "$(pyenv init -)"`` to your bash_profile.

This can be done by running::

    $ echo 'eval "$(pyenv init -)"' >> ~/.bash_profile

refresh
::
    $ source ~/.bash_profile

install the python version(s) you want. 
::
    
    $ pyenv install 2.7.13
    $ pyenv install 3.5.3
    $ pyenv install 3.6.1

set global(default) version of python
::

    $ pyenv global 3.5.3

you can see all available versions with ``pyenv install --list``.

References:
    https://github.com/pyenv/pyenv/blob/master/README.md

    https://stackoverflow.com/questions/29950300/what-is-the-relationship-between-virtualenv-and-pyenv

Use Pip so Python doesn’t squeeze you to death
-----------------------------------------------

    https://pip.pypa.io/en/stable/

check to see if you already have it (you almost certainly do):
::

    $ pip --version

if not installed, follow directions in docs -
https://pip.pypa.io/en/stable/installing/#installing-with-get-pip-py

upgrade it
::

    $ pip install --upgrade pip


Install Virtualenv and Virtualenvwrapper so you can achieve a semblance of organization
---------------------------------------------------------------------------------------
::

    pip install virtualenv

..

    reference - http://docs.python-guide.org/en/latest/dev/virtualenvs/
::
    
    pip install virtualenvwrapper

..

    reference - https://virtualenvwrapper.readthedocs.io/en/latest/install.html

add (some permutation of) this to your bash profile::

    # add usr/local to path -- you might not need to do this
    # you can check your $PATH with echo $PATH
    export PATH=/usr/local:$PATH

    # set default python for new virtualenvs
    export VIRTUALENVWRAPPER_PYTHON=""
    # (will set it to "$(command \\which python)")
    
    # set directory your virtualenvs will go in
    export WORKON_HOME=$HOME/.virtualenvs 

    # set directory you keep your projects in
    export PROJECT_HOME=$HOME/code  

    source /usr/local/bin/virtualenvwrapper.sh


then restart the bash profile by running
::
    $ source ~/.bash_profile

check that it worked with
::

    $ workon

if that doesn’t error you, make a test virtualenv
::

    $ mkvirtualenv testvenv

run ``workon`` again to see list of virtualenvs. (It should just have
``testvenv`` in it)

to turn on the virtualenv, run
::
    
    $ workon testvenv

turn off the virtualenv with
::

    $ deactivate


**Adjust virtualenvwrapper slightly to work with pyenv**

change the VIRTUALENVWRAPPER_PYTHON in your bash_profile to "", if it's not that already
::
    
    $ export VIRTUALENVWRAPPER_PYTHON=""

This sets the default python for new virtualenvs to the output of the ``which python`` command. This means that we can change the pyenv global python::

    $ pyenv global 3.6.1

before creating a new environment with ``mkvirtualenv`` and the new environment will use the python version that was global when it was created

example/demonstration/proof::
    
    $ pyenv global 3.6.1
    $ python -V 
    >> Python 3.6.1
    $ mkvirtualenv threesixone
    $ deactivate
    $ pyenv global 3.5.3
    $ python -V 
    >> Python 3.5.3
    $ workon threesixone
    $ python -V 
    >> Python 3.6.1



*disclaimer:* this is not, as far as I am aware, an officially condoned way of cobining pyenv and virtualenv/wrapper. But I like it and so far it has been good to me.

`pyenv-virtualenv <https://github.com/pyenv/pyenv-virtualenv>`_ and `pyenv-virtualenvwrapper <https://github.com/pyenv/pyenv-virtualenvwrapper>`_ are things that you can check out for a more official version of how these should work together.


Use Git so that you don’t lose your mind / get murdered by your co-workers
--------------------------------------------------------------------------

There are a lot of very nice resources for learning git. Here's one to get you started: https://www.atlassian.com/git


