# How-to-use
------------------------------------------------------------------------------------------
Setting up Sublime
Open Terminal and
For Sublime-Text-2: sudo add-apt-repository ppa:webupd8team/sublime-text-2 && sudo apt-get update && sudo apt-get install sublime-text
For Sublime-Text-3: sudo add-apt-repository ppa:webupd8team/sublime-text-3 && sudo apt-get update && sudo apt-get install sublime-text-installer
:Can launch sublime from the terminal with subl or sublime-text 
-------------------------------------------------------------------------------------------
Installing Git
https://git-scm.com/downloads
-------------------------------------------------------------------------------------------
Configuring Git (One time)
1. git config --global credential.helper 'cache --timeout=3600': Set the password cache to timeout after 1 hour (setting is in seconds)
2. git config --global color.ui auto: apply text colors for insertion/deletion of code
3. git config --global core.editor "subl -n -w": use sublime to edit Git Edit Info (ex. commit message)
4. Put [git-prompt.sh] [git-completion.bash] [.bashrc] files in home directory: configure terminal for git purpose
* If .bashrc file already exists in home directory, copy and paste at the end of the existing .bashrc file
5. git config --global push.default upstream
6. git config --global merge.conflictstyle diff3
7. git config --global user.name "Your Name"
8. git config --global user.email you@example.com
---------------------------------------------------------------------------------------------
Initializing Git & Uploading files to the Repository
1. Go to a folder where you want to make it a new Git
2. git init: make a new git (.git folder is included): whatever files were in that folder (or created) are untracted files 
* 3 stage of Git: working directory (untracted files) --> staging area --> repository
3. git status: show which files in working direcotry have been modified/added to staging area or remaining in the working directory
4. git add <fileName>: add <fileName> (untracted files) to staging area
* git reset <fileName>: remove (undo) <fileName> from staging area
* git reset --hard: undo every changes made to working directory and staging area (reset git diff & git diff --staged)[careful]
5. git status
6. git commit: commit files in staging area to repository (upload)
7. git log: show hisotry(versions) of repository (press q to quit)
* git log --stat: gives statistics about which files were affected
* git log -n 1: show most recent commit(head)'s log 

Removing Files from Repository
1. git rm <fileName>: will remove <fileName> from both staging area and working directory
* git rm --cached <fileName>: will only remove <fileName> from staging area
2. git commit -m "remove <fileName>": commit changes to repository

Comparing Files
git diff: show what has been modified after modifying files in working directory (before adding to staging area)
git diff --staged: show differences between most recently committed files (most recent commit) (Head) in repository and files in staging area
git diff <ID number> <ID number>: show differences between versions of repository
---------------------------------------------------------------------------------------------
Making a Branch & Merging Branches
1. git branch: show what branches are present
* git branch -a: show all branches including ones on git hub
* Branch with * symbol indicates currently checked out branch: updates will be applied to that branch
2. git branch <branchName>: create a branch named <branchName>
3. git checkout <branchName>: switch current branch to <branchName>
* git checkout -b <branchName>: create and switch to the <branchName>
4. Add & Commit new files
* git log --graph --oneline <branch name> <branch name> ... <branch name>: shows log for entire branch in timeline
5. git merge <branchName1> <branchName2>: merge branchName2 to branchName1
6. git show <ID number>: show diff btwn the ID number with its parent 
7. git branch -d <branchName>: delete <branchName> branch (only the label, not the commits)
* If merge conflict occurs (same file is modified by different branches) branch name will contain "+|MERGING". 
   --> Resolve the file with conflict --> add it to staging area and commit. 
---------------------------------------------------------------------------------------------

1. git remote: show existing remote repository
2. git remote add <remote> <github repository address>: add a remote repository named <remote> (usually 'origin') on GitHub
3. git remote -v: show more info (where to fetch & push) about remotes 
git push <remote> <branch>: push <branch> to <remote> --> upload branch on remote
git pull <remote> <branch>: download (update) branch from remote
git fetch origin: latest origin (github) will be updated on local (git)
fork: fork other person's github page to your github page

Adding a Repository to Github:
Initialize a repository on Github
git remote add origin <github repository address>
upload files on local (git)
git push origin master
--------------------------------------------------------------------------------------------------


git clone <https://...>: clone a github page


