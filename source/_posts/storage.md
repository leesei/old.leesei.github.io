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

[【科技杂谈 65】记录的史诗，存储的百年马拉松 - YouTube](https://www.youtube.com/watch?v=hPrCDvdfLHQ)
[【科技杂谈 66】机械硬盘发展史 - YouTube](https://www.youtube.com/watch?v=8yDipw1RqEk)

[Seven attempts to speed processing with faster storage – Blocks and Files](https://blocksandfiles.com/2020/09/08/seven-attempts-to-speed-processing-with-faster-storage/)

[PMR？SMR？HAMR？MAMR？氦氣填充？512e？4Kn？硬碟技術一一拆解 - XFastest Hong Kong](https://hk.xfastest.com/2715/hdd-technology-intro/) !important

[SSD vs. HDD: Choosing between solid-state and hard-disk drives | Network World](https://www.networkworld.com/article/3482988/ssd-vs-hdd-how-to-choose-between-solid-state-drives-and-hard-disk-drives.html)
[Solid State vs. Hard Disk: Differences Between SSD and HDD](https://www.backblaze.com/blog/hdd-versus-ssd-whats-the-diff/)

## Platter Drive

[Hard Drive Test Data - Determining Failure Rates and More](https://www.backblaze.com/b2/hard-drive-test-data.html)

[Western Digital Green vs. Red Hard Drives - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/Western-Digital-Green-vs-Red-Hard-Drives-602/)

Cable doesn't matter:
[SATA 3Gb/s vs. 6Gb/s Cable Performance (Revisited) - Puget Custom Computers](https://www.pugetsystems.com/labs/articles/SATA-3Gb-s-vs-6Gb-s-Cable-Performance-Revisited-183/)

Platters of traditional magnetic disks are divided into tracks (rings), then into sectors. Sectors are grouped into block and given addresses.

Physically read and writes are done with sector. On file system it is done with blocks. So the minimum space a file takes up is (sector size \* block size).

[Understanding the WD Rainbow](https://www.pugetsystems.com/labs/articles/Understanding-the-WD-Rainbow-674/)

> how about cylinders, heads or sectors?

### Magnetic Recording

[What are PMR and SMR hard disk drives? | Synology Inc.](https://www.synology.com/en-us/knowledgebase/DSM/tutorial/Storage/PMR_SMR_hard_disk_drives)
Tracks of SMR HDD overlaps to increase density. Writes are performed to PMR cache, then committed back to SMR area during idle time. So they usually have larger buffer to prevent overwriting data and slower write speed.

[Perpendicular recording - Wikiwand](https://www.wikiwand.com/en/Perpendicular_recording) also conventional magnetic recording (CMR)
[Shingled magnetic recording - Wikiwand](https://www.wikiwand.com/en/Shingled_magnetic_recording)

SMR will cause RAID mis-identify disk failure during high workload
[Buyer beware—that 2TB-6TB “NAS” drive you’ve been eyeing might be SMR – Ars Technica](https://arstechnica.com/gadgets/2020/04/caveat-emptor-smr-disks-are-being-submarined-into-unexpected-channels/?amp=1)
[Updated: HDD manufacturers found selling slow SMR drives unsuitable for NAS RAID environments](https://www.techspot.com/amp/news/84914-wd-seagate-toshiba-found-selling-slow-smr-drives.html)
[Use of Shingled Magnetic Recording (SMR) technology in Toshiba Consumer Hard Drives. | Toshiba Electronic Devices & Storage Corporation | Asia-English](https://toshiba.semicon-storage.com/ap-en/company/news/news-topics/2020/04/storage-20200428-1.html)
[SMR in disk drives: PC vendors also need to be transparent – Blocks and Files](https://blocksandfiles.com/2020/04/20/western-digital-smr-drives-statement/)
[Dropbox loves shingled disk drives – Blocks and Files](https://blocksandfiles.com/2019/07/30/dropbox-smr-shingled-hard-drives-experience/)
[Shingled hard drives have non-shingled zones for caching writes – Blocks and Files](https://blocksandfiles.com/2020/04/15/shingled-drives-have-non-shingled-zones-for-caching-writes/)
[【硬件科普】选购机械硬盘的大坑，不看你就上当，详解 SMR 瓦楞式堆叠硬盘 - YouTube](https://www.youtube.com/watch?v=nxmlCNzme34)

LTT
[Hard Drives Are NOT All The Same - YouTube](https://www.youtube.com/watch?v=SH_XsrHezN4)
[Why are Drive Manufacturers in BIG TROUBLE? - YouTube](https://www.youtube.com/watch?v=aztTf2gI55k)
WD Red 2TB-6TB (EFAX) employ device-managed shingled magnetic recording (DMSMR) since 2014

HAMR (heat-assisted magnetic recording) by Seagate
MAMR (microwave-assisted magnetic recording) by Western Digital
More precise writing techniques to increase density of magnetic track

[HAMR don’t hurt ’em—laser-assisted hard drives are coming in 2020 – Ars Technica](https://arstechnica.com/gadgets/2020/02/hamr-dont-hurt-em-laser-assisted-hard-drives-are-coming-in-2020/?amp=1)
[Come to MAMR! Western Digital unfurls HDD tech roadmap – Blocks and Files](https://blocksandfiles.com/2020/01/28/western-digital-gives-hdd-technology-roadmap-lesson/)

[ZonedStorage.io](https://www.zonedstorage.io/)
[Making Host Managed SMR Work for You – Dropbox’s Successful Journey - Western Digital Corporate Blog](https://blog.westerndigital.com/host-managed-smr-dropbox/)
[What is Zoned Storage and the Zoned Storage Initiative?](https://blog.westerndigital.com/what-is-zoned-storage-initiative/)

## SSD

[Solid-state storage - Wikiwand](http://www.wikiwand.com/en/Solid-state_storage)
[Solid-state revolution: in-depth on how SSDs really work | Ars Technica](http://arstechnica.com/information-technology/2012/06/inside-the-ssd-revolution-how-solid-state-disks-really-work/)
[How Do SSDs Work? - ExtremeTech](https://www.extremetech.com/extreme/210492-extremetech-explains-how-do-ssds-work)
[How SSDs Work - Intel X25-M SSD: Intel Delivers One of the World's Fastest Drives](http://www.anandtech.com/show/2614/2)
[The SSD Anthology: Understanding SSDs and New Drives from OCZ](http://www.anandtech.com/print/2738)
[The SSD Relapse: Understanding and Choosing the Best SSD](http://anandtech.com/print/2829)
[Explaining SSDs: Form Factors, Interfaces & Technologies - YouTube](https://www.youtube.com/watch?v=EXLfErPEYiw)
[SSD ABC Guide – OCZ Forum](http://oczforum.com/staff/meander/OCZ_SSD_ABC_Guide.pdf) PDF
[Exploring Solid State Drives and 3D NAND - YouTube](https://www.youtube.com/playlist?list=PL6rx9p3tbsMuk0jnC-dBdwb32Z1g7mD0j)

[What's the difference between flash and SSD storage? | PC Gamer](https://www.pcgamer.com/whats-the-difference-between-flash-and-ssd-storage/) flash is one kind of SSD

[Buying a Solid State Drive (SSD): Everything You Need to Know - YouTube](https://www.youtube.com/watch?v=aBfJsoc8zzk)
[Does a Faster SSD Matter for Gamers?? - \$h!t Manufacturers Say - YouTube](https://www.youtube.com/watch?v=4DKLA7w9eeA)
DRAM is more important than the protocol
[【Huan】 如何選擇 M.2 SSD? 這支影片給你參考 How to Choose Your M.2 SSD? - YouTube](https://www.youtube.com/watch?v=xcq5DxdEl_w)

[This should be illegal… - Manufacturers are swapping SSD components - YouTube](https://www.youtube.com/watch?v=K07sEM6y4Uc) ADATA XPG 8200 Pro downgrade 2021-02

[SSDs - Latest Articles and Reviews on AnandTech](https://www.anandtech.com/tag/ssd)
[Best SSDs: Q1 2019](https://www.anandtech.com/show/9799/best-ssds)
[Best SSD 2019: Solid State Drives - Tech Advisor](https://www.techadvisor.co.uk/test-centre/storage/best-ssd-3235200/)
[How to Buy the Right SSD: A Guide for 2019](https://www.tomshardware.com/reviews/ssd-buying-guide,5602.html)
[Best SSDs 2019: SATA, PCIe, and Add-in Cards](https://www.tomshardware.com/reviews/best-ssds,3891.html)
[Sean's SSD Buyers Guide & Information Thread](http://www.overclock.net/t/1179518/seans-ssd-buyers-guide-information-thread)
[Best SSDs for 2019 - CNET](https://www.cnet.com/topics/storage/best-hard-drives-and-storage/ssd/)
[Best SSD for gaming 2020: Faster storage for your gaming PC | PC Gamer](https://www.pcgamer.com/best-ssd-for-gaming/)

[Enterprise versus Client SSD](http://www.kingston.com/en/ssd/enterprise/best_practices/enterprise_versus_client_ssd)
[Solid state / SSD news, tips and information – SearchSolidStateStorage.com](http://searchsolidstatestorage.techtarget.com/)
[Solid State Drive SSD Preturi, Oferte, Solid State Drive SSD Magazine, Solid State Drive SSD ieftine](https://solid-state-drive-ssd.compari.ro/)
[SSD UserBenchmarks - 994 Solid State Drives Compared](https://ssd.userbenchmark.com/)
[From The Wirecutter: The best consumer-grade SSD (for most people) | Ars Technica](http://arstechnica.com/gadgets/2015/04/from-the-wirecutter-the-best-consumer-grade-ssd-for-most-people/)

[SSD: how to optimize your Solid State Drive for Linux Mint 17.3, Ubuntu 14.04 and Debian - Easy Linux tips project](https://sites.google.com/site/easylinuxtipsproject/ssd)

### Thermal Dissipation

[【Huan】 裝上這個 SSD 溫度爆降 30 度! 157 元平價 M.2 散熱片實測 - YouTube](https://www.youtube.com/watch?v=QyTdKJ3Z1Rw) 雙面散熱

### NAND Cell

Cells stores the bits (1 per cell for SLC, 2 for MLC, 3 for [TLC](http://www.anandtech.com/show/5067/understanding-tlc-nand), 4 per cell QLC, 5 per cell PLC).
Cells are then organized into pages, then pages into blocks.
Writes is done on pages and erase is done on blocks.
[How SSD Technology Keeps Getting WORSE! - Intel 660p Review - YouTube](https://www.youtube.com/watch?v=OffzVc7ZB-o) first QLC drive

Samsung's 850 series and Crucial MX300 uses 3D NAND technology that improves performance and durability and overcome density limits of planar NAND.
[Samsung's 850 Pro solid-state drive reviewed - The Tech Report](http://techreport.com/review/26701/samsung-850-pro-solid-state-drive-reviewed) (V-NAND flash)

Crucial uses free unused NAND in SLC mode as write buffer to speed up writes (Dynamic Write Acceleration).

[Enmotus MiDrive: Rethinking SLC Caching For QLC SSDs - Print View](https://www.anandtech.com/print/15442/enmotus-midrive-rethinking-slc-caching-for-qlc-ssds) smart SLC cache via information from host app
[The Enmotus MiDrive combines true SLC and QLC on a single SSD - TechSpot](https://www.techspot.com/amp/news/83511-enmotus-midrive-combines-true-slc-qlc-single-ssd.html)

[QLC vs TLC SSDs: Samsung QVO & EVO - YouTube](https://www.youtube.com/watch?v=WACyyFF_ci0)
[What’s the difference between SLC, MLC and TLC? - Answers - UserBenchmark](http://www.userbenchmark.com/Faq/What-s-the-difference-between-SLC-MLC-and-TLC/107)
[What’s the difference between NAND and V-NAND? - Answers - UserBenchmark](http://www.userbenchmark.com/Faq/What-s-the-difference-between-NAND-and-V-NAND/104)
[SSD Life Expectancy - YouTube](https://www.youtube.com/watch?v=-XZNr7mS0iw)
[How SSD Technology Keeps Getting WORSE! - Intel 660p Review - YouTube](https://www.youtube.com/watch?v=OffzVc7ZB-o) Quad-bit per cell
[Enmotus MiDrive: Rethinking SLC Caching For QLC SSDs - Print View](https://www.anandtech.com/print/15442/enmotus-midrive-rethinking-slc-caching-for-qlc-ssds)
[3D NAND technology: What it is and where it's headed](https://searchstorage.techtarget.com/essentialguide/3D-NAND-technology-What-it-is-and-where-its-headed)

### Controller

[SSD 的核心!! Marvell v.s SandForce Controller 大對決 (下) - 小 P 的 SSD 秘密實驗室](https://www.facebook.com/notes/plextor-台灣/ssd的核心-marvell-vs-sandforce-controller-大對決-下-小p的ssd秘密實驗室/406211976056515)

LSI SandForce controllers will compress data before writing to NAND to enhance data rate and enhance SSD life.
[Technical Brief - What is DuraWrite | Kingston](http://www.kingston.com/en/ssd/enterprise/technical_brief/what_is_durawrite)

[Silicon Motion SM2258 Technical Preview With Micron 3D TLC - Tom's Hardware](https://www.tomshardware.com/reviews/silicon-motion-sm2258-micron-3d-preview,4698.html)

[Silicon Motion SM2263XT HMB SSD Preview - Tom's Hardware | Tom's Hardware](https://www.tomshardware.com/reviews/silicon-motion-sm2263xt-controller-preview,5404.html)
DRAM-less, Host Memory Buffer
[HMB in DRAM-less NVMe SSDs: Their usage and effects on performance](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0229645)

### Degradation

Beware that Samsung's 840 series (using TLC) have [performance degradation](http://www.techspot.com/article/997-samsung-ssd-read-performance-degradation/) problem.
[Consistent Performance: A Reality? - The Intel SSD DC S3700 (200GB) Review](http://www.anandtech.com/show/6433/intel-ssd-dc-s3700-200gb-review/3)
[Researchers publish first large-scale, in-field SSD reliability report - TechSpot](http://www.techspot.com/news/61090-researchers-publish-first-large-scale-field-ssd-reliability.html)
[How NAND flash degrades and what vendors do to increase SSD endurance](http://searchsolidstatestorage.techtarget.com/podcast/How-NAND-flash-degrades-and-what-vendors-do-to-increase-SSD-endurance)

[5 Warning Signs Your SSD Is About to Break Down and Fail](https://www.makeuseof.com/tag/5-warning-signs-ssd-break-fail/)

### Alignment

Alignment used to an issue years ago, but no longer.

[Aligning an SSD on Linux » Cygon's Blog](http://blog.nuclex-games.com/2009/12/aligning-an-ssd-on-linux/)
[Solid State Drive (SSD) – Info and Alignment | Linux.org](http://www.linux.org/threads/solid-state-drive-ssd-%E2%80%93-info-and-alignment.6572/)

### Trim

[Trim (computing) - Wikiwand](http://www.wikiwand.com/en/Trim_%28computing%29)
[Garbage Collection and TRIM in SSDs Explained - An SSD Primer | The SSD Review](http://www.thessdreview.com/daily-news/latest-buzz/garbage-collection-and-trim-in-ssds-explained-an-ssd-primer/)
[Extend the life of your SSD drive with fstrim | Opensource.com](https://opensource.com/article/20/2/trim-solid-state-storage-linux)

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

[The Samsung 983 ZET (Z-NAND) SSD Review: How Fast Can Flash Memory Get? - Print View](https://www.anandtech.com/print/13951/the-samsung-983-zet-znand-ssd-review) Premium SLC SSD

[Samsung 970 EVO Plus SSD: Improved performance and efficiencies | ZDNet](https://www.zdnet.com/article/samsung-970-evo-plus-ssd-improved-performance-and-efficiencies/)

[Samsung 860 Evo review: New SSD has Upgraded Performace & Life - Tech Advisor](https://www.techadvisor.co.uk/review/ssd-hard-drives/samsung-860-evo-review-3670806/)
Interface: SATA
Memory Cache: 512MB LPDDR4
Controller: Samsung MJX Controller
Encryption: AES 256-bit
Flash technology: Samsung V-NAND 3bit TLC

250G $365 500G $568

PM981/PM981a is OEM of 970 Evo
[PM981 spec](https://www.compuram.biz/documents/datasheet/Samsung_PM981_Rev_1_1.pdf)
[The Samsung PM981 SSD Review (512GB, 1TB): Next Generation Controller And 3D NAND - Print View](https://www.anandtech.com/print/12082/the-samsung-pm981-ssd-review-512gb-1tb-phoenix-3d-nand)
Memory Cache: 512MB LPDDR4
Controller: Samsung Phoenix Controller, NVMe 1.2
Encryption: AES 256-bit
Flash technology: 64 layers Samsung V-NAND 3bit TLC
[Samsung PM981 SSD Review - Tom's Hardware | Tom's Hardware](https://www.tomshardware.com/reviews/samsung-pm981-980-nvme-ssd,5323.html)

[Samsung 980 Pro M.2 NVMe SSD Review: Redefining Gen4 Performance | Tom's Hardware](https://www.tomshardware.com/reviews/samsung-980-pro-m-2-nvme-ssd-review)

### Toshiba

[搞机笔记 篇二：旗舰级 PCIe 3.0 M.2 固态硬盘哪家强：东芝 RD500 VS 三星 PM981 对比评测*固态硬盘*什么值得买](https://post.smzdm.com/p/a839973q/)

### Western Digital

[Western Digital Blue SN550 1TB NVMe PCIe Gen3.0x 4 M.2 SSD Review](https://www.tweaktown.com/reviews/9332/western-digital-blue-sn550-1tb-nvme-pcie-gen3-0x-4-2-ssd-review/index.html)
USD\$100 1TB RAM-less value drive

[WD Black P50 Portable Game Drive SSD Review](https://www.tweaktown.com/reviews/9328/wd-black-p50-portable-game-drive-ssd-review/index.html)
USD\$250 1TB

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

[英睿达 bx500 镁光固态硬盘 480G 固态 sata3 固态硬盘 笔记本 2.5 英寸台式机电脑 SSD-tmall.com 天猫](https://detail.tmall.com/item.htm?id=598745625526&skuId=4372736054445) ¥379
[顺丰 英睿达 CRUCIAL/镁光 CT500MX500SSD1 500g ssd 固态硬盘-tmall.com 天猫](https://detail.tmall.com/item.htm?id=564260701078&skuId=3562589516567) ¥489

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

> contrary to flash memory

[Intel® Optane™ Technology](https://www.intel.com/content/www/us/en/architecture-and-technology/intel-optane-technology.html)
[3D XPoint memory: NAND flash killer or DRAM replacement? | InfoWorld](http://www.infoworld.com/article/3194348/flash-storage/3d-xpoint-memory-nand-flash-killer-or-dram-replacement.html)
[What is 3D XPoint and how fast is it? - Answers - UserBenchmark](http://www.userbenchmark.com/Faq/What-is-3D-XPoint-and-how-fast-is-it/106)

[What is Intel Optane? - YouTube](https://www.youtube.com/watch?v=WwH5Q8ZFJvw)
[Intel Optane Memory: everything you need to know | PC Gamer](https://www.pcgamer.com/intel-optane-memory-everything-you-need-to-know/)

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

[Can a USB Thumb Drive "Wear Out"? - Ask Leo!](https://askleo.com/can_a_usb_thumb_drive_wear_out/)

### Counterfeit Flash

[4 Tools to Test and Detect Fake or Counterfeit USB Flash Drives • Raymond.CC](https://www.raymond.cc/blog/test-and-detect-fake-or-counterfeit-usb-flash-drives-bought-from-ebay-with-h2testw/)
[How to Spot a Fake MicroSD Card and Avoid Being Scammed](https://www.makeuseof.com/tag/how-to-spot-fake-microsd-card/)

[F3 by Digirati](http://oss.digirati.com.br/f3/)
[f3 - Fight Flash Fraud — f3 documentation](https://fight-flash-fraud.readthedocs.io/en/stable/introduction.html)
`sudo f3probe --destructive --time-ops /dev/sdf`

[H2testw – best sd memory card speed tester for Windows (how to use & download)](https://howtorecover.me/h2testw-memory-card-tester)
[07 - All about 'Fake' SD cards and USB Flash drives - RMPrepUSB](https://www.rmprepusb.com/tutorials/-fake-usb-flash-memory-drives) FakeFlashTest, Windows

[USB Flash Drive Tester](https://www.vconsole.com/download), Windows
[Flash Drive/Card Tester - Check your USB flash drives and memory cards for errors](https://www.ricksdailytips.com/flash-drive-card-tester/)

[HOME PAGE OF MISHA CHERKES](http://mikelab.kiev.ua/index_en.php?page=PROGRAMS/chkflsh_en) Windows
[ChkFlsh checks your Flash Drives on Windows](https://www.makeuseof.com/tag/chkflsh-checks-your-flash-drives-on-windows/)

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

## Optical Media

[The Story of Laserdisc - YouTube](https://www.youtube.com/playlist?list=PLv0jwu7G_DFUoByWSHHoSTlUIxY7VkJLi)

[The Compact Disc: An Introduction - YouTube](https://www.youtube.com/watch?v=sAbhPeTp51s)
[CDs: More to Talk About (Sony vs. Philips) - YouTube](https://www.youtube.com/watch?v=7olNiMCz9to)
[Dissecting the CD Player: How to Turn Shiny Plastic into Music - YouTube](https://www.youtube.com/watch?v=3yJqlD9RxD4)
[The CD Player with a Robot Inside: Pioneer CLD-M301 - YouTube](https://www.youtube.com/watch?v=L6iyUSnrGk0)
[CD-ROM, CD-R, CD-RW, Books of Red, Blue, Purple, Beige, Orange, Scarlet... - YouTube](https://www.youtube.com/watch?v=TCTWyNstpD0)

[DVD-RAM: The Disc that Behaved like a Flash Drive - YouTube](https://www.youtube.com/watch?v=ecH3OU0R4ls)
[DVD-RAMifications (experiments and other goodies relating to DVD-RAM) - YouTube](https://www.youtube.com/watch?v=U9aZuFOTHtQ)
[DVD+R and DVD-R; What was that about? - YouTube](https://www.youtube.com/watch?v=e1mJv9pxm7M)

[【科技杂谈 77】比脑袋还大的光碟——LD 光碟（镭射光碟）【光盘发展史 1】 - YouTube](https://www.youtube.com/watch?v=CApE95p4GAk)

## Tape

[Linear Tape-Open - Wikiwand](https://www.wikiwand.com/en/Linear_Tape-Open)
[What is LTO Technology? | Ultrium LTO](https://www.lto.org/technology/what-is-lto-technology/)

[We got a \$5,500 TAPE DRIVE! - YouTube](https://www.youtube.com/watch?v=alxqpbSZorA)

## #perfmatters

[Linux disk performance tuning](https://blog.kruyt.org/linux-disk-tuning/)

## Benchmarking/Info

```sh
# info
sudo hdparm -I /dev/sda
### THIS is destructive ###
# read speed test
sudo hdparm -t --direct /dev/sda
sudo hdparm -Tt --direct /dev/sda
```

```sh
# read speed benchmark
sudo dd if=/dev/sdX1 of=/dev/zero bs=1M count=400 iflag=direct
echo 3 | sudo tee /proc/sys/vm/drop_caches  # clear cache first
sudo dd if=/dev/zero of=/dev/sdX1 bs=1M count=400 skip=1000 conv=fdatasync
```

[What's the fastest USB drive for a Raspberry Pi? - YouTube](https://www.youtube.com/watch?v=lxuKqBYvDQs)
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

[Software and Firmware Downloads | WD Support](https://support.wdc.com/downloads.aspx?p=279)
[Western Digital SSD Dashboard Review - StorageReview.com](https://www.storagereview.com/review/western-digital-ssd-dashboard-review)

[ssd-benchmark — command-line utility in Rust // Lib.rs](https://lib.rs/crates/ssd-benchmark)

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

## Bad sectors

`badblocks -s /dev/sda`
`hdparm --write-sector 48095863 --yes-i-know-what-i-am-doing /dev/sda`

[ubuntu - Extremely long time for an ext4 fsck - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/78785/extremely-long-time-for-an-ext4-fsck)
[linux - How to use hdparm to fix a pending sector? - Server Fault](https://serverfault.com/questions/461203/how-to-use-hdparm-to-fix-a-pending-sector)
[Forcing a hard disk to reallocate bad sectors | Bas' Blog](http://www.sj-vs.net/forcing-a-hard-disk-to-reallocate-bad-sectors/)

## SMART

[S.M.A.R.T. - Wikiwand](http://www.wikiwand.com/en/S.M.A.R.T.)
[S.M.A.R.T. - ArchWiki](https://wiki.archlinux.org/index.php/S.M.A.R.T.)
[smartmontools](https://www.smartmontools.org/)
[CrystalDiskInfo - Software - Crystal Dew World](http://crystalmark.info/software/CrystalDiskInfo/index-e.html)
[Hard Drive SMART Stats](https://www.backblaze.com/blog/hard-drive-smart-stats/)
[SMART Drive and Failure Rates (Backblaze)](https://www.backblaze.com/smart)
[Can we believe S.M.A.R.T. ?](http://www.hdsentinel.com/smart/)
[How Hard Disk S.M.A.R.T. Works?](http://www.hdsentinel.com/smart/index.php)
[SMART Devices » ADMIN Magazine](https://www.admin-magazine.com/HPC/Articles/SMART-Devices)

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

[Windows 10: Built-in tools for Hard Disk Health check - TechNet Articles - United States (English) - TechNet Wiki](https://social.technet.microsoft.com/wiki/contents/articles/53235.windows-10-built-in-tools-for-hard-disk-health-check.aspx)

```
wmic diskdrive get status
```

### Enable `smartd`

[smartd - ArchWiki](https://wiki.archlinux.org/index.php/S.M.A.R.T.#smartd)
[smartd(8): SMART Disk Monitoring Daemon - Linux man page](https://linux.die.net/man/8/smartd)

[Know when your drives are failing, with smartd | Linux Journal](https://www.linuxjournal.com/content/know-when-your-drives-are-failing-smartd)
[Linux OS Service ‘smartd’ – The Geek Diary](https://www.thegeekdiary.com/linux-os-service-smartd/)

## Interface and Bus

In the old days of SATA and IDE, interface (the connector) and the bus (the protocol) were one in the same so the distinction was not explicit.
SSD will easily saturate the bandwidth of older interface. With the adoption of new interfaces, new bus was invented (NVMe/PCIe). And the old protocol are applied to the new interface (SATA/M.2).

[Choosing the right SSD: SATA, M.2, PCIe, and NVMe explained by JJ - YouTube](https://www.youtube.com/watch?v=u-kACJLKNOI)
[M.2 As Fast As Possible - YouTube](https://www.youtube.com/watch?v=opwON-7J_wI)
[The FASTEST SSD Technology Explained - M.2, U.2, and MORE - YouTube](https://www.youtube.com/watch?v=ItMY3WHHowQ)
[【Huan】M.2? SATA? SSD 的各種規格介紹，如何選購適合自己的 SSD - YouTube](https://www.youtube.com/watch?v=NbL231dhnKs)

B Key: 左邊短邊 6 pin, PCIe x2, SATA
M Key: 右邊短邊 5 pin, PCIe x4, SATA
M.2 SSD using SATA will be B&M key so they can fit either socket
M.2 SSD with M key uses NVMe

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
- M.2 SSD can run SATA/AHCI (B/M+B keyed) or AHCI/PCIe or NVMe/PCIe (M keyed)
- The old name NGFF (Next Gen Form Factor) is sometimes used to refer M.2 with SATA bus

[Understanding M.2, the interface that will speed up your next SSD | Ars Technica](http://arstechnica.com/gadgets/2015/02/understanding-m-2-the-interface-that-will-speed-up-your-next-ssd/)
[M.2 Interface, Key and Socket explained](https://www.atpinc.com/blog/what-is-m.2-M-B-BM-key-socket-3)

### SAS

[Serial Attached SCSI - Wikiwand](https://www.wikiwand.com/en/Serial_Attached_SCSI)

### NVMe

[NVM Express - Wikiwand](https://www.wikiwand.com/en/NVM_Express)
[NVM Express – scalable, efficient, and industry standard](https://nvmexpress.org/)
Ditches the SCSI and allow CPU to access NAND like RAM. SCSI Express is doing similar thing. NVMe flash can use M.2 or PCI-E interface.

[Why Are PCIe SSDs So Fast? - Stephen Foskett, Pack Rat](http://blog.fosketts.net/2013/06/12/pcie-ssds-fast/)
[Weigh the pros and cons of PCIe-based SSD](http://cdn.ttgtmedia.com/CascadingTargetedDownloads/downloads/PCIe%20solid%20state%20storage%20definition.pdf) (PDF)

[NVMe vs. SATA: Which SSD Technology Is Faster?](https://www.howtogeek.com/657972/nvme-vs.-sata-which-ssd-technology-is-faster/amp/)
[What is NVMe and Why is it Important? A Technical Guide](https://blog.westerndigital.com/nvme-important-data-driven-businesses/)

[The Western Digital WD Blue SN500 SSD Review: Moving The Mainstream To NVMe - Print View](https://www.anandtech.com/print/14223/the-western-digital-wd-blue-sn500-ssd-review)
Higher end NVMe sticks have DRAM buffer for caching the mapping tables for translating logical block addresses (LBAs) into physical memory addresses. Medium range ones without DRAM usually supports Host Memory Buffer feature to utilize system RAM to store the mapping.

[The Next Step in SSD Evolution: NVMe Zoned Namespaces Explained - Print View](https://www.anandtech.com/print/15959/nvme-zoned-namespaces-explained/3) technology used for host controlled SMR drives

[M.2, SATA, and NVMe SSDs Explained: Which Should You Buy for Your PC?](https://theinventory.com/m-2-sata-and-nvme-ssds-explained-which-should-you-bu-1836647003/amp)
[SATA 3 vs M.2 vs NVMe – Overview and Comparison](https://www.online-tech-tips.com/computer-tips/sata-3-vs-m-2-vs-nvme-overview-and-comparison/amp/)
[Everything you need to know about NVMe, the insanely fast future for SSDs | PCWorld](http://www.pcworld.com/article/2899351/everything-you-need-to-know-about-nvme.html)
[What is NVMe, and how is it changing enterprise storage | Network World](https://www.networkworld.com/article/3280991/storage/what-is-nvme-and-how-is-it-changing-enterprise-storage.html)
[Why NVMe? Users weigh benefits of NVMe-accelerated flash storage | Network World](https://www.networkworld.com/article/3290421/storage/why-nvme-users-weigh-benefits-of-nvme-accelerated-flash-storage.html)
[MSI 主機板喊出支援 NVMe，簡單看懂這與通俗的 AHCI 有什麼不同 | T 客邦 - 我只推薦好東西](http://www.techbang.com/posts/22114-shout-out-your-support-msi-motherboard-nvme-ssd-simple-to-understand-this-different-and-popular-ahci)
[NGFF、M.2、PCIe、NVMe 是什麼??? @ 基隆七堵電腦買賣維修(阿三哥) :: 隨意窩 Xuite 日誌](https://m.xuite.net/blog/a06315/twblog/454025311) AHCI/PCIe < NVMe/PCIe
[M.2 NVMe SSD Explained - M.2 vs SSD - YouTube](https://www.youtube.com/watch?v=HvfIeTieXOI)

### SD Card

[SD card - Wikiwand](https://www.wikiwand.com/en/SD_card#/Speed)
UHS bus is used in SD/TF cards. It is marked in roman numerals on the card.

[Top SBC Micro SD Card (Group Benchmark) - YouTube](https://www.youtube.com/watch?v=YUResed38uo)
[Explaining SD Cards: 2020 Update - YouTube](https://www.youtube.com/watch?v=oLQ8A_vcBqU)
[How to choose an SD card: Class and speed ratings explained | Expert Reviews](https://www.expertreviews.co.uk/storage/1404380/how-to-choose-an-sd-card-class-and-speed-ratings-explained)
U{d} for sequential read/write speed d\*10MBps
A{d} for random I/O per second

[A2-class microSD cards offer no better performance for the Raspberry Pi | Jeff Geerling](https://www.jeffgeerling.com/blog/2019/a2-class-microsd-cards-offer-no-better-performance-raspberry-pi)
[Raspberry Pi microSD card performance comparison - 2019 | Jeff Geerling](https://www.jeffgeerling.com/blog/2019/raspberry-pi-microsd-card-performance-comparison-2019)
[Raspberry Pi microSD follow-up, SD Association fools me twice? | Jeff Geerling](https://www.jeffgeerling.com/blog/2019/raspberry-pi-microsd-follow-sd-association-fools-me-twice) A2 cards required special software handling

## Advanced Format

[Advanced Format - Wikiwand](https://www.wikiwand.com/en/Advanced_Format)
[A Brief Introduction of Advanced Format](http://www.minitool.com/lib/advanced-format.html)

Traditional sector size is 512 byte, with 447 bytes usable data, an storage efficiency of 88%.
AD sectors are 4

[HGST Advanced Format Technology Brief](https://www.hgst.com/sites/default/files/resources/AFtechbrief.pdf) (PDF)
[WD Advanced Format Technology Brief Flyer](http://www.wdc.com/wdproducts/library/Flyer/ENG/2178-771123.pdf) (PDF)

## NRAM

[Fujitsu now making DRAM killer with 1,000x performance boost | InfoWorld](http://www.infoworld.com/article/3114220/storage/fujitsu-now-making-dram-killer-with-1000x-performance-boost.html)

## Wiping/Scrubbing Disk

[Securely wipe disk - ArchWiki](https://wiki.archlinux.org/index.php/Securely_wipe_disk)

[Linux Remove All Partitions / Data And Create Empty Disk - nixCraft](https://www.cyberciti.biz/faq/linux-remove-all-partitions-data-empty-disk/)

[Linux AWS: Find And Delete All Files Securely So That No One Can Recover It Ever - nixCraft](https://www.cyberciti.biz/faq/linux-unix-disk-scrubbing-program-for-cloud/)
[How do I completely wipe my hard drive in Ubuntu?: wipe, srm, scrub, shred and dd. – Linux Hint](https://linuxhint.com/completely_wipe_hard_drive_ubuntu/)

[hard drive - Quickest way to wipe an SSD clean of all its partitions for repartitioning in Linux? - Super User](https://superuser.com/questions/1284450/quickest-way-to-wipe-an-ssd-clean-of-all-its-partitions-for-repartitioning-in-li)
[Solid state drive/Memory cell clearing - ArchWiki](https://wiki.archlinux.org/index.php/Solid_state_drive/Memory_cell_clearing)
[Securely Erasing Your SSD with Linux: A How-To – Techgage](https://techgage.com/article/securely-erasing-your-ssd-with-linux-a-how-to/)

`blkdiscard` for SSDs (which should map to erase), `shred`/`scrub` for spinning disks.

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
