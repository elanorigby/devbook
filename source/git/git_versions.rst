Versions and how to tag them
=============================

Annotated Tags
---------------
Annotated tags are stored as full objects in the Git database. They’re checksummed; contain the tagger name, email, and date; have a tagging message; and can be signed and verified with GNU Privacy Guard (GPG). It’s generally recommended that you create annotated tags so you can have all this information; but if you want a temporary tag or for some reason don’t want to keep the other information, lightweight tags are available too.

Creating an annotated tag in Git is simple. The easiest way is to specify -a when you run the tag command::

	$ git tag -a v1.4 -m "my note about this"

The -m specifies a tagging message, which is stored with the tag. If you don’t specify a message for an annotated tag, Git launches your editor so you can type it in.

To view annotated tag deets
::
	$ git show v1.4


Lightweight Tags
-----------------

Another way to tag commits is with a lightweight tag. This is basically the commit checksum stored in a file – no other information is kept. To create a lightweight tag, don’t supply the -a, -s, or -m option::

	$ git tag v1.4


List Tags
----------
::
	$ git tag


Pushing Tags
-------------
By default, the git push command doesn’t transfer tags to remote servers. You will have to explicitly push tags to a shared server after you have created them.
::
	$ git push origin v1.5


https://git-scm.com/book/en/v2/Git-Basics-Tagging