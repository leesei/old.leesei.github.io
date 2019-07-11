---
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

Git is a content addressable file system

- workspace/working tree
  current file system
- index/staging area
  `add`-ed, `rm`-ed, ready for commit
- local repo
  committed, `HEAD` commit
- upstream/remote
  a bare repo to `push` to
- stash
  temporary area to store your changes

[10 Years of Git: An Interview with Git Creator Linus Torvalds - The Linux Foundation](https://www.linuxfoundation.org/blog/10-years-of-git-an-interview-with-git-creator-linus-torvalds/)
[The Architecture and History of Git: A Distributed Version Control System](https://medium.com/@willhayjr/the-architecture-and-history-of-git-a-distributed-version-control-system-62b17dd37742)
[Tech Talk: Linus Torvalds on git - YouTube](https://www.youtube.com/watch?v=4XpnKHJAok8)
[[Linux.conf.au 2013] - Git For Ages 4 And Up - YouTube](https://www.youtube.com/watch?v=1ffBJ4sVUb4)
[The Biggest Misconception About Git – David Gohberg – Medium](https://medium.com/@gohberg/the-biggest-misconception-about-git-b2f87d97ed52)
[History of Git | Hackaday](https://hackaday.com/2017/05/11/history-of-git/)

You can always check reflog to restore commit no matter how you messed with your tree.
[Git back to the future | Phil Nash](https://philna.sh/blog/2017/01/04/git-back-to-the-future/)

[git man page generator](https://git-man-page-generator.lokaltog.net/) fake git man page
[Highlights from Git 2.21 - The GitHub Blog](https://github.blog/2019-02-24-highlights-from-git-2-21/)

## Tutorials

[Learn Git Version Control using Interactive Browser-Based Labs | Katacoda](https://www.katacoda.com/courses/git)
[Learn git concepts, not commands - DEV Community 👩‍💻👨‍💻](https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc)

[git - the simple guide - no deep shit!](http://rogerdudler.github.io/git-guide/)
[Git Tutorial - Try Git](https://try.github.io/)
[On Demand Training](https://services.github.com/on-demand/) [source](https://github.com/github/training-kit)
[git ready » learn git one commit at a time](http://gitready.com/)
[Git Immersion - Brought to you by Neo](http://gitimmersion.com/) guided tour
[Home // Think Like (a) Git](http://think-like-a-git.net/)
[Git Tutorials and Training | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials)
[Git Succinctly - Tuts+ Code Tutorials](http://code.tutsplus.com/series/git-succinctly--net-33581)
[A Beginner's Git and GitHub Tutorial | Udacity](http://blog.udacity.com/2015/06/a-beginners-git-github-tutorial.html)
[Understanding Git Conceptually](http://www.sbf5.com/~cduan/technical/git/)
[Getting Started With Git - DZone - Refcardz](https://dzone.com/refcardz/getting-started-git?chapter=1)
[Introduction to Git: Installation, Usage, and Branches | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/introduction-to-git-installation-usage-and-branches)
[Git for Teams — Git for Teams — Creating efficiency for teams of one or more.](http://www.gitforteams.com/)
[Learn Git in 30 Minutes | Tutorialzine](http://tutorialzine.com/2016/06/learn-git-in-30-minutes/)
[Git 版本控制系統 | ihower 的 Git 教室](https://ihower.tw/git/)
[Learn Git Branching](https://learngitbranching.js.org/) !important
[Interactive Git Tutorials – Rebase and Bisect – zwischenzugs](https://zwischenzugs.com/2016/04/24/interactive-git-tutorials-rebase-and-bisect/)
[How to become a Git expert – freeCodeCamp.org](https://medium.freecodecamp.org/how-to-become-a-git-expert-e7c38bf54826)
[Git It Right » Linux Magazine](http://www.linux-magazine.com/Issues/2018/216/Version-Control-with-Git)
[Many Branches » Linux Magazine](http://www.linuxpromagazine.com/Online/Features/Remote-Git-Repositories)

[The Ultimate GIT 5-day Challenge | Udemy](https://www.udemy.com/the-ultimate-git-5-day-challenge/)
[Getting Started With Git: Key Concepts for Beginners | Udemy](https://www.udemy.com/git-quick-start/)
[Short and Sweet: Get Started with Git and GitHub Right Now | Udemy](https://www.udemy.com/short-and-sweet-get-started-with-git-and-github-right-now/)

[Practical Git for Everyday Professional Use from @trevordmiller on @eggheadio](https://egghead.io/courses/practical-git-for-everyday-professional-use)
[Understanding Git's Behaviour • Steve Smith - YouTube](https://www.youtube.com/watch?v=SiokK8Q1wo0)

## Books

[Pro Git](http://git-scm.com/book/en/v2)
[Git Community Book](http://alx.github.io/gitbook/)
["Pro Git" Cliff Notes | Jason Meridth Blog](https://lostechies.com/jasonmeridth/2010/04/05/quot-pro-git-quot-cliff-notes/)
[Git Magic - Preface](http://www-cs-students.stanford.edu/~blynn/gitmagic/)
[Git for Everyone](http://anotheruiguy.gitbooks.io/gitforeveryone/content/)
[Learn Enough Git to Be Dangerous | Learn Enough to Be Dangerous](https://www.learnenough.com/git-tutorial)
[Learn Version Control with Git](https://www.git-tower.com/learn/git/ebook/en/command-line/introduction)

## manual/reference

[Git - Documentation](http://git-scm.com/doc)
[kernel.org user manual](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html)
[kernel.org howto](https://www.kernel.org/pub/software/scm/git/docs/howto/)
[Git Reference](http://gitref.org/)
[A Visual Git Reference](http://marklodato.github.io/visual-git-guide/index-en.html)
[Git SCM Wiki](https://git.wiki.kernel.org/index.php/Main_Page)
[Git Memo](http://git-memo.readthedocs.org/en/latest/introduction.html)

## cheat-sheet

[Git Cheatsheet • NDP Software](http://ndpsoftware.com/git-cheatsheet.html)
[AOSP Git and Repo cheatsheet](https://source.android.com/source/developing.html#git-and-repo-cheatsheet)
[Explain Git with D3](https://onlywei.github.io/explain-git-with-d3/)

## Git Protocols

[Git - The Protocols](https://git-scm.com/book/en/v2/Git-on-the-Server-The-Protocols)
[Introducing Git protocol version 2 | Google Open Source Blog](https://opensource.googleblog.com/2018/05/introducing-git-protocol-version-2.html)
[Git Wire Protocol, Version 2](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/technical/protocol-v2.html)

## commentary/internals

[The Git Parable](http://tom.preston-werner.com/2009/05/19/the-git-parable.html)
[Plastic SCM blog: Linus Torvalds on GIT and SCM](http://codicesoftware.blogspot.com/2007/05/linus-torvalds-on-git-and-scm.html)

[Reset Demystified – Scott Chacon](http://scottchacon.com/2011/07/11/reset.html)
[Note to Self – Scott Chacon](http://scottchacon.com/2010/08/25/notes.html)
[Git Loves the Environment – Scott Chacon](http://scottchacon.com/2010/04/11/environment.html)
[When You “Git” in Trouble: a Version Control Story – Hacker Noon](https://hackernoon.com/when-you-git-in-trouble-a-version-control-story-97e6421b5c0e)

[Git from the inside out - YouTube](https://www.youtube.com/watch?v=fCtZWGhQBvo) [blog](http://maryrosecook.com/blog/post/git-from-the-inside-out)
[Git from the inside out](https://codewords.recurse.com/issues/two/git-from-the-inside-out)
[Unpacking Git packfiles](https://codewords.recurse.com/issues/three/unpacking-git-packfiles)

[Git Source Code Review](http://fabiensanglard.net/git_code_review/index.php)
[The Architecture of Open Source Applications (Volume 2): Git](http://aosabook.org/en/git.html)
[pluralsight/git-internals-pdf](https://github.com/pluralsight/git-internals-pdf)

## Repo size

[Reduce repository size - Atlassian Documentation](https://confluence.atlassian.com/bitbucket/reduce-repository-size-321848262.html)

[BFG Repo-Cleaner by rtyley](https://rtyley.github.io/bfg-repo-cleaner/)
[Rewriting Git project history with The BFG | Info | theguardian.com](https://www.theguardian.com/info/developer-blog/2013/apr/29/rewrite-git-history-with-the-bfg)

[Git - git-filter-branch Documentation](https://git-scm.com/docs/git-filter-branch)

## bindings

[libgit2](https://libgit2.github.com/) [source](https://github.com/libgit2/libgit2)
[notatestuser/gift: A wrapper for the Git CLI in Node.js](https://github.com/notatestuser/gift)

## plugins

[stevemao/awesome-git-addons: A curated list of addons that extends git cli.](https://github.com/stevemao/awesome-git-addons)

[fabiospampinato/awesome-autogit: Curated list of resources for autogit.](https://github.com/fabiospampinato/awesome-autogit)
[Autogit | Autogit](http://fabiospampinato.com/autogit/#features)

[GitUp](http://gitup.co/)

[Welcome | Legit (Git Workflow for Humans)](http://www.git-legit.org/)
[Get Legit with Git (and GitHub): The Art of the Commit Message - The New Stack](https://thenewstack.io/getting-legit-with-git-and-github-the-art-of-the-commit-message/)

[donnemartin/gitsome: A supercharged Git/GitHub command line interface (CLI).](https://github.com/donnemartin/gitsome)
[qw3rtman/gg: Git Goodies: At-A-Glance, Efficient, and Aesthetically Pleasing Git Shortcuts](https://github.com/qw3rtman/gg)
[golbin/git-commander: A git tool with an easy terminal interface.](https://github.com/golbin/git-commander)
[nvie/gitflow: Git extensions to provide high-level repository operations for Vincent Driessen's branching model.](https://github.com/nvie/gitflow)
[tj/git-extras](https://github.com/tj/git-extras) [video](https://vimeo.com/45506445) [commands](https://github.com/tj/git-extras/blob/master/Commands.md)
[nlf/git-gh: github extensions for git](https://github.com/nlf/git-gh)
[hub · the command-line wrapper for git](https://hub.github.com/) [github/hub](https://github.com/github/hub)
[Gitsu: User management and pairing for Git](http://drrb.github.io/gitsu/)

[myrepos](https://myrepos.branchable.com/)

[Gitless](http://gitless.com/#documentation)

You can name you custom script as `git-mycmd`, place it in you PATH and use `git mycmd` to invoke it.
[Extending Git: add a custom command](http://blog.santosvelasco.com/2012/06/14/extending-git-add-a-custom-command/)
[Extend Git with Custom Commands](https://coderwall.com/p/bt93ia/extend-git-with-custom-commands)
[Extending Git functionality - Stack Overflow](http://stackoverflow.com/questions/10978257/extending-git-functionality/10978296#10978296)
[Atlassian Blogs: Extending git](http://blogs.atlassian.com/2013/04/extending-git/)

### Tig

[Tig: text-mode interface for Git](http://jonas.nitro.dk/tig/)
[The Tig Manual](http://jonas.nitro.dk/tig/manual.html)

[tig: nice text-mode (ncurses) Git repo viewer - YouTube](https://www.youtube.com/watch?v=udCXubFr5Yo)

[git ready » tig, the ncurses front-end to Git](http://gitready.com/advanced/2009/07/31/tig-the-ncurses-front-end-to-git.html)
[git? tig! | Atlassian Blogs](http://blogs.atlassian.com/2013/05/git-tig/)

## GUI Clients

[Git - GUI Clients](https://git-scm.com/downloads/guis)
[Sublime Merge - Git Client, done Sublime](https://www.sublimemerge.com/)
[Git GUI for Windows, Mac & Linux | GitKraken](https://www.gitkraken.com/)
[GitEye | CollabNet](http://www.collab.net/products/giteye)
[GitUp](http://gitup.co/) Mac only, innovative UX

## `repo`

[Repo command reference | Android Open Source Project](https://source.android.com/source/using-repo.html)

```sh
# requires python
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo
```

Integrates git repo with review system (Gerrit).

## Blob

[git-annex](https://git-annex.branchable.com/) add file to git
[joeyh/git-annex: manage large files with git](https://github.com/joeyh/git-annex)

[Git Large File Storage | Git Large File Storage (LFS) replaces large files such as audio samples, videos, datasets, and graphics with text pointers inside Git, while storing the file contents on a remote server like GitHub.com or GitHub Enterprise.](https://git-lfs.github.com/)
[cloudmazing/lfs-server-go: LFS server with multiple file stores and backing stores](https://github.com/cloudmazing/lfs-server-go)

[VFS for Git: Git at Enterprise Scale](https://vfsforgit.org/) formerly GVFS
[Microsoft/VFSForGit: Virtual File System for Git: Enable Git at Enterprise Scale](https://github.com/Microsoft/VFSForGit)

---

## Workflow

[Git Branching Model](http://www.slideshare.net/lemiorhan/git-branching-model)
[A successful Git branching model » nvie.com](http://nvie.com/posts/a-successful-git-branching-model/)
[Understanding the GitHub Flow · GitHub Guides](https://guides.github.com/introduction/flow/)
[Low Level Manager: using git-flow with github](http://www.lowlevelmanager.com/2011/03/using-git-flow-with-github.html)
[a simple git branching model](https://gist.github.com/jbenet/ee6c9ac48068889b0912)
[GitHub Workflow (used by Frameworks team at BBC News)](http://www.integralist.co.uk/posts/github-workflow.html)
[GitHub Flow – Scott Chacon](http://scottchacon.com/2011/08/31/github-flow.html)
[How to GitHub: Fork, Branch, Track, Squash and Pull Request - Gun.io](https://gun.io/blog/how-to-github-fork-branch-and-pull-request/)
[Git Branching Strategies for Maintainable Test Automation - DZone DevOps](https://dzone.com/articles/git-branching-strategies-for-maintainable-test-aut)

[stevenharman/git-workflows](https://github.com/stevenharman/git-workflows)
[reenhanced/gitreflow](https://github.com/reenhanced/gitreflow)
[hub · the command-line wrapper for git](https://hub.github.com/)

[My Git Workflow](http://blog.osteele.com/posts/2008/05/my-git-workflow/)
[Commit Policies](http://blog.osteele.com/posts/2008/05/commit-policies/)

[Git 常用命令备忘 – 尘埃落定](http://www.lovelucy.info/git-command-cheatsheet.html)

### Rebase

[A Rebase Workflow for Git | RandyFay.com](http://www.randyfay.com/node/91)
[Avoiding Git Disasters: A Gory Story | RandyFay.com](http://www.randyfay.com/node/89)
[Merging vs. Rebasing | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/merging-vs-rebasing/)
[Merge or Rebase? | SourceTree Blog](https://blog.sourcetreeapp.com/2012/08/21/merge-or-rebase/)
[Learn Git Rebase Interactively – zwischenzugs](https://zwischenzugs.com/2018/04/05/learn-git-rebase-interactively/)

[Github workflow · servo/servo Wiki](https://github.com/servo/servo/wiki/Github-workflow)
`rebase --interactive --autosquash`
`fixup`

[version control - git workflow and rebase vs merge questions - Stack Overflow](http://stackoverflow.com/questions/457927/git-workflow-and-rebase-vs-merge-questions)
[version control - When do you use git rebase instead of git merge? - Stack Overflow](http://stackoverflow.com/questions/804115/when-do-you-use-git-rebase-instead-of-git-merge)

## Video

[Git The Basics Tutorial - excess.org](http://excess.org/article/2008/07/ogre-git-tutorial/)
[Tech Talk: Linus Torvalds on git - YouTube](https://www.youtube.com/watch?v=4XpnKHJAok8)
[GitHub Training & Guides - YouTube](https://www.youtube.com/user/GitHubGuides)

[Deep Dive into Git • Edward Thomson - YouTube](https://www.youtube.com/watch?v=dBSHLb1B8sw)
[Introduction to Git with Scott Chacon of GitHub - YouTube](https://www.youtube.com/watch?v=ZDR433b0HJY)
[Advanced Git: Graphs, Hashes, and Compression, Oh My! - YouTube](https://www.youtube.com/watch?v=ig5E8CcdM9g)

## Presentations

[schacon/tale_of_three_trees](https://github.com/schacon/tale_of_three_trees)
[schacon/showoff-wrangling-git](https://github.com/schacon/showoff-wrangling-git)
May need [puppetlabs/showoff](https://github.com/puppetlabs/showoff)

## Tips and Tricks

[First Aid git](http://firstaidgit.io/#/)
[git-tips/tips: Most commonly used git tips and tricks.](https://github.com/git-tips/tips)
[nirajpandkar/git-tip: CLI that gives a random git-tip.](https://github.com/nirajpandkar/git-tip)
[A few git tips you didn't know about](http://mislav.uniqpath.com/2010/07/git-tips/)
[25 Tips for Intermediate Git Users](https://www.andyjeffries.co.uk/25-tips-for-intermediate-git-users/)
[Git tips and tricks](http://blog.mixu.net/2012/04/06/git-tips-and-tricks/)
[GIT Conventions — Medium](https://medium.com/@tjholowaychuk/git-conventions-a940ee20862d)
[10 Git Commands You Should Know – Towards Data Science](https://towardsdatascience.com/10-git-commands-you-should-know-df54bea1595c)
[git Archives - Everything CLI](https://www.everythingcli.org/tag/git/)

[Five Key Git Concepts Explained the Hard Way – zwischenzugs](https://zwischenzugs.com/2018/03/14/five-key-git-concepts-explained-the-hard-way/)
[Create Your Own Git Diagrams – zwischenzugs](https://zwischenzugs.com/2018/03/08/create-your-own-git-diagrams/)

[Advanced Git Commands: Rewriting History - DZone Open Source](https://dzone.com/articles/advanced-git-commands-rewriting-history)

[How (and why!) to keep your Git commit history clean | GitLab](https://about.gitlab.com/2018/06/07/keeping-git-commit-history-clean/)
[Git tips: 合并 commit 保持分支干净整洁 – 尘埃落定](http://www.lovelucy.info/git-tips-combine-commits-keep-your-branch-clean.html)
[The Elements of Commit Style](http://mcandre.gitbooks.io/elements-of-commit-style/content/index.html)

## Githooks

[Git Hooks | Learn how to use pre-commit hooks, post-commit hooks, post-receive hooks, and more. | Matthew Hudson](http://githooks.com/)
[typicode/husky: Git hooks made easy](https://github.com/typicode/husky)

<!-- more -->

---

# Koan

## Specify SSH key to use

Starting from Git 2.3.0

[ssh - How to tell git which private key to use? - Super User](http://superuser.com/questions/232373/how-to-tell-git-which-private-key-to-use)
[Connecting to GitHub with SSH - User Documentation](https://help.github.com/articles/connecting-to-github-with-ssh/)

```sh
GIT_SSH_COMMAND="ssh -vv -i ~/.ssh/KEY" git clone

# `-F` ignores default SSH config
git config --local core.sshCommand "ssh -i ~/.ssh/KEY -F /dev/null"
```

## Change author

[drrb/gitsu: User management and pairing for Git](https://github.com/drrb/gitsu)
Adds `git su` subcommand to set user from `~/.gitsu`.

[git - How to change the commit author for one specific commit? - Stack Overflow](https://stackoverflow.com/questions/3042437/how-to-change-the-commit-author-for-one-specific-commit)

```sh
# amend last commit
git commit --amend --author "New Author <new@email>"
```

```sh
#!/bin/sh

git filter-branch --env-filter '

OLD_EMAIL="your-old-email@example.com"
CORRECT_NAME="Your Correct Name"
CORRECT_EMAIL="your-correct-email@example.com"

if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$CORRECT_NAME"
    export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$CORRECT_NAME"
    export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags
```

## Merging from forked repo

[Syncing a fork - User Documentation](https://help.github.com/articles/syncing-a-fork/)  
[Updating Slate · lord/slate Wiki](https://github.com/lord/slate/wiki/Updating-Slate)

```sh
# setup fork origin as upstream
git remote add upstream <fork origin url>

# pull the latest changes from upstream
git fetch upstream
git fetch upstream --tags

# assuming you are on <feature> branch and have uncommitted updates
git stash
git co master

# rebase forked repo to upstream's master
git rebase upstream/master

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

## push empty commits

this is to re-trigger githooks

```sh
git commit --allow-empty -m "Trigger git hook"
```

## commits after release

```sh
# get latest tag on current branch
git describe --abbrev=0 --tags
# show commits since latest tag
git log `git describe --tags --abbrev=0`..HEAD --oneline
```

## updating master

```sh
# assuming you have a <feature> branch and have committed updates
git co master
git stash
# merge feature branch to master, squashing to a single commit
git merge --squash feature
```

## update (unpushed) commit message

```sh
# last commit
git commit --amend
# older commits
# you can also reorder, squash the commits
git rebase -i HEAD~n  # last n commits
git rebase -i $parent_of_flawed_commit
# use 'r' to reword commits
```

[Edit an incorrect commit message in Git - Stack Overflow](http://stackoverflow.com/questions/179123/a/180085)
[Changing a commit message - User Documentation](https://help.github.com/articles/changing-a-commit-message/)

## check diff before merge

[How to check real git diff before merging from remote branch? - Stack Overflow](https://stackoverflow.com/questions/4944376/how-to-check-real-git-diff-before-merging-from-remote-branch)

## show files on another branch/commit

```sh
git show git show <committish>:<path/to/file>
```

[Display a file from another branch - DEV Community 👩‍💻👨‍💻](https://dev.to/math2001/display-a-file-from-another-branch-1efp)

## list changed files

```sh
git diff-index --shortstat HEAD
```

## Cherry-picking changes to add

```sh
git add --patch <file>
git add -p <file>
```

http://stackoverflow.com/questions/1085162/commit-only-part-of-a-file-in-git

## drop changes

```sh
# replace `file` in file system with copy in local repo
git checkout -- <file>
# unadd
git reset HEAD
# uncommit, changes still added to staging
git reset --soft
# reset local repo and workspace to upstream
git reset --hard origin/master
```

## check unpushed commits

```sh
git log --branches --not --remotes

# Git 2.5+
git log @{push}
```

## Deleting branch

```sh
# delete remote branch
git push origin :<branch>

# delete local branch
git branch -d <branch>

# delete local branch (force)
git branch -D <branch>
```

## Renaming branch

```sh
git branch -m old_branch new_branch         # Rename branch locally
# push and set default branch to new_branch if using GitHub
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
# deploy to server
git archive --format=tar origin/master | gzip -9c | ssh user@yourserver.com "tar --directory=/var/www -xvzf -"
```

Tagging and pushing tag to Github will aldo allow you to download the zipped code.

## reduce repo size

[How to Shrink a Git Repository](http://stevelorek.com/how-to-shrink-a-git-repository.html)
[Reduce git repository size - Stack Overflow](http://stackoverflow.com/questions/2116778/reduce-git-repository-size)
[Git pull error: unable to create temporary sha1 filename - Stack Overflow](http://stackoverflow.com/questions/685319/git-pull-error-unable-to-create-temporary-sha1-filename/)

```sh
git gc --aggressive --prune=now
```

## better `diff`

[A better Vimdiff Git mergetool - Vim Tips Wiki](http://vim.wikia.com/wiki/A_better_Vimdiff_Git_mergetool)

[Use vimdiff as git mergetool - Ruslan Osipov](http://www.rosipov.com/blog/use-vimdiff-as-git-mergetool/)

## Get current branch in shell

```sh
parse_git_branch(){
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/[\1]/';
}
```

## submodules

Submodule saves a commit hash of another (library) repo in the current (master) repo

[Mastering Git submodules — Medium](https://medium.com/@porteneuve/mastering-git-submodules-34c65e940407)

### using project with submodules

```sh
# clone project with submodules
git clone --recursive
# or `git submodule update --init` after clone

# update local submodule hash
git submodule update --remote

git submodule sync
git submodule status
```

## subtree

[git/git-subtree.txt at master · git/git](https://github.com/git/git/blob/master/contrib/subtree/git-subtree.txt)

[Alternatives To Git Submodule: Git Subtree](http://blogs.atlassian.com/2013/05/alternatives-to-git-submodule-git-subtree/)
[The power of Git subtree - Atlassian Developers](https://developer.atlassian.com/blog/2015/05/the-power-of-git-subtree/)
[Mastering Git subtrees — Medium](https://medium.com/@porteneuve/mastering-git-subtrees-943d29a798ec)
[Understanding Git Subtree - HPC @ Uni.lu](https://hpc.uni.lu/blog/2014/understanding-git-subtree/)

[git migrate from submodule to subtree | Life & Note - winterTTr](http://winterttr.me/2015/09/08/git-migrate-from-submodule-to-subtree/)

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
