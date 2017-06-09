Some useful pip packages for development
========================================

pipdeptree
----------
a more informative version of ``pip list`` - 
it shows not only packages installed, but what package installed that package and package requirements and versions

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

OR do yourself a favor and alias it::

	$ alias pdt="pipdeptree"
	$ pdt


https://www.digitalocean.com/community/tutorials/an-introduction-to-useful-bash-aliases-and-functions

