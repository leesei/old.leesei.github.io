title: Linux Desktop
date: 2014-12-12 16:06:50
categories:
- linux
tags:
- desktop
- xinput
- xdg-utils
- gjs
toc: true
---

This post is about using GNU/Linux with desktop environment for daily use.

To distinguish GNU and Linux, and why it it not "correct" to say Linux system, read: [Linux and GNU](http://www.gnu.org/gnu/linux-and-gnu.html) and 
[GNU/Linux FAQ](http://www.gnu.org/gnu/gnu-linux-faq.html#why)

[Main Linux problems on the desktop, 2015 edition](http://linuxfonts.narod.ru/why.linux.is.not.ready.for.the.desktop.current.html)
[Linux video tools](http://www.videohelp.com/tools/sections/linux-video-tools)

<!-- more -->

## File Association

https://wiki.archlinux.org/index.php/Default_applications
http://stackoverflow.com/a/31836/665507
https://www.google.com.hk/search?q=linux+associate+file+extension+with+application
https://developer.gnome.org/integration-guide/stable/desktop-files.html.en
http://ubuntugenius.wordpress.com/2009/11/19/create-your-own-file-types-in-ubuntu-with-assogiate/

How to set gpicview to default image viewer? Use following command line:
```sh
xdg-mime default gpicview.desktop `grep 'MimeType=' /usr/share/applications/gpicview.desktop | sed -e 's/.*=//' -e 's/;/ /g'`
```

NOTE: [xdg-utils](http://portland.freedesktop.org/wiki/XdgUtils) is needed here. It's a tool released by Portland project of Freedesktop.org. Most modern Linux distros have this tool installed by default.

### `.desktop` folders

```
/usr/local/share/applications
/usr/share/applications
~/.local/share/applications
```

### Open folder with

```sh
vi .~/local/share/applications/mimeapps.list
```

Add this to `[Added Associations]`
```
inode/directory=sublime_text.desktop
```

## `xinput`

```
xinput list
xinput test <id>/<name>
xinput list-props <id>/<name>
xinput set-prop <id>/<name> <prop id>/<prop name> <value>
```

Settings are put in:
- `/etc/X11/xorg.conf.d` (Arch)
- `/usr/share/X11/xorg.conf.d` (Debian)

Look up with `locate xorg.conf.d | grep d$`

## xdg-utils

[xdg-utils](http://portland.freedesktop.org/xdg-utils-1.0/)

## Gjs

[Projects/Gjs - GNOME Wiki!](https://wiki.gnome.org/action/show/Projects/Gjs?action=show&redirect=Gjs)
[石頭閒語:JavaScript分類文章簡文 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/cat_242544.html)

[JavaScript 與 Desktop - WebKit - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/14282187.html)
[JavaScript 與 Desktop - Desktop and WebKit - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/14456843.html)
[JavaScript 與 Desktop - DBus - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/14229429.html)

## Wine

[WineHQ - Run Windows applications on Linux, BSD, Solaris and Mac OS X](https://www.winehq.org/)
[轉子男: [Ubuntu] 使用 Wine 安裝 Office 2010 於 Ubuntu 12.04](http://open-rotorman.blogspot.com/2012/11/ubuntu-wine-office-2010-ubuntu-1204.html)

## update kernel

```sh
sudo apt-cache search linux-image-*
sudo apt-cache search linux-image-X.X.XX-generic

sudo apt-get install linux-image-X.X.XX-generic
# headers is optional
sudo apt-get install linux-headers-X.X.XX-generic
sudo update-initramfs -u -k all
# OR
sudo update-initramfs -u -k `uname -r`
sudo update-grub 
sudo reboot

# remove old kernel
# list kernels
dpkg --get-selections | grep linux-image
sudo apt-get purge linux-image-X.X.XX-XX-generic
```

