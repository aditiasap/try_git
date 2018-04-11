Init

- git init
- git status
- git add fil.txt
- git status
- git commit -m "Adding files"
- git add '*.txt'
- git commit -m 'Adding all txt files'
- git log	==> history
- git remote add origin https://github.com/aditiasap/try_git.git
- git push -u origin master	==> push changes to remote with name origin, the default local branch is master. -u tell git to remember the parameters, so next time we can simply run "git push". 


- git pull origin master	==> To pull from remote repo for the newest version
- git diff HEAD			==> To check the different between the newest pull with our latest commit (HEAD pointer)
- git add octofamily/octodog.txt	==> Another scenario for staged differences below.
- git diff --staged		==> To check the different with the staged files. (Staged files are files not commited yet, but added)
- git reset octofamily/octodog.txt	==> To unstage files


- git checkout -- octocat.txt		==> [UNDO] To revert back the conditions where the last commit of octocat.txt. <target> is octocat.txt here

- git branch clean_up			==> create copy (branch) of code with name clean_up, which then can be merged to master once it ready
- git branch				==> List local branches
- git checkout clean_up			==> Switching branch to branch clean_up


- git rm '*.txt'			==> Remove files from disk and stage the removal for us. *.txt include all txt files inside subdirectory
- git commit -m "Remove all the cats"	==> Commit the removal


- git checkout master			==> switch to master branch so we can copy (or merge) back from clean_up branch into master branch

- git merge clean_up			==> merge clean_up branch into master branch

- git branch -d clean_up		==> since clean_up already merged, it no need anymore, so we delete it

- git push				==> push to remote repo

- git push origin master

Managing conflicts :
- git pull --rebase origin master ==> put commit to the top of master branch

Manual resolve conflicting files :
- git status
- git add <some-file>
- git rebase --continue

- git rebase --abort ==> back to previous rebase

Centralize workflow :
https://www.atlassian.com/git/tutorials/comparing-workflows#centralized-workflow

Feature branch workflow :
https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow

- git checkout -b marys-feature master
- git status
- git add <some-file>
- git commit

- git push -u origin marys-feature
- git push

File Pull Request..
Once done, Merge..

- git checkout master
- git pull
- git pull origin marys-feature
- git push
