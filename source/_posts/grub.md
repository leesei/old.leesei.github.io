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
[GRUB/Tips and tricks - ArchWiki](https://wiki.archlinux.org/index.php/GRUB/Tips_and_tricks)
[GNU GRUB Manual](http://www.gnu.org/software/grub/manual/html_node/)
[Grub2 - Community Help Wiki](https://help.ubuntu.com/community/Grub2/)

[Commands in the Grub Command-line | Linux.org](http://www.linux.org/threads/commands-in-the-grub-command-line.7536/)
[Understanding the Various Grub Modules | Linux.org](http://www.linux.org/threads/understanding-the-various-grub-modules.7535/)

[How to Configure the GRUB2 Boot Loader’s Settings](http://www.howtogeek.com/196655/how-to-configure-the-grub2-boot-loaders-settings/)

## iso boot

[Grub2/ISOBoot - Community Help Wiki](https://help.ubuntu.com/community/Grub2/ISOBoot)
[How to Boot Linux ISO Images Directly From Your Hard Drive](http://www.howtogeek.com/196933/how-to-boot-linux-iso-images-directly-from-your-hard-drive/)
[Grub4dos Guide - Configuration File Entries](http://diddy.boot-land.net/grub4dos/files/menu.htm)

## Kernel params

[Kernel/KernelBootParameters - Ubuntu Wiki](https://wiki.ubuntu.com/Kernel/KernelBootParameters)

```sh
# this is equivalent to setting `psmouse.proto=bare` upon boot
sudo modprobe -r psmouse && sudo modprobe -r psmouse proto=bare
```

## Restore GRUB after Windows install

```sh
# check Linux partition
sudo fdisk -l
# mount Linux root (say sda5)
sudo mount /dev/sda5 /mnt
# install grub
sudo grub-install /dev/sda --root-directory=/mnt
sudo reboot

# this will also add Window entry to menu (with os-prober)
sudo grub-mkconfig
```

[Restore the GRUB Bootloader - Manjaro Linux](https://wiki.manjaro.org/index.php/Restore_the_GRUB_Bootloader)

[Boot-Repair - Community Help Wiki](https://help.ubuntu.com/community/Boot-Repair)
[Ubuntu Boot Repair Tutorial – Linux Hint](https://linuxhint.com/ubuntu_boot_repair_tutorial/)
[Windows ＋ Linux 雙系統救回 grub 選單的步驟 | 簡睿隨筆 | 學習過程的紀錄與備忘](http://jdev.tw/blog/3776/grub-menu-rescue)

## Restore Windows after GRUB install

```sh
# this will wipe GRUB out
bootrec /fixmbr
# this won't
bootrec.exe /fixboot
bootrec.exe /RebuildBcd
```

## Edit GRUB entries

`grub-mkconfig` uses the config in `/etc/default/grub` and rules in `/etc/grub.d` to generate `grub.cfg`.
`update-grub` in Debian system is just a wrapper to `grub-mkconfig`.

```sh
sudo grub-mkconfig -o /boot/grub/grub.cfg

# diff first
sudo su
grub-mkconfig -o grub.cfg
diff grub.cfg /boot/grub/grub.cfg
# fish single line
sudo diff (sudo grub-mkconfig | psub)  /boot/grub/grub.cfg
# commit
mv grub.cfg /boot/grub/grub.cfg
```

[How to Configure the Linux Grub2 Boot Menu the Easy Way](https://www.howtogeek.com/howto/43471/how-to-configure-the-linux-grub2-boot-menu-the-easy-way/)

```sh
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
sudo apt-get update
sudo apt-get install grub-customizer
```

### Save default

[Grub2/Submenus - Community Help Wiki](https://help.ubuntu.com/community/Grub2/Submenus)

```
GRUB_DEFAULT=saved
GRUB_SAVEDEFAULT=true
```

`grub-set-default`

## References

[kernel-parameters.txt](https://www.kernel.org/doc/Documentation/kernel-parameters.txt)
[GRUB | LinuxNorth](https://linuxnorth.wordpress.com/category/grub/)

[OS Prober no longer ran by default as of today's update of grub - General system - EndeavourOS](https://forum.endeavouros.com/t/os-prober-no-longer-ran-by-default-as-of-todays-update-of-grub/15187/38)
