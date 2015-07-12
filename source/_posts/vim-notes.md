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

<!-- more -->

[Vimcasts - Free screencasts about the text editor Vim](http://vimcasts.org/)
[A guide to getting started with Vim](http://www.integralist.co.uk/posts/vim-1.html)
[Vim Workflow](http://www.integralist.co.uk/posts/vim-2.html)
[Vim Workflow (Part Deux)](http://www.integralist.co.uk/posts/vim-3.html)
[简明 Vim 练级攻略 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/5426.html)
[无插件Vim编程技巧 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/11312.html)

## hex mode

Enter hex mod
```
:%!xxd
```

Exit hex mod
```
:%!xxd -r
```

## diff mode

`vimdiff file1 file2`

```
]c :        - next difference
[c :        - previous difference
do          - diff obtain
dp          - diff put
zo          - open folded text
zc          - close folded text
:diffupdate, :diffu - re-scan the files for differences
:set [no]scrollbind - disable/enable scroll binding
```

[Vim documentation: diff](http://vimdoc.sourceforge.net/htmldoc/diff.html)
[chrisbra/vim-diff-enhanced](https://github.com/chrisbra/vim-diff-enhanced)
