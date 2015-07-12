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

steam

# https://github.com/Nowaker/aur-packages#oracle-jdk

pdfchain  # gcc 4.8

# shell check
sudo apt-get install ghc libghc-parsec3-dev libghc-json-dev libghc-regex-compat-dev libghc-quickcheck2-dev cabal-install
git clone https://github.com/koalaman/shellcheck
cd shellcheck; cabal install
```

```sh
# [Microcode - ArchWiki](https://wiki.archlinux.org/index.php/Microcode)
intel-ucode
# console tools
bzip2 colordiff dos2unix curl guake gvim lndir mlocate roxterm tmux tree unrar unzip zip zsh
# system tools
dconf-editor htop lsof mimeo sshfs teamviewer udev-browse-git xsel
# package tools
pacmatic pkgcacheclean pkgtools namcap
# hardware tools
cpu-g hardinfo hddtemp hwinfo inxi i-nex-git lm_sensors lshw
# VirtualBox
virtualbox virtualbox-guest-utils 

# dev tools
bzr git mercurial subversion
base-devel cabal-install cppcheck ghc jdk libstdc++5 maven
erlang go lua openssl wireshark-qt
# linters
tidy-html5

# cloud storage
dropbox copy-agent
# ui tools
filezilla google-chrome pyrenamer qbittorrent remmina zenity

# editors
atom calibre meld sublime-text-dev wps-office wxhexeditor-git
# graphic tools
graphviz hugin inkscape pencil pinta shotwell xdot

# fonts
ttf-liberation wqy-zenhei 

# input method
# [黑眼珠2: GNOME3： 選擇您的輸入法(openSUSE 13.1)](http://swyear.blogspot.hk/2013/12/gnome3-opensuse-131.html)
fcitx-im fcitx-configtool fcitx-table-extra 
gcin

# media tools
avidemux-qt mediainfo mediainfo-gui mplayer rtmpdump smplayer subtitleeditor
# server tools
couchdb hk heroku-client-latest mongodb nginx redis robomongo
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

### steam

[Steam - ArchWiki](https://wiki.archlinux.org/index.php/Steam)

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

### subl

`sublime-text-dev` is installed as `subl3`

```sh
sudo ln -s /usr/bin/subl3 /usr/bin/subl
# use my settings in Dropbox/caravan
mv ~/.config/sublime-text-3/Packages ~/.config/sublime-text-3/Packages.bak
ln -s ~/caravan/home/apps.conf/sublime-text-3/Packages/ ~/.config/sublime-text-3/Packages
```

Add [license key](https://mail.google.com/mail/ca/u/0/#apps/sublime+key/14490727c2159976)

### teamviewer

```sh
sudo -v
sudo mkdir /etc/systemd/system/graphical.target.wants
sudo ln -s '/usr/lib/systemd/system/teamviewerd.service' '/etc/systemd/system/graphical.target.wants/teamviewerd.service'
```

### mlocate 

```sh
sudo updatedb
```

### wireshark

Add user to group:

```sh
sudo usermod -a -G wireshark ${USER}
```

### Chinese

#### font

[Debian 8 (jessie) 安裝筆記 中文環境篇 - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/31556973.html)

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
