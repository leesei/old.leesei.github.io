title: "Git notes"
date: 2014-12-11 17:34:15
categories:
- app
tags:
- shell-tool
- git
- notes
toc: true
---

http://ndpsoftware.com/git-cheatsheet.html

[Low Level Manager: using git-flow with github](http://www.lowlevelmanager.com/2011/03/using-git-flow-with-github.html)
[GitHub Workflow (used by Frameworks team at BBC News)](http://www.integralist.co.uk/posts/github-workflow.html)

[tj/git-extras](https://github.com/tj/git-extras)

<!-- more -->

## Merging from forked repo

https://www.openshift.com/wiki/github-workflow-for-submitting-pull-requests

https://help.github.com/articles/syncing-a-fork

```sh
# setup fork origin as upstream
git remote add upstream <fork origin url>

# pull the latest changes from upstream
git fetch upstream
git fetch upstream --tags

# assuming you are on <feature> branch and have uncommited updates
git stash
git co master

# merge the latest changes to current repo's master
git merge upstream/master

# push the updates changes to our fork
git push origin master
git push origin --tags

# rebase <feature> branch onto latest code from master (expect conflicts)
# can also used before submitting pull request/push to repo
git co <feature>
git rebase master

# apply uncommitted changes
git stash pop
```

## check diff before merge

http://stackoverflow.com/questions/4944376/how-to-check-real-git-diff-before-merging-from-remote-branch

## Deleting branch

```sh
# delete remote branch
git push origin :<branch>

# delete remote branch with dash
git push origin :refs/heads/<branch-with-dash>

# delete local branch
git branch -d <branch>

# delete local branch (force)
git branch -D <branch>
```

## Set tracking branch

```sh
git branch --set-upstream feature_branch origin/origin_branch
```

## abandoning merge

```sh
git merge --abort  # git > 1.7.4
git reset --merge  # git < 1.7.4
git reset --hard HEAD # git < 1.6.2
```

## create repo archive

```sh
git archive master -o <repo>.<tag>.zip
```

Tagging and pushing tag to Github will allow you to download the zipped code.

## gitweb

```sh
# start server
git instaweb -d webrick --start

# visit http://localhost:1234

# stop server
git instaweb -d webrick --stop
```

## Get current branch in shell

```sh
parse_git_branch(){
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/[\1]/';
}
```

## submodules

### using project with submodules

```sh
# clone project with submodules
git submodule init
git submodule sync
git submodule update
git submodule status
```

## Old notes 

```sh
git checkout -b redesign

# update working branch
git pull origin
git merge master
# OR
? git pull origin master:redesign

# commit
git pull origin
git checkout master
git merge redesign
git push origin master:master
# OR 
git checkout redesign
git rebase master
git push origin redesign:master

# delete local branch
git branch -d redesign # after merge
git branch -D redesign # force

# delete remote branch
git push origin :redesign

# delete whole tree
git push origin :master

# update a commit (unpushed)
git commit --amend <file>

# show commit info
git log [<some/path>]
git show [<some commit id>]
```
