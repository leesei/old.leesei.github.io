---
title: "GRUB"
date: 2014-12-17 13:38:19
categories:
- linux
tags:
- grub
toc: true
---

Grub is both boot loader and boot menu.  
It loads `/boot/grub/grub.cfg` and present the menu.

<!-- more -->

[GNU GRUB - Wikiwand](https://www.wikiwand.com/en/GNU_GRUB)
[GRUB - ArchWiki](https://wiki.archlinux.org/index.php/GRUB)

[Commands in the Grub Command-line | Linux.org](http://www.linux.org/threads/commands-in-the-grub-command-line.7536/)
[Understanding the Various Grub Modules | Linux.org](http://www.linux.org/threads/understanding-the-various-grub-modules.7535/)

[How to Configure the GRUB2 Boot Loader’s Settings](http://www.howtogeek.com/196655/how-to-configure-the-grub2-boot-loaders-settings/)

## iso boot

[Grub2/ISOBoot - Community Help Wiki](https://help.ubuntu.com/community/Grub2/ISOBoot)
[How to Boot Linux ISO Images Directly From Your Hard Drive](http://www.howtogeek.com/196933/how-to-boot-linux-iso-images-directly-from-your-hard-drive/)

## Restore GRUB after Windows install

```sh
# check Linux partition
sudo fdisk -l
# mount Linux root (say sda5)
sudo mount /dev/sda5 /mnt
# install grub
sudo grub-install /dev/sda --root-directory=/mnt
sudo reboot

# add Window entry to menu
sudo update-grub
```

[Restore the GRUB Bootloader - Manjaro Linux](https://wiki.manjaro.org/index.php/Restore_the_GRUB_Bootloader)

## Restore Windows after GRUB install

```sh
# this will wipe GRUB out
bootrec /fixmbr
# this won't
bootrec.exe /fixboot
bootrec.exe /RebuildBcd
```

## Edit GRUB entries

`grub-mkconfig` uses the template `/etc/default/grub` and rules in `/etc/grub.d` to generate `grub.cfg`. `update-grub` in Debian system is just a wrapper to `grub-mkconfig`.

```sh
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

## References

https://wiki.archlinux.org/index.php/GRUB
https://wiki.archlinux.org/index.php/GRUB_Legacy
http://jdev.tw/blog/3776/grub-menu-rescue
https://sites.google.com/site/easylinuxtipsproject/grub
http://linuxnorth.wordpress.com/category/grub/
