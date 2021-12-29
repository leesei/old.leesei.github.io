---
title: "Shell string expansion"
date: 2014-12-08 12:03:44
categories:
  - linux
tags:
  - shell
  - notes
---

## Parameter Expansion

[Parameter Expansion - Bash Reference Manual](http://www.gnu.org/software/bash/manual/bash.html#Shell-Parameter-Expansion)
[Parameter Substitution](https://tldp.org/LDP/abs/html/parameter-substitution.html)

[bash assign default value - Stack Overflow](https://stackoverflow.com/a/26899206)

`${parameter-default}, ${parameter:-default}`
The extra : makes a difference only when parameter has been declared, but is null.

```bash
unset EGGS
echo 1 ${EGGS-spam}   # 1 spam
echo 2 ${EGGS:-spam}  # 2 spam

EGGS=
echo 3 ${EGGS-spam}   # 3
echo 4 ${EGGS:-spam}  # 4 spam

EGGS=cheese
echo 5 ${EGGS-spam}   # 5 cheese
echo 6 ${EGGS:-spam}  # 6 cheese
```

## string manipulation/expansion

> After reading `fish` shell's philosophy, I now think using `sed` and other tools is better than relying on shell features.

[Manipulating Strings](https://tldp.org/LDP/abs/html/string-manipulation.html)
[Parameter expansion [Bash Hackers Wiki]](https://wiki.bash-hackers.org/syntax/pe)
[Bash string processing](https://aty.sdsu.edu/bibliog/latex/debian/bash.html)
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
