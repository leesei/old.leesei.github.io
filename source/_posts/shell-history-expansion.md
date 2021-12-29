---
title: "Shell history expansion"
date: 2014-12-08 12:03:44
categories:
  - linux
tags:
  - shell
  - notes
---

## History Expansion

http://www.eriwen.com/bash/effective-shorthand/
http://www.catonmat.net/blog/the-definitive-guide-to-bash-command-line-history/
[Bash One-Liners Explained, Part IV: Working with history - good coders code, great coders reuse](http://www.catonmat.net/blog/bash-one-liners-explained-part-four/)
[zshexpn: zsh expansion and substitution - man page](https://www.mankier.com/1/zshexpn)
[bash: History_Expansion - man page](https://www.mankier.com/1/bash#History_Expansion)
[Bang Bang - Command Recall in Linux](http://craig-russell.co.uk/2011/09/28/bang-bang-command-recall-in-linux.html#.WsrpAnVuay8)
[Unix history and bang commands — Jack Hsu](https://jaysoo.ca/2009/09/16/unix-history-and-bang-commands/)

> TODO: add zsh manual

```sh
man history
```

Each line of history is a _command_, consisting of more than one _words_ (0-indexed).

```sh
cp myfile.txt my/directory/path
cd !$  # cd my/directory/path

vi /etc/fstabs  # oops!
sudo !!  # sudo vi /etc/fstab

echo 1 2 3 4 5 6 7 8 9 10  # test word designators
/path/to/file/a.b.c        # test modifiers

echo $_  # last argument of last command
```

Event designators:
`!` start a history substitution, will use last command if no event designator specified
`!!` expands to the last command
`!42` expands to the 42nd command in the history list
`!-3` 3 commands before (all arguments)
`!string` most recent command stating with _string_
`!?string?` most recent command stating with _string_
`^foo^bar` last command with the first occurrence of _foo_ replaced with _bar_
`!#` expands to current command typed so far

Word Designators:
Word designators follow event designators, separated by `:`

`:0` command name
`:n` n-th word, 0-indexed, of the command (= n-th argument, 1-indexed)
`:x-y` range of words from x to y (0-indexed, -y is synonymous with 0-y)
`:^` 1st word, 0-indexed (= first argument)
`:$` last word (= last argument)
`:*` all words but the zeroth (synonymous with 1-$)
`:n*` n-th (0-indexed) to last words (synonymous with n-$) (= n-th to last argument)

Shortcuts:
`!*` `!:*`
`!$` `!:$`
`!^` `!:^`

Modifiers:
Modifiers follow word designators, separated by `:`

`:h` head pathname (`dirname`)
`:t` tail pathname (`basename`)
`:e` suffix
`:r` remove suffix
`:p` print but not execute (TAB in mordern shell does this)
`:q`/`:x` quote substituted words to prevent further substitutions
`:Q` unquote words
`:u` uppercase all words
`:l` lowercase all words
`:s/foo/bar/` replace _foo_ with _bar_
`:gs/foo/bar/` global replace _foo_ with _bar_

`!!:$:e` suffix of the last argument of the last command
`!!:$:h` basepath of the last argument of the last command

```sh
ls /path/to/file/a.b.c
!$:h   # /path/to/file
!$:t   # a.b.c
!$:e   # c
!$:r   # /path/to/file/a.b

echo 1 2 3 4 5 6 7 8 9 10
!:q    #'echo' '1' '2' '3' '4' '5' '6' '7' '8' '9' '10'
!:2-5  # 2 3 4 5
!:*    # 1 2 3 4 5 6 7 8 9 10
!:1-3:s/1/foo/:s/2/bar/:s/3/baz/:q  # 'foo' 'bar' 'baz'
```
