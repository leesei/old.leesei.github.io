---
title: "Shell Tools"
date: 2015-01-14 12:48:30
categories:
  - app
tags:
  - shell-tool
  - cpio
  - cut
  - diff
  - find
  - grep
  - inotify-tools
  - openRTSP
  - pt
  - rsync
  - mega
  - sort
  - tar
  - tr
  - xargs
  - useradd
  - usermod
toc: true
---

[All commands | commandlinefu.com](http://www.commandlinefu.com/commands/browse)
[explainshell.com - match command-line arguments to their help text](http://explainshell.com/)
[Core utilities - ArchWiki](https://wiki.archlinux.org/index.php/Core_utilities)
[Tools & Reference - Linode Guides & Tutorials](https://www.linode.com/docs/tools-reference/)
[Linux 101 Hacks eBook, by Ramesh Natarajan](http://www.thegeekstuff.com/linux-101-hacks-ebook/)
[The Unix CD Bookshelf, v3.0](http://docstore.mik.ua/orelly/unix3/)

[TLDR pages](https://tldr.sh/)
[Pantz.org Technical Reference Site](https://www.pantz.org/)

[7 command-line tools for data science](http://jeroenjanssens.com/2013/09/19/seven-command-line-tools-for-data-science.html)

[5 Useful Tools to Remember Linux Commands Forever](https://www.tecmint.com/remember-linux-commands/amp/)
[A - Z Linux Commands - Overview with Examples](https://www.tecmint.com/linux-commands-cheat-sheet/)
[Everything CLI - It is all about the unix cli](https://www.everythingcli.org/)

[My favorite command-line utilities](https://hackernoon.com/macbook-my-command-line-utilities-f8a121c3b019#.h92el0w0k)
[Coreutils Gotchas](http://www.pixelbeat.org/docs/coreutils-gotchas.html#dd)
[New zine: Bite Size Command Line! - Julia Evans](https://jvns.ca/blog/2018/08/05/new-zine--bite-size-command-line/)

[k4m4/terminals-are-sexy: 💥 A curated list of Terminal frameworks, plugins & resources for CLI lovers.](https://github.com/k4m4/terminals-are-sexy)
[alebcay/awesome-shell: A curated list of awesome command-line frameworks, toolkits, guides and gizmos. Inspired by awesome-php.](https://github.com/alebcay/awesome-shell)
[aharris88/awesome-cli-apps: A curated list of command line apps](https://github.com/aharris88/awesome-cli-apps)
[herrbischoff/awesome-command-line-apps: Use your terminal shell to do awesome things.](https://github.com/herrbischoff/awesome-command-line-apps)
[jlevy/the-art-of-command-line: Master the command line, in one page](https://github.com/jlevy/the-art-of-command-line)
[nvbn/thefuck: Magnificent app which corrects your previous console command.](https://github.com/nvbn/thefuck)
[facebook/PathPicker](https://github.com/facebook/pathpicker/) `fpp` provides interactive links to files in shell output
[Pipecut Project Home](http://www.pipecut.org/)
[How to do math on the Linux command line | Network World](https://www.networkworld.com/article/3268964/linux/how-to-do-math-on-the-linux-command-line.html)

[rmdupes](https://xyne.archlinux.ca/projects/rmdupes/)

## simple manpage

[tldr-pages/tldr: Simplified and community-driven man pages](https://github.com/tldr-pages/tldr)
[chrisallenlane/cheat: cheat allows you to create and view interactive cheatsheets on the command-line.](https://github.com/chrisallenlane/cheat)
[bro: just get to the point!](http://bropages.org/)

## user management

> Ubuntu has an `adduser` wrapper to `useradd`

`/etc/passwd` defines the users
`/etc/group` defines the groups

```sh
# print user info
id $USER

# new user with secondary group
useradd -G group[,group] user

# add secondary group to existing user
usermod -a -G group[,group] user

# delete user
userdel user
# delete user and home folder
userdel -r user

# relogin to take effect
su - $USER

# password expiry policy can be set with `passwd` and `chage`
passwd -n 0 user  # 0 day between password changes
passwd -x 90 user # days for password to be valid
passwd -w 7 user  # days of warning before expiration
chage -l user

# forces user to change at next login
passwd -l user    # lock user password
```

[shell - Reload a Linux user's group assignments without logging out - Super User](http://superuser.com/questions/272061/reload-a-linux-users-group-assignments-without-logging-out)

## Term recorder

[chjj/ttystudio](https://github.com/chjj/ttystudio) record to GIF
[theonewolf/TermRecord](https://github.com/theonewolf/TermRecord) record to HTML
[asciinema/asciinema](https://github.com/asciinema/asciinema) record and post to [asciinema.org](asciinema.org).

## openRTSP

http://www.live555.com/openRTSP/#option-summary

## tar

```sh
# list content
tar -tf tarball.tar.gz | head

# skip 1 level (container folder)
tar -xvf ZendFramework-1.7.2.tar.gz --strip 1
```

## grep

[grep - Wikiwand](http://www.wikiwand.com/en/Grep)
[Grep](http://www.grymoire.com/Unix/Grep.html)
[grep is a beautiful tool](http://www.eriwen.com/tools/grep-is-a-beautiful-tool/)

```sh
# list file name only
grep -l pattern file

# grep | xarg combo
grep -lZ pattern file | xargs -0 ls -l

# find files without word "foo"
grep -L "foo" *
grep -c "foo" * | grep ":0" | awk -F: '{ print $1 }'
```

## uniq

```sh
cat a b | sort | uniq > c   # c is a union b
cat a b | sort | uniq -d > c   # c is a intersect b
cat a b b | sort | uniq -u > c   # c is set difference a \ b

```

## date

[Doing Date Math on the Command Line, Part I | Linux Journal](https://www.linuxjournal.com/content/doing-date-math-command-line-part-i)
[Doing Date Math on the Command Line - Part II | Linux Journal](https://www.linuxjournal.com/content/doing-date-math-command-line-part-ii)

## pt

[monochromegane/the_platinum_searcher](https://github.com/monochromegane/the_platinum_searcher)

## find

[grep - Wikiwand](http://www.wikiwand.com/en/Grep)
[Find](http://www.grymoire.com/Unix/Find.html)
[Find is a beautiful tool](http://www.eriwen.com/productivity/find-is-a-beautiful-tool/)
[Mommy, I found it! — 15 Practical Linux Find Command Examples](http://www.thegeekstuff.com/2009/03/15-practical-linux-find-command-examples/)
[Unix Find Tutorial](http://www.softpanorama.org/Tools/Find/index.shtml)
[UsingFind - Greg's Wiki](http://mywiki.wooledge.org/UsingFind)

[Capturing output of find . -print0 into a bash array - Stack Overflow](http://stackoverflow.com/questions/1116992/capturing-output-of-find-print0-into-a-bash-array)
[linux - exclude directory from find . command - Stack Overflow](http://stackoverflow.com/questions/4210042/exclude-directory-from-find-command/24565095#24565095)
[regex - How to use '-prune' option of 'find' in sh? - Stack Overflow](http://stackoverflow.com/questions/1489277/how-to-use-prune-option-of-find-in-sh/1489405#1489405)
[How to rsync files by date or by size](https://coolaj86.com/articles/how-to-rsync-files-by-date-or-by-size.html) (actually `find` trickery)

```sh
# find | xarg combo
find . -print0 | xargs -0 ls -l

# all files greater than 1mb
find $HOME/. -size +1024k

# all .js files inside current directory greater than 500k
find . -name '*.js' -size +500k

# find all files larger than zero but less than 500bytes
find . -size +0 -a -size -500c # (-a is AND, -c is bytes)

# find all files larger than zero OR (-o) any that haven't been accessed in over a year
find . -size 0 -o -atime +365

# find all files modified more than 5 days ago
find . -type f -mtime +5
# find all files modified within last 60 minutes
find . -type f -mmin -60

# find all files of size between 50-100MB
find . -size +50M -size -100M

# concat all Java files and print to console, note the space before '\'
find . -type f -name "*.java"-exec cat {} \;

# find executables
find . -perm /a=x

# find empty directories
find . -type d -empty

# excluding folders
# prune is faster than `-not` for files are skipped
find build -not \(-type d -path build/external -prune \) -name \*.js
```

### operate files using inum

This is useful when the file name is particularly long or contains weird characters.

```sh
# list inum of files
ls -i

cd "$(find -inum 123456)"
mv "$(find -inum 123456)" ../some/where/
```

## rsync

[rsync - man page](https://www.mankier.com/1/rsync)
[又一枚瑞士军刀：rsync – Canvas](http://cinvro.com/post/rsync/)
[Replace Storage Drives with Rsync in Arch Linux | DominicMDominicM](http://dominicm.com/replace-storage-drives-rsync-arch-linux/)
[How to use advanced rsync for large Linux backups | Opensource.com](https://opensource.com/article/19/5/advanced-rsync?utm_campaign=intrel)

```sh
rsync -avihXP --info=progress2 --stats <SRC> <DEST>

rsync -r -t -v -progress -s -e "ssh -p 1234" /mnt/media/coding user@backup:/mnt/media

# use rsync to copy files while retaining folder structure
# an alternative to `cp --parents`
rsync -avR dir1/file1 dir2/file2 target/
# target/dir1/file1, target/dir2/file2 will be created
```

[rsync 的核心算法 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/7425.html)

### rsnapshot

[rsnapshot | rsnapshot](http://rsnapshot.org/)
[Guide to rsnapshot and incremental backups on Linux](https://linuxconfig.org/guide-to-rsnapshot-and-incremental-backups-on-linux)
[Easy Automated Snapshot-Style Backups with Rsync](http://www.mikerubel.org/computers/rsync_snapshots/) inspiration for rsnapshot

## rename

```sh
# to lower (y = transliterating, character substitution)
rename 'y/A-Z/a-z/' *
# remove '.txt' suffix
rename 's/.txt$//' *
# add '.txt' suffix
rename 's/$/.txt/' *
```

## sort

[sort (Unix) - Wikiwand](http://www.wikiwand.com/en/Sort_(Unix%29)
[sort - man page](https://www.mankier.com/1/sort)

## xargs

[xargs - Wikiwand](http://www.wikiwand.com/en/Xargs)
[xargs - man page](https://www.mankier.com/1/xargs)
[Xargs - Charles Martin Reid](http://charlesmartinreid.com/wiki/Xargs)
[Things you (probably) didn't know about xargs](http://offbytwo.com/2011/06/26/things-you-didnt-know-about-xargs.html)
[8 Practical Examples of Linux Xargs Command for Beginners](https://www.howtoforge.com/tutorial/linux-xargs-command/)
[find -exec vs find | xargs](https://www.everythingcli.org/find-exec-vs-find-xargs/)

```sh
# simple use case
echo "U R L" | xargs -n1 echo

# `-I` may be needed for more complex use case (`mv @ @.bak`)
# however `-I` implies `-L` (takes input as line)
# so split before call
echo "U R L" | sed 's/ /\n/g' | xargs -I@ echo @

# or do with temp file
echo "U\nR\nL" > file
cat file | xargs -I@ echo @
```

```sh
# custom delimiter, custom replace-str
echo -n 4500 10500 30000 | xargs -n1 -d" " -I@ math @*200/1024
```

## diff

```sh
# left only
diff --changed-group-format='%<' --unchanged-group-format='' FILE1 FILE2
# right only
diff --changed-group-format='%>' --unchanged-group-format='' FILE1 FILE2
```

https://superuser.com/questions/125376/how-do-i-compare-binary-files-in-linux

```sh
vimdiff <(xxd file1) <(xxd file2)
```

## inotify-tools

https://github.com/rvoicilas/inotify-tools

## cpio

[cpio - man page](https://www.mankier.com/1/cpio)
[Linux cpio Examples: How to Create and Extract cpio Archives (and tar archives)](http://www.thegeekstuff.com/2010/08/cpio-utility/)
[cpio - Wikiwand](https://www.wikiwand.com/en/Cpio)

copy files to destination folder keeping the tree structure of the path specified

```sh
# in ~/source
# these files are reachable in ~/source with their relative paths
cat ~/filelist
frameworks/av/media/libstagefright/foundation/ANetworkSession.cpp
frameworks/av/media/libstagefright/wifi-display/Android.mk
frameworks/av/media/libstagefright/wifi-display/MediaSender.cpp
frameworks/av/media/libstagefright/wifi-display/source/Converter.cpp
frameworks/av/media/libstagefright/wifi-display/source/PlaybackSession.cpp
frameworks/av/media/libstagefright/wifi-display/source/TSPacketizer.cpp
frameworks/av/media/libstagefright/wifi-display/source/WifiDisplaySource.cpp
frameworks/av/media/libstagefright/wifi-display/source/WifiDisplaySource.h
frameworks/av/media/libstagefright/wifi-display/VideoFormats.cpp
frameworks/av/media/libstagefright/wifi-display/wfd.cpp

cpio -pud ~/dest < ~/filelist

# cpio single file
echo "frameworks/base/cmds/pm/src/com/android/commands/pm/Pm.java" \
| cpio -pud ${ANDROID_PATCH}/board/common/
```

## cut

```sh
# get n-th to m-th word in string, using ':' as separator
echo ${LINE} | cat -d: -f n,m
```

## tr

replace character in SET1 with characters in SET2

```sh
echo "foo\nbar\nbaz" | tr "bf" "\!"
# negates SET1
echo "foo\nbar\nbaz" | tr -c "bf\n" "\!"
# ROT13
alias rot13="tr '[A-Za-z]' '[N-ZA-Mn-za-m]'"
```

## lsof

[akme/lsofgraph-python: python version of lsof to graphviz parser](https://github.com/akme/lsofgraph-python)
[zevv/lsofgraph: lsof to graphviz](https://github.com/zevv/lsofgraph)
[10 lsof Command Examples in Linux](https://www.tecmint.com/10-lsof-command-examples-in-linux/)

## funny

[20 amusing Linux commands to have fun with the terminal](http://www.binarytides.com/linux-fun-commands/)
[cowsay - Wikiwand](https://www.wikiwand.com/en/Cowsay)

```sh
cowsay -l
fortune | cowsay -f stegosaurus
```

## JSON manipulation

[JSONSelect](http://jsonselect.org/#overview)
[json(1) - JSON love for your command line](http://trentm.com/json/)
[maxogden/jsonmap: CLI JSON mapping/transformation utility](https://github.com/maxogden/jsonmap)
[FGRibreau/jq.node: jq.node - like jq but WAY MORE powerful](https://github.com/FGRibreau/jq.node)

### [jq](https://stedolan.github.io/jq/)

[jq Manual](https://stedolan.github.io/jq/manual/)
[jqterm: jq as a service](https://jqterm.com/?query=.)
[jq play](https://jqplay.org/)

[jq/builtin.jq at master · stedolan/jq](https://github.com/stedolan/jq/blob/master/src/builtin.jq)
[FAQ · stedolan/jq Wiki](https://github.com/stedolan/jq/wiki/FAQ#numbers)
[Advanced Topics · stedolan/jq Wiki](https://github.com/stedolan/jq/wiki/Advanced-Topics)
[Cookbook · stedolan/jq Wiki](https://github.com/stedolan/jq/wiki/Cookbook)
[For JSONPath users · stedolan/jq Wiki](https://github.com/stedolan/jq/wiki/For-JSONPath-users)
[Docs for Oniguruma Regular Expressions (RE.txt) · stedolan/jq Wiki](https://github.com/stedolan/jq/wiki/Docs-for-Oniguruma-Regular-Expressions-(RE.txt%29)
[How to: Avoid Pitfalls · stedolan/jq Wiki](https://github.com/stedolan/jq/wiki/How-to:-Avoid-Pitfalls)

[jq recipes](https://remysharp.com/drafts/jq-recipes)
[JSON Tools: Jq - Hyperpolyglot](http://hyperpolyglot.org/json)
[jq Primer: Munging JSON Data - Andrew Gibiansky](http://andrew.gibiansky.com/blog/command-line/jq-primer/)
[jq is sed for JSON](https://robots.thoughtbot.com/jq-is-sed-for-json)
[Reshaping JSON with jq | Programming Historian](http://programminghistorian.org/lessons/json-and-jq#the-pipe-)
[Parsing JSON with jq](http://www.compciv.org/recipes/cli/jq-for-parsing-json/)
[Wrestling JSON with jq by Arjan van der Gaag](http://arjanvandergaag.nl/blog/wrestling-json-with-jq.html)

[joelpurra/jqnpm: A package manager built for the command-line JSON processor jq.](https://github.com/joelpurra/jqnpm)

```sh
# pick field from array
cat JSON | jq  '[ .[] | { a: .field1, } ]'
cat JSON | jq  'map({ a: .field1, })'

# pick field from files, shorthand for `slideId`
find . -maxdepth 2 -name *json | xargs -I@ jq -c '{slideId, w: .width, h: .height}' @
# collect NDJSON as array and convert to CSV
find . -maxdepth 2 -name *json | xargs -I@ jq -c '{slideId, w: .width, h: .height}' @ | jq -s -f ~/tocsv.jq

# match field
cat JSON | jq -c 'select(.row === 33089)'
cat JSON | jq -c 'select(.list | contains(["foo", "bar"]) | select(.access | test("(deny|disallow)") | not)'
```

`tocsv.jq`:

```
def tocsv($x):
    $x
    |(map(keys)
        |add
        |unique
        |sort
    ) as $cols
    |map(. as $row
        |$cols
        |map($row[.]|tostring)
    ) as $rows
    |$cols,$rows[]
    | @csv;

tocsv(.)
```

[How to convert arbirtrary simple JSON to CSV using jq? - Stack Overflow](https://stackoverflow.com/questions/32960857/how-to-convert-arbirtrary-simple-json-to-csv-using-jq)
[Create JSON using jq from pipe-separated keys and values in bash - Stack Overflow](https://stackoverflow.com/questions/38860529/create-json-using-jq-from-pipe-separated-keys-and-values-in-bash)

## Toolbelt

[ericfreese/rat: Compose shell commands to build interactive terminal applications](https://github.com/ericfreese/rat)
[danielstjules/pjs](https://github.com/danielstjules/pjs)
Perl for regex
find
grep
pt
sed
tr
JSON manipulation
