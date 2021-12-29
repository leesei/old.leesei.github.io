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
[kernel - What is hardware enablement (HWE)? - Ask Ubuntu](https://askubuntu.com/questions/248914/what-is-hardware-enablement-hwe)

<!-- more -->

## HiDPI

[HiDPI - ArchWiki](https://wiki.archlinux.org/index.php/HiDPI)
[Xorg#Display_size_and_DPI - ArchWiki](https://wiki.archlinux.org/index.php/Xorg#Display_size_and_DPI)
[What is HiDPI - elementary - Medium](https://medium.com/elementaryos/what-is-hidpi-and-why-does-it-matter-b024eabea20d)

[How to find and change the screen DPI? - Ask Ubuntu](http://askubuntu.com/questions/197828/how-to-find-and-change-the-screen-dpi)
[multiple monitors - Is it possible to have two different DPI configurations for two different screens? - Ask Ubuntu](http://askubuntu.com/questions/393400/is-it-possible-to-have-two-different-dpi-configurations-for-two-different-screen)
[[SOLVED] Openbox - setting different dpi on external monitor / Applications & Desktop Environments / Arch Linux Forums](https://bbs.archlinux.org/viewtopic.php?id=177660)

Wayland allows different DPI on multihead setup

## Battery

[A Closer Look At The Linux Laptop Power Use Between Ubuntu, Fedora, Clear & Antergos - Phoronix](https://www.phoronix.com/scan.php?page=article&item=laptop-battery-july18&num=1)
[How to Maximize Your Linux Laptop’s Battery Life](https://www.howtogeek.com/55185/how-to-maximize-the-battery-life-on-your-linux-laptop/)
[7 Simple Tips to Improve Your Linux Laptop's Battery Life](https://www.makeuseof.com/tag/easily-increase-battery-life-tlp-linux/)
[7 Tips To Reduce Battery Usage On Linux](https://fosspost.org/tutorials/7-tips-to-reduce-battery-usage-on-linux)

[linrunner.de: TLP – Linux Advanced Power Management](https://linrunner.de/en/tlp/tlp.html)
[TLP – Quickly Increase and Optimize Linux Laptop Battery Life](https://www.tecmint.com/tlp-increase-and-optimize-linux-battery-life/)

[A Handy Battery Optimizer for Ubuntu Laptops - OMG! Ubuntu!](https://www.omgubuntu.co.uk/2019/05/slimbook-battery-optimizer-ubuntu)

[5 Ways To Check Laptop Battery Status And Level From Linux Terminal | 2daygeek.com](https://www.2daygeek.com/check-laptop-battery-status-and-charging-state-in-linux-terminal/)

```sh
sudo tlp-stat -b
sudo tlp-stat -s
batstat
gnome-power-statistics
cat /sys/class/power_supply/BAT0/*
```

[PowerTOP | 01.org](https://01.org/powertop)
[PowerTop - Monitors Total Power Usage and Improve Linux Laptop Battery Life](https://www.tecmint.com/powertop-monitors-linux-laptop-battery-usage/)

[How to Monitor Laptop Battery Usage in Linux - Make Tech Easier](https://www.maketecheasier.com/monitor-laptop-battery-usage-linux/)

[Battery life on linux systems : linux](https://www.reddit.com/r/linux/comments/7wn791/battery_life_on_linux_systems/)

## Wifi

[Category:Wireless adapter - WikiDevi](https://wikidevi.com/wiki/Category:Wireless_adapter)
[Top Linux Compatible USB Wireless Adapters | WirelesSHack](https://www.wirelesshack.org/top-linux-compatible-usb-wireless-adapters.html)

[wpa_supplicant authentication timed out / Networking, Server, and Protection / Arch Linux Forums](https://bbs.archlinux.org/viewtopic.php?id=231987)
[How to Connect to WiFi from the Terminal in Ubuntu Linux](https://itsfoss.com/connect-wifi-terminal-ubuntu/)

[WifiDocs/Driver/bcm43xx - Community Help Wiki](https://help.ubuntu.com/community/WifiDocs/Driver/bcm43xx)

[netctl - ArchWiki](https://wiki.archlinux.org/title/netctl) `wifi-menu`
[Accessing and Using the WiFi Menu – Enplug Support Center](https://support.enplug.com/hc/en-us/articles/212689223-Accessing-and-Using-the-WiFi-Menu)
[How To Setup A WiFi Network In Arch Linux Using Terminal﻿](https://www.linuxandubuntu.com/home/how-to-setup-a-wifi-in-arch-linux-using-terminal)

```sh
iwconfig

sudo lshw -c network
sudo iwlist scan
iwd
iw dev
sudo iw dev wlp0s20u11 scan

rfkill list all  # toggle wireless devices

nmcli dev wifi list
nmcli device wifi connect "{{SSID}}" password "{{PASSPHRASE}}"
nmcli device wifi hotspot ssid "{{SSID}}" password "{{PASSPHRASE}}"

ifconfig wlan0 up
iwconfig wlan0 essid "{{SSID}}"
iwconfig wlan0 essid "{{SSID}}" key "{{WEP KEY}}"
iwconfig wlan0 essid "{{SSID}}" key s:"{{WPA/WPA2 KEY}}"
dhcpcd wlan0

wpa_supplicant -i wlp0s20u11 -c <(wpa_passphrase "{{SSID}}" "{{PASSPHRASE}}") -d
```

### NetworkManager logs

Enable debugging of NetworkManager

```sh
sudo vi /usr/lib/systemd/system/NetworkManager.service
sudo journalctl -fu wpa_supplicant.service
sudo journalctl -fu NetworkManager # show logs
```

```diff
- ExecStart=/usr/sbin/NetworkManager --no-daemon
+ ExecStart=/usr/sbin/NetworkManager --no-daemon --log-level=debug
```

### TL-WN823N (dongle)

[clnhub/rtl8192eu-linux: Realtek rtl8192eu official Linux driver v5.2.19.1](https://github.com/clnhub/rtl8192eu-linux) better than `Mange/rtl8192eu-linux-driver`?

[TP-Link TL-WN823N on Arch Linux – mheap](https://michaelheap.com/tp-link-tl-wn823n-on-arch-linux/)
[Mange/rtl8192eu-linux-driver: Drivers for the rtl8192eu chipset for wireless adapters (D-Link DWA-131 rev E1 included!)](https://github.com/Mange/rtl8192eu-linux-driver)
[Ubuntu 16.04 解决 TL-WN826N 的驱动问题 - CSDN 博客](https://blog.csdn.net/sxbyyy/article/details/73865023)
[How to compile Mange/rtl8192eu-linux-driver driver.. – Site Title](https://scdas141.wordpress.com/2017/01/28/how-to-compile-mangertl8192eu-linux-driver-driver/)

```sh
git clone https://github.com/Mange/rtl8192eu-linux-driver /usr/src/rtl8192eu-linux-driver
cd rtl8192eu-linux-driver
sudo dkms add .
sudo dkms install rtl8192eu/1.0

sudo dkms uninstall rtl8192eu/1.0
sudo dkms remove rtl8192eu/1.0 --all

ln -s /var/lib/dkms/rtl8192eu/1.0/source /usr/src/rtl8192eu-1.0
sudo dkms install rtl8192eu/1.0 -k 4.14.56-1-lts
sudo dkms install rtl8192eu/1.0 -k 5.8.7-arch1-1

rmmod rtl8xxxu
```

[[SOLVED] rtl8192eu USB Wifi not working / Kernel & Hardware / Arch Linux Forums](https://bbs.archlinux.org/viewtopic.php?id=219909)
[I already installed the driver, but I can not connect to a wifi network · Issue #46 · Mange/rtl8192eu-linux-driver](https://github.com/Mange/rtl8192eu-linux-driver/issues/46#issuecomment-323710229)

Disable kernel rtl8xxxu driver:

```sh
sudo su
mkdir -p /etc/modprobe.d
cat << EOF > /etc/modprobe.d/rtl8xxxu-blacklist.conf
# Do not load the 'rtl8xxxu' module on boot.
blacklist rtl8xxxu
EOF
```

### BCM3413 (Toshiba C660)

Using `bcmwl-kernel-source` proprietary driver on Ubuntu Mate 18.04

[networking - Ubuntu 18.04 LTS wifi problems - Ask Ubuntu](https://askubuntu.com/questions/1087090/ubuntu-18-04-lts-wifi-problems)
[networking - Installing Broadcom Wireless Drivers - Ask Ubuntu](https://askubuntu.com/questions/55868/installing-broadcom-wireless-drivers)

```sh
sudo vi /etc/default/crda

REGDOMAIN=HK
```

[linux - alternative to bcmwl-kernel-source package - Super User](https://superuser.com/questions/626601/alternative-to-bcmwl-kernel-source-package)
vs `linux-firmware-nonfree`, `firmware-b43-installer`, `b43-fwcutter`?
[Why Broadcom 802.11 Linux STA driver sucks, and how to fix it | pofHQ](http://pof.eslack.org/2012/05/23/why-broadcom-80211-linux-sta-driver-sucks-and-how-to-fix-it/)(2012)
