---
title: "Arch Post Install"
date: 2021-01-08 14:55:26
categories:
  - linux
tags:
  - arch-linux
  - desktop
toc: true
---

> desktop agnostic installations (but expects GTK-based ones)
> see `cinnamon-setup.md`

> try to automate these after installing packages

- Copy old Dropbox folder
- Copy old Google Drive folder

```sh
ln -sf ~/Dropbox/caravan ~/carvan
set CARAVAN_ENV [home|64.48]
~/caravan/home/0-install-caravan.sh $CARAVAN_ENV
```

- merge `~/caravan/home/rfs`, `~/caravan/home/rfs.$CARAVAN_ENV`, `~/caravan/home/.local`, `~/caravan/home/$CARAVAN_ENV.local`

The packages are to be installed with `yay -S --needed` (aliased to `yinst`).
Look them up in [Arch](https://www.archlinux.org/packages/) and [AUR](https://aur.archlinux.org/packages/) repo to find info about them if you are using other distro/OS.

See [pigmonkey/spark: Arch Linux Provisioning with Ansible](https://github.com/pigmonkey/spark)
[Create A List Of Installed Packages And Install Them Later From The List In Arch Linux - OSTechNix](https://www.ostechnix.com/create-list-installed-packages-install-later-list-arch-linux/)

> TODO: link to `cinnamon-setup.md` for the spices I'm using

```sh
# priority packages
# console tools
yay -S fish guake ttf-firacode nerd-fonts-fira-code sshfs tmux vim xsel
yay -S bat diff-so-fancy colordiff fd fpp fzf httpie jq mlocate ripgrep shellcheck-bin starship tldr tmux xsel
yay -S pyenv python-pipenv
# new way to rebind mouse/keyboard keys (rather than using X11 conf)
yay -S xbindkeys xautomation
yay -S dropbox google-chrome sublime-text-dev visual-studio-code-bin

# admin tools
baobab dconf lnav
# system tools
cmake dconf-editor docker nethogs udev-browse-git sysstat

# runtime
jre11-openjdk-headless
jdk11-openjdk
dotnet-sdk nuget

# browser
firefox google-chrome
# cloud storage
dropbox
# graphics
gimp inkscape pinta yed pencil-bin
# ui tools
clipit metamorphose2 zenity
albert muparser goldendict
mediainfo-gui meld sublime-merge
# office tools
calibre libreoffice-fresh teams signal-desktop teamviewer turbovnc

# network
openconnect networkmanager-openconnect networkmanager-pptp

# server tools
robo3t-bin
```

```sh
# need review
meh
feh

pdfchain  # gcc 4.8
lostfiles
```

## increase inotify limit

> see `caravan/home/rfs/etc/`

For Dropbox, and possibly more.
When Dropbox seems to fail to sync files, start Dropbox in CLI, see if it reports "Unable to monitor entire Dropbox folder hierarchy."

Permanently:

```sh
su
vi /etc/sysctl.d/30-dropbox.conf
# change max_user_watches to 300000
sysctl --system
```

Temporarily:

```sh
cat /proc/sys/fs/inotify/max_user_watches
sudo echo 150000 > /proc/sys/fs/inotify/max_user_watches
```

## Dracula theme

[Dark theme for Gnome Terminal and 142+ apps — Dracula](https://draculatheme.com/gnome-terminal)
[Dark theme for Gedit and 142+ apps — Dracula](https://draculatheme.com/gedit/)

```sh
cd /tmp && git clone https://github.com/dracula/gnome-terminal
cd gnome-terminal && install.sh
cd /tmp && https://raw.githubusercontent.com/dracula/gedit/master/dracula.xml
mkdir -p $HOME/.local/share/gedit/styles/
cp dracula.xml $HOME/.local/share/gedit/styles/
```

## Terminal

```sh
rm -rf ~/.config/fish
ln -sf ~/caravan/home/apps.conf/fish ~/.config/fish

curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher

ln -s ~/caravan/home/apps.conf/starship.toml ~/.config/
```

## overGrive

Add `~/caravan/applications/overGrive-3.3.9-x86_64.AppImage` to startup

## Sublime Text

`sublime-text-dev` is installed as `subl3`

```sh
# use my settings in Dropbox/caravan
mv ~/.config/sublime-text-3/Packages ~/.config/sublime-text-3/Packages.bak
ln -s ~/caravan/home/apps.conf/sublime-text-3/Packages/ ~/.config/sublime-text-3/Packages
```

## Visual Studio Code

> see `vscode.md#settings-sync`

Better code old Settings Sync setting to `~/.config/Code/User/syncLocalSettings.json`
Do a force download

## SSH Server

[OpenSSH - ArchWiki](https://wiki.archlinux.org/index.php/OpenSSH)

```sh
sudo systemctl enable --now sshd
```

## Java

[Java - ArchWiki](https://wiki.archlinux.org/index.php/Java)

Use `archlinux-java` to select Java Runtime

## Samba

[smb.conf.default](https://git.samba.org/samba.git/?p=samba.git;a=blob_plain;f=examples/smb.conf.default;hb=HEAD)

```sh
sudo cp ~/caravan/home/rfs/etc/samba/smb.conf /etc/samba/
sudo systemctl enable --now smb.service

# add samba user
sudo smbpasswd -a $USER
sudo pdbedit -L -v
```

## display driver

Proprietary (non-free) drivers is a source of problem. You will have to rebuild the driver every time the kernel is updated. Otherwise X will fail to start.
If performance is not an issue it is [recommended](https://wiki.archlinux.org/index.php/Enhance_system_stability#Choose_open-source_drivers) to use the free drivers.

[Install Video Drivers on Arch Linux | DominicM](http://dominicm.com/install-video-drivers-on-arch-linux/)

[Vulkan - Industry Forged](https://www.khronos.org/vulkan/)
[Vulkan (API) - Wikiwand](<https://www.wikiwand.com/en/Vulkan_(API)>)

[arunsivaramanneo/GPU-Viewer: A front-end to glxinfo, vulkaninfo, clinfo and es2_info - Linux](https://github.com/arunsivaramanneo/GPU-Viewer) `gpu-viewer`

### AMD

[AMD: Download Drivers](http://support.amd.com/en-us/download)
[Installing AMD Catalyst drivers on Arch Linux](http://www.neuraladvance.com/installing-amd-catalyst-drivers-on-arch-linux.html)

### nVidia

[NVIDIA - ArchWiki](https://wiki.archlinux.org/index.php/NVIDIA)
[NVIDIA/Tips and tricks - ArchWiki](https://wiki.archlinux.org/index.php/NVIDIA/Tips_and_tricks#Fixing_terminal_resolution)
[Nvidia installer – Discovery](https://discovery.endeavouros.com/nvidia/nvidia-installer/2021/03/)

[Nvidia glx is not loading / Kernel & Hardware / Arch Linux Forums](https://bbs.archlinux.org/viewtopic.php?id=249344)
`(EE) NVIDIA: Failed to load module "glxserver_nvidia" (module does not exist, 0)` in `Xorg.0.log`, `glxinfo` shows MESA driver

[ubuntu-mate/mate-optimus: NVIDIA Optimus GPU switcher](https://github.com/ubuntu-mate/mate-optimus)

```sh
# drivers
nvidia nvidia-lts nvidia-utils nvidia-libgl lib32-nvidia-utils lib32-nvidia-libgl

## reinstall this upon uninstall
mesa-libgl

# legacy (for Quadro FX 570)

```

### Intel

[Intel graphics - ArchWiki](https://wiki.archlinux.org/index.php/intel_graphics)
`man intel`

`xf86-video-intel` now used DRI3 by default, modify `/etc/X11/xorg.conf.d/20-intel.conf` to change to DRI2:

```
Section "Device"
  Identifier  "Intel Graphics"
  Driver      "intel"
  Option      "DRI" "2"             # DRI3 is now default
  #Option      "AccelMethod"  "sna" # default
  #Option      "AccelMethod"  "uxa" # fallback
EndSection
```

### Hardware acceleration

[Hardware video acceleration - ArchWiki](https://wiki.archlinux.org/index.php/Hardware_video_acceleration)
[HardwareVideoAcceleration - Debian Wiki](https://wiki.debian.org/HardwareVideoAcceleration)
There are two APIs for hardware video acceleration: VA-API and VDPAU. It's better to install both.

Note: mpv's wiki says both are old and not needed for hardware decoding

```sh
# tools
# libva-* or driver for graphic card
libvdpau-va-gl      # VDPAU backend for VA-API
libva-vdpau-driver  # VA-API backend for VDPAU
libva-utils vdpauinfo
```

## ~~pacman repo~~

> not needed for modern distro like Endeavour OS

[Multilib - ArchWiki](https://wiki.archlinux.org/index.php/Multilib)

```sh
sudo vi /etc/pacman.conf
# Uncomment `[multilib]` section

# update mirrorlist
sudo su
sudo pacman-mirrors -i # or -g

sudo pacman -Syy

# update
pacman -Syyu
```

## Chinese

[黑眼珠 2: GNOME3： 選擇您的輸入法(openSUSE 13.1)](http://swyear.blogspot.hk/2013/12/gnome3-opensuse-131.html)

### fcitx

[Fcitx - Fcitx](https://fcitx-im.org/wiki/Fcitx)
[Fcitx - ArchWiki](https://wiki.archlinux.org/index.php/Fcitx)

[Fcitx5 - ArchWiki](https://wiki.archlinux.org/index.php/Fcitx5)
[hosxy/Fcitx5-Material-Color: 一款使用 Material Design 配色的 fcitx5 皮肤，喜欢的话给个 star 吧 ヾ(≧ へ ≦)〃 😉](https://github.com/hosxy/Fcitx5-Material-Color)
[fcitx/fcitx5-table-extra](https://github.com/fcitx/fcitx5-table-extra)

```sh
yay -S fcitx5-im fcitx5-table-extra

# reload
fcitx5 -r
# dump settings and environments
fcitx5-diagnose
```

```sh
$ vi ~/.xprofile
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS=@im=fcitx
```

Settings

- "Global Options" -> "Hotkey" -> "Trigger Input Method" -> <kbd>Super</kbd> + <kbd>Space</kbd>
- "Global Options" -> "Behavior" -> Check "Show info when changing focus"
- "Addons" -> "Clipboard" -> "Trigger Key" -> <kbd>Super</kbd> + <kbd>H</kbd>
- These config for "Cangjie3" and "SmartCangJie6"
  - "Input Method" -> "Cangjie3" -> "Order Policy" -> "No"
  - "Input Method" -> "Cangjie3" -> "Candidate List Orientation" -> "Horizontal"

"Cangjie3" has <kbd>\</kbd> as Pinyin shortcut and <kbd>?</kbd> as wildcard

### gcin

[Gcin - ArchWiki](https://wiki.archlinux.org/index.php/Gcin)
[Chinese input in terminal w Gcin issue / ArchBang Forums](http://bbs.archbang.org/viewtopic.php?id=457)

```sh
$ vi ~/.xprofile
export GTK_IM_MODULE=gcin
export XMODIFIERS=@im=gcin
export LC_CTYPE=zh_TW.UTF-8
gcin &
```

## Bluetooth

[Bluetooth - ArchWiki](https://wiki.archlinux.org/index.php/Bluetooth)
[Bluetooth – EndeavourOS](https://endeavouros.com/docs/hardware-and-network/bluetooth/)
[Get bluetooth auto-connected with A2DP – EndeavourOS](https://endeavouros.com/docs/hardware-and-network/bluetooth/get-bluetoth-auto-connected-with-a2dp/)

## Remove indexer (Antergos only?)

```sh
pacman -Rs tracker bijiben gnome-music gnome-online-miners totem zeitgeist
```

## Network

[systemd-networkd - ArchWiki](https://wiki.archlinux.org/index.php/Systemd-networkd)

### DNS resolver

`~/caravan/home/rfs/etc/resolv.conf`

[Get Started | Public DNS | Google Developers](https://developers.google.com/speed/public-dns/docs/using#linux)

### Static IP

Edit `/etc/systemd/network/wired.network`:

```ini
[Match]
Name=enp63s0

[Network]
Address=10.6.64.48/24
Gateway=10.6.64.1
```

Revert to DHCP:

```ini
[Match]
Name=enp63s0

[Network]
DHCP=ipv4
```

```sh
sudo systemctl enable systemd-networkd
sudo systemctl restart systemd-networkd
```

You can lookup interface name with `ifconfig`/`ls /sys/class/net`.
[Network configuration - ArchWiki](https://wiki.archlinux.org/index.php/Network_configuration)
[systemd-networkd - ArchWiki](https://wiki.archlinux.org/index.php/Systemd-networkd#Basic_DHCP_network)

## virtualbox

`virtualbox` may require new kernel, update kernel before installing it

add `/etc/modules-load.d/virtualbox.conf`:

```
vboxdrv
vboxnetadp
vboxnetflt
vboxpci
```

## Steam

[Steam - ArchWiki](https://wiki.archlinux.org/index.php/Steam)
[You can now move your game install folders using Steam](https://windowsreport.com/move-games-install-folders-steam/)
[Moving a Steam Installation and Games - General Troubleshooting - Knowledge Base - Steam Support](https://support.steampowered.com/kb_article.php?ref=7418-YUBN-8129)

[VaporOS | SteamOS with extra features](https://vaporos.net/)
[GamerOS | The definitive couch gaming experience](https://gamer-os.github.io/)
[5 Reasons Why This Linux Gaming OS Is Great For Your Living Room](https://www.forbes.com/sites/jasonevangelho/2020/03/31/5-reasons-why-this-linux-gaming-os-is-great-for-your-living-room/amp/)
[gamer-os/steam-tweaks: Various tools for tweaking Steam/game settings](https://github.com/gamer-os/steam-tweaks)

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

## teamviewer

```sh
sudo systemctl enable --now teamviewerd
```

## mlocate

```sh
sudo updatedb
```

## add user to group

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
