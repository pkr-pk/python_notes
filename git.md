`git clone <url> [where to clone]` - clone repository to given location

`git config --list` - print list of settings

`git config --global user.name "user name"` - change username

`git config --global user.email "user email"` - change user email

`git help <verb>` - help

`git <verb> --help` - help

`git add -A` - add all files to staging area

`git status` - check git status

`git reset [filename]` - remove given file from staging area

`git reset` - remove all files from staging area

`git commit -m "message"` - commit changes

`git log` - print log

`git remote -v` - print repository info

`git branch -a` - print all branches (local and remote)

`git branch <branch name>` - create new branch

`git branch --merged` - print merged branches

`git branch -d <branch name>` - delete given branch on local

`git checkout <branch name>` - checkout to given branch

`git diff` - print changes in files

`git fetch` - fetch all new branches on local

`git pull` - download changes from remote to local for currently activated branch

`git push -u origin <branch name>` - upload changes on server for currently activated branch (use only when branch was created on local)

`git push` - upload changes on server for currently activated branch

`git push origin --delete <branch name>` - delete given branch on remote

**&nbsp;**

`git checkout <file name>` - remove ale changes for given file in working directory

`git commit --amend -m "message"` - change last commit (NOTE: change id of the commit and thus history)

`git commit --amend` - add files from staging area to the last commit (NOTE: change id of the commit and thus history)

`git cherry-pick <id>` - add commit to currently activated branch (do not delete commit from other branch)

`git reset --soft <id>` - delete all commits up to the one selected (selected one stays), tracking changes will be kept in staging area

`git reset <id>` - delete all commits up to the one selected (selected one stays), tracking changes will be kept in working directory

`git reset --hard <id>` - delete all commits up to the one selected (selected one stays), tracking changes will be deleted

`git clean -df` - delete all untacking changes (d - directories, f - files)

`git revert <id>` - create new commit which will undo all changes in the listed commits (not modify history but add a new commit)

`git reflog` - shows the entire log, including removed commits (protection when we delete something by accident)

Using the reflog (after restoring the commit branch will be unpinned from the HEAD and need to be pinned again):

`git checkout <id>`

`git branch <branch name>`

**&nbsp;**

`git stash save "message"` - move changes to clipboard (`git stash` is enough)

`git stash list` - show a list of changes saved in the clipboard

`git stash apply <id>` - take the changes from the clipboard but not delete them in clipboard

`git stash pop` - takes the last data from the clipboard and delete it in the clipboard

`git stash drop <id>` - delete changes in the clipboard

`git stash clear` - delete everything from the clipboard (NOTE)

**&nbsp;**

`git -c user.name="<user name>" -c user.email=<user email> commit --amend --reset-author` - overwrite user for last commit

`git gc --prune=now` - solve reference problem 
