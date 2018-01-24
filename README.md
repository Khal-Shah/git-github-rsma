# git-github-rsma
testing
date: 01-18-2018

First create remote repo (central repository) on github (soen341, already done)

How to sync repos:

Create a folder on your computer where you wanna keep the files.

initialize local repository (your computer) with: terminal ==> 'cd path_name_of_folder git init'

After creating local repo, link it (to online repo on github) so you can pull all the files/changes from remote repo:

•Use command 'git remote add origin "link_address"' to add remote repo...the link can be found on the github repo ("Clone or Download" buttoon).

•Pull files with command 'git pull'

ex: 'git pull origin master' (will fetch/update files from remote to local repo)

•Push your own changes into central repo with 'git push' (read below)


Making Changes:

There is an intermediary layer between your workspace and local repo
To commit changes into local repo, those files must be added to index first.

git status: tells you which files are added to index and are ready to commit

git add: lets you add files to your index

git add -A (to add all new files to index)

git commit: after adding to index, lets you make changes to local repo

Ex: git commit -m "description"

git commit -a -m "message" to commit all the files
For files that have already been added to index but modified after, you could do without re-adding them, just git commit -m will do (or git commit -a -m "for multiple modified files at once".

finally use git push to push it to central repo

Branching:

to create new branch: git branch branchName

to move to another branch: git checkout nameOfBranchYouWannaMoveTo
(checks out from the branch you were on and moves to another branch).

Merging:

files created in another branch would not show up on the masters branch, so if I wanna merge it with the master branch I would have to: go to the destination branch (Master) then...git merge branchYouWannaMergeWith
