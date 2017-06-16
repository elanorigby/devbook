Extra more Virtualenv stuff 
===========================

There is a lot you can do with virutalenv courtesy of its soulmate, virtualenvwrapper.
Check the docs for a full list. 
	https://virtualenvwrapper.readthedocs.io/en/latest/#

Useful commands
----------------
list all virtualenvs
::

	$ workon

if you have a project (see below) associated with your virtuaenv, you can change to that diretory with
::

	$ cdproject


delete the virtualenv with
::

    $ rmvirtualenv <venv_name>


List of all the commands
	http://virtualenvwrapper.readthedocs.io/en/latest/command_ref.html

Project Directories
---------------------
To associate a directory with a virtualenv use ``mkproject`` instead of ``mkvirtualenv``
::
	cd <directory_of_project>
	mkproject <venv_name>

To bind an existing project directory to a virtualenv, use ``setvirtualenvproject``
::
	cd <directory_of_project>
	setvirtualenvproject <virtualenv_path project_path>

..

	http://virtualenvwrapper.readthedocs.io/en/latest/projects.html

Templates
-------------
Automatically create a new project/virtualenv from an existing template
::
	mkproject -t <template_name> <venv_name>
	
..
	
	https://virtualenvwrapper.readthedocs.io/en/latest/projects.html#using-templates

Choose from templates others have made, like the django template
	http://virtualenvwrapper.readthedocs.io/en/latest/extensions.html#extensions-templates

Or make your own template for your own nefarious porpoises
	http://virtualenvwrapper.readthedocs.io/en/latest/developers.html#developer-templates


Other helpful links
-------------------

	http://docs.python-guide.org/en/latest/dev/virtualenvs

