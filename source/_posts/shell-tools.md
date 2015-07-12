title: "Shell Tools"
date: 2015-01-14 12:48:30
categories:
- app
tags:
- shell-tool
- convert
- cpio
- cut
- diff
- find
- grep
- ImageMagick
- inotify-tools
- netcat
- openRTSP
- pt
- rsync
- sort
- tar
- tr
- xarg
- useradd
- usermod
toc: true
---

[All commands | commandlinefu.com](http://www.commandlinefu.com/commands/browse)
[Core utilities - ArchWiki](https://wiki.archlinux.org/index.php/Core_utilities)
[Tools & Reference - Linode Guides & Tutorials](https://www.linode.com/docs/tools-reference/)
[Linux 101 Hacks eBook, by Ramesh Natarajan](http://www.thegeekstuff.com/linux-101-hacks-ebook/)

## user management

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
```

## ImageMagick

[ImageMagick: Convert, Edit, Or Compose Bitmap Images](http://www.imagemagick.org/script/index.php)
[ImageMagick使用心得](http://www.charry.org/docs/linux/ImageMagick/ImageMagick.html)

```sh
# resizing image
convert -resize 300x300 image.jpg image-small.jpg

# add shadow
convert screenshot.jpg \( +clone -background black -shadow 60×5+0+5 \) +swap -background white -layers merge +repage shadow.jpg

# add timestamp, http://www.imagemagick.org/script/escape.php
convert *.jpg -font Arial -pointsize 72 -gravity SouthEast -fill yellow -annotate +100+100 %[exif:datetime] output-%d.jpg

# convert to pdf
convert a.png b.png -compress jpeg -resize 1240x1753 \
                      -extent 1240x1753 -gravity center \
                      -units PixelsPerInch -density 150x150 multipage.pdf
```

## netcat

http://nc110.sourceforge.net/
http://www.catonmat.net/blog/unix-utilities-netcat/
http://blog.hawkhost.com/2009/12/12/using-netcat-as-an-intercepting-proxy/
http://www.g-loaded.eu/2006/11/06/netcat-a-couple-of-useful-examples/

## netstat

```sh
# list listening TCP ports
netstat -antlp
lsof -i udp:24000
lsof -i tcp:80
```

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

## pt

[monochromegane/the_platinum_searcher](https://github.com/monochromegane/the_platinum_searcher)

## find

[grep - Wikiwand](http://www.wikiwand.com/en/Grep)
[Find](http://www.grymoire.com/Unix/Find.html)
[Find is a beautiful tool](http://www.eriwen.com/productivity/find-is-a-beautiful-tool/)
[Mommy, I found it! — 15 Practical Linux Find Command Examples](http://www.thegeekstuff.com/2009/03/15-practical-linux-find-command-examples/)
[Unix Find Tutorial](http://www.softpanorama.org/Tools/Find/index.shtml)

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

# concat all files and print to console, note the space before '\'
find . -type f -exec cat {} \;

# find executables
find . -perm /a=x

# find empty directories
find . -type d -empty
```

### operate files using inum

This is useful when the file name is particularly long or contains wierd characters.

```sh
# list inum of files
ls -i

cd "$(find -inum 123456)"
mv "$(find -inum 123456)" ../some/where/
```

## rsync

[又一枚瑞士军刀：rsync – Canvas](http://cinvro.com/post/rsync/)
[rsync - man page](https://www.mankier.com/1/rsync)
[rsync 的核心算法 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/7425.html)

## sort

[sort (Unix) - Wikiwand](http://www.wikiwand.com/en/Sort_(Unix))
[sort - man page](https://www.mankier.com/1/sort)

## xarg

[xargs - Wikiwand](http://www.wikiwand.com/en/Xargs)
[xargs - man page](https://www.mankier.com/1/xargs)
[Xargs - Charles Martin Reid](http://charlesmartinreid.com/wiki/Xargs)

## diff

```sh
# left only
diff --changed-group-format='%<' --unchanged-group-format='' FILE1 FILE2
# right only
diff --changed-group-format='%>' --unchanged-group-format='' FILE1 FILE2
```

## inotify-tools

https://github.com/rvoicilas/inotify-tools

## cpio

[cpio - man page](https://www.mankier.com/1/cpio)
[Linux cpio Examples: How to Create and Extract cpio Archives (and tar archives)](http://www.thegeekstuff.com/2010/08/cpio-utility/)

copy files to destination folder keeping the tree sturcture of the path specified 

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
