---
title: "Git Settings"
date: 2014-12-17 13:53:33
categories:
  - app
tags:
  - git
  - settings
toc: true
---

[git - Can I specify multiple users for myself in .gitconfig? - Stack Overflow](https://stackoverflow.com/questions/4220416/can-i-specify-multiple-users-for-myself-in-gitconfig/43654115#43654115)

## Minimal config

```sh
# minimal git config
git config --global pull.rebase true
git config --global rebase.autosquash true
git config --global rebase.autostash true
git config --global log.decorate true
git config --global help.autocorrect 5
git config --global core.autocrlf true # on Windows machine
git config --global core.autocrlf input # otherwise
```

## Backup

```sh
.gitignore
.ssh/config
.ssh/git.id_rsa{,.pub}
```

## Reference

[Git - Git Configuration](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)
[git-config man page - git-core-doc - General Commands](https://www.mankier.com/1/git-config)
