---
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

[The GNU Awk User’s Guide](http://www.gnu.org/software/gawk/manual/gawk.html)
[Cover - GNU AWK](https://learnbyexample.github.io/learn_gnuawk/)
[How To Use awk In Bash Scripting - nixCraft](https://www.cyberciti.biz/faq/bash-scripting-using-awk/)
[The many faces of awk | Network World](https://www.networkworld.com/article/3454979/the-many-faces-of-awk.html)
[Doing math with awk | Network World](https://www.networkworld.com/article/2974753/doing-math-with-awk.html)
[How to Use the awk Command on Linux](https://www.howtogeek.com/562941/how-to-use-the-awk-command-on-linux/amp/)

```sh
awk '{PROGRAM}' file
awk -f <PROGRAM.awk> file

# passing variable to AWK
n1=5; n2=10;
echo | awk -v x=$n1 -v y=$n2 -f program.awk
```

```awk
BEGIN {...}
CONDITION {action}
CONDITION {action}
END {...}
```

<!-- more -->

A Awk program is executed on a row basis, with optional rules to switch the statements (block) to execute
each row is parsed into fields by the separator.
The default action is `{ print $0 }` (print the whole row).
We can add condition before statement to serve as filter, condition can use field, regular expression and comparisons.

Awk program:

```awk
#!/usr/bin/awk -f

# This line is a comment

BEGIN {
    printf "%s\n","User accounts:"
    print "=============="
    FS=":"
    n=0
}

# Now we'll run through the data
{
    if ($3 >= 1000) {
        print $1
        n ++
    }
}

END {
    print "=============="
    print n " accounts"
}
```

```
NR      Number of Row
NF      Number of Fields
$()     field substitution
```

## filtering

```sh
# print first field of first row
awk 'NR==1 { print $1 }'

# print rows with third field >= 1000
awk -F":" 'BEGIN {print "user accounts:"} $3 >= 1000 ' /etc/passwd

# print rows starts with systemd (regular expression)
awk '/^systemd/' /etc/group

# print rows not ending with ":" (having member) (regular expression)
awk '! /:$/' /etc/group
```

## field separator

`$N` is the N-th field, `$NF` is the the last field

```sh
# get second field with ":" as separator
awk 'BEGIN { FS = ":" } ; { print $2 }'
awk -F: '{ print $2 }'

# comma separate the output fields, otherwise they will be concatenated to a single string
date | awk '{print $4 $3 $2}'   # 2019Dec05
# specify output field separator, `$4-$3-$2` does a mathematical subtraction
date | awk '{OFS="-"; print $4,$3,$2}'
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

| Task                                 | Command                                |
| ------------------------------------ | -------------------------------------- |
| 显示文件的第一列                     | `awk '{print $1}' <file>`              |
| 反序显示文件的前两列                 | `awk '{print $2,”\t”,$1}' <file>`      |
| 输出前两列的总和                     | `awk '{print $1 + $2}' <file>`         |
| 查找所有包括”money” 行并输出最后一列 | `awk '/money/ {print $NF}' <file>`     |
| 查找第二列中包含 “money”             | `awk '$2 ~ /money/ {print $0}' <file>` |
| 查找第三列中不包括”A”                | `awk '$3 !~ /A$/ {print $0}' <file>`   |

## print first 16K lines

```sh
awk -F '' 'NF < 16384' infile >outfile
awk 'length($0) < 16384' infile >outfile
# which is equivalent to
awk '{ if (length($0) < 16384) print }' infile >outfile
```

## Reference

[The GNU Awk User’s Guide](http://www.gnu.org/software/gawk/manual/gawk.html)
[AWK Programming](http://www.softpanorama.org/Tools/awk.shtml)
[awk is a beautiful tool](http://www.eriwen.com/tools/awk-is-a-beautiful-tool/)
[awk 使用手册 - fanqiang.com](http://fanqiang.chinaunix.net/program/other/2005-09-07/3621.shtml)
[AWK 简明教程 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/9070.html)
[AWK Tutorial](http://www.tutorialspoint.com/awk/)

[Awk - A useful little language](https://dev.to/rrampage/awk---a-useful-little-language-2fhf)

[Famous Awk One-Liners Explained, Part I: File Spacing, Numbering and Calculations - good coders code, great reuse](http://www.catonmat.net/blog/awk-one-liners-explained-part-one/)
[Famous Awk One-Liners Explained, Part II: Text Conversion and Substitution - good coders code, great reuse](http://www.catonmat.net/blog/awk-one-liners-explained-part-two/)
[Famous Awk One-Liners Explained, Part III: Selective Printing and Deleting of Certain Lines - good coders code, great reuse](http://www.catonmat.net/blog/awk-one-liners-explained-part-three/)
[Update on Famous Awk One-Liners Explained: String and Array Creation - good coders code, great reuse](http://www.catonmat.net/blog/update-on-famous-awk-one-liners-explained/)
http://www.pement.org/awk/awk1line.txt

[AWK GTF! How to Analyze a Transcriptome Like a Pro - Part 1 - Blog - Reason I Am Here - Nacho Caballero](http://reasoniamhere.com/2013/09/16/awk-gtf-how-to-analyze-a-transcriptome-like-a-pro-part-1/)
[AWK GTF! How to Analyze a Transcriptome Like a Pro - Part 2 - Blog - Reason I Am Here - Nacho Caballero](http://reasoniamhere.com/2013/09/17/awk-gtf-how-to-analyze-a-transcriptome-like-a-pro-part-2/)
[AWK GTF! How to Analyze a Transcriptome Like a Pro - Part 3 - Blog - Reason I Am Here - Nacho Caballero](http://reasoniamhere.com/2013/09/18/awk-gtf-how-to-analyze-a-transcriptome-like-a-pro-part-3/)

[Common threads: Awk by example, Part 1](http://www.ibm.com/developerworks/library/l-awk1/)
[Common threads: Awk by example, Part 2](http://www.ibm.com/developerworks/library/l-awk2/)

[Awk by Example, Part 1 : An intro to the great language with the strange name](http://www.funtoo.org/Awk_by_Example,_Part_1)
[Awk by Example, Part 2 : Records, loops, and arrays](http://www.funtoo.org/Awk_by_Example,_Part_2)
[Awk by Example, Part 3 : String functions and ... checkbooks?](http://www.funtoo.org/Awk_by_Example,_Part_3)

[Awk, Nawk and GNU Awk Cheat Sheet - good coders code, great reuse](http://www.catonmat.net/blog/awk-nawk-and-gawk-cheat-sheet/)

[Awk - A Tutorial and Introduction - by Bruce Barnett](http://www.grymoire.com/Unix/Awk.html)
[Awk Quick Reference - Bruce Barnett](http://www.grymoire.com/Unix/AwkRef.html)
[Top Examples of Awk Command in Unix](http://www.folkstalk.com/2011/12/good-examples-of-awk-command-in-unix.html)
[8 Powerful Awk Built-in Variables – FS, OFS, RS, ORS, NR, NF, FILENAME, FNR](http://www.thegeekstuff.com/2010/01/8-powerful-awk-built-in-variables-fs-ofs-rs-ors-nr-nf-filename-fnr/)

[sed & awk, 2nd Edition](https://library.oreilly.com/book/9781565922259/sed-amp-awk/toc.xhtml)
