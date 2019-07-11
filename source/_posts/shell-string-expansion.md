---
title: "Shell string expansion"
date: 2014-12-08 12:03:44
categories:
- linux
tags:
- shell
- notes
---

## string manipulation/expansion

> After reading `fish` shell's philosophy, I now think using `sed` and other tools is better than relying on shell features.

http://tldp.org/LDP/abs/html/string-manipulation.html
http://wiki.bash-hackers.org/syntax/pe
http://mintaka.sdsu.edu/GF/bibliog/latex/debian/bash.html
[Bash One-Liners Explained, Part II: Working with strings - good coders code, great coders reuse](http://www.catonmat.net/blog/bash-one-liners-explained-part-two/)

> TODO: add zsh manual

```sh
# to upper
echo $string | tr [:lower:] [:upper:]
newstring=${string^^}
# to lower
echo $string | tr [:upper:] [:lower:]
newstring=${string,,}

# substring extraction
substring=${string:1:-2}

# string expansion
${var:-default} # means $var if $var is defined and otherwise "default"
${var:-} # default $var to null string to avoid error when `set -u` is used
${var:+value} # means if $var is defined use "value"; otherwise nothing

# string substitution
${string/substring/replacement}   # replace "substring" with "replacement"
${string//substring/replacement}  # replace all occurrences (g) of "substring" with "replacement"
${string/#substring/replacement}  # replace front match (^) "substring" with "replacement"
${string/%substring/replacement}  # replace end match ($) "substring" with "replacement"

# file path manipulation
# get dir from full path
$(dirname "$path")
${path%/*}
# get file name from full path
$(basename "$path")
${path##*/}

FILE="example.tar.gz"
${FILE%%.*}          # "example", stripped longest extension
${FILE%.*}           # "example.tar", stripped shortest extension
${FILE#*.}           # "tar.gz", longest extension
${FILE##*.}          # "gz", shortest extension

# mimic https://nodejs.org/api/path.html#path_path_parse_pathstring
declare -A pathObj
base=${file##*/}
pathObj[dir]=${file%/*}
pathObj[base]=${base}
pathObj[name]=${base%.*}
pathObj[ext]=.${base##*.} # note added '.' prefix
# NOTE: ext has bug if $file has no extension

if [ ${path:0:1} = '/' ]; then
    tmp=${path:1}    # strip leading '/'
fi
tmp=${path#/}        # strip leading '/'
tmp=${path%/}        # strip trailing '/'
```
