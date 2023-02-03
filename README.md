# trial-and-error
repo for experimenting with git &amp; this website\
>_if you are reading this ur mom gay_

## hello
<br>

* lorem ipsum dolor sit on chair. Set temper element remaster, this is not actual lorem sorry.

# git bash terminal cheat sheet

* ## navigating directories

> cd `path`

steps into a folder (parent folder with `../` or siblibg folder with `../path`)

>ls `filename`

searches for files with filename name in directory

> ls -la

gives you all the items in teh folder

> cat `filename`

writes a file to the terminal (i think?)

<br>

* ## working on a github repo

> git clone `link`

clones a repo from git to local machine

> git status

tells you if files are committed or not

> git commit -m "`change title`" -m"`change description`"

commits a file locally (after saving it with ctrl+s) so git knows that it changed

> ssh-keygen -t rsa -b 4096 -C "`email address`"  
eval "$(ssh-agent -s)"  
ssh-add ~/.ssh/`id_rsa`

create an SSH key named `id_rsa` to authorize this machine on the `email address`'s github account

> git push -u origin main (later: git push)

set the default git push to origin main & publish committed changes to the github repo  
-u = --set-upstream

<br>

* ## making new github repo

> git init

initializes a new empty git repo

> git add `filename`

adds a file to the git repo. filename can be `.` which adds all. files need to be added before committing.

> git remote add origin `link`

connects the new repo to the link of a github repo

> git remote -v

list the active origin repo

<br>

* ## git branches

> git branch

the branch you are on

> git checkout `branchname`

switch to an existing branch

> git checkout -b `branchname`

create a new branch & switch to it

> git diff `branchname`

shows what code changed on this branch compared to branchname

> git merge `branchname`

merge branchname into this branch (scarcely used)

<br>

* ## roll back to previous commit

> git log

gives a list of commits and their hash

> git reset `hash`  
> git reset HEAD  
> git reset HEAD~`int`

rolls back the version to a previous commit identified by hash  
OR previous commit  
OR the commit int (number) away from the current version  
AND unstages the commits (but keeps it on your computer to commit again)

> git reset --hard `hash or other id`

rolls back to a previous version and changes local files back to that version  
making it impossible to commit them again. you continue work from the older commit.

