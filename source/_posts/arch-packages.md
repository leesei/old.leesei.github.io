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

> TODO: link to `cinnamon-setup.md` for the spices I'm using

``` sh
# need review
meh
feh

keymon > screenkey
# http://arch.acgtyrant.com/2015/01/31/show-mouse-click-and-keyboard-press/

steam steam-wrapper-git
steam-native steam-lib

oracle-jdk
# https://github.com/Nowaker/aur-packages#oracle-jdk

pdfchain  # gcc 4.8
```

```sh
# [Microcode - ArchWiki](https://wiki.archlinux.org/index.php/Microcode)
intel-ucode
# console tools
bzip2 colordiff dos2unix cpio curl gtkterm-git guake lnav lndir mlocate roxterm tmux tree unrar unzip zip zsh
# system tools
dconf-editor htop lsof mimeo sshfs teamviewer udev-browse-git xdg-utils xsel
# package tools
pacmatic pkgcacheclean pkgtools namcap
# hardware tools
cpu-x hardinfo hwinfo inxi lm_sensors lshw
# i-nex-git  # too much dependency
# storage tools
hdparm hddtemp
# iso tools
# winusb
# VirtualBox
virtualbox virtualbox-guest-utils

# dev tools
bzr git git-extras mercurial subversion
base-devel cabal-install cppcheck ghc jdk libstdc++5 
erlang go lua openssl wireshark-qt
maven # after jdk to have java-environment properly resolved

# cloud storage
dropbox copy-agent
# ui tools
filezilla google-chrome pyrenamer qbittorrent zenity
# remote access
teamviewer remmina freerdp

# editors
atom-editor-bin gvim meld sublime-text-dev wps-office wxhexeditor-git
# text utils
calibre pandoc
# graphic tools
graphviz hugin inkscape pencil pinta shotwell xdot yed

# greeters
lightdm-gtk-greeter lightdm-gtk-greeter-settings

# python
python-pip

# fonts
ttf-font ttf-liberation wqy-zenhei adobe-source-han-sans-otc-fonts

# input method
fcitx-im fcitx-configtool fcitx-table-extra 
gcin

# media tools
avidemux-qt dms mediainfo mediainfo-gui mkvtoolnix mplayer rtmpdump smplayer subtitleeditor
# server tools
couchdb heroku-client-standalone mongodb nginx orientdb-community redis robomongo samba
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

### cabal

```sh
cabal update
cabal install shellcheck
```

### Steam

[Steam - ArchWiki](https://wiki.archlinux.org/index.php/Steam)
[SteamCMD - Valve Developer Community](https://developer.valvesoftware.com/wiki/SteamCMD)

[pyamsoft/steam-wrapper](https://github.com/pyamsoft/steam-wrapper)
[AUR (en) - steam-wrapper-git](https://aur.archlinux.org/packages/steam-wrapper-git/)
[AUR (en) - steam-libs](https://aur.archlinux.org/packages/steam-libs/)
[AUR (en) - steam-native](https://aur.archlinux.org/packages/steam-native/)

install 32 bits graphic drivers!!!

Use `/usr/bin/steam` to start Steam in console, it reports:

```
Running Steam on antergos  64-bit
STEAM_RUNTIME is enabled automatically
Installing breakpad exception handler for appid(steam)/version(0_client)
libGL error: unable to load driver: r600_dri.so
libGL error: driver pointer missing
libGL error: failed to load driver: r600
libGL error: unable to load driver: swrast_dri.so
libGL error: failed to load driver: swrast
```

```sh
rm ~/.local/share/Steam/ubuntu12_32/steam-runtime/i386/usr/lib/i386-linux-gnu/libstdc++.so.6
rm ~/.local/share/Steam/ubuntu12_32/steam-runtime/i386/usr/lib/i386-linux-gnu/libgcc_s.so.1
```

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

### teamviewer

```sh
sudo systemctl enable teamviewerd
```

### mlocate 

```sh
sudo updatedb
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
