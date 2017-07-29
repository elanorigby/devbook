irissi_intro.rst


https://irssi.org/documentation/
https://opensource.com/life/16/6/irc-quickstart-guide

connecting
::
	$ irssi
	$ /CONNECT Freenode

will be prompted for nick

set nick
::
	$ /msg NickServ REGISTER password emailaddress

identify self
::
	$ /msg NickServ IDENTIFY password

join channel
::
	$ /JOIN #python
	# or
	$ /j #python

leave channel
::
	$ /part

get out of irssi
::
	$ /exit