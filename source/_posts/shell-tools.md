title: "Shell Tools"
date: 2015-01-14 12:48:30
categories:
- app
tags:
- shell-tool
- convert
- cpio
- cron
- cut
- find
- grep
- ImageMagick
- netcat
- openRTSP
- pt
- tar
- tr
toc: true
---

http://www.commandlinefu.com/commands/browse

## ImageMagick

http://www.charry.org/docs/linux/ImageMagick/ImageMagick.html

```sh
# resizing image`
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

http://www.eriwen.com/tools/grep-is-a-beautiful-tool/

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

https://github.com/monochromegane/the_platinum_searcher

## find

http://www.eriwen.com/productivity/find-is-a-beautiful-tool/

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

# find all files modified 5 days ago
find . -mtime 5 -type f
```

### operate files using inum

This is useful when the file name is particularly long or contains wierd characters.

```sh
# list inum of files
ls -i

cd "$(find -inum 123456)"
mv "$(find -inum 123456)" ../some/where/
```

## cpio

http://www.thegeekstuff.com/2010/08/cpio-utility/

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
# get n-th to m-th word in string
echo ${LINE} | cat -d ' ' -f n,m
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

## cron

http://www.marksanborn.net/linux/learning-cron-by-example/

```sh
# view our crontab entries without editing them
crontab -l

# view our crontab entries without editing them
crontab -e

# remove your crontab file and start fresh
crontab -r   ## !! dangerous !!
```

```
#min hour dom month dow command
30 8-18/2 * * 1-5 ./path/to/backup_wiki.sh
# Minutes [0-59]
# Hour [0-23]
# Day of Month [1-31]
# Month [1-12] - January is 1, obviously
# Day of Week [0-6] - Sunday is 0
# Command to run (can have spaces)
```

Logs for `cron` can usually be found in `/var/log/cron.log` or `/var/log/messages`
