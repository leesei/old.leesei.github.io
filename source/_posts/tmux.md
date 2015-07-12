title: "Tmux"
date: 2014-12-11 17:59:04
categories:
- app
tags:
- shell-tool
- tmux
- tmuxifier
toc: true
---

tmux includes `.bash_profile`/`.profile` but not `.bashrc`

## reference

http://www.openbsd.org/cgi-bin/man.cgi?query=tmux
https://wiki.archlinux.org/index.php/tmux
http://www.rdegges.com/tools-i-use-tmux/
http://mutelight.org/practical-tmux
http://robots.thoughtbot.com/a-tmux-crash-course
http://tangosource.com/blog/a-tmux-crash-course-tips-and-tweaks/

## .tmux.conf

https://gist.github.com/snuggs/800936/raw
http://files.floriancrouzat.net/dotfiles/.tmux.conf
https://gist.github.com/napcs/1147532
http://justinlilly.com/dotfiles/tmux.html
http://zanshin.net/2013/09/05/my-tmux-configuration/
http://tonkersten.com/2011/07/104-switching-to-tmux/

[jimeh/tmux-themepack](https://github.com/jimeh/tmux-themepack)

`bind -n (-n: no prefix)`

## tmuxifier

[jimeh/tmuxifier](https://github.com/jimeh/tmuxifier)

```sh
git clone https://github.com/jimeh/tmuxifier.git ~/.tmuxifier
```

## tmux not loading bashrc 

```sh
$echo case $- in *i*) . ~/.bashrc;; esac >> .bash_profile 
```

## key bindings (cheatsheet)

[dayid's screen and tmux cheat sheet](http://www.dayid.org/os/notes/tm.html)
[tmux cheatsheet](https://gist.github.com/andreyvit/2921703)
