# trial-and-error
repo for experimenting with git &amp; this website\
>_if you are reading this ur mom gay_

## hello
<br>

* lorem ipsum dolor sit on chair. Set temper element remaster, this is not actual lorem sorry.

# git bash terminal cheat sheet

* ## navigating directories

> cd `path`

steps into a folder (parent folder with `../` or sibling folder with `../path`)

> ls `filename`

searches for files with filename name in directory

> ls -lah

gives you all the items in the folder (-l long-listing format, -a shows all, -h shows file size in human-readable format)

> cat `filename`

writes a file to the terminal (i think?)

<br>

* ## making new github repo

> mkdir `directory name`

creates a folder in the terminal's directory (you need to move into it with cd `directory name`)

> git init

initializes a new empty git repo in current directory (creates .git folder)

> git add `filename`

adds a file to the git repo. filename can be `.` which adds all. files need to be added before committing.

> git remote add `origin` `link`

connects the new repo to the link of a github repo

> git remote -v

list the active origin repo

<br>

* ## working on a github repo

> git clone `link`

clones a repo from git to local machine, used for the first time

> git pull

updates your local repo to the remote repo, used to get back to work

> git fetch

syncs your remote-tracking branch to the remote branches. git fetch + git merge = git pull

> git status

tells you if files are committed or not

> git commit -m "`change title`" -m"`change description`"

commits a file locally (after saving it with ctrl+s) so git knows that it changed

> git push -u origin main (later: git push)

set the default git push to origin main & publish committed changes to the github repo  
-u = --set-upstream

<br>

* ## authentication

> ssh-keygen -t rsa -b 4096 -C "`email address`"  

create an SSH key named `id_rsa` by default, identified by `email address` 

> eval "$(ssh-agent -s)"  
ssh-add ~/.ssh/`id_rsa`

Authorize this machine on the `email address`'s github account using `id-rsa` private key

<br>

* ## git branches

> git branch

lists local branches, places `*` before the branch you are on

> git checkout `branchname`

switch to an existing branch

> git checkout -b `branchname`

builds a new branch & switch to it

> git diff `branchname`

shows what code changed on current branch compared to branchname

> git merge `branchname`

merge branchname into this branch (only used locally, remotely you make pull requests instead)

> git branch -d `branchname`

delete branch LOCALLY

> git push `origin` --delete `branchname`

delete branch REMOTELY

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

