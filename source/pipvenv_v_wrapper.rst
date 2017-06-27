A few differences to wrap your brain around as you move from virtualenvwrapper to pipenv:
==============================================================================================

..
- Virtualenvwrapper - one can call ``workon venv_name`` from anywhere and that virtualenv will be activated.
- Pipenv - your virtual environments do not have names. You must be in the same directory as a pipfile and then run ``pipenv shell`` to activate the environment that the pipfile describes.

..
- Virtualenvwrapper - you must have the environment activated to install pip packages in it.
- Pipenv - you can use ``pipenv install <package>`` when the environment is not activated and the package will be added to the virtualenv associated with the pipfile in your directory. (Do it this way when the environment is activated, too. Plain ol' pip install won't add packages to your pipfile. Yet.)

..
- Virtualenvwrapper - If you want to associate the directory with your project files in with your virtualenv, you've got to  explicitly set it up and use different commands. 

	https://virtualenvwrapper.readthedocs.io/en/latest/command_ref.html#project-directory-management
- Pipenv - Where the pipfile resides, there be the project directory. (Pipenv does honor your ``WORKON_HOME``, however.)






