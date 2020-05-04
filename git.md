## (my) GIT documentation
[extra cheatsheet](https://github.com/richistron/aprendiendo-git/tree/master/docs)

Init a new git repo in current folder
>git init

List braches in local. Use `-r` option to list branches in repo
>git branch (--list)

>git branch -r

Change to different branc. Use `-b` to create new branch
>git checkout <branch>

>git checkout -b <branch>

Check status of local repo
>git status

Add file to stage. Use `-A` to stage all changes
>git add ./filename

>git add -A

Commit changes staged. It is required a message.
>git commit -m message

Merge current branch with branch in repo
>git merge repository/branch

Update changes in repo to current branch. Combination of fetch+merge
>git pull repository branch

Push yout local commits to a branch in the repo. Use `-f` to force push
>git push repository branch
>git push -f repository branch

Update last changes to local from repository. Also, you can fetch specific branch
>git fetch repository

>git fetch repository branch

Show log of last commits. Use `-n 1` to show 1 result
>git log

>git log -n1

List all repositories
>git remote -v

Add a new repository
>git remote add <new-repository> <url.git>

Update url from a repo
>git remote set-url <repository> ssh://user@ip/project.git

Rebase certain numbers of commits, or rebase branches. be very careful here
>git rebase -i HEAD~num
>git rebase -i branch_to_rebase

Most common options to choose are:

* pick - keep commit
* drop - drop commit
* squash - squash commit

Merge one particular commit in current branch
>git cherry-pick commit-hashs


#### Bonus track: stash

While working in a branch, you may want to save your current changes to keep working later. Most common actions are:
>git stash save message.

To recover one stash already save
>git stash drop apply@{num}

Delete stash number
>git stash drop stash@{num}

To list all stash
>git stash list

To get and delete first stash
>git stash pop