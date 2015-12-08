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

[Beginners' guide - ArchWiki](https://wiki.archlinux.org/index.php/Beginners%27_guide)
[System maintenance - ArchWiki](https://wiki.archlinux.org/index.php/System_maintenance)
[[Arch Linux Survival Guide] : LinuxActionShow](http://www.reddit.com/r/LinuxActionShow/comments/1fccny/arch_linux_survival_guide/)

[Going to try Arch Linux. Any advice? : linux](http://www.reddit.com/r/linux/comments/cdnhe/going_to_try_arch_linux_any_advice/)
[Arch compared to other distributions - ArchWiki](https://wiki.archlinux.org/index.php/Arch_compared_to_other_distributions)
[arch-announce Info Page](https://lists.archlinux.org//listinfo/arch-announce)

<!-- more -->

## Arch Distros

[DistroWatch.com: based on Arch ](http://distrowatch.com/search.php?ostype=Linux&category=All&origin=All&basedon=Arch&notbasedon=None&desktop=All&architecture=All&status=Active)

[Manjaro Linux](https://manjaro.github.io/) [iso](http://sourceforge.net/projects/manjarolinux/files/) [torrent](http://sourceforge.net/projects/manjarotorrents/files/)
Desktops (official): Xfce, KDE, CLI
Desktops (community): GNOME, LXQT, LXDE, Openbox, Cinnamon, MATE, Enlightenment
[Antergos Linux](http://antergos.com/)
Desktops: GNOME 3, KDE, Cinnamon, Xfce, Openbox, LXQT, MATE, CLI
[ArchBang](http://www.archbang.org/) [iso](http://sourceforge.net/projects/archbang/files/)
Desktops: Openbox
[Bridge Linux](http://millertechnologies.net/bridgelinux.html) 
Desktops: Xfce, LXDE, Openbox, KDE, GNOME 3
[Papyros](http://papyros.io/)
Desktops: Papyros

### Manjaro NET-Edition

This provides a minimal install of Manjaro Arch, boots to terminal only.
Install graphic driver and DE yourself.

[Installation Guide for the NET Edition 0.8.10 - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_Guide_for_the_NET_Edition_0.8.10)
[Installation Guide for Experienced Users 0.8.2 - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_Guide_for_Experienced_Users_0.8.2)
[Installation to SSD (quick guide) - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_to_SSD_(quick_guide))
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
1. it does not install LibreOffice (which I don't use) by default
2. it downloads the latest packages from network during install (but the install is slower)

### ArchBang

ArchBang kick-start you with OpenBox WM.

[Announcements page](http://bbs.archbang.org/viewforum.php?id=2)

[ArchBang Brings Arch Linux's Greatest Features to Your PC Without the Stressful Installation](http://lifehacker.com/5857636/archbang-brings-arch-linuxs-greatest-features-to-your-pc-without-the-stressful-installation)

## Installation

[Installation guide - ArchWiki](https://wiki.archlinux.org/index.php/Installation_guide)
[Installation to SSD (quick guide) - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Installation_to_SSD_(quick_guide))

[Arch Linux 2014.05.01 Released - Installation and Configuration Guide with Screenshots](http://www.tecmint.com/arch-linux-installation-guide/)

[Build a Killer Customized Arch Linux Installation (and Learn All About Linux in the Process)](http://lifehacker.com/5680453/build-a-killer-customized-arch-linux-installation-and-learn-all-about-linux-in-the-process)

[Installing GUI (Cinnamon Desktop) and Basic Softwares in Arch Linux](http://www.tecmint.com/install-cinnamon-desktop-in-arch-linux/)
[My Arch Linux setup](http://blog.mixu.net/2011/11/10/my-arch-linux-setup/)
[Setting up my Arch-Linux-based production environment](http://cs.iupui.edu/~pengw/writing/arch-setup.html)
[Setting up my Arch-Linux-based production environment: II](http://cs.iupui.edu/~pengw/writing/arch-setup-2.html)

## Post-install

### pacman repo

[Multilib - ArchWiki](https://wiki.archlinux.org/index.php/Multilib)

```sh
sudo vi /etc/pacman.conf
# Uncomment `[multilib]` section

# update mirrorlist
sudo vi /etc/pacman.d/mirrorlist # OR
sudo pacman-mirrors -i # or -g
sudo pacman -Syy
sudo pacman-optimize && sync

# update
pacman -Syyu
```

### increase inotify limit

For Dropbox, and possibly more

Permanently:

```sh
su
echo "fs.inotify.max_user_watches=150000" > /etc/sysctl.d/10-sysctl.conf
sysctl --system
```

Temporarily:

```sh
cat /proc/sys/fs/inotify/max_user_watches
sudo echo 150000 > /proc/sys/fs/inotify/max_user_watches
```

> See `caravan/home/rfs.common/etc/`

### install priority packages

```sh
yaourt -S dropbox guake pacmatic zsh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
# copy Dropbox backup to ~/Dropbox to save download time
yaourt -S --needed google-chrome gvim sublime-text-dev
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

#### AMD

[AMD: Download Drivers](http://support.amd.com/en-us/download)
[Installing AMD Catalyst drivers on Arch Linux](http://www.neuraladvance.com/installing-amd-catalyst-drivers-on-arch-linux.html)

#### nVidia

```sh
# drivers
nvidia nvidia-lts nvidia-utils nvidia-libgl lib32-nvidia-utils lib32-nvidia-libgl

# legacy (for Quadro FX 570)
nvidia-340xx nvidia-340xx-lts nvidia-340xx-utils nvidia-340xx-libgl lib32-nvidia-340xx-utils lib32-nvidia-340xx-libgl
```

### Remove indexer (Antergos only?)

```sh
yaourt -Rs tracker bijiben gnome-music gnome-online-miners gnome-photos totem zeitgeist 
```

### Network

[systemd-networkd - ArchWiki](https://wiki.archlinux.org/index.php/Systemd-networkd)

#### DNS resolver

`~/caravan/home/rfs.common/etc/resolv.conf`

[Get Started  |  Public DNS  |  Google Developers](https://developers.google.com/speed/public-dns/docs/using#linux)

#### static IP address

Edit `/etc/systemd/network/wired.network`:

```
[Match]
Name=enp63s0

[Network]
Address=10.6.64.47/24
Gateway=10.6.64.1
```

Revert to DHCP:
```
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

### hardware propbing

[Hardware Probing Via Command-line | Linux.org](http://www.linux.org/threads/hardware-probing-via-command-line.7565/)

`fstab`

```sh
sudo blkid
lsblk
ls /dev/disk/by-{id,label,uuid}
```

## Package manager

### pacman-key

`pacman-key` is a wrapper around gpg

#### add key

```sh
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
[Powerpill - ArchWiki](https://wiki.archlinux.org/index.php/Powerpill)
[Pacman troubleshooting - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Pacman_troubleshooting)

`/etc/pacman.conf`

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

#### creating package

[Arch Linux 的靈魂：PKGBUILD、AUR 和 ABS | Tyrant's Arch Linux](http://arch.acgtyrant.com/2013/12/26/soul/)
[Arch Build System - ArchWiki](https://wiki.archlinux.org/index.php/Arch_Build_System)
[Arch packaging standards - ArchWiki](https://wiki.archlinux.org/index.php/Arch_packaging_standards)
[PKGBUILD - ArchWiki](https://wiki.archlinux.org/index.php/PKGBUILD)

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
# tree view of dependencies
pactree package_name
```

#### clean cache (-S -c|--clean)

```sh
pacman -Sc
# pacman only keeps install version so it is not possible to rollback
# use `pkgcacheclean` from AUR
pkgcacheclean
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
# search installed packages
pacman -Qs <query>
# query files in packages
pacman -Ql package_name
# query package that installed the file
pacman -Qo <file path>
# query orphaned packages
# https://wiki.manjaro.org/index.php?title=Orphan_Package_Removal
pacman -Qdt
# query explicitly installed
pacman -Qet
# list dependents, requires `pkgtools`
whoneeds package_name
```

### pacmatic

[Pacmatic: Get emails about pending system updates with cron-pacmatic](http://kmkeen.com/pacmatic/)

Pacmatic:
- alert you the updates of **your installed applications**
- forces you to resolve [pacman conflicts]https://wiki.archlinux.org/index.php/Pacnew_and_Pacsave_files)

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

[DominicM – Install Packer on Arch Linux](http://dominicm.com/install-packer-on-arch-linux/)
[Packer and the Arch User Repository | Rory Garand](http://rorygarand.com/blog/2013/02/12/packer-and-the-arch-user-repository)

Same command as `pacman`, but also checks AUR.

### creating package

[Arch Build System - ArchWiki](https://wiki.archlinux.org/index.php/Arch_Build_System)
[makepkg - ArchWiki](https://wiki.archlinux.org/index.php/Makepkg)
