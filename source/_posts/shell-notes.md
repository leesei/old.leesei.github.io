title: Shell notes
toc: true
date: 2014-12-08 12:03:44
tags:
- shell
- notes
---

Notes on shell usage.
Most of the following are compatible to `bash` and `zsh`.

<!-- more -->

## Choosing shell

[Unix Shells: Bash, Fish, Ksh, Tcsh, Zsh - Hyperpolyglot](http://hyperpolyglot.org/unix-shells)

Most distro comes with `bash` as default login shell.
Since `bash` is ubiqutious and more feature-rich than POSIX shell (`/bin/sh`), it is recommanded to write shell scripts in `bash`.
Since `zsh` is `bash` (and hence POSIX) -compatible. Most command lines found on the web can be pasted in `zsh` directly (unlike `fish` which is not POSIX-compatible). It is recommanded to use `zsh` as the interactive shell.
However I found `fish` [design](http://fishshell.com/docs/current/design.html) quite sensible. I'll try to use external binaries as mush as possible instead of relying on shell features. On the same line of thought, eventhough `zsh` has more powerful syntax than `bash`, it may not be worthy to use them to avoid lock-in and maintain portability.

### login shell

You can set a shell as your default shell with `chsh`.
But interactive shells must be added to `/etc/shells` first before used as a login shell.

http://fishshell.com/docs/2.1/faq.html#faq-default

## dotfiles

> most contain useful aliases, functions and scripts

It is recommanded to use source control to store your config files (_dotfiles_, as they usually begins with a `.`) and use symlinks (`ln -s`) to deploy them to the machine.

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
{% label TODO warning %} add my links in /caravan/github-watch/dotfiles

## Common tasks

### detect undefined vars 

its more meaningful in scripts to report error then to continue with empty string

```sh
set -u  # throw error on uninitialised variable, `set -o nounset`
set -e  # exit on statement error, `set -o errexit`
```

### key bindings

[Bash Shortcuts Quick Reference](http://www.ice2o.com/bash_quick_ref.html)

### color

http://misc.flogisoft.com/bash/tip_colors_and_formatting
http://www.calmar.ws/vim/256-xterm-24bit-rgb-color-chart.html

zsh have color macros predefined, see themes in `oh-my-zsh`

### calculation

```bash
# do math calculation in $(( )), it is faster then `expr`
# and we can specify the number system with 8#, 10#, 16#
# useful for doing operation on variables with leeding zeros
a=005
$((10#${a} + 1))
$(expr ${a} + 1)  # slower
```

or use `bc`, or use `math` (inspired by `fish`)

```sh math
#!/bin/sh
# thin wrapper around bc for easier math expression in shell
# inspired by fish
echo "$@" | bc -l
```

## shell expansion

### history expansion

http://www.eriwen.com/bash/effective-shorthand/
http://www.catonmat.net/blog/the-definitive-guide-to-bash-command-line-history/
{% label TODO warning %} add zsh manual

```sh
cp myfile.txt my/directory/path
cd $!  # cd my/directory/path

vi /etc/fstabs  # oops!
sudo !!  # sudo vi /etc/fstab
```

`!!` expands to the last command and all arguments
`!-3` 3rd-to-last command and all arguments
`!^` first argument of the last command in history
`!:2` 2nd argument of the last command
`!$` last argument of the last command
`!*` all arguments of the last command, but not the command itself
`!42` expands to the 42nd command in the history list
`!foo` last command beginning with “foo”
`!?baz` last command containing “baz”
`^foo^bar` last command with the first occurrence of “foo” replaced with “bar”
`!:gs/foo/bar` last command with all occurrences of “foo” replaced with “bar”
`<any_above>:p` prints command without executing

### string manipulation/expansion
http://tldp.org/LDP/abs/html/string-manipulation.html
http://wiki.bash-hackers.org/syntax/pe
http://mintaka.sdsu.edu/GF/bibliog/latex/debian/bash.html
{% label TODO warning %} add zsh manual

```bash
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
${string//substring/replacement}  # replace all occurrences of "substring" with "replacement"
${string/#substring/replacement}  # replace front match (^) "substring" with "replacement"
${string/%substring/replacement}  # replace end match ($) "substring" with "replacement"

# file path manipulation
$(dirname "$path")   # get dir from full path
$(basename "$path")  # get file name from full path

FILE="example.tar.gz"
${FILE%%.*}          # "example", stripped longest extension
${FILE%.*}           # "example.tar", stripped shortest extension
${FILE#*.}           # "tar.gz", longest extension
${FILE##*.}          # "gz", shortest extension

if [ ${path:0:1} = '/' ]; then
    tmp=${path:1}    # strip leading '/'
fi
tmp=${path#/}        # strip leading '/'
tmp=${path%/}        # strip trailing '/'
```

## trap 
> `bash` specific?

```bash
# clean up
trap cleanUp INT TERM EXIT
# cannot be killed
trap - INT TERM EXIT
```

### proper critical section
> `bash` specific?

```bash
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

## shell script constructs

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

```bash
until [ -z $1 ] ; do
    echo $1
    shift
done
```

### array

```sh
cherries+=(54758)
cherries+=(54761)
cherries+=(55075)
echo ${cherries[@]}

# convert string to array
FILES=("${@}")
NUMFILES=${#FILES[@]}
for (( i = 0; i < ${NUMFILES}; i++ )); do
    echo ${FILES[${i}]}
done
```

### function

```bash
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

**Bash**:
http://justinlilly.com/bash/forgotten_friend_1.html
http://justinlilly.com/bash/forgotten_friend_2.html
http://justinlilly.com/bash/forgotten_friend_3.html
**Zsh**:
http://zsh.sourceforge.net/Doc/Release/zsh_toc.html
http://grml.org/zsh/zsh-lovers.html
http://www.zzapper.co.uk/zshtips.html
http://fendrich.se/blog/2012/09/28/no/
http://www.tuxradar.com/content/z-shell-made-easy
**Fish**:
https://wiki.archlinux.org/index.php/Fish
