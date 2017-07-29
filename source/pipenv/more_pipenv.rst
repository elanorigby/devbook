more Pipenv tidbits
=====================

Pipenv will name the virtualenv <name_of_project_dir>-<somestringofcharacters>
Example:  ~/.virtualenvs/ponyproj-7wj1n8cd

If you are connecting a pipenv as a project interpreter in Pycharm, this will be useful to know. 


Why keep virtualenvs together in a specific directory? 
Because 
 - you don't want to distribute the virtualenv, you want to distribute what it needs (pipfile)
 - moving a dir with a virtualenv in it will mess things up for you

- https://stackoverflow.com/questions/12184846/where-should-virtualenvs-be-created