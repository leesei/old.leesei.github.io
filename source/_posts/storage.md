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

## HDD

[Western Digital Green vs. Red Hard Drives - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/Western-Digital-Green-vs-Red-Hard-Drives-602/)

Cable doesn't matter:
[SATA 3Gb/s vs. 6Gb/s Cable Performance (Revisited) - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/SATA-3Gb-s-vs-6Gb-s-Cable-Performance-Revisited-183/)

Platters of traditional maganetic disks are divided into tracks (rings), then into sectors. Sectors are grouped into block and given addresses.
> how about cylinders, heads or sectors?

Data is written on blocks. So the minimum space a file takes up is (sector size * block size).

Ext4 defined "Extens" on block 

## SSD

[How SSDs Work - Intel X25-M SSD: Intel Delivers One of the World's Fastest Drives](http://www.anandtech.com/show/2614/2)
[The SSD Anthology: Understanding SSDs and New Drives from OCZ](http://www.anandtech.com/print/2738)
[The SSD Relapse: Understanding and Choosing the Best SSD](http://anandtech.com/print/2829)

Cells stores the bits (1 per cell for SLC, 2 for MLC, 3 for [TLC](http://www.anandtech.com/show/5067/understanding-tlc-nand)). Beware that Samsung's 840 serie (using TLC) have [performance degradation](http://www.techspot.com/article/997-samsung-ssd-read-performance-degradation/) problem.  
Cells are then organized into pages, then pages into blocks.  
Writes is done on pages and erase is done on blocks.

[SSD ABC Guide – OCZ Forum](http://oczforum.com/staff/meander/OCZ_SSD_ABC_Guide.pdf)

[Consistent Performance: A Reality? - The Intel SSD DC S3700 (200GB) Review](http://www.anandtech.com/show/6433/intel-ssd-dc-s3700-200gb-review/3)

[Researchers publish first large-scale, in-field SSD reliability report - TechSpot](http://www.techspot.com/news/61090-researchers-publish-first-large-scale-field-ssd-reliability.html)

[How NAND flash degrades and what vendors do to increase SSD endurance](http://searchsolidstatestorage.techtarget.com/podcast/How-NAND-flash-degrades-and-what-vendors-do-to-increase-SSD-endurance)

### Alignment

[Aligning an SSD on Linux » Cygon's Blog](http://blog.nuclex-games.com/2009/12/aligning-an-ssd-on-linux/)
[Solid State Drive (SSD) – Info and Alignment | Linux.org](http://www.linux.org/threads/solid-state-drive-ssd-%E2%80%93-info-and-alignment.6572/)

### Trim

[Trim (computing) - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Trim_(computing))
[Garbage Collection and TRIM in SSDs Explained - An SSD Primer | The SSD Review](http://www.thessdreview.com/daily-news/latest-buzz/garbage-collection-and-trim-in-ssds-explained-an-ssd-primer/)

### ADATA SP-920 256GB

Launch: 2014-04
NAND: Micron 128Gbit 20nm Sync MLC
Controller: Marvell

It's actually a rebranded Crucial M550.

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

[SSD Benchmarking - ArchWiki](https://wiki.archlinux.org/index.php/SSD_Benchmarking)

