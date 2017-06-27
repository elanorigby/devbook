How does virtualenv, like, work, though?
=========================================

Virtualenv makes fully isolated environments for your convenience and pleasure.

A fully isolated environment, in the context of developing on your computer, means that the system ``site-packages`` are ignored, and the ``site-packages`` in a specific place are used. 

Site packages are third party modules and ``site-packages`` is the name of the directory in which they live. 

Third party modules means anything not included in the Python standard libaray. Basically anything you install with pip or pipenv, take from github, easy-install, etc.

When Python starts, a module called ``site.py`` in the standard library looks for what to set ``sys.prefix`` as. Basically, a virtualenv redirects ``sys.prefix`` away from your system Python (the one that came with your computer\*) and gives one that will lead it to use your virtualenv packages.


https://virtualenv.pypa.io/en/stable/


http://pyvideo.org/pycon-us-2011/pycon-2011--reverse-engineering-ian-bicking--39-s.html


\* Unless you're on windows. No sneks on windows unless you put them there. 