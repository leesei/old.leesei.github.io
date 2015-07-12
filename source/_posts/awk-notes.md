title: "awk notes"
date: 2015-01-13 12:56:24
categories:
- app
tags:
- shell-tool
- awk
- notes
toc: true
---

[AWK](http://en.wikipedia.org/wiki/AWK) is an interpreted programming language designed for text processing and typically used as a data extraction and reporting tool.

```sh
awk '{PROGRAM}' file
awk -f <PROGRAM.awk> file
```

<!-- more -->

program is executed on a row basis, with optional rules to switch the statements (block) to execute
each row is parsed into fields by the seperator

```
NR      Number of Row
NF      Number of Fields
$()     field substitution
```

## field seperator

```sh
awk 'BEGIN { FS = ":" } ; { print $2 }'
awk -F: '{ print $2 }'
```

## print number of lines

```sh
awk 'BEGIN {sum=0} {sum=sum+1} END {print sum}' filename
awk 'END{print NR}' filename
```

## print line number and second last field

```sh
awk '{ print "Line " NR ": " $(NF-1) }' test.txt
```

Task | Command
--- | ---
显示文件的第一列 | `awk '{print $1}' <file>`
反序显示文件的前两列 | `awk '{print $2,”\t”,$1}' <file>`
输出前两列的总和 | `awk '{print $1 + $2}' <file>`
查找所有包括”money” 行并输出最后一列 | `awk '/money/ {print $NF}' <file>`
查找第二列中包含 “money” | `awk '$2 ~ /money/ {print $0}' <file>`
查找第三列中不包括”A” | `awk '$3 !~ /A$/ {print $0}' <file>`

## print first 16K lines

```
awk -F '' 'NF < 16384' infile >outfile
awk 'length($0) < 16384' infile >outfile
# which is equivalent to
awk '{ if (length($0) < 16384) print }' infile >outfile
```

## Reference

[The GNU Awk User’s Guide](http://www.gnu.org/software/gawk/manual/gawk.html)
[AWK Programming](http://www.softpanorama.org/Tools/awk.shtml)
[awk is a beautiful tool](http://www.eriwen.com/tools/awk-is-a-beautiful-tool/)
[awk使用手册 - fanqiang.com](http://fanqiang.chinaunix.net/program/other/2005-09-07/3621.shtml)

[Famous Awk One-Liners Explained, Part I: File Spacing, Numbering and Calculations - good coders code, great reuse](http://www.catonmat.net/blog/awk-one-liners-explained-part-one/)
[Famous Awk One-Liners Explained, Part II: Text Conversion and Substitution - good coders code, great reuse](http://www.catonmat.net/blog/awk-one-liners-explained-part-two/)
[Famous Awk One-Liners Explained, Part III: Selective Printing and Deleting of Certain Lines - good coders code, great reuse](http://www.catonmat.net/blog/awk-one-liners-explained-part-three/)
[Update on Famous Awk One-Liners Explained: String and Array Creation - good coders code, great reuse](http://www.catonmat.net/blog/update-on-famous-awk-one-liners-explained/)

[Awk, Nawk and GNU Awk Cheat Sheet - good coders code, great reuse](http://www.catonmat.net/blog/awk-nawk-and-gawk-cheat-sheet/)

[Awk - A Tutorial and Introduction - by Bruce Barnett](http://www.grymoire.com/Unix/Awk.html)
[Awk Quick Reference - Bruce Barnett](http://www.grymoire.com/Unix/AwkRef.html)

http://www.pement.org/awk/awk1line.txt
