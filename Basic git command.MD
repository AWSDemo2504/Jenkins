Basic git commands:

(1)git config
(2)git init
(3)git clone
(4)git add
(5)git commit
(6)git diff
(7)git reset
(8)git status
(9)git rm
(10)git log
(11)git show
(12)git tag
(13)git branch
(14)git checkout
(15)git merge
(16)git push
(17)git pull
(18)git stash


(1)git config : This command sets the author name and email address respectively to be used with your commits.

git config --global user.name "piyush"
git config --global user.email " piyush@a.com"

(2)git init : This command is used to start a new repository.

git init /home/ubuntu/piyush

Initialized empty Git repository in /home/ubuntu/piyush/.git/

(3)git clone : This command is used to obtain a repository from an existing URL.

 git clone https://git-codecommit.ap-south-1.amazonaws.com/v1/repos/myfirstrepository

(4)git add : This command adds a file to the staging area.

git add *

(5)git commit : This command records or snapshots the file permanently in the version history.

git commit -m " First Commit"

(6)git diff : This command shows the file differences which are not yet staged.

git diff

This command shows the differences between the files in the staging area and the latest version present.

git diff –staged 

(7)git reset :This command unstages the file, but it preserves the file contents.

git reset –hard [commit]  This command discards all history and goes back to the specified commit.

(8)git status :This command lists all the files that have to be committed.

git status


(9)git rm : This command deletes the file from your working directory and stages the deletion.


(10)git log : This command is used to list the version history for the current branch.

(11)git show : This command shows the metadata and content changes of the specified commit.

(12)git tag : This command is used to give tags to the specified commit.
git tag [commitID]
git tag abc
git tag


(13)git branch : This command lists all the local branches in the current repository.
git branch

git branch [branch name]

This command creates a new branch.

git branch -d [branch name]  

This command deletes the feature branch.

(14)git checkout :This command is used to switch from one branch to another.

git checkout -b [branch name]  

This command creates a new branch and also switches to it.


(15)git merge : This command merges the specified branch’s history into the current branch.

git merge branch_2

(16)git push :git push [variable name] master  

This command sends the committed changes of master branch to your remote repository.

git push origin master

git push –all [variable name]  

This command pushes all branches to your remote repository.

git push --all origin master

(17)git pull : This command fetches and merges changes on the remote server to your working directory.

git pull https://git-codecommit.ap-south-1.amazonaws.com/v1/repos/myfirstrepository


(18)git stash : This command temporarily stores all the modified tracked files.

git stash save 




