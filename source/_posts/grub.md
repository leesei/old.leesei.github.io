title: "GRUB"
date: 2014-12-17 13:38:19
categories:
- linux
tags:
- grub
toc: true
---

## Restore GRUB after Windows install

```sh
# check Linux partition
sudo fdisk -l
# mount Linux root (say sda5)
sudo mount /dev/sda5 /mnt
# install grub
sudo grub-install /dev/sda --root-directory=/mnt
sudo reboot

# add Window to menu
sudo update-grub
```

## Restore Windows after GRUB install

```sh
# boot to DOS mode with CD
bootrec /fixmbr
```
## Edit GRUB entries

> TODO

## MBR

http://support.microsoft.com/kb/927392
http://windows7themes.net/how-to-fix-mbr-in-windows-7.html
http://www.tomshardware.com/news/win7-windows-7-mbr,10036.html
http://www.sevenforums.com/general-discussion/17521-how-fix-mbr-through-command-prompt.html
http://ubuntuforums.org/showthread.php?t=1014708

## Reference

http://jdev.tw/blog/3776/grub-menu-rescue

https://sites.google.com/site/easylinuxtipsproject/grub

http://linuxnorth.wordpress.com/category/grub/
