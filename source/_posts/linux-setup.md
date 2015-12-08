---
title: "Linux setup"
date: 2015-01-23 13:47:38
categories:
- linux
tags:
- desktop
toc: true
---

ArchLinux has IMO the best Linux [wiki](https://www.archlinux.org/).
Most of the Linux tricks can be found there.

[Linux Toolkits](http://linuxtoolkit.blogspot.hk/)

<!-- more -->

## Bootable USB key

Creating a bootable USB key in Linux is [straight forward](https://wiki.archlinux.org/index.php/USB_flash_installation_media).

```
sudo dd if=[iso] of=[usb device] bs=4M
```

Also see `dd-usb-iso`.

Note [some utils](http://antergos.com/wiki/article/create-a-working-live-usb/) modify the partition label of the ISO, that can cause problem during bootup.

- [UNetbootin][UNetbootin - Homepage and Downloads](http://unetbootin.github.io/)
- Linux Live USB Creator
- Universal USB Installer
- Live USB Creator
- [Rufus](https://rufus.akeo.ie/)

## XBox360 gamepad

### Wired gamepad

Wired XBox360 pad should work out of the box using `xpad` driver

### Wireless gamepad (using `xboxdrv`)

http://pingus.seul.org/~grumbel/xboxdrv/

```sh
sudo add-apt-repository ppa:grumbel/ppa
sudo apt-get update
sudo apt-get install xboxdrv
```

```sh
xboxdrv -L
xboxdrv --daemon
```

http://pingus.seul.org/~grumbel/xboxdrv/xboxdrv.html

[Xbox360Controller - Community Help Wiki](https://help.ubuntu.com/community/Xbox360Controller)
