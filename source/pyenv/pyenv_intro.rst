Install pyenv with Homebrew to manage your Python versions
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

    https://stackoverflow.com/questions/29950300/what-is-the-relationship-between-virtualenv-and-pyenv