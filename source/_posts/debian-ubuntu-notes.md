---
title: "Debian/Ubuntu notes"
date: 2014-12-08 13:04:28
categories:
  - linux
tags:
  - debian
  - ubuntu
  - desktop
  - package-manager
  - notes
toc: true
---

[The Debian Administrator's Handbook](http://debian-handbook.info/browse/stable/)
[Ubuntu Desktop Guide](https://help.ubuntu.com/lts/ubuntu-help/index.html)
[CommunityHelpWiki - Community Help Wiki](https://help.ubuntu.com/community/CommunityHelpWiki)

[Trying To Make Ubuntu 18.10 Run As Fast As Intel's Clear Linux - Phoronix](https://www.phoronix.com/scan.php?page=article&item=ubuntu1810-fast-clear&num=1)

<!-- more -->

## Dist upgrade

[Upgrade Ubuntu 16.04 LTS to Ubuntu 18.04 LTS Server](https://websiteforstudents.com/upgrade-ubuntu-16-04-lts-to-ubuntu-18-04-lts-beta-server/)
[How To Upgrade To Ubuntu 18.04 LTS Bionic Beaver - LinuxConfig.org](https://linuxconfig.org/how-to-upgrade-to-ubuntu-18-04-lts-bionic-beaver)

## Package managers

[What is the difference between dpkg and aptitude/apt-get? - Ask Ubuntu](http://askubuntu.com/questions/309113/what-is-the-difference-between-dpkg-and-aptitude-apt-get)
[6.4. Frontends: aptitude, synaptic](http://debian-handbook.info/browse/stable/sect.apt-frontends.html)
[How to Use APT and Say Goodbye to APT-GET in Debian and Ubuntu](https://www.makeuseof.com/tag/how-to-use-apt-debian-ubuntu/)
[APT Cheat Sheet - Packagecloud Blog](https://blog.packagecloud.io/eng/2015/03/30/apt-cheat-sheet/)
[Apt-Cacher-NG User Manual](https://www.unix-ag.uni-kl.de/~bloch/acng/html/index.html)
[aptly - Debian repository management tool](https://www.aptly.info/)

list upgrades: `apt-get -s upgrade`

[Ubuntu Apps Directory](https://apps.ubuntu.com/cat/)
[APT Browse - Home](https://www.apt-browse.org/)

[Good PPAs](https://ppas.fosspost.org/)

### update packages

```sh
# update package cache
sudo apt update
# list upgradable packages
apt-get -s upgrade

sudo apt update && sudo apt dist-upgrade && sudo apt autoremove
```

### repo source

```sh
inxi -r
cat /etc/apt/sources.list
ls /etc/apt/sources.list.d
```

Packages info are cached at `/var/cache/apt`

```sh
# clean cache
sudo apt-get clean
# this fix "Hash Sum mismatch" issue
sudo rm -rf /var/lib/apt/lists/*
```

List available versions and origin repo

```sh
apt policy docker-ce
apt-cache madison docker-ce
```

[apt - what is the file /var/lib/dpkg/status about and why do I need it - Ask Ubuntu](https://askubuntu.com/questions/898163/what-is-the-file-var-lib-dpkg-status-about-and-why-do-i-need-it)
[command line - What do the numbers in the output of apt-cache policy tell us? - Ask Ubuntu](https://askubuntu.com/questions/282602/what-do-the-numbers-in-the-output-of-apt-cache-policy-tell-us)
[Fixing APT Hash Sum Mismatch: Consistent APT Repositories - Packagecloud Blog](https://blog.packagecloud.io/eng/2016/09/27/fixing-apt-hash-sum-mismatch-consistent-apt-repositories/)

### installed packages

```sh
apt list --installed

dpkg --get-selections
dpkg -l
# backup installed packages
dpkg --get-selections > /var/lib/backup/dpkg-state
```

[apt - How to list all installed packages? - Ask Ubuntu](http://askubuntu.com/questions/17823/how-to-list-all-installed-packages)
[Apt get list installed packages | Ubuntu list installed packages | RoseHosting](https://www.rosehosting.com/blog/list-all-installed-packages-with-apt-on-ubuntu/)

The 'autoremove' option is used to remove packages that were installed as dependencies of another package that has since been removed (so long as no other package depends on them).

#### locally installed

[apt - Why are packages listed as "installed", "installed,automatic", or "installed,local"? - Ask Ubuntu](https://askubuntu.com/questions/965942/why-are-packages-listed-as-installed-installed-automatic-or-installed-loc)
These are packages not found in repos.

```sh
apt list --installed | grep ",local"
apt list --installed | awk -F/ '/local]/{print $1}' | xargs apt policy

# DANGEROUS, review before use
apt list --installed | awk -F/ '/local]/{print $1}' | sudo xargs apt purge -y
```

#### residual-config

```sh
apt list | grep residual-config
dpkg -l | grep '^rc'

# DANGEROUS, review before use
apt list | awk -F/ '/residual-config]/{print $1}' | sudo xargs apt purge -y
dpkg -l | grep '^rc' | awk '{print $2}' | sudo xargs dpkg --purge
```

If a package has "residual config", it means that the package was indeed uninstalled, but any configuration files were left behind, such that if you reinstall the package, it will be configured as it was. The 'purge' option uninstalls a package AND its configuration files, if any. This does NOT, BTW, include user's configuration data in their own home directory - it applies to system-wide configuration (e.g., stuff in /etc or /usr/share).

### files in package

[List files of a Debian or Ubuntu package | Slopjong](http://slopjong.de/2013/01/29/list-files-of-a-debian-package/)

For installed packages:

```sh
dpkg -L vim
```

For not-yet-installed packages:

```sh
# (optional) download package from repo with:
apt-get --download-only vim
dpkg --contents vim_7.3.547-6ubuntu5_amd64.deb
```

### list dependent package

### offline install

`sudo dpkg -i *.deb`

> example from [Ubuntu - WineHQ Wiki](https://wiki.winehq.org/Ubuntu#Installing_without_Internet)

```sh
# add PPA for wine
sudo add-apt-repository ppa:wine/wine-builds
sudo apt-get update

# clean cache and download to cache
sudo apt-get clean
sudo apt-get --download-only install winehq-devel
sudo apt-get --download-only dist-upgrade  # needed?

# copy to usb-drive
cp -R /var/cache/apt/archives/ /media/usb-drive/deb-pkgs/

# install from usb-drive
cd /media/usb-drive/deb-pkgs
sudo dpkg -i *.deb
```

### outdated release

When you would like to keep using the release without upgrade

```sh
sudo sed -i -e 's/archive.ubuntu.com\|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list

# for mint
sudo sed -i -e 's/archive.ubuntu.com\|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list.d/official-package-repositories.list
```

[How to fix Ubuntu/Debian apt-get 404 Not Found Package Repository Errors (Saucy, Raring, Quantal, Oneiric, Natty…) | sMyl.es](https://smyl.es/how-to-fix-ubuntudebian-apt-get-404-not-found-package-repository-errors-saucy-raring-quantal-oneiric-natty/)

### install old package

```sh
# list all versions
apt show -a libtiff5

apt install -y --allow-downgrades libtiff5=4.0.6-1 libtiff5-dev=4.0.6-1 libtiffxx5=4.0.6-1

apt mark libtiff5=4.0.6-1 libtiff5-dev=4.0.6-1 libtiffxx5=4.0.6-1
```

## Post-install

[UbuntuUpdates - All package updates](https://www.ubuntuupdates.org/)
[Things To Do After Installing Ubuntu 18.04 (Bionic Beaver)](https://www.fossmint.com/things-to-do-after-installing-ubuntu-18-04/)
[12 Easy Steps to Speed Up Ubuntu Linux](https://www.fossmint.com/speed-up-ubuntu-linux/amp/)

### Netbook

eDongCity NB1000

```sh
sudo apt install xinput rfkill intel-microcode fonts-noto-cjk
```

```sh
# https://www.ubuntuupdates.org/ppa/google_chrome
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt update
sudo apt install google-chrome-stable
```

> add [linux-installs.md](https://gist.github.com/leesei/65bf019431fc418f8ce3) here

## Timezone

```sh
$ date
Thu Mar 21 18:02:49 MST 2012
$ more /etc/timezone
US/Arizona

$ sudo dpkg-reconfigure tzdata
```

> http://www.christopherirish.com/2012/03/21/how-to-set-the-timezone-on-ubuntu-server/

## Network

#### Static IP

Edit `/etc/network/interfaces`:

```
# Configuration for eth0
auto eth0
allow-hotplug eth0

iface eth0 inet static
address 10.6.64.26/24
gateway 10.6.64.1
dns-nameservers 10.6.2.12 10.6.2.11
```

## update kernel

```sh
sudo apt-cache search linux-image-*
sudo apt-cache search linux-image-X.X.XX-generic

sudo apt-get install linux-image-X.X.XX-generic
# headers is optional
sudo apt-get install linux-headers-X.X.XX-generic
sudo update-initramfs -u -k all
# OR
sudo update-initramfs -u -k `uname -r`
sudo update-grub
sudo reboot

# remove old kernel
# list kernels
dpkg --get-selections | grep linux-image
sudo apt-get purge linux-image-X.X.XX-XX-generic
```
