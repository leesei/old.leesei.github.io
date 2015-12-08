title: "Storage"
date: 2015-05-11 17:09:10
categories:
- comp.hardware
tags:
- ssd
- harddisk
- storage
toc: true
---

## Platters Drive

[Western Digital Green vs. Red Hard Drives - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/Western-Digital-Green-vs-Red-Hard-Drives-602/)

Cable doesn't matter:
[SATA 3Gb/s vs. 6Gb/s Cable Performance (Revisited) - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/SATA-3Gb-s-vs-6Gb-s-Cable-Performance-Revisited-183/)

Platters of traditional maganetic disks are divided into tracks (rings), then into sectors. Sectors are grouped into block and given addresses.
> how about cylinders, heads or sectors?

Data is written on blocks. So the minimum space a file takes up is (sector size * block size).

Ext4 defined "Extens" on block 

## SSD

[Solid-state storage - Wikiwand](http://www.wikiwand.com/en/Solid-state_storage)
[Solid-state revolution: in-depth on how SSDs really work | Ars Technica](http://arstechnica.com/information-technology/2012/06/inside-the-ssd-revolution-how-solid-state-disks-really-work/)
[How SSDs Work - Intel X25-M SSD: Intel Delivers One of the World's Fastest Drives](http://www.anandtech.com/show/2614/2)
[The SSD Anthology: Understanding SSDs and New Drives from OCZ](http://www.anandtech.com/print/2738)
[The SSD Relapse: Understanding and Choosing the Best SSD](http://anandtech.com/print/2829)
[SSD ABC Guide – OCZ Forum](http://oczforum.com/staff/meander/OCZ_SSD_ABC_Guide.pdf)

Cells stores the bits (1 per cell for SLC, 2 for MLC, 3 for [TLC](http://www.anandtech.com/show/5067/understanding-tlc-nand)). Beware that Samsung's 840 series (using TLC) have [performance degradation](http://www.techspot.com/article/997-samsung-ssd-read-performance-degradation/) problem.  
Cells are then organized into pages, then pages into blocks.  
Writes is done on pages and erase is done on blocks.

[Consistent Performance: A Reality? - The Intel SSD DC S3700 (200GB) Review](http://www.anandtech.com/show/6433/intel-ssd-dc-s3700-200gb-review/3)
[Researchers publish first large-scale, in-field SSD reliability report - TechSpot](http://www.techspot.com/news/61090-researchers-publish-first-large-scale-field-ssd-reliability.html)
[How NAND flash degrades and what vendors do to increase SSD endurance](http://searchsolidstatestorage.techtarget.com/podcast/How-NAND-flash-degrades-and-what-vendors-do-to-increase-SSD-endurance)

[Samsung's 850 Pro solid-state drive reviewed - The Tech Report](http://techreport.com/review/26701/samsung-850-pro-solid-state-drive-reviewed) (V-NAND flash)
[From The Wirecutter: The best consumer-grade SSD (for most people) | Ars Technica](http://arstechnica.com/gadgets/2015/04/from-the-wirecutter-the-best-consumer-grade-ssd-for-most-people/)

### Alignment

[Aligning an SSD on Linux » Cygon's Blog](http://blog.nuclex-games.com/2009/12/aligning-an-ssd-on-linux/)
[Solid State Drive (SSD) – Info and Alignment | Linux.org](http://www.linux.org/threads/solid-state-drive-ssd-%E2%80%93-info-and-alignment.6572/)

### Trim

[Trim (computing) - Wikiwand](http://www.wikiwand.com/en/Trim_%28computing%29)
[Garbage Collection and TRIM in SSDs Explained - An SSD Primer | The SSD Review](http://www.thessdreview.com/daily-news/latest-buzz/garbage-collection-and-trim-in-ssds-explained-an-ssd-primer/)

### ADATA SP-920 256GB

Launch: 2014-04
NAND: Micron 128Gbit 20nm Sync MLC
Controller: Marvell

It's actually a re-branded Crucial M550.

[Premier Pro SP920 Series Solid State Drive_Premier Pro_Solid State Drives_Products_ADATA Technology](http://www.adata.com/us/ssd/feature/286)
[ADATA SP920 (128GB, 256GB, 512GB & 1TB) Review](http://www.anandtech.com/show/7908/adata-sp920-128gb-256gb-512gb-1tb-review)
[Crucial M550 Review: 128GB, 256GB, 512GB and 1TB Models Tested](http://www.anandtech.com/show/7864/crucial-m550-review-128gb-256gb-512gb-and-1tb-models-tested)
[Marvell 主控、效能更優勝 ADATA SP920 固態硬碟 - 電腦領域 HKEPC Hardware - 全港 No.1 PC網站](http://www.hkepc.com/11176)

### Linux setup

> move to linux-{desktop,setup}.md?

[SSDOptimization - Debian Wiki](https://wiki.debian.org/SSDOptimization)
[Solid State Drives - ArchWiki](https://wiki.archlinux.org/index.php/Solid_State_Drives)
[Techblog » Blog Archive » How to check TRIM is working on your SSD running Linux](http://andyduffell.com/techblog/?p=852)
[How to properly activate TRIM for your SSD on Linux: fstrim, lvm and dm-crypt | synaptic fault](http://blog.neutrino.es/2013/howto-properly-activate-trim-for-your-ssd-on-linux-fstrim-lvm-and-dmcrypt/)

mount with 'discard' and 'noatime' option in `/etc/fstab`
use anacron to schedule a weekly `fstrim`
add udev rule to set I/O scheduler to `noop` or `deadline`

```sh
#!/bin/sh
#
# To find which FS support trim, we check that DISC-MAX (discard max bytes)
# is great than zero. Check discard_max_bytes documentation at
# https://www.kernel.org/doc/Documentation/block/queue-sysfs.txt
#
for fs in $(lsblk -o MOUNTPOINT,NAME,DISC-MAX,FSTYPE | grep -E '^/.* [1-9]+.* ' | awk '{print $1}'); do
    fstrim "$fs"
done
```

## Benchmarking/Info

```sh
# perform speed test
sudo hdparm -t /dev/sda
sudo hdparm -I /dev/sda
```

```sh
sudo smartctl -a /dev/sda
```

```
# read speed benchmark
sudo dd if=/dev/sdX1 of=/dev/zero bs=1M count=400 iflag=direct
# write speed benchmark
sudo dd if=/dev/zero of=/dev/sdX1 bs=1M count=400 skip=1000 oflag=direct
```

GNOME Disk has built-in benchmarking feature.

[SSD Benchmarking - ArchWiki](https://wiki.archlinux.org/index.php/SSD_Benchmarking)

## Interface

### Parallel ATA

This is obsolete.

[Parallel ATA - Wikiwand](http://www.wikiwand.com/en/Parallel_ATA)

### SATA

[Serial ATA - Wikiwand](http://www.wikiwand.com/en/Serial_ATA)

### M.2

Replaces mSATA.

[M.2 - Wikiwand](http://www.wikiwand.com/en/M.2)
[Understanding M.2, the interface that will speed up your next SSD | Ars Technica](http://arstechnica.com/gadgets/2015/02/understanding-m-2-the-interface-that-will-speed-up-your-next-ssd/)

### USB

[USB in a NutShell](http://www.beyondlogic.org/usbnutshell/usb1.shtml)

[Faster USB 3.0 Performance: Examining UASP And Turbo Mode](http://www.tomshardware.com/print/usb-3-uas-turbo,reviews-3215.html)



