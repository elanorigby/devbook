Use Conda to maintain order among the sneks
=============================================
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




Should I use Conda instead?
===========================

Conda allows you to create environments that keep the packages you need for a project all neatly bundled together along with the version of Python that that project uses. Very nice.

There are two ways to get Conda: through Anaconda or through Miniconda. Anaconda automatically includes a fat passel of science/maths/data packages, and if you need those you probably already know about it. Miniconda does not automatically include all that stuff so that's what I use.


I am checking out Conda to have one tool that 

1. manages python versions (instead of pyenv)
2. creates virtual environments (instead of vitualenv)

I'm using Miniconda because I do not need the vast array of mathy/sciency tools that Anaconda automatically installs for you. 

I am going to use conda to replace pyenv and virtualenv, but continue to use pip for all my package installs. This is for simplicity, and also so that I can continue to use my true dev loves, pipdeptree and pip-tools. 


Install Miniconda 
-------------------------
https://conda.io/docs/install/quick.html

Take the tour
----------------------
https://conda.io/docs/test-drive.html

Hook it up to your text editor or IDE
-------------------------------------

	Sublime Text
		https://stackoverflow.com/questions/34865717/use-conda-environment-in-sublime-text-3

More Infos
++++++++++
https://jakevdp.github.io/blog/2016/08/25/conda-myths-and-misconceptions/