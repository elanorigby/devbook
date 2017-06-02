More and alternate Virtualenv install infos
============================================

This can be done in a fell swoop with

``pip install virtualenv-burrito``

now a moment of gratitude to the person who created virtualenv-burrito
and saved you 15 minutes of figuring out exactly what to add to your
bash profile - https://github.com/brainsik/virtualenv-burrito

check that it worked by running

``workon``

if that doesn’t error you, make a test virtualenv

``mkvirtualenv testvenv``

run ``workon`` again to see list of virtualenvs. (It should just have
``testvenv`` in it)

to turn on the virtualenv, run

``workon testvenv``

turn off the virtualenv with

``deactivate``

delete the virtualenv with

``rmvirtualenv testvenv``


If virtualenv-burrito doesn't work for some reason
-----------------------------------------------------

``pip install virtualenv``

	reference - http://docs.python-guide.org/en/latest/dev/virtualenvs/

``pip install virtualenvwrapper``

	reference - https://virtualenvwrapper.readthedocs.io/en/latest/install.html

add (some permutation of) this to your bash profile::

	# adding usr/local to path -- you might not need to do this
	export PATH=/usr/local:$PATH

	# default python for new virtualenvs 
	export VIRTUALENVWRAPPER_PYTHON=""
	# "" will set it to "$(command \which python)"S
	
 	# directory your virtualenvs will go in
	export WORKON_HOME=$HOME/.virtualenvs 

	# directory you keep your projects in
	export PROJECT_HOME=$HOME/code  

	source /usr/local/bin/virtualenvwrapper.sh


then restart the bash profile by running

``source ~/.bash_profile``

