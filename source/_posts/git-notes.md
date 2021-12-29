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
[The History Behind Git - DEV Community](https://dev.to/ahmedgouda/the-history-behind-git-53ag)
[Tech Talk: Linus Torvalds on git - YouTube](https://www.youtube.com/watch?v=4XpnKHJAok8)
[[Linux.conf.au 2013] - Git For Ages 4 And Up - YouTube](https://www.youtube.com/watch?v=1ffBJ4sVUb4)
[The Biggest Misconception About Git – David Gohberg – Medium](https://medium.com/@gohberg/the-biggest-misconception-about-git-b2f87d97ed52)
[History of Git | Hackaday](https://hackaday.com/2017/05/11/history-of-git/)
[git - the simple guide - no deep shit!](https://rogerdudler.github.io/git-guide/)

[Opinionated Git](http://opinionatedgit.com/)

You can always check reflog to restore commit no matter how you messed with your tree.
[Git back to the future | Phil Nash](https://philna.sh/blog/2017/01/04/git-back-to-the-future/)

[Git Explained in 100 Seconds - YouTube](https://www.youtube.com/watch?v=hwP7WQkmECE)
[13 Advanced (but useful) Git Techniques and Shortcuts - YouTube](https://www.youtube.com/watch?v=ecK3EnyGD8o)

[Highlights from Git 2.21 - The GitHub Blog](https://github.blog/2019-02-24-highlights-from-git-2-21/)
[Highlights from Git 2.22 - The GitHub Blog](https://github.blog/2019-06-07-highlights-from-git-2-22/)

[git man page generator](https://git-man-page-generator.lokaltog.net/) fake git man page
[Lokaltog/git-man-page-generator: Git man page generator.](https://github.com/Lokaltog/git-man-page-generator)

[evil git man page](http://git-scms.com/)
[dellis23/evil-git-man-page-generator: An evil fork of this project, no warnings https://github.com/Lokaltog/baba-git-man-page-generator](https://github.com/dellis23/evil-git-man-page-generator)

## Tutorials

[Learn Git Version Control using Interactive Browser-Based Labs | Katacoda](https://www.katacoda.com/courses/git)
[Learn git concepts, not commands - DEV Community 👩‍💻👨‍💻](https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc)
[Git: A Complete Guide. Covering the essential commands for a… | by Rahul Pathak | Towards Data Science](https://towardsdatascience.com/git-a-complete-guide-d49675d02a5d)

[Git Tutorials and Training | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials) !important
[Git Handbook · GitHub Guides](https://guides.github.com/introduction/git-handbook/)
[git - the simple guide - no deep shit!](http://rogerdudler.github.io/git-guide/)
[Git Tutorial - Try Git](https://try.github.io/)
[On Demand Training](https://services.github.com/on-demand/) [source](https://github.com/github/training-kit)
[git ready » learn git one commit at a time](http://gitready.com/)
[Git Immersion - Brought to you by Neo](http://gitimmersion.com/) guided tour
[Learn Version Control with Git for Free](https://www.git-tower.com/learn/)
[Home // Think Like (a) Git](http://think-like-a-git.net/)
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
[Git for Professionals Tutorial - Tools & Concepts for Mastering Version Control with Git - YouTube](https://www.youtube.com/watch?v=Uszj_k0DGsg)
[Git and GitHub for Beginners - Crash Course - YouTube](https://www.youtube.com/watch?v=RGOj5yH7evk)
[Understanding Git's Behaviour • Steve Smith - YouTube](https://www.youtube.com/watch?v=SiokK8Q1wo0)
[Introduction to Git - Core Concepts - YouTube](https://www.youtube.com/watch?v=uR6G2v_WsRA)
[Lecture 6: Version Control (git) (2020) - YouTube](https://www.youtube.com/watch?v=2sjqTHE0zok)

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

## Git Protocols

[Git - The Protocols](https://git-scm.com/book/en/v2/Git-on-the-Server-The-Protocols)
[Introducing Git protocol version 2 | Google Open Source Blog](https://opensource.googleblog.com/2018/05/introducing-git-protocol-version-2.html)
[Git Wire Protocol, Version 2](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/technical/protocol-v2.html)

## commentary/internals

[The Git Parable](http://tom.preston-werner.com/2009/05/19/the-git-parable.html)
[Plastic SCM blog: Linus Torvalds on GIT and SCM](http://codicesoftware.blogspot.com/2007/05/linus-torvalds-on-git-and-scm.html)

[Scaling git's merge and rename-detection machinery | Palantir Blog](https://medium.com/palantir/optimizing-gits-merge-machinery-1-127ceb0ef2a1)
[Optimizing git’s merge machinery, #2 | by Palantir | Palantir Blog | Mar, 2021 | Medium](https://medium.com/palantir/optimizing-gits-merge-machinery-2-d81391b97878)

[Reset Demystified – Scott Chacon](http://scottchacon.com/2011/07/11/reset.html)
[Note to Self – Scott Chacon](http://scottchacon.com/2010/08/25/notes.html)
[Git Loves the Environment – Scott Chacon](http://scottchacon.com/2010/04/11/environment.html)
[When You “Git” in Trouble: a Version Control Story – Hacker Noon](https://hackernoon.com/when-you-git-in-trouble-a-version-control-story-97e6421b5c0e)

[Git from the inside out - YouTube](https://www.youtube.com/watch?v=fCtZWGhQBvo) [blog](http://maryrosecook.com/blog/post/git-from-the-inside-out)
[Git from the inside out](https://codewords.recurse.com/issues/two/git-from-the-inside-out)
[Unpacking Git packfiles](https://codewords.recurse.com/issues/three/unpacking-git-packfiles)

[Git Pathspecs and How to Use Them | CSS-Tricks](https://css-tricks.com/git-pathspecs-and-how-to-use-them/)

[Get up to speed with partial clone and shallow clone - The GitHub Blog](https://github.blog/2020-12-21-get-up-to-speed-with-partial-clone-and-shallow-clone/)

[Git Source Code Review](http://fabiensanglard.net/git_code_review/index.php)
[The Architecture of Open Source Applications (Volume 2): Git](http://aosabook.org/en/git.html)
[pluralsight/git-internals-pdf](https://github.com/pluralsight/git-internals-pdf)

[Remediating the May 2018 Git Security Vulnerability | Azure DevOps Blog](https://devblogs.microsoft.com/devops/announcing-the-may-2018-git-security-vulnerability/) `.git/` which contains user script was pushed to remote and allows remote code execution

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

[Introduction - complate wiki](https://replicadse.github.io/complate/)
[complate — command-line utility in Rust // Lib.rs](https://lib.rs/crates/complate)

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

## GUI Clients

[Git - GUI Clients](https://git-scm.com/downloads/guis)
[Sublime Merge - Git Client, done Sublime](https://www.sublimemerge.com/) !important
[GitLens: where have you been all my life! - DEV Community 👩‍💻👨‍💻](https://dev.to/glsolaria/gitlens-where-have-you-been-all-my-life-1c2d) !important, VSCode extension

[Git GUI for Windows, Mac & Linux | GitKraken](https://www.gitkraken.com/)
[GitEye | CollabNet](http://www.collab.net/products/giteye)
[GitUp](http://gitup.co/) Mac only, innovative UX

[Git Cola: The highly caffeinated Git GUI](https://git-cola.github.io/)
[Make Git easy with Git Cola | Opensource.com](https://opensource.com/article/20/3/git-cola)

[Supercharging the Git Commit Graph | Azure DevOps Blog](https://devblogs.microsoft.com/devops/supercharging-the-git-commit-graph/)
[Supercharging the Git Commit Graph II: File Format | Azure DevOps Blog](https://devblogs.microsoft.com/devops/supercharging-the-git-commit-graph-ii-file-format/)
[Supercharging the Git Commit Graph III: Generations and Graph Algorithms | Azure DevOps Blog](https://devblogs.microsoft.com/devops/supercharging-the-git-commit-graph-iii-generations/)
[Supercharging the Git Commit Graph IV: Bloom Filters | Azure DevOps Blog](https://devblogs.microsoft.com/devops/super-charging-the-git-commit-graph-iv-bloom-filters/)

### Terminal GUI

[extrawurst/gitui: Blazing 💥 fast terminal-ui for git written in rust 🦀](https://github.com/Extrawurst/gitui)

[Tig: text-mode interface for Git](http://jonas.nitro.dk/tig/)
[The Tig Manual](http://jonas.nitro.dk/tig/manual.html)

[tig: nice text-mode (ncurses) Git repo viewer - YouTube](https://www.youtube.com/watch?v=udCXubFr5Yo)

[git ready » tig, the ncurses front-end to Git](http://gitready.com/advanced/2009/07/31/tig-the-ncurses-front-end-to-git.html)
[git? tig! | Atlassian Blogs](http://blogs.atlassian.com/2013/05/git-tig/)

## `repo`

[repo](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/README.md)
[Repo Command Reference | Android Open Source Project](https://source.android.com/setup/develop/repo)

```sh
# requires python
curl https://storage.googleapis.com/git-repo-downloads/repo > repo
chmod a+x ~/bin/repo
```

Integrates git repo with review system (Gerrit).

## Blob

[git-annex](https://git-annex.branchable.com/) add file to git
[joeyh/git-annex: manage large files with git](https://github.com/joeyh/git-annex)

[Git Large File Storage | Git Large File Storage (LFS) replaces large files such as audio samples, videos, datasets, and graphics with text pointers inside Git, while storing the file contents on a remote server like GitHub.com or GitHub Enterprise.](https://git-lfs.github.com/)
[cloudmazing/lfs-server-go: LFS server with multiple file stores and backing stores](https://github.com/cloudmazing/lfs-server-go)
[Large Media overview | Netlify Docs](https://docs.netlify.com/large-media/overview/)

[VFS for Git: Git at Enterprise Scale](https://vfsforgit.org/) formerly GVFS
[Microsoft/VFSForGit: Virtual File System for Git: Enable Git at Enterprise Scale](https://github.com/Microsoft/VFSForGit)

---

## Workflow

[Git Branching Model](http://www.slideshare.net/lemiorhan/git-branching-model)
[A successful Git branching model » nvie.com](https://nvie.com/posts/a-successful-git-branching-model/)
[Understanding the GitHub Flow · GitHub Guides](https://guides.github.com/introduction/flow/)
[a simple git branching model](https://gist.github.com/jbenet/ee6c9ac48068889b0912)
[GitHub Workflow ⋆ Mark McDonnell](https://www.integralist.co.uk/posts/github-workflow/)
[GitHub Flow – Scott Chacon](http://scottchacon.com/2011/08/31/github-flow.html)
[How to GitHub: Fork, Branch, Track, Squash and Pull Request - Gun.io](https://gun.io/blog/how-to-github-fork-branch-and-pull-request/)
[Git Branching Strategies for Maintainable Test Automation - DZone DevOps](https://dzone.com/articles/git-branching-strategies-for-maintainable-test-aut)
[How to Use Git and Git Workflows – a Practical Guide](https://www.freecodecamp.org/news/practical-git-and-git-workflows/)

[stevenharman/git-workflows](https://github.com/stevenharman/git-workflows)
[reenhanced/gitreflow](https://github.com/reenhanced/gitreflow)
[hub · the command-line wrapper for git](https://hub.github.com/)

[My Git Workflow](http://blog.osteele.com/posts/2008/05/my-git-workflow/)
[Commit Policies](http://blog.osteele.com/posts/2008/05/commit-policies/)

[Git 常用命令备忘 – 尘埃落定](http://www.lovelucy.info/git-command-cheatsheet.html)

Git Flow:

- `master`: release candidate, release, and hotfix
- `develop`: gatekeeper branch, parent of feature branches, CI/CD
- merge hotfix on `master` to `develop`

Truck:

- `master`: parent of feature branches, CI/CD

Commits to `master` kicks off CI/CD

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

[GOTO 2015 • Deep Dive into Git • Edward Thomson - YouTube](https://www.youtube.com/watch?v=dBSHLb1B8sw)
[TechDays 2017 - Edward Thomson - Inside Git - YouTube](https://www.youtube.com/watch?v=yupKgmYdy40)
[Introduction to Git with Scott Chacon of GitHub - YouTube](https://www.youtube.com/watch?v=ZDR433b0HJY)
[Advanced Git: Graphs, Hashes, and Compression, Oh My! - YouTube](https://www.youtube.com/watch?v=ig5E8CcdM9g)

## Presentations

[schacon/tale_of_three_trees](https://github.com/schacon/tale_of_three_trees)
[schacon/showoff-wrangling-git](https://github.com/schacon/showoff-wrangling-git)
May need [puppetlabs/showoff](https://github.com/puppetlabs/showoff)

## Tips and Tricks

[First Aid git](http://firstaidgit.io/#/)
[First Aid Kit for Git | Learn Version Control with Git](https://www.git-tower.com/learn/git/first-aid-kit/)
[git-tips/tips: Most commonly used git tips and tricks.](https://github.com/git-tips/tips)
[nirajpandkar/git-tip: CLI that gives a random git-tip.](https://github.com/nirajpandkar/git-tip)
[A few git tips you didn't know about](http://mislav.uniqpath.com/2010/07/git-tips/)
[25 Tips for Intermediate Git Users](https://www.andyjeffries.co.uk/25-tips-for-intermediate-git-users/)
[Git tips and tricks](http://blog.mixu.net/2012/04/06/git-tips-and-tricks/)
[GIT Conventions — Medium](https://medium.com/@tjholowaychuk/git-conventions-a940ee20862d)
[10 Git Commands You Should Know – Towards Data Science](https://towardsdatascience.com/10-git-commands-you-should-know-df54bea1595c)
[10 insanely useful Git commands you wish existed - and their alternatives - datree](https://datree.io/git-commands/)
[Dangit, git!](https://dangitgit.com/)
[git Archives - Everything CLI](https://www.everythingcli.org/tag/git/)

[Five Key Git Concepts Explained the Hard Way – zwischenzugs](https://zwischenzugs.com/2018/03/14/five-key-git-concepts-explained-the-hard-way/)
[Create Your Own Git Diagrams – zwischenzugs](https://zwischenzugs.com/2018/03/08/create-your-own-git-diagrams/)
[Martin Heinz - Advanced Git Features You Didn’t Know You Needed](https://martinheinz.dev/blog/43)

[A Guide To Undoing Mistakes With Git (Part 1) — Smashing Magazine](https://www.smashingmagazine.com/2021/05/undoing-mistakes-git-part1/)
[A Guide To Undoing Mistakes With Git (Part 2) — Smashing Magazine](https://www.smashingmagazine.com/2021/05/undoing-mistakes-git-part2/)

[Advanced Git Commands: Rewriting History - DZone Open Source](https://dzone.com/articles/advanced-git-commands-rewriting-history)

[tryexceptpass - Episode 6 - Underused Git Commands that Simplify Your Life](https://tryexceptpass.org/podcast/ep6-underused-git-commands/)

[How (and why!) to keep your Git commit history clean | GitLab](https://about.gitlab.com/2018/06/07/keeping-git-commit-history-clean/)
[Git tips: 合并 commit 保持分支干净整洁 – 尘埃落定](http://www.lovelucy.info/git-tips-combine-commits-keep-your-branch-clean.html)
[The Elements of Commit Style](http://mcandre.gitbooks.io/elements-of-commit-style/content/index.html)
[6 best practices for teams using Git | Opensource.com](https://opensource.com/article/20/7/git-best-practices)

## Githooks

[Git Hooks | Learn how to use pre-commit hooks, post-commit hooks, post-receive hooks, and more. | Matthew Hudson](http://githooks.com/)
[How I Learned to Stop Worrying and Love Git Hooks | CSS-Tricks](https://css-tricks.com/how-i-learned-to-stop-worrying-and-love-git-hooks/)
[How to write custom Git hooks and publishing your code to a website | Opensource.com](https://opensource.com/life/16/8/how-construct-your-own-git-server-part-6)

[okonet/lint-staged: 🚫💩 — Run linters on git staged files](https://github.com/okonet/lint-staged)
[typicode/husky: Git hooks made easy](https://github.com/typicode/husky)

[Using lint-staged, husky, and pre-commit hooks to fail fast and early](https://codeburst.io/continuous-integration-lint-staged-husky-pre-commit-hook-test-setup-47f8172924fc)

<!-- more -->

---

# Koan

[Git Cheatsheet • NDP Software](http://ndpsoftware.com/git-cheatsheet.html)
[AOSP Git and Repo cheatsheet](https://source.android.com/source/developing.html#git-and-repo-cheatsheet)
[Explain Git with D3](https://onlywei.github.io/explain-git-with-d3/)
[Oh Shit, Git!?!](https://ohshitgit.com/)

## Conditional config

[Edward Thomson: Git Conditional Includes](https://edwardthomson.com/blog/git_conditional_includes.html)
Use folder prefix to include different gitconfig

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

[How can I change the author (name / email) of a commit? | Learn Version Control with Git](https://www.git-tower.com/learn/git/faq/change-author-name-email/)

```sh
# amend several commits, useful for not yet pushed commits
git rebase -i HEAD^5 # or commitish
# pick commits to change author to `edit`
# for each commit
git commit --amend --author "New Author <new@email>" --no-edit
git rebase --continue
```

```sh
#!/bin/sh

FILTER_BRANCH_SQUELCH_WARNING=1 git filter-branch --env-filter '
OLD_EMAIL="leesei@gmail.com"
CORRECT_NAME="Seasoned Bits Solutions"
CORRECT_EMAIL="seasoned.bits@gmail.com"

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

## force pull

```sh
git fetch origin master
git reset --hard FETCH_HEAD
git clean -df
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

[Commit only part of a file in Git - Stack Overflow](https://stackoverflow.com/questions/1085162/commit-only-part-of-a-file-in-git)
[Git - git-add Documentation](https://git-scm.com/docs/git-add#Documentation/git-add.txt-patch)

`Stage this hunk [y,n,q,a,d,/,j,J,g,s,e,?]?`

Here is a description of each option:

- <kbd>y</kbd> stage this hunk for the next commit
- <kbd>n</kbd> do not stage this hunk for the next commit
- <kbd>q</kbd> quit; do not stage this hunk or any of the remaining hunks
- <kbd>a</kbd> stage this hunk and all later hunks in the file
- <kbd>d</kbd> do not stage this hunk or any of the later hunks in the file
- <kbd>g</kbd> select a hunk to go to
- <kbd>/</kbd> search for a hunk matching the given regex
- <kbd>j</kbd> leave this hunk undecided, see next undecided hunk
- <kbd>J</kbd> leave this hunk undecided, see next hunk
- <kbd>k</kbd> leave this hunk undecided, see previous undecided hunk
- <kbd>K</kbd> leave this hunk undecided, see previous hunk
- <kbd>s</kbd> split the current hunk into smaller hunks
- <kbd>e</kbd> manually edit the current hunk
- <kbd>?</kbd> print hunk help

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

Tagging and pushing tag to GitHub will aldo allow you to download the zipped code.

## reduce repo size

[How to Shrink a Git Repository](http://stevelorek.com/how-to-shrink-a-git-repository.html)
[What is git gc and how does it work? | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/git-gc)
[Reduce git repository size - Stack Overflow](http://stackoverflow.com/questions/2116778/reduce-git-repository-size)
[Git pull error: unable to create temporary sha1 filename - Stack Overflow](http://stackoverflow.com/questions/685319/git-pull-error-unable-to-create-temporary-sha1-filename/)
[Optimize your repository using Git GC | by Ameet Prajapati | codeburst](https://codeburst.io/optimize-your-repository-using-git-gc-c4675ed8b7b2)

```sh
git fsck # show dangling (orphaned) commit
git gc --aggressive --prune=now
git reflog expire --expire-unreachable=now --all git gc --prune=now
```

## worktree

[Git - git-worktree Documentation](https://git-scm.com/docs/git-worktree)
[Using multiple working trees in Git - DEV Community 👩‍💻👨‍💻](https://dev.to/oliverjumpertz/using-multiple-working-trees-in-git-122d)
[Experiment on your code freely with Git worktree | Opensource.com](https://opensource.com/article/21/4/git-worktree)

## Get current branch

```sh
git branch --show-current  # Git 2.22+
git rev-parse --abbrev-ref HEAD
```

## Rebase feature branch

```sh
git reset --soft master
```

## Commits count

This can be used as build number

```sh
git rev-list --count <branch>
```

## difftool/mergetool

Using `diff-so-fancy` as PAGER

[Git - git-difftool Documentation](https://www.git-scm.com/docs/git-difftool)
[Git - git-mergetool Documentation](https://www.git-scm.com/docs/git-mergetool)

[Setting up and using Meld as your git difftool and mergetool - Stack Overflow](https://stackoverflow.com/questions/34119866/setting-up-and-using-meld-as-your-git-difftool-and-mergetool)
[git merge - How to set Meld as git mergetool - Stack Overflow](https://stackoverflow.com/questions/12956509/how-to-set-meld-as-git-mergetool)
[Git Tutorial: Diff and Merge Tools - YouTube](https://www.youtube.com/watch?v=iCGrKFH2oeo)

### vimdiff

[A better Vimdiff Git mergetool | Vim Tips Wiki | FANDOM powered by Wikia](https://vim.fandom.com/wiki/A_better_Vimdiff_Git_mergetool)

[Use vimdiff as git mergetool - Ruslan Osipov](http://www.rosipov.com/blog/use-vimdiff-as-git-mergetool/)

## Monorepos

> many of these discussions are on Node.js/Frontend dev
> see `node-js-notes.md#local-dev-dependency`

[Rush](https://rushjs.io/)

[Mono-repo or multi-repo? Why choose one, when you can have both?](https://medium.com/@patrickleet/mono-repo-or-multi-repo-why-choose-one-when-you-can-have-both-e9c77bd0c668) `meta`
[Repo style wars: mono vs multi](http://www.gigamonkeys.com/mono-vs-multi/)

[Advantages of monorepos](https://danluu.com/monorepo/)
[Pros and Cons of Using Monorepos - FOSSA](https://fossa.com/blog/pros-cons-using-monorepos/)
[babel/monorepo.md at master · babel/babel](https://github.com/babel/babel/blob/master/doc/design/monorepo.md)
[Monorepos: Please don’t!. Here we are at the beginning of 2019… | by Matt Klein | Medium](https://medium.com/@mattklein123/monorepos-please-dont-e9a279be011b)
[Monorepo: please do!. You should choose a monorepo because… | by Adam Jacob | Medium](https://medium.com/@adamhjk/monorepo-please-do-3657e08a4b70)

[Nx: Smart, Extensible Build Framework](https://nx.dev/)
[Nx Quickstart - How to Scale a JavaScript Project - YouTube](https://www.youtube.com/watch?v=VUyBY72mwrQ)

### Meta

[Bring your monorepo down to size with sparse-checkout - The GitHub Blog](https://github.blog/2020-01-17-bring-your-monorepo-down-to-size-with-sparse-checkout/)
[Developing a plugin for meta. In my last post, I introduced meta and… | by Patrick Lee Scott | Medium](https://patrickleet.medium.com/developing-a-plugin-for-meta-bd2e9c39882d)
[mateodelnorte/meta: tool for turning many repos into a meta repo. why choose many repos or a monolithic repo, when you can have both with a meta repo?](https://github.com/mateodelnorte/meta)
[mateodelnorte/loop: loop through commands in fun and amazing ways!](https://github.com/mateodelnorte/loop)

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
