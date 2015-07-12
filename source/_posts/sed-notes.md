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

http://eriwen.com/tools/get-sed-savvy-1/
http://eriwen.com/tools/get-sed-savvy-2/
http://eriwen.com/tools/get-sed-savvy-3/
http://www.catonmat.net/blog/awk-one-liners-explained-part-one/
http://www.catonmat.net/blog/sed-one-liners-explained-part-two/
http://www.catonmat.net/blog/sed-one-liners-explained-part-three/
http://www.catonmat.net/blog/sed-stream-editor-cheat-sheet/
http://sed.sourceforge.net/sed1line.txt
[Sed by Example, Part 1](http://www.funtoo.org/Sed_by_Example,_Part_1)
[Sed by Example, Part 2](http://www.funtoo.org/Sed_by_Example,_Part_2)
[Sed by Example, Part 3](http://www.funtoo.org/Sed_by_Example,_Part_3)
[Sed - An Introduction and Tutorial](http://www.grymoire.com/Unix/Sed.html)

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
# count length of line 10
sed -n '10 p' filename | wc -c
```
