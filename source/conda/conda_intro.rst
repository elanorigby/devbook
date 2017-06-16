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