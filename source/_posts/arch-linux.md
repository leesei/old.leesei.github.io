---
title: "Arch linux"
date: 2014-12-08 17:43:40
categories:
  - linux
tags:
  - arch-linux
  - manjaro
  - antergos
  - archbang
  - bridge-linux
  - desktop
  - package-manager
  - notes
toc: true
---

[Arch Linux - Wikiwand](http://www.wikiwand.com/en/Arch_Linux)
[Arch Linux Wiki](https://www.archlinux.org/)
[Manjaro Linux](https://wiki.manjaro.org/index.php?title=Main_Page)
[Community Wiki | Antergos](http://antergos.com/wiki/)
[Arch Linux ARM](https://archlinuxarm.org/)

[Arch Linux - ArchWiki](https://wiki.archlinux.org/index.php/Arch_Linux#Principles) The Arch Way
[The Arch Way | The Arch Action Show! - YouTube](https://www.youtube.com/watch?v=iyiaiF_-A2M)
[greg-js/arch-wiki-man: Search a local, updated copy of the entire Arch Wiki and open the article in `man`](https://github.com/greg-js/arch-wiki-man)

[Beginners' guide - ArchWiki](https://wiki.archlinux.org/index.php/Beginners%27_guide)
[System maintenance - ArchWiki](https://wiki.archlinux.org/index.php/System_maintenance)
[[Arch Linux Survival Guide] : LinuxActionShow](http://www.reddit.com/r/LinuxActionShow/comments/1fccny/arch_linux_survival_guide/)
[Arch Linux guide: the always up-to-date Arch Linux tutorial | Linux Veda](http://www.linuxveda.com/2016/02/08/the-always-up-to-date-guide-to-install-arch-linux/)
[Why I always recommend Arch Linux](https://dev.to/supermanitu/why-i-always-recommend-arch-linux)
[5 Ways to Make Arch Linux More Stable - Make Tech Easier](https://www.maketecheasier.com/make-arch-linux-more-stable/)
[Arch Linux for Devs](https://dev.to/svettwer/arch-linux-for-devs-26dm)
[Traveling through the Arch — Vol. 2](https://dev.to/svettwer/traveling-through-the-arch--vol-2-2kl)
[Traveling through the Arch — Vol. 3](https://dev.to/svettwer/traveling-through-the-arch--vol-3-ii4)
[Traveling through the Arch — Vol. 4](https://dev.to/svettwer/traveling-through-the-arch--vol-4-oe4)

[Going to try Arch Linux. Any advice? : linux](http://www.reddit.com/r/linux/comments/cdnhe/going_to_try_arch_linux_any_advice/)
[Arch compared to other distributions - ArchWiki](https://wiki.archlinux.org/index.php/Arch_compared_to_other_distributions)
[arch-announce Info Page](https://lists.archlinux.org//listinfo/arch-announce)

<!-- more -->

## Arch Distros

[DistroWatch.com: based on Arch ](http://distrowatch.com/search.php?ostype=Linux&category=All&origin=All&basedon=Arch&notbasedon=None&desktop=All&architecture=All&status=Active)

[ArcoLinux.info | Linux Made Easy and Beautiful](https://arcolinux.info/)
DE: Xfce, Openbox, i3 (ArcoLinux); varies (ArcoLinuxD/ArcoLinuxB)
[Antergos Linux](http://antergos.com/) discontinued
[Manjaro Linux](https://manjaro.github.io/) [iso](http://sourceforge.net/projects/manjarolinux/files/) [torrent](http://sourceforge.net/projects/manjarotorrents/files/) uses own repo, quirky
DE (official): Xfce, KDE, CLI
DE (community): GNOME, LXQT, LXDE, Openbox, Cinnamon, MATE, Enlightenment
DE: GNOME 3, KDE, Cinnamon, Xfce, Openbox, LXQT, MATE, CLI
[ArchBang](http://www.archbang.org/) [iso](http://sourceforge.net/projects/archbang/files/)
DE: Openbox

### ArcoLinux

[arcolinux](https://github.com/arcolinux)
[arcolinuxd](https://github.com/arcolinuxd)

[ArcoLinuxD - YouTube](https://www.youtube.com/playlist?list=PLlloYVGq5pS7Cf0dqiYbs_no7P6sRtqQH)
[ArcoLinux : 523 ArcoLinux the what, who, where, want, why, when, way and how - YouTube](https://www.youtube.com/watch?v=QWqfXmtXD2E)
[ArcoLinux : 431 what is ArcoLinux and what is Arch Linux - difference - YouTube](https://www.youtube.com/watch?v=zR5XlpWPbXg)

### Manjaro NET-Edition

This provides a minimal install of Manjaro Arch, boots to terminal only.
Install graphic driver and DE yourself.

[Installation Guide for the NET Edition 0.8.10 - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_Guide_for_the_NET_Edition_0.8.10)
[Installation Guide for Experienced Users 0.8.2 - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_Guide_for_Experienced_Users_0.8.2)
[Installation to SSD (quick guide) - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_to_SSD_(quick_guide%29)
[UEFI - Install Guide - Manjaro Linux](https://wiki.manjaro.org/index.php?title=UEFI_-_Install_Guide)

```sh
# [Configure Graphics Cards - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Configure_Graphics_Cards)
sudo mhwd -a pci nonfree 0300

# [Install Desktop Environments - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Install_Desktop_Environments)
sudo pacman -S cinnamon
sudo pacman -S gnome-terminal
```

### Antergos

Antergos LiveCD boots into GNOME3 and comes with a `Cnchi` graphical installer.
It is better to update Cnchi (`pacman -Syu cnchi`) before installation.
The good (may be bad for you) things about Antergos are:

1. it does not install LibreOffice by default
2. it downloads the latest packages from network during install (but the install is slower)

### ArchBang

ArchBang kick-start you with OpenBox WM.

[Announcements page](http://bbs.archbang.org/viewforum.php?id=2)

[ArchBang Brings Arch Linux's Greatest Features to Your PC Without the Stressful Installation](http://lifehacker.com/5857636/archbang-brings-arch-linuxs-greatest-features-to-your-pc-without-the-stressful-installation)

## Installation

[Installation guide - ArchWiki](https://wiki.archlinux.org/index.php/Installation_guide)
[Installation to SSD (quick guide) - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_to_SSD_%28quick_guide%29)

[Installing Arch Linux (Standard Procedure) - YouTube](https://www.youtube.com/watch?v=lizdpoZj_vU) 2015-10
[Full Arch Linux Install (SAVAGE Edition!) - YouTube](https://www.youtube.com/watch?v=4PBqpX0_UOc) 2018-03

[picodotdev/alis: Arch Linux Install Script (alis) installs unattended, automated and customized Arch Linux system.](https://github.com/picodotdev/alis)
[slayerizer/arch_installer: script to install arch linux very quickly](https://github.com/slayerizer/arch_installer)
[Zen Installer download | SourceForge.net](https://sourceforge.net/projects/revenge-installer/)

[Arch Linux Challenge: Tips & Tricks](https://docs.google.com/document/d/1kWQRBDL_N0CImPV5t0W2xj7bsAFcZOLmRsf-kX-eR9M/mobilebasic)
[Arch Linux OS Challenge: Install Arch 'The Easy Way' With These 2 Alternative Methods](https://www.forbes.com/sites/jasonevangelho/2019/06/10/arch-linux-os-challenge-2-alternatives-install-gui-script-easy/amp/)
[picodotdev/alis: Arch Linux Install Script (alis) installs unattended, automated and customized Arch Linux system.](https://github.com/picodotdev/alis)
[Zen Installer download | SourceForge.net](https://sourceforge.net/projects/revenge-installer/)

[Arch Linux Tutorial [updated April 2015] | Linux Veda](http://www.linuxveda.com/2015/02/18/arch-linux-tutorial-updated-feb-2015/)
[Arch Linux 2014.05.01 Released - Installation and Configuration Guide with Screenshots](http://www.tecmint.com/arch-linux-installation-guide/)
[How To Install Arch Linux](https://www.addictivetips.com/ubuntu-linux-tips/how-to-install-arch-linux/)
[Arch Linux Installation and Configuration on UEFI Machines](https://www.tecmint.com/arch-linux-installation-and-configuration-guide/)
[Build a Killer Customized Arch Linux Installation (and Learn All About Linux in the Process)](http://lifehacker.com/5680453/build-a-killer-customized-arch-linux-installation-and-learn-all-about-linux-in-the-process)
[Installing GUI (Cinnamon Desktop) and Basic Softwares in Arch Linux](http://www.tecmint.com/install-cinnamon-desktop-in-arch-linux/)
[Setting up my Arch-Linux-based production environment: II](http://cs.iupui.edu/~pengw/writing/arch-setup-2.html)

```sh
sudo su
curl https://www.archlinux.org/mirrorlist/all/https/ |\
sed 's/^#//g' > /etc/pacman.d/mirrorlist
# https://www.archlinux.org/mirrorlist/

# Antergos specific
pacman -Syy && pacman -S cnchi
cnchi -indv --disable-rank-mirrors --disable-update
```

`/etc/pacman.d/mirrorlist`:

```ini
## Hong Kong
# Hong Kong
Server = https://arch-mirror.wtako.net/$repo/os/$arch
Server = http://arch-mirror.wtako.net/$repo/os/$arch

# United States
Server = https://mirror.rackspace.com/archlinux/$repo/os/$arch
Server = https://mirrors.kernel.org/archlinux/$repo/os/$arch
#Server = https://kwk.pw/arch/$repo/os/$arch
#Server = https://arch.localmsp.org/arch/$repo/os/$arch
#Server = https://mirror.lty.me/archlinux/$repo/os/$arch
#Server = https://lug.mtu.edu/archlinux/$repo/os/$arch
#Server = https://mirrors.ocf.berkeley.edu/archlinux/$repo/os/$arch

# China
#Server = https://mirrors.ustc.edu.cn/archlinux/$repo/os/$arch
```

## Post-install

### pacman repo

[Multilib - ArchWiki](https://wiki.archlinux.org/index.php/Multilib)

```sh
sudo vi /etc/pacman.conf
# Uncomment `[multilib]` section

# update mirrorlist
sudo su
sudo pacman-mirrors -i # or -g

sudo pacman -Syy
sudo pacman-optimize && sync

# update
pacman -Syyu
```

### increase inotify limit

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

> see `caravan/home/rfs.common/etc/`

### install priority packages

```sh
yaourt -S dropbox guake pacmatic zsh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
# copy Dropbox backup to ~/Dropbox to save download time
yaourt -S --needed google-chrome gvim sublime-text-dev-imfix2
```

### SSH Server

[OpenSSH Server on Arch Linux | DominicMDominicM](http://dominicm.com/openssh-server-arch-linux/)

### Samba

[Configure Home Server Samba Shares | DominicMDominicM](http://dominicm.com/configure-home-server-samba-shares/)

```sh
sudo pdbedit -L -v
```

### setup mail

> this is mostly for `pacmatic`'s update

[msmtp - ArchWiki](https://wiki.archlinux.org/index.php/Msmtp#Using_the_mail_command)

```sh
cron-pacmatic <email>
```

### display driver

Proprietary (non-free) drivers is a source of problem. You will have to rebuild the driver every time the kernel is updated. Otherwise X will fail to start.
If performance is not an issue it is [recommended](https://wiki.archlinux.org/index.php/Enhance_system_stability#Choose_open-source_drivers) to use the free drivers.

[Install Video Drivers on Arch Linux | DominicM](http://dominicm.com/install-video-drivers-on-arch-linux/)

[Vulkan - Industry Forged](https://www.khronos.org/vulkan/)
[Vulkan (API) - Wikiwand](https://www.wikiwand.com/en/Vulkan_%28API%29)

#### AMD

[AMD: Download Drivers](http://support.amd.com/en-us/download)
[Installing AMD Catalyst drivers on Arch Linux](http://www.neuraladvance.com/installing-amd-catalyst-drivers-on-arch-linux.html)

#### nVidia

[NVIDIA - ArchWiki](https://wiki.archlinux.org/index.php/NVIDIA)
[NVIDIA/Tips and tricks - ArchWiki](https://wiki.archlinux.org/index.php/NVIDIA/Tips_and_tricks#Fixing_terminal_resolution)

```sh
# drivers
nvidia nvidia-lts nvidia-utils nvidia-libgl lib32-nvidia-utils lib32-nvidia-libgl

## reinstall this upon uninstall
mesa-libgl

# legacy (for Quadro FX 570)
nvidia-340xx nvidia-340xx-lts nvidia-340xx-utils nvidia-340xx-libgl lib32-nvidia-340xx-utils lib32-nvidia-340xx-libgl
```

#### Intel

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

#### Hardware acceleration

[Hardware video acceleration - ArchWiki](https://wiki.archlinux.org/index.php/Hardware_video_acceleration)
There are two APIs for hardware video acceleration: VA-API and VDPAU. It's better to install both.

```sh
# tools
# libva-* or driver for graphic card
libvdpau-va-gl      # VDPAU backend for VA-API
libva-vdpau-driver  # VA-API backend for VDPAU
libva-utils vdpauinfo
```

### Remove indexer (Antergos only?)

```sh
pacman -Rs tracker bijiben gnome-music gnome-online-miners gnome-photos totem zeitgeist
pacman -Rs transmission-cli transmission-gtk
```

### Network

[systemd-networkd - ArchWiki](https://wiki.archlinux.org/index.php/Systemd-networkd)

#### DNS resolver

`~/caravan/home/rfs/etc/resolv.conf`

[Get Started  |  Public DNS  |  Google Developers](https://developers.google.com/speed/public-dns/docs/using#linux)

#### Static IP

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

## Troubleshooting

### "Failed to set default locale"

```sh
sudo vi /etc/locale.gen
# enable "en_US.UTF8    UTF-8"
sudo locale-gen
```

### `/` space used up

```sh
sudo du -hs /var/*
sudo baobab /
```

1. clean pacman cache
   ```sh
   # remove all cache !!CAUTION!!
   sudo pacman -Sc
   ```
2. clean journal
   ```sh
   journalctl --disk-usage
   sudo journalctl --vacuum-size=500M
   ```
   [systemd not cleaning up old journal entries | two minutes hate](https://fmorcos.wordpress.com/2013/02/27/systemd-not-cleaning-up-old-journal-entries/)
3. clean coredump
   ```sh
   sudo rm -rf /var/lib/systemd/coredump/*
   ```
4. use `smallfiles` for MongoDB
   [linux - Is it safe to delete the journal file of mongodb? - Stack Overflow](http://stackoverflow.com/questions/19533019/is-it-safe-to-delete-the-journal-file-of-mongodb)

### future key (Manjaro issue)

I encountered a PGP key error complaining my local key is created in the future in a Manjaro installation.

```sh
# verify PGP key
sudo pacman-key --refresh

# backup invalid key
sudo mv /etc/pacman.d/gnupg/ /etc/pacman.d/gnupgold
# this takes some while
sudo pacman-key --init
sudo pacman-key --populate archlinux manjaro
sudo pacman-key --refresh

# delete backup
sudo rm -rf /etc/pacman.d/gnupgold
```

### dirmngr (Manjaro issue)

If GPG reports `gpg: keyserver refresh failed: No dirmngr`:

```sh
sudo rm -rf ~/.gnupg /root/.gnupg
dirmngr --debug-level guru  # then breaks
sudo su
dirmngr --debug-level guru  # then breaks
# touch dirmngr_ldapservers.conf if needed
sudo pacman-key --refresh

# this is also suggested
sudo -i dirmngr < /dev/null
```

### emergency mode

You boot into emergency/rescue mode when error occurs during boot.

`journalctl -xb` to list boot log, look for errors.
`dbcpcd` (mnemonic: **c**lient **d**aemon) to kick off network.
`sudo mount -o remount,rw /` to make root file system writable.

You may then modify files and use `pacman` to try fix issues.

`systemctrl default`/<kbd>Ctrl</kbd>+<kbd>D</kbd> to start a normal boot.

### hardware probing

[Hardware Probing Via Command-line | Linux.org](http://www.linux.org/threads/hardware-probing-via-command-line.7565/)
[ubuntu - Linux retrieve monitor names - Stack Overflow](http://stackoverflow.com/questions/10500521/linux-retrieve-monitor-names)

### partition probing

Block ID is recommended for `fstab`

```sh
sudo blkid
lsblk
ls /dev/disk/by-{id,label,uuid}
```

[Examining partitions on Linux systems | Network World](https://www.networkworld.com/article/3297916/linux/examining-partitions-on-linux-systems.html)

## Package manager

### gpg

```sh
# this init `~/.gpg`
gpg --list-keys
# add key
gpg --recv-keys 1D1F0DC78F173680
```

### pacman-key

`pacman-key` is a wrapper around gpg

```sh
# if antergos-keyring reports unknown trust
sudo pacman -S antergos-keyring
sudo pacman-key --refresh-keys
# install a specific key
sudo pacman-key -r 1D1F0DC78F173680
```

Add pacman's key to `~/.gnupg/gpg.conf`:

```sh
keyring /etc/pacman.d/gnupg/pubring.gpg
```

or add key automatically:

```sh
keyserver-options auto-key-retrieve
```

### pacman

https://wiki.archlinux.org/index.php/Pacman
https://wiki.archlinux.org/index.php/Pacman_Tips
https://wiki.manjaro.org/index.php?title=Pacman_Tips
http://www.hahack.com/wiki/arch-pacman.html
[Improve pacman performance - ArchWiki](https://wiki.archlinux.org/index.php/Improve_pacman_performance)
[Pacman troubleshooting - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Pacman_troubleshooting)

`/etc/pacman.conf`

[Powerpill - ArchWiki](https://wiki.archlinux.org/index.php/Powerpill)
[bauerbill](https://xyne.archlinux.ca/projects/bauerbill/)

#### repo source

`pacman` only installs from [official repositories](https://wiki.archlinux.org/index.php/Official_repositories): core, extra, community. But the gem of Arch Linux in the [Arch User Repository (AUR)](https://wiki.archlinux.org/index.php/Arch_User_Repository). You can find literally any linux apps there. If it is not there, you can create a PKGBUILD and submit to it.

[Arch Linux - Package Search](https://www.archlinux.org/packages/)
[AUR (en) - Packages](https://aur.archlinux.org/packages/)

[Arch Linux - Mirror Overview](https://www.archlinux.org/mirrors/)
[Arch Linux - Pacman Mirrorlist Generator](https://www.archlinux.org/mirrorlist/)
http://repo.manjaro.org

```sh
sudo pacman-mirrors -i # or -g

# mirror list is located at
sudo vi /etc/pacman.d/mirrorlist
```

#### using AUR

[AUR helpers - ArchWiki](https://wiki.archlinux.org/index.php/AUR_helpers)
[[SOLVED] Should I install programs using pacman or packer? (Page 1) / Pacman/Packages / ArchBang Forums](http://bbs.archbang.org/viewtopic.php?id=2474)
[How To Use Yaourt to Easily Download Arch Linux Community Packages | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-yaourt-to-easily-download-arch-linux-community-packages)

[Don't Install Yaourt! Use These Alternatives for AUR in Arch Linux](https://itsfoss.com/best-aur-helpers/)

`yay -S --aur package_name` force install from AUR

#### sync database (-S -y|--refresh)

```sh
# sync the database
pacman -Sy
# force sync the database
pacman -Syy

# optimze after update
pacman-optimize && sync
```

#### updating (-S -u|--sysupgrade)

```sh
# check packages that can be updated
checkupdates

# chech arch news
pacmatic
# update packages
pacman -Su
# sync and udpate
pacman -Syu
```

#### installing (-S|--sync)

```sh
pacman -S package_name
pacman -S testing/package_name
pacman -S group_name
# local package
pacman -U /package_path/package_name.pkg.tar.xz
```

#### search (-S -s|--search)

```sh
pacman -Ss package_name/package_regex
# name only
pacman -Ssq package_name/package_regex
# package info
pacman -Si package_name
pacman -Sii package_name
# resolve group
pacman -Sg group_name
```

#### clean cache (-S -c|--clean)

```sh
sudo pacman -Scc
# pacman only keeps install version so it is not possible to rollback
# use `pkgcacheclean` from AUR
sudo pkgcacheclean
```

#### remove (-R|--remove)

```sh
pacman -R package_name
# also remove unneeded dependencies
pacman -Rs package_name
# remove orphaned packages
pacman -Rsn $(pacman -Qdtq)
```

#### query installed (-Q|--query)

```sh
# query installed packages, with version
pacman -Q
# backup installed packages
pacman -Q > arch-installed
# use `yaourt -Ss` to show package info
pacman -Qq | xargs -I@ yaourt -Ss ^@$
# query manual installs, use `pac-info` to show package info
pacman -Qeq | xargs -n1 pac-info
# search installed packages
pacman -Qs <query>
# query files in packages
pacman -Ql package_name
# query package that installed the file
pacman -Qo <file path>
# query orphaned packages
# https://wiki.manjaro.org/index.php?title=Orphan_Package_Removal
pacman -Qdt
# query packages installed from sync db
pacman -Qen
# query explicitly installed (and not as dependency)
pacman -Qet
# query packages installed from AUR
pacman -Qem
```

### tools

```sh
# tree view of dependencies
pactree -c package_name

# show reverse dependencies
pactree -cru package_name
# wrapper, requires `pkgtools`
whoneeds package_name
```

### pacmatic

[Pacmatic: Get emails about pending system updates with cron-pacmatic](http://kmkeen.com/pacmatic/)

Pacmatic:

- alert you the updates of **your installed applications**
- forces you to resolve [pacman conflicts](https://wiki.archlinux.org/index.php/Pacnew_and_Pacsave_files)

Just use `pacmatic` instead of `pacman`.

### yaourt

[Yaourt - ArchWiki](https://wiki.archlinux.org/index.php/yaourt)
[yaourt: a pacman frontend « Archlinux.fr](https://archlinux.fr/yaourt-en)
[AUR (en) - yaourt](https://aur.archlinux.org/packages/yaourt/)

Yaourt uses AUR automatically.

```sh
# update packages from official repo and AUR
yaourt -Syua
```

`~/.yaourtrc`:

```sh
#! .rcfile for yaourt
# http://archlinux.fr/man/yaourtrc.5.html

## PROMPT OPTIONS
SUDONOVERIF=1
EDITFILES=0
BUILD_NOCONFIRM=1

## COMMAND OPTIONS
PACMAN="pacmatic"
DIFFEDITCMD="meld"
```

### packer

[keenerd/packer](https://github.com/keenerd/packer)
[AUR (en) - packer](https://aur.archlinux.org/packages/packer/)

[Install Packer on Arch Linux | DominicMDominicM](http://dominicm.com/install-packer-on-arch-linux/)

```sh
sudo pacman -S --needed wget git expac jshon
mkdir packer
cd packer
sudo wget https://aur.archlinux.org/cgit/aur.git/plain/PKGBUILD?h=packer
mv PKGBUILD?h=packer PKGBUILD
makepkg
sudo pacman -U packer-*.pkg.tar.xz
```

Or just get `packer` script from
https://raw.githubusercontent.com/keenerd/packer/master/packer

[Packer and the Arch User Repository | Rory Garand](http://rorygarand.com/blog/2013/02/12/packer-and-the-arch-user-repository)

Same command as `pacman`, but also checks AUR.

### cower

[AUR Helpers - jasonwryan.com](http://jasonwryan.com/blog/2013/04/09/helpers/)
[falconindy/cower](https://github.com/falconindy/cower)
[e36freak/meat](https://github.com/e36freak/meat)

### creating package

[Arch Linux 的靈魂：PKGBUILD、AUR 和 ABS | Tyrant's Arch Linux](http://arch.acgtyrant.com/2013/12/26/soul/)
[Arch Build System - ArchWiki](https://wiki.archlinux.org/index.php/Arch_Build_System)
[Arch packaging standards - ArchWiki](https://wiki.archlinux.org/index.php/Arch_packaging_standards)
[PKGBUILD - ArchWiki](https://wiki.archlinux.org/index.php/PKGBUILD)
[makepkg - ArchWiki](https://wiki.archlinux.org/index.php/Makepkg)
