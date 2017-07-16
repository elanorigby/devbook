Git Tips
==========

Unstage file changes
---------------------
::
	$ git reset HEAD <filePath>


Resolve merge conflict
-----------------------
https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/


Add all currently untracked files to .gitignore
------------------------------------------------
::
	$ git status -s | grep -e "^\?\?" | cut -c 4- >> .gitignore
..
	https://stackoverflow.com/questions/15862598/how-to-add-all-currently-untracked-files-folders-to-git-ignore

Add file/dir to .gitignore without opening it
----------------------------------------------
::
	$ echo 'file-name' >> .gitignore
..
	http://www.tilcode.com/how-to-quickly-add-lines-to-gitignore-using-the-command-line/


Extra links
............

https://dev.to/gonedark/tweak-your-terminal-for-git

https://csswizardry.com/2017/05/little-things-i-like-to-do-with-git/

http://marklodato.github.io/visual-git-guide/index-en.html