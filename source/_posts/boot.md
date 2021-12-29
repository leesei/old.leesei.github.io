---
title: "Boot"
date: 2015-05-10 22:07:17
categories:
  - linux
tags:
  - desktop
toc: true
---

[Booting - Wikiwand](https://www.wikiwand.com/en/Booting#/SPL)

POST -> BIOS/ROM code -> MBR of boot partition -> Bootloader ->
Kernel -> [`init`](https://wiki.archlinux.org/index.php/Init)/[`systemd`](https://wiki.archlinux.org/index.php/Systemd) ->
shell/display manager (login) -> `startx`/`xinit` -> DE

1. CPU starts in real mode, executes instruction at 0xFFFF0
   → top of BIOS ROM
2. self test (POST), configuration of devices (e.g. PCI
   resource allocation), initialization of BIOS extensions
   (option ROMs)
3. load first sector of boot device ("boot sector", MBR) to
   0x7C00  
   MBR relocates itself, loads first sector of active partition to
   0x7C00
4. boot sector loads "second stage" boot loader
   a. boot loader knows how to read kernel from file system
   b. usually loads kernel to an address > 1MB and switches to
   protected mode before jumping to kernel entry point

```
+--------+----------------+----------------+----------+
| Boot   | Terminology #1 | Terminology #2 | Actual   |
| stage  |                |                | program  |
| number |                |                | name     |
+--------+----------------+----------------+----------+
| 1      |  Primary       |  -             | ROM code |
|        |  Program       |                |          |
|        |  Loader        |                |          |
|        |                |                |          |
| 2      |  Secondary     |  1st stage     | u-boot   |
|        |  Program       |  bootloader    | SPL      |
|        |  Loader (SPL)  |                |          |
|        |                |                |          |
| 3      |  -             |  2nd stage     | u-boot   |
|        |                |  bootloader    |          |
|        |                |                |          |
| 4      |  -             |  -             | kernel   |
|        |                |                |          |
+--------+----------------+----------------+----------+
```

[System Initialization (x86) - OSDev Wiki](<https://wiki.osdev.org/System_Initialization_(x86)>)
[Linux startup process - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Linux_startup_process)
[Arch boot process - ArchWiki](https://wiki.archlinux.org/index.php/Arch_boot_process)
[Inside the Linux boot process](http://www.ibm.com/developerworks/linux/library/l-linuxboot/)
[The BIOS/MBR Boot Process](https://neosmart.net/wiki/mbr-boot-process/)
[鳥哥的 Linux 私房菜 -- 第十九章、開機流程、模組管理與 Loader](http://linux.vbird.org/linux_basic/0510osloader.php)
[如何訂製 Linux X 視窗環境 - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/19886616.html)

[LinuxBoot](https://www.linuxboot.org/)

[Some basics of MBR v/s GPT and BIOS v/s UEFI - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Some_basics_of_MBR_v/s_GPT_and_BIOS_v/s_UEFI)
[What’s the Difference Between GPT and MBR When Partitioning a Drive?](https://www.howtogeek.com/193669/whats-the-difference-between-gpt-and-mbr-when-partitioning-a-drive/)
[MBR vs GPT: What's the Difference Between an MBR Partition and a GPT Partition? [Solved]](https://www.freecodecamp.org/news/mbr-vs-gpt-whats-the-difference-between-an-mbr-partition-and-a-gpt-partition-solved/)
MBR: up to 2TB, 4 primary partitions
GPT (Windows): 128 partitions, bootable only with UEFI

## Bootloader

[Bootloader - OSDev Wiki](https://wiki.osdev.org/Bootloader)
[What is the difference between a Bootrom vs bootloader on ARM systems - Stack Overflow](https://stackoverflow.com/questions/15665052/what-is-the-difference-between-a-bootrom-vs-bootloader-on-arm-systems)
[linux - Why do we need a bootloader in an embedded device? - Stack Overflow](https://stackoverflow.com/questions/15548004/why-do-we-need-a-bootloader-in-an-embedded-device)

SPL (secondary program loader) is needed when the static RAM cannot hold the whole bootloader and this abstract the hardware form bootloader
[what is the use of SPL (secondary program loader) - Stack Overflow](https://stackoverflow.com/questions/31244862/what-is-the-use-of-spl-secondary-program-loader)

[TPL: SPL loading SPL](https://www.denx.de/wiki/pub/U-Boot/MiniSummitELCE2013/tpl-presentation.pdf)

[Home · kexecboot/kexecboot Wiki](https://github.com/kexecboot/kexecboot/wiki) Kexecboot is a nice Linux-As-a-Bootloader implementation based on kexec.

[WebHome < U-Boot < DENX](https://www.denx.de/wiki/U-Boot)
[Das U-Boot - Wikiwand](https://www.wikiwand.com/en/Das_U-Boot)
[Introduction to the U-Boot bootloader - YouTube](https://www.youtube.com/watch?v=e6wlg9ntPVY)
[Embedded Linux Booting Process (Multi-Stage Bootloaders, Kernel, Filesystem) - YouTube](https://www.youtube.com/watch?v=DV5S_ZSdK0s)

[Lennart Talks Up systemd's SD-Boot + Boot Loader Specification - Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=ASG-2019-systemd-SD-Boot)

## Boot Partition

[Master boot record - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Master_boot_record)
[MBR (x86) - OSDev Wiki](<http://wiki.osdev.org/MBR_(x86)>)
[GUID Partition Table - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/GUID_Partition_Table)
[Make the most of large drives with GPT and Linux](http://www.ibm.com/developerworks/linux/library/l-gpt/index.html)
[Converting to or from GPT](http://www.rodsbooks.com/gdisk/mbr2gpt.html)

[FGA: What "boot" and "system" volumes are](http://homepage.ntlworld.com/jonathan.deboynepollard/FGA/boot-and-system-volumes.html)
[FGA: How operating systems determine the location of the system volume when bootstrapped](http://homepage.ntlworld.com/jonathan.deboynepollard/FGA/determining-system-volume.html)

## BIOS

[Arch boot process - ArchWiki](https://wiki.archlinux.org/index.php/Arch_boot_process)
[Boot with GRUB | Linux Journal](http://www.linuxjournal.com/article/4622)

Flash BIOS with bare motherboard:

- Flashback from Asus
- Q-Flash Plus from Gigabyte

### OpenBIOS

[OpenBIOS - Wikiwand](https://www.wikiwand.com/en/OpenBIOS)
[OpenBIOS](http://www.openfirmware.info/Welcome_to_OpenBIOS)
[Category:Free BIOS implementations - Wikipedia, the free encyclopedia](https://en.wikipedia.org/wiki/Category:Free_BIOS_implementations)

[coreboot](https://www.coreboot.org/) [coreboot - Wikiwand](https://www.wikiwand.com/en/Coreboot)
[Libreboot project](https://libreboot.org/)

### Fixing MBR

http://support.microsoft.com/kb/927392
http://windows7themes.net/how-to-fix-mbr-in-windows-7.html
http://www.tomshardware.com/news/win7-windows-7-mbr,10036.html
http://www.sevenforums.com/general-discussion/17521-how-fix-mbr-through-command-prompt.html
http://ubuntuforums.org/showthread.php?t=1014708

## Bootable USB key

Creating a bootable USB key in Linux is [straight forward](https://wiki.archlinux.org/index.php/USB_flash_installation_media).

```sh
sudo dd if=${iso} of=${usb device} bs=4M
# note: the package is gddrescue
sudo ddrescue ${iso} ${usb device} --force -D
```

[Useless Use Of dd – Vidar’s Blog](https://www.vidarholen.net/contents/blog/?p=479)
[Ddrescue - GNU Project - Free Software Foundation (FSF)](http://www.gnu.org/software/ddrescue/ddrescue.html) GNU ddrescue/gddrescue

[Multiboot USB drive - ArchWiki](https://wiki.archlinux.org/index.php/Multiboot_USB_drive#Workstation_live_medium)
[jsamr/bootiso: A bash script to securely create a bootable USB device from one ISO file. Just curl it, chmod it and go!](https://github.com/jsamr/bootiso)
See also my `iso2usb`.

Note some utils modify the partition label of the ISO, that can cause problem during bootup.

- [probonopd/SystemImageKit: Run (multiple) operating systems directly from image files. Add extensions, apps and configuration, which are one file each.](https://github.com/probonopd/SystemImageKit) multiple ISOs
- [Ventoy](https://www.ventoy.net/en/index.html) Windows, Linux, _support Windows ISO_, multiple ISOs
- [UNetbootin](http://unetbootin.github.io/) multiplatform, _support Windows ISO_  
  `unetbootin method=diskimage isofile="my.iso" installtype=USB targetdrive=/dev/sdc`
- [Etcher](https://etcher.io/) multiplatform
- [Rufus](https://rufus.ie/) Windows, fast, _support Windows ISO_
- [slacka/WoeUSB:](https://github.com/slacka/WoeUSB) _support Windows ISO_
- Linux Live USB Creator
- [Universal USB Installer](https://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/) Windows, wine, fast, _support Windows ISO_
- [YUMI - Multiboot USB Creator](https://www.pendrivelinux.com/yumi-multiboot-usb-creator/) Windows, wine, multiple ISOs
- Live USB Creator

Ventoy also supports [Persistence Plugin](https://www.ventoy.net/en/plugin_persistence.html), where you can define a image file for persistent storage (per ISO).

The Windows ISO cannot be `dd`-ed to USB flash. We must create a bootable NTFS partition then copy the contents over.

[The best places to find Windows 10 ISOs | Computerworld](https://www.computerworld.com/article/3269118/microsoft-windows/best-places-to-find-windows-10-isos.html)
[Download Windows USB/DVD Download Tool from Official Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=56485)
[ValdikSS/windows2usb: Windows 7/8/8.1/10 ISO to Flash Drive burning utility for Linux (MBR/GPT, BIOS/UEFI, FAT32/NTFS)](https://github.com/ValdikSS/windows2usb)

## PXEBoot

[What Is Network Booting (PXE) and How Can You Use It?](http://www.howtogeek.com/57601/what-is-network-booting-pxe-and-how-can-you-use-it/)
[Preboot Execution Environment - Wikiwand](https://www.wikiwand.com/en/Preboot_Execution_Environment)

## UEFI

POST -> UEFI -> Boot Manager (in UEFI) ->
UEFI application (in EFI System partition) -> Bootloader -> Kernel -> ...

[Unified Extensible Firmware Interface - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface)
[Unified Extensible Firmware Interface - ArchWiki](https://wiki.archlinux.org/index.php/Unified_Extensible_Firmware_Interface)
[rEFInd - ArchWiki](https://wiki.archlinux.org/index.php/REFInd)

[UEFI - OSDev Wiki](http://wiki.osdev.org/UEFI)
[FGA: The EFI boot process.](http://homepage.ntlworld.com/jonathan.deboynepollard/FGA/efi-boot-process.html)
[UEFI boot: how does that actually work, then?](https://www.happyassassin.net/2014/01/25/uefi-boot-how-does-that-actually-work-then/)
[UEFI - Install Guide - Manjaro Linux](https://wiki.manjaro.org/index.php?title=UEFI_-_Install_Guide)

[The Boot Loader Specification | systemd](https://systemd.io/BOOT_LOADER_SPECIFICATION)
[systemd-boot](https://www.freedesktop.org/wiki/Software/systemd/systemd-boot/)
[pop-os/kernelstub: A simple EFI boot manager manager for Linux](https://github.com/pop-os/kernelstub/)
[pbatard/uefi-ntfs: UEFI:NTFS - Boot NTFS partitions from UEFI](https://github.com/pbatard/uefi-ntfs)

[Linux on your laptop: A closer look at EFI boot options | ZDNet](https://www.zdnet.com/article/linux-on-your-laptop-a-closer-look-at-efi-boot-options/)
[Linux on your laptop: Here's what you need to know about UEFI firmware | ZDNet](https://www.zdnet.com/article/linux-on-your-laptop-heres-what-you-need-to-know-about-uefi-firmware/)

http://www.rodsbooks.com/refind/installing.html
`refind-efi`

### howtogeek.com

[HTG Explains: Learn How UEFI Will Replace Your PC’s BIOS](http://www.howtogeek.com/56958/htg-explains-how-uefi-will-replace-the-bios/)
[Beginner Geek: Hard Disk Partitions Explained](http://www.howtogeek.com/184659/beginner-geek-hard-disk-partitions-explained/)
[What’s the Difference Between GPT and MBR When Partitioning a Drive?](http://www.howtogeek.com/193669/whats-the-difference-between-gpt-and-mbr-when-partitioning-a-drive/)

### rodsbooks.com

[A BIOS to UEFI Transformation](https://www.rodsbooks.com/bios2uefi/index.html)
[Managing EFI Boot Loaders for Linux](http://www.rodsbooks.com/efi-bootloaders/)
[Linux on UEFI: A Quick Installation Guide](http://www.rodsbooks.com/linux-uefi/)
[The rEFInd Boot Manager](http://www.rodsbooks.com/refind/index.html)
[Managing EFI Boot Loaders for Linux: Dealing with Secure Boot](http://www.rodsbooks.com/efi-bootloaders/secureboot.html)

[Programming for EFI](http://www.rodsbooks.com/efi-programming/index.html)

### x86asm.net

[Introduction to UEFI](http://x86asm.net/articles/introduction-to-uefi/index.html)
[UEFI Programming - First Steps](http://x86asm.net/articles/uefi-programming-first-steps/index.html)
[UEFI Hypervisors - Winning the Race to Bare Metal](http://x86asm.net/articles/uefi-hypervisors-winning-the-race-to-bare-metal/index.html)

## Init System (pid 1)

[Linux PID 1 和 Systemd | | 酷 壳 - CoolShell](https://coolshell.cn/articles/17998.html)

### `init`/`sysvinit`

[init - Wikiwand](http://www.wikiwand.com/en/Init)

Originates from System V, the oldest and most widely used init system.
`init` is [LSB](http://refspecs.linuxfoundation.org/lsb.shtml)-compliant.
Debian switched to `systemd` in 2015 with [Debian 8 Jessie](http://arstechnica.com/information-technology/2015/05/debian-8-linuxs-most-reliable-distro-makes-its-biggest-change-since-1993/) and caused the [Devuan](https://devuan.org/) fork.

[sysv-rc-conf - Run-level configuration for SysV like init script links](http://sysv-rc-conf.sourceforge.net/) UI tool

https://github.com/Fleshgrinder/nginx-sysvinit-script  
https://github.com/JasonGiedymin/nginx-init-ubuntu

```sh
$ sudo update-rc.d
usage: update-rc.d [-n] [-f] <basename> remove
       update-rc.d [-n] <basename> defaults [NN | SS KK]
       update-rc.d [-n] <basename> start|stop NN runlvl [runlvl] [...] .
       update-rc.d [-n] <basename> disable|enable [S|2|3|4|5]
                -n: not really
                -f: force

The disable|enable API is not stable and might change in the future.
```

Examples:

```sh
sudo update-rc.d -f nginx remove
sudo update-rc.d nginx defaults
```

### `upstart`

> `upstart` is deprecated

[Upstart - Wikiwand](http://www.wikiwand.com/en/Upstart)
[upstart - event-based init daemon](http://upstart.ubuntu.com/)

Use `upstart` instead of `init.d` for Ubuntu:  
http://casear.chuto.tw/2013/05/31/upstart-setting-for-nginx-on-ubuntu/  
http://casear.chuto.tw/2013/05/31/upstart-setting-for-redis-on-ubuntu/

Ubuntu followed Debian's footstep and moved to `systemd` since [15.04](http://www.theregister.co.uk/2015/05/05/ubuntu_15_04_review/).

```sh
sudo service nginx status
sudo service nginx start
sudo service nginx stop
```

WordPress Upstart script example:

```
# /etc/init/docker-wordpress.conf
# assuming an image with `--name=docker-wordpress` has been created
description "Wordpress - example.com"
author "Doker Guru"
start on filesystem and started docker
stop on runlevel [!2345]
respawn
exec /usr/bin/docker start -a docker-wordpress
pre-stop exec /usr/bin/docker stop -a docker-wordpress
```

### `systemd`

> see `systemd.md`

### `Launchd`

used by MacOS

[Launchd: One Program to Rule them All - YouTube](https://www.youtube.com/watch?v=SjrtySM9Dns)
[About Daemons and Services](https://developer.apple.com/library/archive/documentation/MacOSX/Conceptual/BPSystemStartup/Chapters/Introduction.html)
