---
title: "File Systems"
date: 2015-05-20 12:14:46
categories:
  - linux
tags:
  - file-system
  - storage
toc: true
---

[File system - Wikiwand](http://www.wikiwand.com/en/File_system)
[List of file systems - Wikiwand](https://www.wikiwand.com/en/List_of_file_systems)

[Part I. File Systems](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Storage_Administration_Guide/part-file-systems.html)
[Virtual filesystems: Why we need them and how they work | Opensource.com](https://opensource.com/article/19/3/virtual-filesystems-linux)

> see `distributed-file-systems.md`

> TODO: add corruption info on NTFS and HFS+

## Well-known file systems

[Explaining File Systems: NTFS, exFAT, FAT32, ext4 & More - YouTube](https://www.youtube.com/watch?v=_h30HBYxtws)

[Be File System - Wikiwand](http://www.wikiwand.com/en/Be_File_System)
[exFAT - Wikiwand](http://www.wikiwand.com/en/ExFAT)
[ext4 - Wikiwand](http://www.wikiwand.com/en/Ext4)
[F2FS - Wikiwand](http://www.wikiwand.com/en/F2FS)
[HFS Plus - Wikiwand](http://www.wikiwand.com/en/HFS_Plus)
[NILFS - Wikiwand](http://www.wikiwand.com/en/NILFS)
[NTFS - Wikiwand](http://www.wikiwand.com/en/NTFS)

[marook/tagfs](https://github.com/marook/tagfs)
[NHFS - Nonhierarchical File System - 0815 Blog](https://rffr.de/nhfs-nonhierarchical-file-system/)

[The Smorgasbord of Linux File Systems, Part One: The Extended Family | Learning Tree Blog](https://blog.learningtree.com/the-smorgasbord-of-linux-file-systems-part-one-the-extended-family/)
[Linux File Systems Part Two: The XFS File System | Learning Tree Blog](https://blog.learningtree.com/linux-file-systems-part-two-the-xfs-file-system/)
[Linux File Systems: Heading Toward Btrfs | Learning Tree Blog](https://blog.learningtree.com/linux-file-systems-heading-toward-btrfs/)

[Why Do Removable Drives Still Use FAT32 Instead of NTFS?](https://www.howtogeek.com/177529/htg-explains-why-are-removable-drives-still-using-fat32-instead-of-ntfs/)

### Comparison

[Linux 4.0 Hard Drive Comparison With EXT4 / Btrfs / XFS / NTFS / NILFS2 / ReiserFS - Phoronix](http://www.phoronix.com/scan.php?page=article&item=linux-40-hdd&num=1)
[Linux 4.4 To 4.7 - EXT4 vs. F2FS vs. Btrfs Benchmarks - Phoronix](http://www.phoronix.com/scan.php?page=article&item=linux-44-47-fs&num=1)
[Linux 5.0 File-System Benchmarks: Btrfs vs. EXT4 vs. F2FS vs. XFS - Phoronix](https://www.phoronix.com/scan.php?page=article&item=linux-50-filesystems&num=1)
[Review EXT4 vs. Btrfs vs. XFS | Unixmen](http://www.unixmen.com/review-ext4-vs-btrfs-vs-xfs/)
[XFS vs ZFS | [H]ard|Forum](https://hardforum.com/threads/xfs-vs-zfs.1593111/)
[ZFS, BTRFS, XFS, EXT4 and LVM with KVM – a storage performance comparison](http://www.ilsistemista.net/index.php/virtualization/47-zfs-btrfs-xfs-ext4-and-lvm-with-kvm-a-storage-performance-comparison.html)
[XFS vs EXT4 – Comparing MongoDB Performance on AWS EC2](https://scalegrid.io/blog/xfs-vs-ext4-comparing-mongodb-performance-on-aws-ec2/) XFS is useful on high end systems with high speed disks

### bcachefs

[The bcachefs filesystem [LWN.net]](https://lwn.net/Articles/655366/)
[bcache - Wikiwand](https://www.wikiwand.com/en/Bcache)
[Bcachefs](https://bcache.evilpiepirate.org/Bcachefs/)

[Kent Overstreet is creating bcachefs - a next generation Linux filesystem | Patreon](https://www.patreon.com/bcachefs)

### Btrfs

[Btrfs - Wikiwand](http://www.wikiwand.com/en/Btrfs)

Btrfs is not stable for use outside a test system.
[btrfs Meltdown | LUP 87 | Jupiter Broadcasting](http://www.jupiterbroadcasting.com/80097/btrfs-meltdown-lup-87/)
[Churning Over Btrfs | LUP 88 | Jupiter Broadcasting](http://www.jupiterbroadcasting.com/80442/churning-over-btrfs-lup-88/)

### XFS

[XFS - Wikiwand](http://www.wikiwand.com/en/XFS)
[XFS: There and back ... and there again? [LWN.net]](http://lwn.net/Articles/638546/)

### ZFS

[ZFS - Wikiwand](http://www.wikiwand.com/en/ZFS)
ZFS provides bitrot protection.

[ZFS on Linux](http://zfsonlinux.org/)

[Create a ZFS volume on Ubuntu – JamesCoyle.net](http://www.jamescoyle.net/how-to/478-create-a-zfs-volume-on-ubuntu)

[From BFS to ZFS: past, present, and future of file systems | Ars Technica](http://arstechnica.com/gadgets/2008/03/past-present-future-file-systems/)
[Ars walkthrough: Using the ZFS next-gen filesystem on Linux | Ars Technica](http://arstechnica.com/information-technology/2014/02/ars-walkthrough-using-the-zfs-next-gen-filesystem-on-linux/2/)

[How ZFS continues to be better than btrfs — Rudd-O.com in English](https://rudd-o.com/linux-and-free-software/ways-in-which-zfs-is-better-than-btrfs)
[The ZFS Story: Clearing Up the Confusion - Datamation](http://www.datamation.com/data-center/the-zfs-story-clearing-up-the-confusion-1.html)
[Why I do not use ZFS as a file system for my NAS](http://louwrentius.com/why-i-do-not-use-zfs-as-a-file-system-for-my-nas.html) in 2011
[Why I Do Use ZFS as a File System for My NAS](http://louwrentius.com/why-i-do-use-zfs-as-a-file-system-for-my-nas.html) in 2015

[An Introduction to the Implementation of ZFS (part 1 of 2) - YouTube](https://www.youtube.com/watch?v=UP_JfUUmDZo)
[An Introduction to the Implementation of ZFS (part 2 of 2) - YouTube](https://www.youtube.com/watch?v=l-RCLgLxuSc)

### techniques/internals

[inode - Wikiwand](https://www.wikiwand.com/en/Inode)
[Intro to Inodes | Linux.org](http://www.linux.org/threads/intro-to-inodes.4130/)
[LINUX Understanding inodes - YouTube](https://www.youtube.com/watch?v=_6VJ8WfWI4k)
[Detailed Understanding Of Linux Inodes With Example](https://linoxide.com/linux-command/linux-inode/)
[inode and its structure in linux](https://www.slashroot.in/inode-and-its-structure-linux)
Check inode usage: `df -i`
[Is the file table in the filesystem or in memory? - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/21325/is-the-file-table-in-the-filesystem-or-in-memory)

[Hard and Soft Links in Linux - YouTube](https://www.youtube.com/watch?v=kYonC93SvpE)

[Intro to Extents | Linux.org](http://www.linux.org/threads/intro-to-extents.4131/)
[Journal File System | Linux.org](http://www.linux.org/threads/journal-file-system.4136/)
[Journaling file system - Wikiwand](http://www.wikiwand.com/en/Journaling_file_system)
[Direct I/O | Linux.org](http://www.linux.org/threads/direct-i-o.4230/)
[Extent (file systems) - Wikiwand](https://www.wikiwand.com/en/Extent_%28file_systems%29)

[Ext4 Wiki](https://ext4.wiki.kernel.org/index.php/Main_Page)

## Articles

[Bitrot and atomic COWs: Inside “next-gen” filesystems | Ars Technica](http://arstechnica.com/information-technology/2014/01/bitrot-and-atomic-cows-inside-next-gen-filesystems/)
[Microsoft introduces new robust “Resilient File System” for Windows Server 8 | Ars Technica](http://arstechnica.com/information-technology/2012/01/microsoft-introduces-new-robust-resilient-file-system-for-windows-server-8/)

## Linux LVM

[Logical Volume Manager (Linux) - Wikiwand](https://www.wikiwand.com/en/Logical_Volume_Manager_%28Linux%29)

[LVM - ArchWiki](https://wiki.archlinux.org/index.php/LVM)
[Software RAID and LVM - ArchWiki](https://wiki.archlinux.org/index.php/Software_RAID_and_LVM)

[Linux lvm - Logical Volume Manager](https://linuxconfig.org/linux-lvm-logical-volume-manager)
[The Linux Logical Volume Manager | Red Hat](https://www.redhat.com/magazine/009jul05/features/lvm2/)
[A Beginner's Guide To LVM](https://www.howtoforge.com/linux_lvm)
[LVM HOWTO](http://www.tldp.org/HOWTO/LVM-HOWTO/)
[How to Set Up LVM Physical Volumes | Learning Tree Blog](https://blog.learningtree.com/set-lvm-physical-volumes/)

[Cool Solutions: Recovering a Lost LVM Volume Disk](https://www.novell.com/coolsolutions/appnote/19386.html)
[Recovery of LVM partitions](http://www.softpanorama.org/Commercial_linuxes/LVM/recovery_of_lvm_partitions.shtml)
[Recovery of LVM partitions](http://www.softpanorama.org/Commercial_linuxes/LVM/recovery_of_lvm_partitions.shtml)

[Restoring LVM volumes | Jethro Carr](https://www.jethrocarr.com/2013/11/23/restoring-lvm-volumes/)

## Mhddfs

[mhddfs: join several filesystems together to form a single larger one - rm's homepage](https://romanrm.net/mhddfs)
[Mhddfs - Combine Several Smaller Partition into One Large Virtual Storage](http://www.tecmint.com/combine-partitions-into-one-in-linux-using-mhddfs/)
[Install & Configure MHDDFS Virtual Storage Pool | DominicM](http://dominicm.com/install-and-configure-mhddfs-virtual-storage-pool/)
[Why I ditched RAID and Greyhole for MHDDFS | Zorn Software](http://zornsoftware.codenature.info/blog/why-i-ditched-raid-and-greyhole-for-mhddfs.html)

[Install MHDDFS on Arch Linux | DominicM](http://dominicm.com/install-configure-mhddfs-on-arch-linux/)

## > 2TB partition

http://www.thegeekstuff.com/2011/09/parted-command-examples/
http://www.systutorials.com/46294/making-gpt-partition-table-and-creating-partitions-with-parted-on-linux/
http://www.thegeekstuff.com/2012/08/2tb-gtp-parted/
