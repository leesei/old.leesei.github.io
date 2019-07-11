---
title: "vim notes"
date: 2015-01-14 12:48:30
categories:
- app
tags:
- shell-tool
- vim
- notes
---

[vim](http://en.wikipedia.org/wiki/Vim_(text_editor)) is a screen-oriented text editor originally created for the Unix operating system

[Vim documentation: help](http://vimdoc.sourceforge.net/htmldoc/help.html)

[Home - Neovim](https://neovim.io/)
[spf13-vim - The Ultimate Vim Distribution](http://vim.spf13.com/)
[Home | SpaceVim](http://spacevim.org/)

<!-- more -->

[Vimcasts - Free screencasts about the text editor Vim](http://vimcasts.org/)
[vimgifs](https://vimgifs.com/)
[A guide to getting started with Vim](http://www.integralist.co.uk/posts/vim-1.html)
[Vim Workflow](http://www.integralist.co.uk/posts/vim-2.html)
[Vim Workflow (Part Deux)](http://www.integralist.co.uk/posts/vim-3.html)
[Vim workflows](http://mrmrs.io/writing/2013/12/21/vim-workflows/)
[简明 Vim 练级攻略 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/5426.html)
[无插件Vim编程技巧 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/11312.html)
[Interactive Vim tutorial](http://www.openvim.com/tutorial.html)
[How to Learn Vim](http://mrmrs.io/writing/2013/12/19/how-to-learn-vim/)
[VimGolf - real Vim ninjas count every keystroke!](http://www.vimgolf.com/)
[Learn Vimscript the Hard Way](http://learnvimscriptthehardway.stevelosh.com/)
[How To Learn Vim: A Four Week Plan – Actualize – Medium](https://medium.com/actualize-network/how-to-learn-vim-a-four-week-plan-cd8b376a9b85)

[aharris88/learn-vimscript: My solutions to the exercises in Learn Vimscript the Hard Way](https://github.com/aharris88/learn-vimscript)
[Vim Cheat Sheet - English](https://vim.rtorr.com/)

## hex mode

Enter hex mod: `:%!xxd`
Exit hex mod: `:%!xxd -r`

## diff mode

`vimdiff file1 file2`

```
Ctrl+w Ctrl+w - change focus
]c          - next difference
[c          - previous difference
do          - diff obtain
dp          - diff put
zo          - open folded text
zc          - close folded text
:diffupdate, :diffu - re-scan the files for differences
:set [no]scrollbind - disable/enable scroll binding
```

[Vim documentation: diff](http://vimdoc.sourceforge.net/htmldoc/diff.html)
[chrisbra/vim-diff-enhanced](https://github.com/chrisbra/vim-diff-enhanced)
[Pacmatic: Get emails about pending system updates with cron-pacmatic](http://kmkeen.com/pacmatic/)

## paste

[editor - Turning off auto indent when pasting text into vim - Stack Overflow](http://stackoverflow.com/questions/2514445/turning-off-auto-indent-when-pasting-text-into-vim)
[coderwall.com : establishing geek cred since 1305712800](https://coderwall.com/p/if9mda/automatically-set-paste-mode-in-vim-when-pasting-in-insert-mode)

enter paste mode: `:set paste`
exit paste mode:  `:set nopaste`

You can toggle paste mode with key by adding this to your `.vimrc`:

```
set pastetoggle=<F9>
```
