=====
Bash
=====

Bash Aliasing
===============

one sets an alias thusly::
	
	$ alias alias_name="command_to_run"

example::

	$ alias ll="ls -la"

``ls -la`` lists contents of current folder with details

This will only last as long as your session lasts.

To set a permanent alias open your bash_profile
::
	$ nano ~/.bash_profile

add your aliases to it, carefully not desturbing whatever else is in there.

example::

	# conda aliases
	alias sourA="source activate"
	alias sourD="source deactivate"

	# pip aliases
	alias pdt="pipdeptree"

save and exit, then restart your terminal or run 
::
	$ source ~/.bash_profile

that should do it

here's some more infos about aliasing: https://www.digitalocean.com/community/tutorials/an-introduction-to-useful-bash-aliases-and-functions


*note*: this is not how you set aliases for git. git has its own thing.