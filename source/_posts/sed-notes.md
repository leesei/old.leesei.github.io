title: "sed notes"
date: 2015-01-13 12:55:35
categories:
- app
tags:
- shell-tool
- sed
- notes
toc: true
---

[sed](http://en.wikipedia.org/wiki/Sed) (stream editor) is a Unix utility that parses and transforms text, using a simple, compact programming language.

```sh
sed 'commands' file
sed -f <PROGRAM.sed> file
```

<!-- more -->

## Reference

[Get sed savvy - part 1](http://www.eriwen.com/tools/get-sed-savvy-1/)
[Get sed savvy - part 2](http://www.eriwen.com/tools/get-sed-savvy-2/)
[Get sed savvy - part 3](http://www.eriwen.com/tools/get-sed-savvy-3/)
[Famous Sed One-Liners Explained, Part I: File Spacing, Numbering and Text Conversion and Substitution - good coders code, great reuse](http://www.catonmat.net/blog/sed-one-liners-explained-part-one/)
[Famous Sed One-Liners Explained, Part II: Selective Printing of Certain Lines - good coders code, great reuse](http://www.catonmat.net/blog/sed-one-liners-explained-part-two/)
[Famous Sed One-Liners Explained, Part III: Selective Deletion of Certain Lines and Special Applications - good coders code, great reuse](http://www.catonmat.net/blog/sed-one-liners-explained-part-three/)
[Sed - UNIX Stream Editor - Cheat Sheet - good coders code, great reuse](http://www.catonmat.net/blog/sed-stream-editor-cheat-sheet/)
[Sed one-liners](http://sed.sourceforge.net/sed1line.txt)
[Sed by Example, Part 1](http://www.funtoo.org/Sed_by_Example,_Part_1)
[Sed by Example, Part 2](http://www.funtoo.org/Sed_by_Example,_Part_2)
[Sed by Example, Part 3](http://www.funtoo.org/Sed_by_Example,_Part_3)
[Sed - An Introduction and Tutorial](http://www.grymoire.com/Unix/Sed.html)
[Using Sed | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/using-sed)
[sed 简明教程 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/9104.html)
[Your Own Linux..!: sed](http://www.yourownlinux.com/search/label/sed)

## Examples

```sh
# trim leading and trailing whitespace
echo ${string} | sed 's/^[[:space:]]*\(.*\)[[:space:]]*$/\1/'

# search and replace in file (inplace)
sed -i 's/STRING_TO_REPLACE/STRING_TO_REPLACE_IT/g' file
# replace "apple" with "(apple)", not '&' is reference
sed s/apple/(&)/ file
# or use regex group
sed s/\(apple\)/(\1)/ file
```

```sh
# get n-th line from file
sed -n '<n> p' filename
echo filename | sed "<n>q;d"
# count length of line 10
sed -n '10 p' filename | wc -c
```

```sh
# insert at N-th line of file
sed -i 'N i <LINE-TO-BE-ADDED>' FILE.txt
```
