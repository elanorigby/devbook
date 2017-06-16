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


Use Conda to maintain order among the sneks
-------------------------------------------
Conda is a package manager and also allows you to create environments that keep the packages you need for a project all neatly bundled together along with the version of Python that that project uses. Very nice.

There are two ways to get conda: through Anaconda or through Miniconda. Anaconda automatically includes a fat passel of science/maths/data packages, and if you need those you probably already know about it. Miniconda does not automatically include all that stuff so that's what I use.

Download Miniconda for your OS
    https://conda.io/docs/install/quick.html

Consider taking the whole `Conda Test Drive <https://conda.io/docs/test-drive.html>`_ but here's the basics:

to check that installation worked
::

    $ conda --version

to create a conda environment
::

    $ conda create --name <env_name> <packages>
    # ex:
    $ conda create --name testenv pip

to specify which python
::
    $ conda create --name testenv python=3.5 pip


you can use ``-n`` instead of ``--name`` if you're into that kind of thing.

I use conda as an environment manager, not as a package manager, so the only package I install with conda when I create an environment is pip. Then I install the packages I want within the environment usig pip.

see a list of your environments
::  
    $ conda info --envs

you can use ``-e`` instead of ``--envs`` if you're into that kind of thing.

to list all conda packages in an environment
::
    conda list

activate an environment
:: 
    $ source activate <env_name>

deactivate an environment
::
    $ source deactivate

*protip* ~ if 'source activate' and 'source deactivate' seem long to type, :doc:`alias </bash/bash_aliasing>` them.

to delete an environment
::
    conda remove --name flowers --all

The ``--all`` means all packages and you have to include it


Use Pip so Python doesn’t squeeze you to death
-----------------------------------------------
When you create a conda environment include pip.
::
    $ conda create --name newenv pip

Inside the environment you can then use pip to install and manage any python packages you need.

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

You'll need :doc:`pip/pip_commands` to survive.


Use Git so that you don’t lose your mind / get murdered by your co-workers
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
There are a lot of very nice resources for learning git. Here's one to get you started: https://www.atlassian.com/git


Your workflow will look something like this
---------------------------------------------
the first time you start a new project
::
    $ conda create -n baller_project pip

that and every time after
::
    $ source activate baller_project
    (baller_project)$ pip install <any packages needed>
    # work on project, committing diligently with git
    (baller_project)$ source deactivate



True, we haven't talked about how to get your environment recognized by your project, but that varies pretty widely depending on what IDE or text editor you're using. I'll get into some at some point.









