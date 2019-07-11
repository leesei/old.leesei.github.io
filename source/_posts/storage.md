---
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

[A history of storage media](https://codewords.recurse.com/issues/seven/a-history-of-storage-media)

## Platters Drive

[Hard Drive Test Data - Determining Failure Rates and More](https://www.backblaze.com/b2/hard-drive-test-data.html)

[Western Digital Green vs. Red Hard Drives - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/Western-Digital-Green-vs-Red-Hard-Drives-602/)

Cable doesn't matter:
[SATA 3Gb/s vs. 6Gb/s Cable Performance (Revisited) - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/SATA-3Gb-s-vs-6Gb-s-Cable-Performance-Revisited-183/)

Platters of traditional magnetic disks are divided into tracks (rings), then into sectors. Sectors are grouped into block and given addresses.

> how about cylinders, heads or sectors?

Data is written on blocks. So the minimum space a file takes up is (sector size \* block size).

[Solid State vs. Hard Disk: Differences Between SSD and HDD](https://www.backblaze.com/blog/hdd-versus-ssd-whats-the-diff/)

## SSD

[Solid-state storage - Wikiwand](http://www.wikiwand.com/en/Solid-state_storage)
[Solid-state revolution: in-depth on how SSDs really work | Ars Technica](http://arstechnica.com/information-technology/2012/06/inside-the-ssd-revolution-how-solid-state-disks-really-work/)
[How SSDs Work - Intel X25-M SSD: Intel Delivers One of the World's Fastest Drives](http://www.anandtech.com/show/2614/2)
[The SSD Anthology: Understanding SSDs and New Drives from OCZ](http://www.anandtech.com/print/2738)
[The SSD Relapse: Understanding and Choosing the Best SSD](http://anandtech.com/print/2829)
[How Do SSDs Work? - ExtremeTech](https://www.extremetech.com/extreme/210492-extremetech-explains-how-do-ssds-work)
[SSD ABC Guide – OCZ Forum](http://oczforum.com/staff/meander/OCZ_SSD_ABC_Guide.pdf) PDF
[How Do SSDs Work? - ExtremeTech](https://www.extremetech.com/extreme/210492-extremetech-explains-how-do-ssds-work)

[Buying a Solid State Drive (SSD): Everything You Need to Know - YouTube](https://www.youtube.com/watch?v=aBfJsoc8zzk)

[SSDs - Latest Articles and Reviews on AnandTech](https://www.anandtech.com/tag/ssd)
[Best SSDs: Q1 2019](https://www.anandtech.com/show/9799/best-ssds)
[Best SSD 2019: Solid State Drives - Tech Advisor](https://www.techadvisor.co.uk/test-centre/storage/best-ssd-3235200/)
[How to Buy the Right SSD: A Guide for 2019](https://www.tomshardware.com/reviews/ssd-buying-guide,5602.html)
[Best SSDs 2019: SATA, PCIe, and Add-in Cards](https://www.tomshardware.com/reviews/best-ssds,3891.html)
[Sean's SSD Buyers Guide & Information Thread](http://www.overclock.net/t/1179518/seans-ssd-buyers-guide-information-thread)
[Best SSDs for 2019 - CNET](https://www.cnet.com/topics/storage/best-hard-drives-and-storage/ssd/)

[Enterprise versus Client SSD](http://www.kingston.com/en/ssd/enterprise/best_practices/enterprise_versus_client_ssd)
[Solid state / SSD news, tips and information – SearchSolidStateStorage.com](http://searchsolidstatestorage.techtarget.com/)
[Solid State Drive SSD Preturi, Oferte, Solid State Drive SSD Magazine, Solid State Drive SSD ieftine](https://solid-state-drive-ssd.compari.ro/)
[SSD UserBenchmarks - 994 Solid State Drives Compared](https://ssd.userbenchmark.com/)
[From The Wirecutter: The best consumer-grade SSD (for most people) | Ars Technica](http://arstechnica.com/gadgets/2015/04/from-the-wirecutter-the-best-consumer-grade-ssd-for-most-people/)

[SSD: how to optimize your Solid State Drive for Linux Mint 17.3, Ubuntu 14.04 and Debian - Easy Linux tips project](https://sites.google.com/site/easylinuxtipsproject/ssd)

### NAND Cell

Cells stores the bits (1 per cell for SLC, 2 for MLC, 3 for [TLC](http://www.anandtech.com/show/5067/understanding-tlc-nand)). Beware that Samsung's 840 series (using TLC) have [performance degradation](http://www.techspot.com/article/997-samsung-ssd-read-performance-degradation/) problem.
Cells are then organized into pages, then pages into blocks.
Writes is done on pages and erase is done on blocks.

Samsung's 850 series and Crucial MX300 uses 3D NAND technology that improves performance and durability and overcome density limits of planar NAND.
[Samsung's 850 Pro solid-state drive reviewed - The Tech Report](http://techreport.com/review/26701/samsung-850-pro-solid-state-drive-reviewed) (V-NAND flash)

Crucial uses free unused NAND in SLC mode as write buffer to speed up writes (Dynamic Write Acceleration).

[What’s the difference between SLC, MLC and TLC? - Answers - UserBenchmark](http://www.userbenchmark.com/Faq/What-s-the-difference-between-SLC-MLC-and-TLC/107)
[What’s the difference between NAND and V-NAND? - Answers - UserBenchmark](http://www.userbenchmark.com/Faq/What-s-the-difference-between-NAND-and-V-NAND/104)
[SSD Life Expectancy - YouTube](https://www.youtube.com/watch?v=-XZNr7mS0iw)
[How SSD Technology Keeps Getting WORSE! - Intel 660p Review - YouTube](https://www.youtube.com/watch?v=OffzVc7ZB-o) Quad-bit per cell
[3D NAND technology: What it is and where it's headed](https://searchstorage.techtarget.com/essentialguide/3D-NAND-technology-What-it-is-and-where-its-headed)

### Controller

[SSD 的核心!! Marvell v.s SandForce Controller 大對決 (下) - 小 P 的 SSD 秘密實驗室](https://www.facebook.com/notes/plextor-台灣/ssd的核心-marvell-vs-sandforce-controller-大對決-下-小p的ssd秘密實驗室/406211976056515)

LSI SandForce controllers will compress data before writing to NAND to enhance data rate and enhance SSD life.
[Technical Brief - What is DuraWrite | Kingston](http://www.kingston.com/en/ssd/enterprise/technical_brief/what_is_durawrite)

[Silicon Motion SM2258 Technical Preview With Micron 3D TLC - Tom's Hardware](https://www.tomshardware.com/reviews/silicon-motion-sm2258-micron-3d-preview,4698.html)

### Degradation

[Consistent Performance: A Reality? - The Intel SSD DC S3700 (200GB) Review](http://www.anandtech.com/show/6433/intel-ssd-dc-s3700-200gb-review/3)
[Researchers publish first large-scale, in-field SSD reliability report - TechSpot](http://www.techspot.com/news/61090-researchers-publish-first-large-scale-field-ssd-reliability.html)
[How NAND flash degrades and what vendors do to increase SSD endurance](http://searchsolidstatestorage.techtarget.com/podcast/How-NAND-flash-degrades-and-what-vendors-do-to-increase-SSD-endurance)

### Alignment

Alignment used to an issue years ago, but no longer.

[Aligning an SSD on Linux » Cygon's Blog](http://blog.nuclex-games.com/2009/12/aligning-an-ssd-on-linux/)
[Solid State Drive (SSD) – Info and Alignment | Linux.org](http://www.linux.org/threads/solid-state-drive-ssd-%E2%80%93-info-and-alignment.6572/)

### Trim

[Trim (computing) - Wikiwand](http://www.wikiwand.com/en/Trim_%28computing%29)
[Garbage Collection and TRIM in SSDs Explained - An SSD Primer | The SSD Review](http://www.thessdreview.com/daily-news/latest-buzz/garbage-collection-and-trim-in-ssds-explained-an-ssd-primer/)

### ADATA SP-920 256GB

Launch: 2014-04
NAND: Micron 128Gbit 20nm Sync Planar MLC
Controller: Marvell

It's actually a re-branded Crucial M550.

[Premier Pro SP920 Series Solid State Drive_Premier Pro_Solid State Drives_Products_ADATA Technology](http://www.adata.com/us/ssd/feature/286)
[ADATA SP920 (128GB, 256GB, 512GB & 1TB) Review](http://www.anandtech.com/show/7908/adata-sp920-128gb-256gb-512gb-1tb-review)
[Crucial M550 Review: 128GB, 256GB, 512GB and 1TB Models Tested](http://www.anandtech.com/show/7864/crucial-m550-review-128gb-256gb-512gb-and-1tb-models-tested)
[Marvell 主控、效能更優勝 ADATA SP920 固態硬碟 - 電腦領域 HKEPC Hardware - 全港 No.1 PC 網站](http://www.hkepc.com/11176)

### Adata Ultimate

Launch: 2016
NAND: Micron 384Gbit 3D TLC + SLC Cache (1/3) + DRAM Cache
Controller: SMI SM2258

[Adata's Ultimate SU900 Brings SLC Buffers To 3D MLC SSDs](https://www.tomshardware.com/news/adata-ultimate-su900-tlc-mlc,33183.html)
[Adata Ultimate SU800 SSD Review - Tom's Hardware](https://www.tomshardware.com/reviews/adata-ultimate-su800-ssd-review,4824.html) not so "ultimate" at all

[Ultimate SU800 SSD | ADATA Consumer](https://www.adata.com/us/feature/410) 256G \$580

### Samsung

[Samsung 970 EVO Plus SSD: Improved performance and efficiencies | ZDNet](https://www.zdnet.com/article/samsung-970-evo-plus-ssd-improved-performance-and-efficiencies/)

[Samsung 860 Evo review: New SSD has Upgraded Performace & Life - Tech Advisor](https://www.techadvisor.co.uk/review/ssd-hard-drives/samsung-860-evo-review-3670806/)
Interface: SATA
Memory Cache: 512MB LPDDR4
Controller: Samsung MJX Controller
Encryption: AES 256-bit
Flash technology: Samsung V-NAND 3bit MLC

250G $365 500G $568

### Verbatim

Interface: SATA
Flash technology: 3D TLC
Controller: Phison PS3111

[Vi550 S3 SSD 512GB\* | Verbatim Online Shop](https://www.verbatim-europe.co.uk/en/prod/vi550-s3-ssd-512gb-49352/)
[Solid State Drives](https://www.verbatim.com/prod/ssd/vi550-sata-iii-2.5-internal-ssds/512gb-vi550-sata-iii-2.5-internal-ssd-sku-49352/)

Vi550 256G $229 512G $378

### SanDisk

SanDisk SSD Plus 240G $275 480G $510
SanDisk SSD Ultra 250G $460 500G $680

### Crucial

[Crucial MX500 Review - Tech Advisor](https://www.techadvisor.co.uk/review/ssd-hard-drives/crucial-mx500-review-3670490/)
Interface: SATA
Controller: Silicon Motion SM2258
Encryption: AES 256-bit
Flash technology: Micron 2nd Generation 64-layer 3D TLC NAND

250G $395 500G $535

### Kingston

[Kingston UV500 Review: The First SSD with 4-bit V-NAND - Tech Advisor](https://www.techadvisor.co.uk/review/ssd-hard-drives/kingston-uv500-3690331/)
Interface: SATA
Controller: Marvell 88SS1074
Flash technology: TOSHIBA 15nm Toogle 3D TLC + SLC Cache (1/16)

120G \$298

[UV500 2.5”/m.2/mSATA SSD – 120GB–960GB | Kingston](https://www.kingston.com/us/ssd/consumer/suv500)
[Kingston UV500 Review: The First SSD with 4-bit V-NAND - Tech Advisor](https://www.techadvisor.co.uk/review/ssd-hard-drives/kingston-uv500-3690331/)
[搶攻舊機升級市場 Kingston UV500 系列 SATA SSD - 電腦領域 HKEPC Hardware - 全港 No.1 PC 網站](https://www.hkepc.com/16817/%E6%90%B6%E6%94%BB%E8%88%8A%E6%A9%9F%E5%8D%87%E7%B4%9A%E5%B8%82%E5%A0%B4_Kingston_UV500_%E7%B3%BB%E5%88%97_SATA_SSD)

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

## 3D XPoint/Optane

[Intel® Optane™ Technology](https://www.intel.com/content/www/us/en/architecture-and-technology/intel-optane-technology.html)
[3D XPoint memory: NAND flash killer or DRAM replacement? | InfoWorld](http://www.infoworld.com/article/3194348/flash-storage/3d-xpoint-memory-nand-flash-killer-or-dram-replacement.html)
[What is 3D XPoint and how fast is it? - Answers - UserBenchmark](http://www.userbenchmark.com/Faq/What-is-3D-XPoint-and-how-fast-is-it/106)

[What is Intel Optane? - YouTube](https://www.youtube.com/watch?v=WwH5Q8ZFJvw)

[The Intel Optane Memory H10 Review: QLC and Optane In One SSD - Print View](https://www.anandtech.com/print/14249/the-intel-optane-memory-h10-review-two-ssds-in-one)
[A Frankenstein SSD - Intel Optane Memory H10 EXPLAINED! - YouTube](https://www.youtube.com/watch?v=Ch-OPEDMoxk)

### Optane Memory

> using Optane as HDD cache, on Intel platform only

[Intel® Optane™ memory—Revolutionary Memory](https://www.intel.com/content/www/us/en/architecture-and-technology/optane-memory.html)
[Intel Optane Memory: everything you need to know | PC Gamer](https://www.pcgamer.com/intel-optane-memory-everything-you-need-to-know/)

## Flash

[SD Memory Card Formatter - SD Association](https://www.sdcard.org/downloads/formatter_4/)
[Speed Class - SD Association](https://www.sdcard.org/developers/overview/speed_class/)
[5 Mistakes to Avoid When Buying a MicroSD Card](https://www.makeuseof.com/tag/5-mistakes-avoid-buying-next-microsd-card/)

[The Best microSD Cards: Reviews by Wirecutter | A New York Times Company](https://thewirecutter.com/reviews/best-microsd-card/)
[The partition is not resized to full SD card size. - Allwinner A20 - Armbian forum](https://forum.armbian.com/topic/3776-the-partition-is-not-resized-to-full-sd-card-size/?tab=comments#comment-27413)

### Counterfeit Flash

[4 Tools to Test and Detect Fake or Counterfeit USB Flash Drives • Raymond.CC](https://www.raymond.cc/blog/test-and-detect-fake-or-counterfeit-usb-flash-drives-bought-from-ebay-with-h2testw/)
[How to Spot a Fake MicroSD Card and Avoid Being Scammed](https://www.makeuseof.com/tag/how-to-spot-fake-microsd-card/)

[F3 by Digirati](http://oss.digirati.com.br/f3/)
[f3 - Fight Flash Fraud — f3 documentation](https://fight-flash-fraud.readthedocs.io/en/stable/introduction.html)
`sudo f3probe --destructive --time-ops /dev/sdf`

[H2testw – best sd memory card speed tester for Windows (how to use & download)](https://howtorecover.me/h2testw-memory-card-tester)
[07 - All about 'Fake' SD cards and USB Flash drives - RMPrepUSB](https://www.rmprepusb.com/tutorials/-fake-usb-flash-memory-drives) FakeFlashTest, Windows

[Flash Drive/Card Tester - Check your USB flash drives and memory cards for errors](https://www.ricksdailytips.com/flash-drive-card-tester/) [USB Flash Drive Tester](https://www.vconsole.com/download), Windows

### UFS

[Universal Flash Storage - Wikiwand](https://www.wikiwand.com/en/Universal_Flash_Storage)

### eMMC

SSD > eMMC > SD
SSD: R:500MB W: 100MB
eMMC R: 280MB W: 45MB
SD R: 100MB W: 100MB

[eMMC vs. SSD: Not All Solid-State Storage is Equal](http://www.howtogeek.com/196541/emmc-vs.-ssd-not-all-solid-state-storage-is-equal/)
[eMMC vs SD Cards | Panasonic Industrial Devices](https://na.industrial.panasonic.com/blog/emmc-vs-sd-cards)
[What is eMMC Memory – software support | Reliance Nitro | Datalight](https://www.datalight.com/solutions/technologies/emmc/what-is-emmc)

## Benchmarking/Info

```sh
# info
sudo hdparm -I /dev/sda
### THIS is destructive ###
# read speed test
sudo hdparm -t /dev/sda
sudo hdparm -Tt /dev/sda
```

```sh
# read speed benchmark
sudo dd if=/dev/sdX1 of=/dev/zero bs=1M count=400 iflag=direct
echo 3 | sudo tee /proc/sys/vm/drop_caches  # clear cache first
sudo dd if=/dev/zero of=/dev/sdX1 bs=1M count=400 skip=1000 conv=fdatasync
```

[USB UserBenchmarks - 639 USB Flash Drives Compared](http://usb.userbenchmark.com/)
[SSD UserBenchmarks - 929 Solid State Drives Compared](http://ssd.userbenchmark.com/)

GNOME Disk (`gnome-disks`) has built-in benchmarking feature.

[6 Tools to Test Read and Write Speed of USB Flash Drives • Raymond.CC - Page 2](https://www.raymond.cc/blog/test-read-and-write-speed-of-usb-flash-drives-with-usbdeview/2/)
[How to test the speed of your USB drives | PCWorld](https://www.pcworld.com/article/2455205/test-the-speed-of-your-usb-drives.html)
[Performance Tuning Dojo » ADMIN Magazine](http://www.admin-magazine.com/Articles/Assess-USB-performance-while-exploring-storage-caching)
[Benchmark flash memory on Linux](http://kernelreloaded.com/benchmark-flash-memory-on-linux/)
[Iometer project](http://www.iometer.org/)

[HD Tune website](http://www.hdtune.com/download.html)
[CrystalDiskMark – Crystal Dew World](https://crystalmark.info/en/software/crystaldiskmark/) tests file system only
[Disk Benchmark Software | ATTO](https://www.atto.com/disk-benchmark/)
[AS SSD Benchmark Download](https://www.guru3d.com/files-details/as-ssd-benchmark.html)

[fio(1): flexible I/O tester - Linux man page](https://linux.die.net/man/1/fio)
[io - FIO reporting slow write speeds while DD reports fast ones - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/480169/fio-reporting-slow-write-speeds-while-dd-reports-fast-ones) `dd` only tests seq write and blocks of zeros are optimized

```sh
fio --ioengine=libaio --size=1024m --filename=$HOME/tempfile --direct=1 --loops=5 --name=test --bs=1m --rw=write --zero_buffers=1
```

[How to use 'dd' to benchmark your disk or CPU? - rm's homepage](https://romanrm.net/dd-benchmark)
[How to properly use 'dd' on Linux to benchmark the write speed of your disk? | Linuxaria](https://linuxaria.com/pills/how-to-properly-use-dd-on-linux-to-benchmark-the-write-speed-of-your-disk)
[Linux and Unix Test Disk I/O Performance With dd Command - nixCraft](https://www.cyberciti.biz/faq/howto-linux-unix-test-disk-performance-with-dd-command/)
[Test Hard Disk Speed With dd](http://appsintheopen.com/posts/27-test-hard-disk-speed-with-dd)
[SSD Benchmarking - ArchWiki](https://wiki.archlinux.org/index.php/SSD_Benchmarking)
[How We Test Enterprise SSDs - Tom's IT Pro](http://www.tomsitpro.com/articles/enterprise-ssd-testing,2-863.html)

[SSD-Z ](http://aezay.dk/aezay/ssdz/)
[SSD-Z: Information tool for Solid State Drives and other disk devices | TechPowerUp Forums](https://www.techpowerup.com/forums/threads/ssd-z-information-tool-for-solid-state-drives-and-other-disk-devices.210209/)

## Wiping Device

[How to securely erase your hard drive | PCWorld](https://www.pcworld.com/article/261702/how_to_securely_erase_your_hard_drive.html)

[Eraser – Secure Erase Files from Hard Drives](https://eraser.heidi.ie/) only works on HDD
[The Eraser Open Source Project on Open Hub](https://www.openhub.net/p/eraser)
[Eraser Alternatives and Similar Software - AlternativeTo.net](https://alternativeto.net/software/eraser/)

[Roadkil.Net - Roadkil's Disk Wipe Program Download](http://www.roadkil.net/program.php/P14/Disk%20Wipe) also works for flash

[PartedMagic - Partitioning, Cloning, Rescue, and Erasing.](https://partedmagic.com/) also works for flash

## SMART

[S.M.A.R.T. - Wikiwand](http://www.wikiwand.com/en/S.M.A.R.T.)
[smartmontools](https://www.smartmontools.org/)
[CrystalDiskInfo - Software - Crystal Dew World](http://crystalmark.info/software/CrystalDiskInfo/index-e.html)
[Hard Drive SMART Stats](https://www.backblaze.com/blog/hard-drive-smart-stats/)
[SMART Drive and Failure Rates (Backblaze)](https://www.backblaze.com/smart)
[Can we believe S.M.A.R.T. ?](http://www.hdsentinel.com/smart/)
[How Hard Disk S.M.A.R.T. Works?](http://www.hdsentinel.com/smart/index.php)

[Known ATA S.M.A.R.T. attributes - Wikiwand](http://www.wikiwand.com/en/S.M.A.R.T.#/Known_ATA_S.M.A.R.T._attributes)
[Can we believe S.M.A.R.T. ? - S.M.A.R.T. attribute list](http://www.hdsentinel.com/smart/smartattr.php)
[S.M.A.R.T. Monitoring | Knowledge Base](https://kb.acronis.com/content/9636) with description article

Backblaze uses these 5 to diagnose drive failure:
SMART 5 – Reallocated_Sector_Count. !important
SMART 187 – Reported_Uncorrectable_Errors.
SMART 188 – Command_Timeout.
SMART 197 – Current_Pending_Sector_Count. !important
SMART 198 – Offline_Uncorrectable. !!important

[What SMART Hard Disk Errors Actually Tell Us](https://www.backblaze.com/blog/what-smart-stats-indicate-hard-drive-failures/)

```sh
# all SMART tools require su
sudo su
# show SMART attributes
smartctl -A /dev/sda
# query device info
smartctl -P show /dev/sda
# enable SMART
smartctl -s on /dev/sda
# do test
smartctl -t short /dev/sda
smartctl -t long /dev/sda
# show all info
smartctl -a /dev/sda
# or use the GUI
gsmartcontrol
```

## Interface and Bus

In the old days of SATA and IDE, interface (the connector) and the bus (the protocol) were one in the same so the distinction was not explicit.
SSD will easily saturate the bandwidth of older interface. With the adoption of new interfaces, new bus was invented (NVMe/PCIe). And the old protocol are applied to the new interface (SATA/M.2).

[Choosing the right SSD: SATA, M.2, PCIe, and NVMe explained by JJ - YouTube](https://www.youtube.com/watch?v=u-kACJLKNOI)
[M.2 As Fast As Possible - YouTube](https://www.youtube.com/watch?v=opwON-7J_wI)
[The FASTEST SSD Technology Explained - M.2, U.2, and MORE - YouTube](https://www.youtube.com/watch?v=ItMY3WHHowQ)

[2016 Guide: The Best M.2 Solid-State Drives, Tested - ComputerShopper.com](http://www.computershopper.com/feature/2016-guide-the-best-m.2-solid-state-drives-tested)
[M.2 SSD roundup: Tiny drives deliver huge performance | PCWorld](http://www.pcworld.com/article/2977024/storage/m2-ssd-roundup-tiny-drives-deliver-huge-performance.html)

### Parallel ATA

This interface is obsolete.

[Parallel ATA - Wikiwand](http://www.wikiwand.com/en/Parallel_ATA)

### SATA

[Serial ATA - Wikiwand](http://www.wikiwand.com/en/Serial_ATA)
SATA interface devices will use SATA bus.

SATA 1 - 1.5 Gb/s (150 MB)
SATA 2 – 3 Gb/s (300 MB/s)
SATA 3 – 6 Gb/s (600 MB/s) (NCQ)
SATA 3.1 – 6 Gb/s (600 MB/s) (mSATA) (TRIM)
SATA 3.2 – 16 Gb/s (1969 MB/s)

### M.2

[M.2 - Wikiwand](http://www.wikiwand.com/en/M.2)

[Explaining M.2 SSDs - YouTube](https://www.youtube.com/watch?v=SP0Brsc0dMY)

- Replaces mSATA
- 2280 means 22mm x 80mm
- M.2 SSD can have SATA or PCIe bus

[Understanding M.2, the interface that will speed up your next SSD | Ars Technica](http://arstechnica.com/gadgets/2015/02/understanding-m-2-the-interface-that-will-speed-up-your-next-ssd/)

### SAS

[Serial Attached SCSI - Wikiwand](https://www.wikiwand.com/en/Serial_Attached_SCSI)

### SD Card

[SD card - Wikiwand](https://www.wikiwand.com/en/SD_card#/Speed)
UHS is used in SD/TF cards. It is marked in roman numerals on the card.

[How to choose an SD card: Class and speed ratings explained | Expert Reviews](https://www.expertreviews.co.uk/storage/1404380/how-to-choose-an-sd-card-class-and-speed-ratings-explained)

### PCIe

[Why Are PCIe SSDs So Fast? - Stephen Foskett, Pack Rat](http://blog.fosketts.net/2013/06/12/pcie-ssds-fast/)
[Weigh the pros and cons of PCIe-based SSD](http://cdn.ttgtmedia.com/CascadingTargetedDownloads/downloads/PCIe%20solid state%20storage%20definition.pdf) (PDF)

### NVMe

[NVM Express - Wikiwand](https://www.wikiwand.com/en/NVM_Express)
[NVM Express – scalable, efficient, and industry standard](https://nvmexpress.org/)
Ditches the SCSI and allow CPU to access NAND like RAM. SCSI Express is doing similar thing. NVMe flash can use M.2 or PCI-E interface.

[The Western Digital WD Blue SN500 SSD Review: Moving The Mainstream To NVMe - Print View](https://www.anandtech.com/print/14223/the-western-digital-wd-blue-sn500-ssd-review)
Higher end NVMe sticks have DRAM buffer for caching the mapping tables for translating logical block addresses (LBAs) into physical memory addresses. Medium range ones without DRAM usually supports Host Memory Buffer feature to utilize system RAM to store the mapping.

[Everything you need to know about NVMe, the insanely fast future for SSDs | PCWorld](http://www.pcworld.com/article/2899351/everything-you-need-to-know-about-nvme.html)
[What is NVMe, and how is it changing enterprise storage | Network World](https://www.networkworld.com/article/3280991/storage/what-is-nvme-and-how-is-it-changing-enterprise-storage.html)
[Why NVMe? Users weigh benefits of NVMe-accelerated flash storage | Network World](https://www.networkworld.com/article/3290421/storage/why-nvme-users-weigh-benefits-of-nvme-accelerated-flash-storage.html)
[MSI 主機板喊出支援 NVMe，簡單看懂這與通俗的 AHCI 有什麼不同 | T 客邦 - 我只推薦好東西](http://www.techbang.com/posts/22114-shout-out-your-support-msi-motherboard-nvme-ssd-simple-to-understand-this-different-and-popular-ahci)

## Advanced Format

[Advanced Format - Wikiwand](https://www.wikiwand.com/en/Advanced_Format)
[A Brief Introduction of Advanced Format](http://www.minitool.com/lib/advanced-format.html)

[HGST Advanced Format Technology Brief](https://www.hgst.com/sites/default/files/resources/AFtechbrief.pdf) (PDF)
[WD Advanced Format Technology Brief Flyer](http://www.wdc.com/wdproducts/library/Flyer/ENG/2178-771123.pdf) (PDF)

## NRAM

[Fujitsu now making DRAM killer with 1,000x performance boost | InfoWorld](http://www.infoworld.com/article/3114220/storage/fujitsu-now-making-dram-killer-with-1000x-performance-boost.html)

## Decoding Part Numbers

### Western Digital

[WD Model Number Format for OEM and Distribution Channels](http://www.wdc.com/wdproducts/library/other/2579-001028.pdf)

**WD 0000 ABCD**
0000: Capacity
A: Capacity Unit/Form Factor
B: Business Unit/Brand
C: RPM/Buffer Size or Attribute
D: Interface/Connector

### HGST

[How to find your Serial, Part, Model or Item Number | HGST](https://www.hgst.com/support/hard-drive-support/warranty-returns/find-serial-number)
[How to read most of the Hitachi Global Storage Technologies model number - Free Data Recovery Quote](http://freedatarecoveryquote.com/hitachi-global-storage-technologies-model-number/) (2012)
[Ultrastar-7K6000-DS.pdf](https://www.hgst.com/sites/default/files/resources/Ultrastar-7K6000-DS.pdf)

How to read the Ultrastar model number
Example: HUS7260xxAL421y = xTB, 4Kn SAS 12Gb/s

H = HGST
U = _Series_
S = _Type_
72 = 7200 RPM
60 = Full capacity
xx = _Capacity_ of this model
A = Generation code
L = 26.1mm z-height
42 = _Interface_
1 = 128MB buffer (for Ultrastar)
y = _Data Security Mode_

| Series (U)     | Type (S)                  | Capacity (xx)         | Interface (42)                    | Data Security Mode (y)                                    |
| -------------- | ------------------------- | --------------------- | --------------------------------- | --------------------------------------------------------- |
| T = Travelstar | S = Standard              | 80 = 8TB              | 42 = 4Kn SAS 12Gb/s               | 0 = Instant Secure Erase                                  |
| D = Deskstar   | E = Enhanced Availability | 60 = 6TB              | 52 = 512e SAS 12Gb/s              | 1 = Bulk Data Encryption (SATA), TCG SED encryption (SAS) |
| C = Compact    | 50 = 5TB                  | E6 = 512e SATA 6Gb/s  | 4 = Secure Erase (overwrite only) |
| U = Ultrastar  |                           | 40 = 4TB              | N6 = 4Kn SATA 6Gb/s               | 5 = TCG encryption with FIPS (SAS)                        |
| H = He8        |                           | 20 = 2TB              | A6\*= 512n SATA 6Gb/s             |
|                |                           | S2\*= 512n SAS 12Gb/s |

\*Available in 4TB and 2TB capacities

### Seagate’s

[MPECS Inc. Blog: Seagate’s New Model Numbering Scheme](http://blog.mpecsinc.ca/2010/11/seagates-new-model-numbering-scheme.html) (2010)
