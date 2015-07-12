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

[Git - Documentation](http://git-scm.com/doc)  
[git ready » learn git one commit at a time](http://gitready.com/)  
[Git Immersion - Brought to you by Neo](http://gitimmersion.com/)  
[Home // Think Like (a) Git](http://think-like-a-git.net/)  
[Git 版本控制系統 | ihower 的 Git 教室](https://ihower.tw/git/)  
[Understanding Git Conceptually](http://www.sbf5.com/~cduan/technical/git/)  
[GitHub Training](https://training.github.com/kit/) [source](https://github.com/github/training-kit)  
[Git Succinctly - Tuts+ Code Tutorials](http://code.tutsplus.com/series/git-succinctly--net-33581)  
[mojombo/mastering-git-basics](https://github.com/mojombo/mastering-git-basics)  

## manual/reference

[kernel.org user manual](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html)  
[kernel.org howto](https://www.kernel.org/pub/software/scm/git/docs/howto/)  
[Git Reference](http://gitref.org/)  
[A Visual Git Reference](http://marklodato.github.io/visual-git-guide/index-en.html)  
[Git SCM Wiki](https://git.wiki.kernel.org/index.php/Main_Page)  

## cheatsheet

[Git Cheatsheet • NDP Software](http://ndpsoftware.com/git-cheatsheet.html)
[AOSP Git and Repo cheatsheet](https://source.android.com/source/developing.html#git-and-repo-cheatsheet)

## commentary

[The Git Parable](http://tom.preston-werner.com/2009/05/19/the-git-parable.html)  
[Plastic SCM blog: Linus Torvalds on GIT and SCM](http://codicesoftware.blogspot.com/2007/05/linus-torvalds-on-git-and-scm.html)  
[The Architecture of Open Source Applications (Volume 2): Git](http://aosabook.org/en/git.html)  

[Reset Demystified – Scott Chacon](http://scottchacon.com/2011/07/11/reset.html)  
[Note to Self – Scott Chacon](http://scottchacon.com/2010/08/25/notes.html)  
[Git Loves the Environment – Scott Chacon](http://scottchacon.com/2010/04/11/environment.html)  

## Books

[Git - Book](http://git-scm.com/book/en/v2)
[Git Community Book](http://alx.github.io/gitbook/)
["Pro Git" Cliff Notes | Jason Meridth Blog](https://lostechies.com/jasonmeridth/2010/04/05/quot-pro-git-quot-cliff-notes/)
[Git Magic - Preface](http://www-cs-students.stanford.edu/~blynn/gitmagic/)
[Git for Everyone](http://anotheruiguy.gitbooks.io/gitforeveryone/content/)

## Workflow

[A successful Git branching model » nvie.com](http://nvie.com/posts/a-successful-git-branching-model/)
[Understanding the GitHub Flow · GitHub Guides](https://guides.github.com/introduction/flow/)
[Low Level Manager: using git-flow with github](http://www.lowlevelmanager.com/2011/03/using-git-flow-with-github.html)
[GitHub Workflow (used by Frameworks team at BBC News)](http://www.integralist.co.uk/posts/github-workflow.html)
[GitHub Flow – Scott Chacon](http://scottchacon.com/2011/08/31/github-flow.html)
[How to GitHub: Fork, Branch, Track, Squash and Pull Request - Gun.io](https://gun.io/blog/how-to-github-fork-branch-and-pull-request/)
[stevenharman/git-workflows](https://github.com/stevenharman/git-workflows)
[hub · the command-line wrapper for git](https://hub.github.com/)

[My Git Workflow](http://blog.osteele.com/posts/2008/05/my-git-workflow/)
[Commit Policies](http://blog.osteele.com/posts/2008/05/commit-policies/)

### Rebase

[A Rebase Workflow for Git | RandyFay.com](http://www.randyfay.com/node/91)
[Avoiding Git Disasters: A Gory Story | RandyFay.com](http://www.randyfay.com/node/89)
[version control - git workflow and rebase vs merge questions - Stack Overflow](http://stackoverflow.com/questions/457927/git-workflow-and-rebase-vs-merge-questions)
[version control - When do you use git rebase instead of git merge? - Stack Overflow](http://stackoverflow.com/questions/804115/when-do-you-use-git-rebase-instead-of-git-merge)

## Video

[Git The Basics Tutorial - excess.org](http://excess.org/article/2008/07/ogre-git-tutorial/)
[Tech Talk: Linus Torvalds on git - YouTube](https://www.youtube.com/watch?v=4XpnKHJAok8)
[GitHub Training & Guides - YouTube](https://www.youtube.com/user/GitHubGuides)

[Introduction to Git with Scott Chacon of GitHub - YouTube](https://www.youtube.com/watch?v=ZDR433b0HJY)
[Advanced Git: Graphs, Hashes, and Compression, Oh My! - YouTube](https://www.youtube.com/watch?v=ig5E8CcdM9g)

## Tips

[A few git tips you didn't know about](http://mislav.uniqpath.com/2010/07/git-tips/)
[25 Tips for Intermediate Git Users](https://www.andyjeffries.co.uk/25-tips-for-intermediate-git-users/)
[Git tips and tricks](http://blog.mixu.net/2012/04/06/git-tips-and-tricks/)
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

## Renaming branch

```sh
git branch -m old_branch new_branch         # Rename branch locally    
git push origin :old_branch                 # Delete the old branch    
git push --set-upstream origin new_branch   # Push the new branch, set local branch to track the new remote
```

## Set tracking branch

```sh
git branch --set-upstream feature_branch origin/origin_branch
# checkout and track
git checkout -t origin/feature
# push and track
git push -u origin feature
```

## rebase

```sh
git pull --rebase

git rebase HEAD feature && git rebase HEAD @{-2}
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

## better `vimdiff`

[A better Vimdiff Git mergetool - Vim Tips Wiki](http://vim.wikia.com/wiki/A_better_Vimdiff_Git_mergetool)

[Use vimdiff as git mergetool - Ruslan Osipov](http://www.rosipov.com/blog/use-vimdiff-as-git-mergetool/)

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

# diff staged with index
git diff --staged  # alias of --cached

# update a commit (unpushed)
git commit --amend <file>

# show commit info
git log [<some/path>]
git show [<some commit id>]
```
