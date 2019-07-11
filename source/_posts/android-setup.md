---
title: "Android setup"
date: 2015-01-13 13:09:32
categories:
- android
tags:
- linux
- adb
- settings
toc: true
---

Connecting to Android devices on Linux.

<!-- more -->

## Get vendorID

```sh
$ lsusb
...
Bus 008 Device 042: ID 18d1:0003 Google Inc.
Bus 007 Device 053: ID 2207:0010
...
```

The first part of ID is vendorID (18d1 and 2207 in the above example)

## Update `adb_usb.ini`

```sh
# with android-sdk properly setup
android update adb
```

`~/.android/` is created, append vendor id to `~/.android/adb_usb.ini`

```
# ANDROID 3RD PARTY USB VENDOR ID LIST -- DO NOT EDIT.
# USE 'android update adb' TO GENERATE.
# 1 USB VENDOR ID PER LINE.
0x18d1
0x2207
```

## Restart adb server

```sh
adb kill-server
adb devices
# use `sudo` to start server if you see "permissions denied"
sudo $(which adb) devices
```

## Add udev rule

> Newer system should not need this.

[Using Hardware Devices | Android Developers](http://developer.android.com/tools/device.html)
[android-udev-rules/51-android.rules at master · M0Rf30/android-udev-rules](https://github.com/M0Rf30/android-udev-rules/blob/master/51-android.rules)

Add `51-adb.rules` to `/etc/udev/rules.d`:

```
# allwinner board
#SUBSYSTEM=="usb", SYSFS{idVendor}=="18d1", MODE="0666"
SUBSYSTEM=="usb", ATTR{idVendor}=="18d1", MODE="0666", GROUP="plugdev"
SUBSYSTEM=="usb", ATTR{idVendor}=="18d1",ATTR{idProduct}=="0003",SYMLINK+="android_adb"
# rockchip board
#SUBSYSTEM=="usb", SYSFS{idVendor}=="2207", MODE="0666"
SUBSYSTEM=="usb", ATTR{idVendor}=="2207", MODE="0666", GROUP="plugdev"
SUBSYSTEM=="usb", ATTR{idVendor}=="2207",ATTR{idProduct}=="0010",SYMLINK+="android_adb"
```
> make sure your user is in group `plugdev`

```sh
# restart udev
sudo udevadm control --reload-rules
sudo service udev restart
```

## Reference

http://www.slatedroid.com/topic/41219-connecting-to-a-rk3066-based-board-via-adb-on-linux/
https://wiki.archlinux.org/index.php/android
http://community.linuxmint.com/tutorial/view/888
http://stackoverflow.com/questions/14460656/android-debug-bridge-adb-device-no-permissions

## MTP

> http://open-rotorman.blogspot.com/2013/07/samsung-galaxy-s2-usb.html
> http://www.omgubuntu.co.uk/2011/12/how-to-connect-your-android-ice-cream-sandwich-phone-to-ubuntu-for-file-access
> see `/etc/udev/rules.d/` and `/lib/udev/rules.d/`

Add `51-android-mtp.rule` to `/etc/udev/rules.d`: (not working)

> this get rids of "Unable to open MTP device '[usb:007,038]'" [pop-up](https://www.youtube.com/watch?v=SV4x_Oc3EPg), but the device listed is empty

```
# samsung note3
SUBSYSTEM=="usb", ATTR{idVendor}=="04e8", ATTR{idProduct}=="6860", MODE="0666", OWNER="[username]"
```

[HOWTO: Linux and MTP - xda-developers](http://forum.xda-developers.com/showthread.php?t=2055563)
[Intro to MTP, PTP, and UMS | Linux.org](https://www.linux.org/threads/intro-to-mtp-ptp-and-ums.11283/)
[Samsung Galaxy Devices and Linux Mint](http://forums.linuxmint.com/viewtopic.php?t=116879#p660869)
[Android USB Connections Explained: MTP, PTP, and USB Mass Storage](https://www.howtogeek.com/192732/android-usb-connections-explained-mtp-ptp-and-usb-mass-storage/)
[MTP - ArchWiki](https://wiki.archlinux.org/index.php/MTP)
[MTPfs « Dual Elephants](http://www.adebenham.com/mtpfs/)
[Mount MTP device on Debian 7 wheezy | Roger Steneteg](http://roger.steneteg.org/299/mount-mtp-device-on-debian-7-wheezy/)
[[GUIDE] How-To Automount Your Note 10.1 to Linux with MTP - xda-developers](http://forum.xda-developers.com/showthread.php?t=2140939)
[Getting MTP enabled devices to work with Ubuntu? - Ask Ubuntu](http://askubuntu.com/questions/87667/getting-mtp-enabled-devices-to-work-with-ubuntu/308366#308366)
[The easy way: share data between Nexus 7 and Debian | Legen ... d(i)ary!](http://www.legendiary.at/2013/01/27/the-easy-way-share-data-between-nexus-7-and-debian/)
[The hard way: make MTP work with Nexus 7 on Debian | Legen ... d(i)ary!](http://www.legendiary.at/2013/01/27/the-hard-way-make-mtp-work-with-nexus-7-on-debian/)

### issues

http://sourceforge.net/p/libmtp/bugs/574/
https://bugs.launchpad.net/ubuntu/+source/libmtp/+bug/1015010
