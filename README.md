# trial-and-error
repo for experimenting with git &amp; this website\
>_if you are reading this ur mom gay_

## hello
<br>

* lorem ipsum dolor sit on chair. Set temper element remaster, this is not actual lorem sorry.

# git bash terminal cheat sheet

<br>

* ## terminal navigation

> pwd

prints working directory path (where the terminal is)

> cd `path`

change directory to 'path' (parent folder with `../` or sibling folder with `../path`)

> mkdir `directory name`

creates a folder in the terminal's directory

> cp -r `directory name` `target directory`

copies a directory to 'target directory'

> rm -r `directory name`

removes a directory & all contents

> touch `filename.ext`

makes sure that 'filename' file with 'ext' filetype exists in the directory.  
creates the file if missing, else updates modification time 

> cp `filename.ext` `target directory`

copies a file to 'target directory'

> rm `filename.ext`

removes a file

> ls `filename`

searches for files with 'filename' name in directory

> stat `path`

shows the properties of files & dirs at 'path' such as size, type, content count, raw(read-append-write) rights, modification dates, etc.  
'stat `.`' for current dir

> ls -lah

shows properties of all items in directory  
(-l long-listing format, -a shows all, -h shows file size in human-readable format)

> cat `filename.ext`

con**cat**enates & writes the content of a file to the terminal

> explorer `path`

opens file explorer at 'path'
('path' can be `.` which opens current directory)

<br>

* ## making new github repo

> mkdir `directory name`

creates a folder in the terminal's directory (you need to move into it with 'cd directory name')

> git init

initializes a new empty git repo in current directory (creates .git folder)

> git add `filename`

adds a file to the git repo. 'filename' can be `.` which adds all. files need to be added before committing.

> git remote add `origin` `link`

connects the new repo to the link of a github repo

> git remote -v

list the active origin repo

<br>

* ## working on a github repo

> git clone `link`

clones a repo from git to local machine, used for the **first time**

> git pull `origin` `main`

updates your local repo to the remote repo, used **regularly** to get back to work  
default behaviour (git pull): git fetch origin HEAD && git merge HEAD

> git fetch `origin` `main`

syncs your remote-tracking branch to the remote branches.  
use git merge 'origin/main' to update local repo (=git pull)

> git status

tells you if files are committed or not

> git add `.`

adds all files in repo to git

> git commit -am "`change title`" -m"`change description`"

makes a commit locally (after saving it with ctrl+s) for git. -a adds and commits in one, to skip 'git add .'

> git push (-u `origin` `main`) (later: git push)

set the default git push to 'origin main' & publish committed changes to the github repo  
-u = --set-upstream

> saving shorthand: `git commit -am" " && git push`

<br>

* ## authentication

> ssh-keygen -t rsa -b 4096 -C "`email address`"  

create an SSH key named 'id_rsa' by default, identified by 'email address' 

> eval "$(ssh-agent -s)"  
ssh-add ~/.ssh/`id_rsa`

Authorize this machine on the 'email address' github account using 'id-rsa' private key

<br>

* ## git branches

> git branch

lists local branches, places `*` before the branch you are on

> git checkout `branchname`

switch to an existing branch

> git checkout -b `branchname`

builds a new branch & switch to it

> git diff `branchname`

shows what code changed on current branch compared to 'branchname'

> git merge `branchname`

merge 'branchname' into this branch (only used locally, remotely you make pull requests instead)  
you should be **ON** 'main' and git merge 'sidebranch'

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

rolls back the version to a previous commit identified by 'hash'  
OR previous commit  
OR the commit 'int' (number) away from the current version  
AND unstages the commits (but keeps it on your computer to commit again)

> git reset --hard `hash or other id`

rolls back to a previous version and changes local files back to that version  
making it impossible to commit them again. you continue work from the older commit.

