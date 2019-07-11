---
title: "Arch Packages"
date: 2015-05-20 14:55:26
categories:
- linux
tags:
- arch-linux
- desktop
toc: true
---

The packages are to be installed with `yaourt -S --needed` (aliased to `yinst`).
Look them up in [Arch](https://www.archlinux.org/packages/) and [AUR](https://aur.archlinux.org/packages/) repo to find info about them if you are using other distro/OS.

See [pigmonkey/spark: Arch Linux Provisioning with Ansible](https://github.com/pigmonkey/spark)
[Create A List Of Installed Packages And Install Them Later From The List In Arch Linux - OSTechNix](https://www.ostechnix.com/create-list-installed-packages-install-later-list-arch-linux/)

> TODO: link to `cinnamon-setup.md` for the spices I'm using

``` sh
# need review
meh
feh

keymon > screenkey

jdk8
jdk8-openjdk
# https://github.com/Nowaker/aur-packages#oracle-jdk

ipmiview

pdfchain  # gcc 4.8
```

```sh
# console tools
fpp-git
# admin tools
lnav
# system tools
dconf-editor nethogs udev-browse-git sysstat
# winusb

clipit

# flasher for Samsung, talks Odin protocol
# heimdall

# cloud storage
backblaze-b2 backblaze-b2sync
# ui tools
filezilla  pyrenamer qbittorrent zenity

# greeters
lightdm-gtk-greeter lightdm-gtk-greeter-settings

# input method
gcin

# network
openconnect  networkmanager-openconnect

# server tools
redis robomongo-bin
```

## quirks

### virtualbox

[VirtualBox - ArchWiki](https://wiki.archlinux.org/index.php/VirtualBox)

`virtualbox` may require new kernel, update kernel before installing it

add `/etc/modules-load.d/virtualbox.conf`:

```
vboxdrv
vboxnetadp
vboxnetflt
vboxpci
```

[GPU Passthrough with QEMU on Arch Linux | DominicM](http://dominicm.com/gpu-passthrough-qemu-arch-linux/)

### Steam

[Steam - ArchWiki](https://wiki.archlinux.org/index.php/Steam)

```sh
flatpak --user remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak --user install flathub com.valvesoftware.Steam
# to allow using $HOME
sudo flatpak override com.valvesoftware.Steam --filesystem=$HOME
flatpak run com.valvesoftware.Steam
```

```sh
linux-steam-integration steam-native-runtime
```

install 32 bits graphic drivers!!!

```sh
# use native runtime
STEAM_RUNTIME=0 steam
```

### sublime text

`sublime-text-dev` is installed as `subl3`

```sh
# use my settings in Dropbox/caravan
mv ~/.config/sublime-text-3/Packages ~/.config/sublime-text-3/Packages.bak
ln -s ~/caravan/home/apps.conf/sublime-text-3/Packages/ ~/.config/sublime-text-3/Packages
```

Add [license key](https://mail.google.com/mail/ca/u/0/#apps/sublime+key/14490727c2159976)

### Visual Studio Code

`visual-studio-code-bin`

### teamviewer

```sh
sudo systemctl enable teamviewerd
```

### mlocate

```sh
sudo updatedb
```

### albert

```sh
yinst albert
yinst muparser goldendict
```

### add user to group

```sh
# for wireshark
sudo usermod -a -G wireshark ${USER}
# for nginx
# enable `user http;` in `/etc/nginx/nginx.conf`
sudo usermod -a -G http ${USER}
chgrp -R http /www/public/
# for /dev/tty*
sudo usermod -a -G uucp ${USER}
```

### Chinese

[黑眼珠2: GNOME3： 選擇您的輸入法(openSUSE 13.1)](http://swyear.blogspot.hk/2013/12/gnome3-opensuse-131.html)

#### fcitx

[Fcitx - Fcitx](https://fcitx-im.org/wiki/Fcitx)
[Fcitx - ArchWiki](https://wiki.archlinux.org/index.php/Fcitx)

```sh
$ vi ~/.xprofile
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS=@im=fcitx
```

Remove most of the hotkeys (by `Esc`) in "Global Config" -> "Hotkey"
Disable "Adjust Order" ("AdjustNo") in "Input Method" -> Double Click "Chanjie3" -> "table/chanjie3.conf"

#### gcin

[Gcin - ArchWiki](https://wiki.archlinux.org/index.php/Gcin)
[Chinese input in terminal w Gcin issue / ArchBang Forums](http://bbs.archbang.org/viewtopic.php?id=457)

```sh
$ vi ~/.xprofile
export GTK_IM_MODULE=gcin
export XMODIFIERS=@im=gcin
export LC_CTYPE=zh_TW.UTF-8
gcin &
```
