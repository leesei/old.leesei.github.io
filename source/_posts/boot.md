title: "Boot"
date: 2015-05-10 22:07:17
categories:
- linux
tags:
- desktop
toc: true
---

[System Initialization (x86) - OSDev Wiki](http://wiki.osdev.org/System_Initialization_(x86))
[Linux startup process - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Linux_startup_process)
[Arch boot process - ArchWiki](https://wiki.archlinux.org/index.php/Arch_boot_process)
[Inside the Linux boot process](http://www.ibm.com/developerworks/linux/library/l-linuxboot/)

[Some basics of MBR v/s GPT and BIOS v/s UEFI - Manjaro Linux](https://wiki.manjaro.org/index.php?title=Some_basics_of_MBR_v/s_GPT_and_BIOS_v/s_UEFI)

## Boot Partition

[Master boot record - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Master_boot_record)
[MBR (x86) - OSDev Wiki](http://wiki.osdev.org/MBR_(x86))
[GUID Partition Table - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/GUID_Partition_Table)
[Make the most of large drives with GPT and Linux](http://www.ibm.com/developerworks/linux/library/l-gpt/index.html)
[Converting to or from GPT](http://www.rodsbooks.com/gdisk/mbr2gpt.html)

[FGA: What "boot" and "system" volumes are](http://homepage.ntlworld.com/jonathan.deboynepollard/FGA/boot-and-system-volumes.html)
[FGA: How operating systems determine the location of the system volume when bootstrapped](http://homepage.ntlworld.com/jonathan.deboynepollard/FGA/determining-system-volume.html)

## BIOS

POST -> BIOS -> MBR of boot partition -> Bootloader -> Kernel -> 
[`init`](https://wiki.archlinux.org/index.php/Init)/[`systemd`](https://wiki.archlinux.org/index.php/Systemd) -> shell/display manager -> `startx`/`xinit` -> DE

[Arch boot process - ArchWiki](https://wiki.archlinux.org/index.php/Arch_boot_process)
[Boot with GRUB | Linux Journal](http://www.linuxjournal.com/article/4622)

### Fixing MBR

http://support.microsoft.com/kb/927392
http://windows7themes.net/how-to-fix-mbr-in-windows-7.html
http://www.tomshardware.com/news/win7-windows-7-mbr,10036.html
http://www.sevenforums.com/general-discussion/17521-how-fix-mbr-through-command-prompt.html
http://ubuntuforums.org/showthread.php?t=1014708

## UEFI

POST -> UEFI -> Boot Manager (in UEFI) -> 
UEFI application (in EFI System partition) -> Bootloader -> Kernel -> ...

[Unified Extensible Firmware Interface - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface)
[Unified Extensible Firmware Interface - ArchWiki](https://wiki.archlinux.org/index.php/Unified_Extensible_Firmware_Interface)
[rEFInd - ArchWiki](https://wiki.archlinux.org/index.php/REFInd)

[UEFI - OSDev Wiki](http://wiki.osdev.org/UEFI)
[FGA: The EFI boot process.](http://homepage.ntlworld.com/jonathan.deboynepollard/FGA/efi-boot-process.html)
[UEFI boot: how does that actually work, then?](https://www.happyassassin.net/2014/01/25/uefi-boot-how-does-that-actually-work-then/)

### howtogeek.com

[HTG Explains: Learn How UEFI Will Replace Your PC’s BIOS](http://www.howtogeek.com/56958/htg-explains-how-uefi-will-replace-the-bios/)
[Beginner Geek: Hard Disk Partitions Explained](http://www.howtogeek.com/184659/beginner-geek-hard-disk-partitions-explained/)
[What’s the Difference Between GPT and MBR When Partitioning a Drive?](http://www.howtogeek.com/193669/whats-the-difference-between-gpt-and-mbr-when-partitioning-a-drive/)

### rodsbooks.com

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

### init

[init - Wikiwand](http://www.wikiwand.com/en/Init)

Originates from System V, the oldest and most widely used init system.

### upstart

[Upstart - Wikiwand](http://www.wikiwand.com/en/Upstart)
[upstart - event-based init daemon](http://upstart.ubuntu.com/)

### systemd

[systemd - Wikiwand](http://www.wikiwand.com/en/Systemd)
[systemd - freedesktop.org](http://www.freedesktop.org/wiki/Software/systemd/)
[TipsAndTricks](http://www.freedesktop.org/wiki/Software/systemd/TipsAndTricks/)

System services are written in `.service` files, located in:
```
/usr/lib/systemd/system

ln -s '/usr/lib/systemd/system/teamviewerd.service' '/etc/systemd/system/graphical.target.wants/teamviewerd.service'
```

[Archlinux, systemd-free](http://systemd-free.org/)
[Systemd Essentials: Working with Services, Units, and the Journal | DigitalOcean](https://www.digitalocean.com/community/tutorials/systemd-essentials-working-with-services-units-and-the-journal)

```
systemd-ui
systemctl
systemd-analyze
```

### from Lennart Poettering

[Why systemd?](http://0pointer.de/blog/projects/why.html)
[The Biggest Myths](http://0pointer.de/blog/projects/the-biggest-myths.html)
[systemd journal](https://docs.google.com/document/pub?id=1IC9yOXj7j6cdLLxWEBAGRL6wl97tFxgjLUEHIX3MSTs)

#### systemd for Developers

[systemd for Developers I](http://0pointer.net/blog/projects/socket-activation.html)
[systemd for Developers II](http://0pointer.net/blog/projects/socket-activation2.html)
[systemd for Developers III](http://0pointer.net/blog/projects/journal-submit.html)

#### systemd for Administrators

> TODO:
> http://0pointer.net/blog/archives.html
> select "systemd for Administrators" and generate links

[systemd for Administrators, Part 1](http://0pointer.net/blog/projects/systemd-for-admins-1.html)
[systemd for Administrators, Part II](http://0pointer.net/blog/projects/systemd-for-admins-2.html)
[systemd for Administrators, Part III](http://0pointer.net/blog/projects/systemd-for-admins-3.html)
....
[systemd For Administrators, Part XXI](http://0pointer.net/blog/systemd-for-administrators-part-xxi.html)
