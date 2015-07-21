title: "Shell notes"
date: 2014-12-08 12:03:44
categories:
- linux
tags:
- shell
- notes
toc: true
---

Notes on shell usage.
Most of the following are compatible to `bash` and `zsh`.

<!-- more -->

## Choosing shell

[Unix Shells: Bash, Fish, Ksh, Tcsh, Zsh - Hyperpolyglot](http://hyperpolyglot.org/unix-shells)

Most distro comes with `bash` as default login shell.
Since `bash` is ubiquitous and more feature-rich than POSIX shell (`/bin/sh`), it is recommended to write shell scripts in `bash`.
Since `zsh` is `bash` (and hence POSIX) -compatible. Most command lines found on the web can be pasted in `zsh` directly (unlike `fish` which is not POSIX-compatible). It is recommended to use `zsh` as the interactive shell.
However I found `fish` [design](http://fishshell.com/docs/current/design.html) quite sensible. I'll try to use external binaries as mush as possible instead of relying on shell features. On the same line of thought, even-though `zsh` has more powerful syntax than `bash`, it may not be worthy to use them to avoid lock-in and maintain portability.

Fish featured on Ars:
[Fish: the friendly interactive shell | Ars Technica](http://arstechnica.com/information-technology/2005/12/linux-20051218/2/)

### login shell

You can set a shell as your default shell with `chsh`.
But interactive shells must be added to `/etc/shells` first before used as a login shell.

http://fishshell.com/docs/2.1/faq.html#faq-default

## dotfiles

> most contain useful aliases, functions and scripts

It is recommended to use source control to store your config files (_dotfiles_, as they usually begins with a `.`) and use symlinks (`ln -s`) to deploy them to the machine.

### switching OS and host

```sh
SYS_OS=`uname -a`   # linux or mac
SHORT_HOSTNAME=`hostname -s`
 
# system aliases
if [[ "$SYS_OS" == 'Linux' ]]; then
     PATH="..LINUX PATH..."
     source ~/dotfiles/aliases.lx
 else
     PATH="... MAC PATH..."
     source ~/dotfiles/aliases.mac
fi
 
# run host specific profile
if [[ -e ~/dotfiles/profile.$SHORT_HOSTNAME ]]; then
    source ~/dotfiles/profile.$SHORT_HOSTNAME
fi
```

Honorable mentions:
- http://dotfiles.github.io/
- http://chneukirchen.org/dotfiles/
> TODO: add my links in /caravan/github-watch/dotfiles

[Using Dropbox as a Settings Repository](http://coda.caseykuhlman.com//entries/2014/dropbox-as-a-settings-repository.html)

[Steve's Blog: bash aliases](http://siannopollo.blogspot.hk/2007/11/bash-aliases.html)

## environment variable

[Environment variable - Wikiwand](http://www.wikiwand.com/en/Environment_variable)
[Environment variables - ArchWiki](https://wiki.archlinux.org/index.php/Environment_variables)

## Common tasks

[Useless Use of Cat Award](http://www.smallo.ruhr.de/award.html)

Follow [The Art of Unix Programming](http://www.faqs.org/docs/artu/), implement filters.
[Simple filters in Perl, Ruby, and Bourne shell - TechRepublic](http://www.techrepublic.com/blog/software-engineer/simple-filters-in-perl-ruby-and-bourne-shell/)

### parsing command line

[SHELLdorado - cmdargs](http://www.shelldorado.com/goodcoding/cmdargs.html)
[Command Line Options: How To Parse In Bash Using “getopt” — BahmanM.com](http://www.bahmanm.com/blogs/command-line-options-how-to-parse-in-bash-using-getopt)

```sh
#!/bin/bash
# http://www.bahmanm.com/blogs/command-line-options-how-to-parse-in-bash-using-getopt

# “a” and “arga” have optional arguments with default values.
# “b” and “argb” have no arguments, acting as sort of a flag.
# “c” and “argc” have required arguments.

# e.g.:
# ./getopt.sh  1 -a'a' -b 2 -c'c' 3 4
# ./getopt.sh  1 --arga='a' 2 --argc='c' 3 4

# set an initial value for the flag
ARG_B=0

# read the options
TEMP=`getopt -o a::bc: --long arga::,argb,argc: -n 'getopt.sh' -- "$@"`
if [[ $? -ne 0 ]]; then
    echo -e "\e[1;31m""getopt error""\e[0m"
    exit 2
fi

eval set -- "$TEMP"

# extract options and their arguments into variables.
while true ; do
    case "$1" in
        -a|--arga)
            case "$2" in
                "") ARG_A='some default value' ; shift 2 ;;
                *) ARG_A=$2 ; shift 2 ;;
            esac ;;
        -b|--argb) ARG_B=1 ; shift ;;
        -c|--argc)
            case "$2" in
                "") shift 2 ;;
                *) ARG_C=$2 ; shift 2 ;;
            esac ;;
        --) shift ; break ;;
        *) echo "Internal error!" ; exit 2 ;;
    esac
done

# do something with the variables -- in this case the lamest possible one :-)
echo "ARG_A = $ARG_A"
echo "ARG_B = $ARG_B"
echo "ARG_C = $ARG_C"

# positional args
args=("$@")
echo \#: [${#args[@]}]
echo @: [${args[@]}]
for ((i=0; i<${#args[@]}; i++)); do
    echo ${args[i]};
done
```

### redirection

All these redirections are equal:

```sh
$ > file command arg1 arg2 arg3
$ command > file arg1 arg2 arg3
$ command arg1 > file arg2 arg3
$ command arg1 arg2 > file arg3
$ command arg1 arg2 arg3 > file
```

### Here Doc

[linux - How can I write a here doc to a file in Bash script? - Stack Overflow](http://stackoverflow.com/questions/2953081/how-can-i-write-a-here-doc-to-a-file-in-bash-script)
[Here Documents](http://tldp.org/LDP/abs/html/here-docs.html)

This is a technique to embed string block in scripts and feed it to an interactive command.

```sh
interactive-program <<LimitString
command #1
command #2
...
LimitString
```

Single quote (`'`) the commands to prevent string interpolation.

```sh
cat << 'EOF'
I want to print ${FOO} literally
EOF
```

`<<-` will suppress leading tabs (not spaces).

### detect undefined vars 

it's more meaningful in scripts to report error then to continue with empty string

```sh
set -u  # throw error on uninitialized variable, `set -o nounset`
set -e  # exit on statement error, `set -o errexit`
```

### key bindings

[Bash Shortcuts Quick Reference](http://www.ice2o.com/bash_quick_ref.html)

### color

http://misc.flogisoft.com/bash/tip_colors_and_formatting
http://www.calmar.ws/vim/256-xterm-24bit-rgb-color-chart.html

zsh have color macros predefined, see themes in `oh-my-zsh`

### calculation

```sh
# do math calculation in $(( )), it is faster then `expr`
# and we can specify the number system with 8#, 10#, 16#
# useful for doing operation on variables with leading zeros
a=005
$((10#${a} + 1))
$(expr ${a} + 1)  # slower
```

or use `bc`, or use `math` (inspired by `fish`)

```sh
#!/bin/sh
# thin wrapper around bc for easier math expression in shell
# inspired by fish
echo "$@" | bc -l
```

### trap 
> `bash` specific?

```sh
# clean up
trap cleanUp INT TERM EXIT
# cannot be killed
trap - INT TERM EXIT
```

### proper critical section
> `bash` specific?

```sh
if [ ! -e $lockfile ]; then
    trap "rm -f $lockfile; exit" INT TERM EXIT
    touch $lockfile
    critical-section
    rm $lockfile
    trap - INT TERM EXIT
else
    echo "critical-section is already running"
fi
```

## Shell Script Constructs

http://zsh.sourceforge.net/Doc/Release/Shell-Grammar.html

### `if`

```sh
# if construct
if [[ -z "$1" || -z "$2" ]]; then
    echo "Usage: $0 <command> <arg>"
    exit 1
fi
```

```sh
# test existence of binary
if [[ -z "$(which wget)" ]]; then
  doSomething
fi

[[ $(which colordiff) ]] && alias diff='colordiff '
```

### `case`

```sh
case '$param' in
A)
    ;;
B)
    ;;
*)
    ;;
esac
```

```sh
# choose 'open' command
case $(uname) in
    Darwin) OPEN_CMD=open ;;
    Linux) OPEN_CMD=xdg-open ;; # assuming X is present
    CYGWIN*) OPEN_CMD=cygstart ;;
    *) echo "Unknown OS"; exit 1 ;;
esac
```

### `for`

```sh
for file in `ls -v` ; do cat $file >> concat.file ; done

for file in `ls -v` ; do
    cat $file >> concat.file ;
done

# {START..END..INCREMENT}
for i in {1..5}; do
   echo "Welcome $i times"
done
```

### `while`

```sh
while [ -z $1 ] ; do
    echo $1
    shift
done
```

### `until`

```sh
until [ -z $1 ] ; do
    echo $1
    shift
done
```

### array

[Bash associative array examples | Andy Balaam's Blog](http://www.artificialworlds.net/blog/2012/10/17/bash-associative-array-examples/)
[Bash arrays | Andy Balaam's Blog](http://www.artificialworlds.net/blog/2013/09/18/bash-arrays/)
[The Ultimate Bash Array Tutorial with 15 Examples](http://www.thegeekstuff.com/2010/06/bash-array-tutorial/)

```sh
cherries+=(54758)
cherries+=(54761)
cherries+=(55075)
# stringify array
echo ${cherries[@]}

# construct array form string
FILES=("${@}")
NUMFILES=${#FILES[@]}
for (( i = 0; i < ${NUMFILES}; i++ )); do
    echo ${FILES[${i}]}
done
# "${!array[*]}" "${array[*]}"?
# keys: ${!array[@]}
# values ${array[@]}
```

#### passing array to function

[bash how to pass array as an argument to a function - Stack Overflow](http://stackoverflow.com/questions/16461656/bash-how-to-pass-array-as-an-argument-to-a-function)
[Passing arrays as parameters in bash - Stack Overflow](http://stackoverflow.com/questions/1063347/passing-arrays-as-parameters-in-bash)

```sh
# stringify and reconstruct
foo()
{
    array=("$@")
    echo "array is ${array[@]}"
}

array=(one two three)
foo "${array[@]}"
```

```sh
# by reference
foo()
{
    # note: must use a name different from "array"
    local -n a=$1
    echo "array is ${a[@]}"
}

array=(one two three)
foo array
```

```sh
# by reference
foo()
{
    # note: must use a name different from "array1", "array2"
    declare -a argAry1=("${!1}")
    declare -a argAry2=("${!2}")
    declare -p argAry1
    declare -p argAry2
}

array1=(one two three)
array2=(a b c)
foo array1[@] array2[@]
```

### function

```sh
# test element in array
in_array()
{
    local hay needle=$1;
    shift;
    for hay in "$@"; do
        echo $hay
        [[ $hay == $needle ]] && return 0;
    done;
    return 1
}

# test logic expression
Test()
{
    eval "$@" && echo "True" || echo "False";
}
```

## Reference

[Bash Shell Quick Reference, by Aurelio Jargas](http://aurelio.net/articles/shell-reference.html)
[The Linux Command Line by William E. Shotts, Jr.](http://linuxcommand.org/tlcl.php)
[Shell / Command Line | Linux.org](http://www.linux.org/forums/shell-command-line.49/)
[GNU/Linux Command-Line Tools Summary](http://www.tldp.org/LDP/GNU-Linux-Tools-Summary/html/index.html)
[Heiner's SHELLdorado](http://www.shelldorado.com/)

**Bash**:
[BASH Programming - Introduction HOW-TO](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html)
[Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/Bash-Beginners-Guide.html)
[Advanced Bash-Scripting Guide](http://www.tldp.org/LDP/abs/html/)
[Bash Hackers Wiki Frontpage [Bash Hackers Wiki]](http://wiki.bash-hackers.org/doku.php)
http://justinlilly.com/bash/forgotten_friend_1.html
http://justinlilly.com/bash/forgotten_friend_2.html
http://justinlilly.com/bash/forgotten_friend_3.html
http://www.dsj.net/compedge/shellbasics.html
http://www.dsj.net/compedge/shellbasics1.html
http://www.dsj.net/compedge/regex.html
http://www.dsj.net/compedge/morebashfun2.html
http://www.dsj.net/compedge/bashit.html

**Zsh**:
http://zsh.sourceforge.net/Doc/Release/zsh_toc.html
http://grml.org/zsh/zsh-lovers.html
http://www.zzapper.co.uk/zshtips.html
http://fendrich.se/blog/2012/09/28/no/
http://www.tuxradar.com/content/z-shell-made-easy

**Fish**:
https://wiki.archlinux.org/index.php/Fish
