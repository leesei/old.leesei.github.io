---
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

[We all <3 Terminals. - Terminals Are Sexy](https://terminalsare.sexy/)
[Philip James, Asheesh Laroia - Type python, press enter. What happens? - PyCon 2015 - YouTube](https://www.youtube.com/watch?v=XVhSjZYwZJo) how shell invocation works
[Command Line Power User — A free video series for web developers on learning a modern command line workflow with ZSH, Z and related tools.](https://commandlinepoweruser.com/) !important, by Wes Bos
[Coding like a Hacker in the terminal – Caleb Taylor – Medium](https://medium.com/@caleb89taylor/coding-like-a-hacker-in-the-terminal-79e22954968e)
[You’re Missing Out on a Better Mac Terminal Experience](https://medium.com/@caulfieldOwen/youre-missing-out-on-a-better-mac-terminal-experience-d73647abf6d7)

<!-- more -->

## Choosing shell

[Unix Shells: Bash, Fish, Ksh, Tcsh, Zsh - Hyperpolyglot](http://hyperpolyglot.org/unix-shells)
[Evolution of shells in Linux](https://www.ibm.com/developerworks/library/l-linux-shells/)
[Rich’s sh (POSIX shell) tricks](http://www.etalabs.net/sh_tricks.html)
[the xonsh shell — xonsh 0.8.12 documentation](https://xon.sh/)

Most distro comes with `bash` as default login shell.
Since `bash` is ubiquitous and more feature-rich than POSIX shell (`/bin/sh`), it is recommended to write shell scripts in `bash`.
Since `zsh` is `bash` (and hence POSIX) -compatible. Most command lines found on the web can be pasted in `zsh` directly (unlike `fish` which is not POSIX-compatible). It is recommended to use `zsh` as the interactive shell.
However I found `fish` [design](http://fishshell.com/docs/current/design.html) quite sensible. I'll try to use external binaries as mush as possible instead of relying on shell features. On the same line of thought, even-though `zsh` has more powerful syntax than `bash`, it may not be worthy to use them to avoid lock-in and maintain portability.

[Evolution of shells in Linux](https://www.ibm.com/developerworks/linux/library/l-linux-shells/index.html?ca=drs-)

### login shell

You can set a shell as your default shell with `chsh`.
But interactive shells must be added to `/etc/shells` first before used as a login shell.

http://fishshell.com/docs/2.1/faq.html#faq-default

## dotfiles

> most contain useful aliases, functions and scripts

It is recommended to use source control to store your config files (_dotfiles_, as they usually begins with a `.`) and use symlinks (`ln -s`) to deploy them to the machine.

[GitHub does dotfiles - dotfiles.github.io](http://dotfiles.github.io/)
[webpro/awesome-dotfiles: A curated list of dotfiles resources.](https://github.com/webpro/awesome-dotfiles)

Honorable mentions:

- http://chneukirchen.org/dotfiles/
- https://github.com/jukben/dotfiles (Tmux)
  > TODO: add my links in /caravan/github-watch/dotfiles

[Steve's Blog: bash aliases](http://siannopollo.blogspot.hk/2007/11/bash-aliases.html)

[jukben/gbck: 🗳 Intuitive lightweight tool for an easy and seamless backup of your files into Git repository](https://github.com/jukben/gbck)
[gbck— an easy way how to back up your dotfiles – Jakub Beneš – Medium](https://medium.com/@jukben/gbck-an-easy-way-how-to-back-up-your-dotfiles-2a9bf44ab622)
[Yet Another Dotfiles Manager - yadm](https://yadm.io/)

[How to make your Dotfile management a painless affair](https://medium.freecodecamp.org/dive-into-dotfiles-part-2-6321b4a73608)
[ajmalsiddiqui/autodot: A dotfile management system that makes sharing your dotfiles easy while keeping you in the loop.](https://github.com/ajmalsiddiqui/utodot)
[RCM(7)](https://thoughtbot.github.io/rcm/)

[twpayne/chezmoi: Manage your dotfiles across multiple machines, securely.](https://github.com/twpayne/chezmoi)
[Brandon Invergo - Using GNU Stow to manage your dotfiles](http://brandon.invergo.net/news/2012-05-26-using-gnu-stow-to-manage-your-dotfiles.html)
[Managing dotfiles using GNU Stow](https://www.bharatkalluri.in/post/manage-dotfiles-using-stow/)
[svetlyak40wt/dotfiler: Shell agnostic git based dotfiles package manager, written in Python.](https://github.com/svetlyak40wt/dotfiler)
[Using Dropbox as a Settings Repository](http://coda.caseykuhlman.com//entries/2014/dropbox-as-a-settings-repository.html)

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

## environment variable

[Environment variable - Wikiwand](http://www.wikiwand.com/en/Environment_variable)
[Environment variables - ArchWiki](https://wiki.archlinux.org/index.php/Environment_variables)

## Frameworks

[niieani/bash-oo-framework: Bash Infinity is a modern boilerplate for bash](https://github.com/niieani/bash-oo-framework)
[jmmv/shtk: Application toolkit for programmers writing POSIX-compliant shell scripts](https://github.com/jmmv/shtk)

## Common tasks

[Useless Use of Cat Award](http://www.smallo.ruhr.de/award.html)

Follow [The Art of Unix Programming](http://www.faqs.org/docs/artu/), implement filters.
[Simple filters in Perl, Ruby, and Bourne shell - TechRepublic](http://www.techrepublic.com/blog/software-engineer/simple-filters-in-perl-ruby-and-bourne-shell/)

[Capturing output of find . -print0 into a bash array - Stack Overflow](http://stackoverflow.com/questions/1116992/capturing-output-of-find-print0-into-a-bash-array)
[Filenames and Pathnames in Shell (bash, dash, ash, ksh, and so on): How to do it Correctly](http://www.dwheeler.com/essays/filenames-in-shell.html)
[Writing Safe Shell Scripts](https://sipb.mit.edu/doc/safe-shell/)

[Ten Things I Wish I’d Known About bash – zwischenzugs](https://zwischenzugs.com/2018/01/06/ten-things-i-wish-id-known-about-bash/)
[Ten More Things I Wish I'd Known About bash – zwischenzugs](https://zwischenzugs.com/2018/01/21/ten-more-things-i-wish-id-known-about-bash/)
[How to debug bash scripts with two tools - TechRepublic](https://www.techrepublic.com/article/how-to-debug-bash-scripts-with-two-easy-tools/#ftag=RSS56d97e7)

### shebang line

[The #! magic, details about the shebang/hash-bang mechanism](http://www.in-ulm.de/~mascheck/various/shebang/)
[Sambal : Passing options to node on the shebang (#!) line](http://sambal.org/2014/02/passing-options-node-shebang-line/)

[`envns`](http://stackoverflow.com/a/25046028/665507):

```sh
#!/bin/bash

ARGS=( $1 )  # separate $1 into multiple space-delimited arguments.
shift # consume $1

PROG=`which ${ARGS[0]}`
unset ARGS[0] # discard executable name

ARGS+=( "$@" ) # remainder of arguments preserved "as-is".
exec $PROG "${ARGS[@]}"
```

```sh
#!/usr/local/bin/envns node --harmonic
```

`node-es6`: (alias won't work in shebang)

```sh
#!/bin/bash
node --harmonic "$@"
```

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

### Redirection

[Redirections](http://www.gnu.org/software/bash/manual/bash.html#Redirections)
[Bash One-Liners Explained, Part III: All about redirections - good coders code, great coders reuse](http://www.catonmat.net/blog/bash-one-liners-explained-part-three/)

All these redirections are equal:

```sh
$ > file command arg1 arg2 arg3
$ command > file arg1 arg2 arg3
$ command arg1 > file arg2 arg3
$ command arg1 arg2 > file arg3
$ command arg1 arg2 arg3 > file
```

### Process Substitution

[Process Substitution](http://www.gnu.org/software/bash/manual/bash.html#Process-Substitution)

Takes output of process as file

```sh
diff <(ls -a folder1) <(ls -a folder2)
diff <(grep -r -e foo src1/) <(grep -r -e foo src1/)
```

### Command Substitution

[Command Substitution](http://www.gnu.org/software/bash/manual/bash.html#Command-Substitution)

```sh
vim `which a.sh`
vim $(which a.sh)
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

Create file with Here Doc

```sh
cat << EOF > ${FILE}
This is the file content.
Second line.
EOF
```

### detect undefined variables

it's more meaningful in scripts to report error then to continue with empty string

```sh
set -u  # throw error on uninitialized variable, `set -o nounset`
set -e  # exit on statement error, `set -o errexit`
```

### key bindings

[Bash Shortcuts Quick Reference](http://www.ice2o.com/bash_quick_ref.html)

### exit code

[Exit and Exit Status](https://www.tldp.org/LDP/abs/html/exit-status.html)
[Exit Codes With Special Meanings](http://tldp.org/LDP/abs/html/exitcodes.html)

[Command Exit Status — Brandur Leach](https://brandur.org/exit-status)

### color

[bash:tip_colors_and_formatting - FLOZz' MISC](https://misc.flogisoft.com/bash/tip_colors_and_formatting)
[True Colour (16 million colours) support in various terminal applications and terminals](https://gist.github.com/XVilka/8346728)
[256 Terminal colors and their 24bit equivalent (or similar)](http://www.calmar.ws/vim/256-xterm-24bit-rgb-color-chart.html)

A color escape sequence: `<Esc>[<FormatCode>m`, `<Esc>`` can be:

- `\e`
- `\033`
- `\x1B`

zsh have color macros predefined, see themes in `oh-my-zsh`

[scripts/ansi2html.sh at master · pixelb/scripts](https://github.com/pixelb/scripts/blob/master/scripts/ansi2html.sh)
[ralphbean/ansi2html: Convert text with ansi color codes to HTML](https://github.com/ralphbean/ansi2html)

### power tools

[mbrubeck/compleat](https://github.com/mbrubeck/compleat)

```sh
zstyle -L ":completion:*"
```

[clvv/fasd](https://github.com/clvv/fasd)

[rupa/z](https://github.com/rupa/z)

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

[SignalTrap - Greg's Wiki](http://mywiki.wooledge.org/SignalTrap)
[How "Exit Traps" Can Make Your Bash Scripts Way More Robust And Reliable](http://redsymbol.net/articles/bash-exit-traps/)
[Writing shell scripts - Lesson 15: Errors and Signals and Traps (Oh My!) - Part 1](http://linuxcommand.org/wss0150.php)
[Writing shell scripts - Lesson 16: Errors and Signals and Traps (Oh, My!) - Part 2](http://linuxcommand.org/wss0160.php)

```sh
# clean up
trap cleanUp INT TERM EXIT
# cannot be killed
trap - INT TERM EXIT
```

| Number | SIG     | Meaning                      |
| ------ | ------- | ---------------------------- |
| 0      | 0       | On exit from shell           |
| 1      | SIGHUP  | Clean tidyup                 |
| 2      | SIGINT  | Interrupt (usually Ctrl-C)   |
| 3      | SIGQUIT | Quit (usually Ctrl-\\)       |
| 6      | SIGABRT | Abort                        |
| 9      | SIGKILL | Die Now (cannot be trap'ped) |
| 14     | SIGALRM | Alarm Clock                  |
| 15     | SIGTERM | Terminate                    |

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

### `test` command

[The classic test command [Bash Hackers Wiki]](http://wiki.bash-hackers.org/commands/classictest)

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
# array is 1-based
echo ${cherries[1]}  # 54758
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

declare -A CAPITAL
CAPITAL[Alabama]=Montgomery
CAPITAL[Alaska]=Juneau
CAPITAL[Arizona]=Phoenix
CAPITAL[New Mexico]="Santa Fe"

# ${!ARRAY[@]} get the keys
for STATE in "${!CAPITAL[@]}"; do
    echo "The capital of $STATE is ${CAPITAL[$STATE]}."
done
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

### returning values from function

[Returning Values from Bash Functions | Linux Journal](https://www.linuxjournal.com/content/return-values-bash-functions)

## Libraries

[jwerle/q](https://github.com/jwerle/q)
[jmcantrell/bashful](https://github.com/jmcantrell/bashful)
[dominictarr/JSON.sh](https://github.com/dominictarr/JSON.sh)
[ShellCheck – Shell script analyzer](http://www.shellcheck.net/)

[linux - Unit testing for shell scripts - Stack Overflow](http://stackoverflow.com/questions/971945/unit-testing-for-shell-scripts)
[kward/shunit2](https://github.com/kward/shunit2)
[Wiki Pages - shunit2 - shUnit2 - xUnit based unit testing for Unix shell scripts - Google Project Hosting](https://code.google.com/p/shunit2/w/list)
[sstephenson/bats](https://github.com/sstephenson/bats)

## Reference

[Bash Shell Quick Reference, by Aurelio Jargas](http://aurelio.net/articles/shell-reference.html)
[The Linux Command Line by William E. Shotts, Jr.](http://linuxcommand.org/tlcl.php)
[Shell / Command Line | Linux.org](http://www.linux.org/forums/shell-command-line.49/)
[GNU/Linux Command-Line Tools Summary](http://www.tldp.org/LDP/GNU-Linux-Tools-Summary/html/index.html)
[Heiner's SHELLdorado](http://www.shelldorado.com/)
[An Introduction to Shell Scripting | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-shell-scripting)
[Portable Shell - Autoconf](https://www.gnu.org/savannah-checkouts/gnu/autoconf/manual/autoconf-2.69/html_node/Portable-Shell.html#Portable-Shell)
[Shell 特殊变量： $0, $#, $*, $@, $?, $$, $!, $_和命令行参数$n - Gikor - CSDN 博客](https://blog.csdn.net/w746805370/article/details/51044352)

[Writing Secure Shell Scripts | Linux Journal](https://www.linuxjournal.com/content/writing-secure-shell-scripts)

**Bash**:
[denysdovhan/bash-handbook: For those who wanna learn Bash](https://github.com/denysdovhan/bash-handbook)
[BASH Programming - Introduction HOW-TO](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html)
[Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/Bash-Beginners-Guide.html)
[Advanced Bash-Scripting Guide](http://www.tldp.org/LDP/abs/html/)
[Bash Hackers Wiki Frontpage [Bash Hackers Wiki]](http://wiki.bash-hackers.org/doku.php)
[Bash Scripting Tutorial - Ryans Tutorials](http://ryanstutorials.net/bash-scripting-tutorial/)
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
