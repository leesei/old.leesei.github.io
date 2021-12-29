---
title: Enterprise Server
categories:
  - comp.hardware
tags:
  - enterprise
  - server
toc: true
date: 2016-02-17 11:40:16
---

[Data Center - TechRepublic](http://www.techrepublic.com/blog/data-center/)
[ServeTheHome: Server, Storage, Networking and Open Source Software News and Reviews](https://www.servethehome.com/)

[Desktops as Servers](http://tomoconnor.eu/blogish/desktops-servers/)

[Performance Tuning Guide](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Performance_Tuning_Guide/index.html)

[Hyper-converged infrastructure starts to offer greater choice](https://searchconvergedinfrastructure.techtarget.com/podcast/Hyper-converged-infrastructure-starts-to-offer-greater-choice) tightly integrates storage, compute, networking and server virtualization resources in the same box

[如何保护你在服务器里的数据？How Do We Protect Data in Servers?丨科普丨冷知识丨柴知道 ChaiKnows - YouTube](https://www.youtube.com/watch?v=NYW79ucOrEU)
[Arctic Vault | GitHub Archive Program](https://archiveprogram.github.com/arctic-vault/)

## Processors

**4 Categories**
Standard: cost-effective CPUs with moderate performance
Advanced: CPUs offering the highest performance for most applications
High Core Count: ideal for highly multi-threaded applications; CPUs providing the highest number of processor cores (sometimes sacrificing clock frequency in favor of core count)
Frequency Optimized: ideal for non-parallel/single-threaded applications; CPUs with the highest clock speeds (sacrificing number of cores in order to provide the highest frequencies)

[In-Depth Comparison of Intel Xeon E5-2600v2 "Ivy Bridge" Processors | Microway](https://www.microway.com/knowledge-center-articles/in-depth-comparison-and-analysis-intel-xeon-e5-2600v2-ivy-bridge-processor/)
[Detailed Specifications of the Intel Xeon E5-2600v3 "Haswell-EP" Processors | Microway](https://www.microway.com/knowledge-center-articles/detailed-specifications-intel-xeon-e5-2600v3-haswell-ep-processors/)
[Detailed Specifications of the Intel Xeon E5-2600v4 "Broadwell-EP" Processors | Microway](https://www.microway.com/knowledge-center-articles/detailed-specifications-of-the-intel-xeon-e5-2600v4-broadwell-ep-processors/)
[Intel Xeon E5-2600 V4 "Broadwell-EP" Launched - First Benchmarks](https://www.servethehome.com/intel-xeon-e5-2600-v4-broadwell-ep-launched/)

[Specifications of the Intel Xeon E5-4600 v3 "Haswell-EP" CPUs](https://www.microway.com/knowledge-center-articles/detailed-specifications-intel-xeon-e5-4600-v3-haswell-ep-processors/)
[In-Depth Comparison of Intel Xeon E5-4600v2 "Ivy Bridge" Processors | Microway](https://www.microway.com/knowledge-center-articles/depth-comparison-intel-xeon-e5-4600v2-ivy-bridge-processors/)

## Storage

> see `distributed-file-systems.md`

[Storage Technology information, news and tips - SearchStorage](https://searchstorage.techtarget.com/)

[Enterprise Drives: Fact or Fiction?](https://www.backblaze.com/blog/enterprise-drive-reliability/) Backblaze built their solution on consumer grade SATA HDDs
[A Look at How Backblaze Buys Petabytes of Hard Drive Storage](https://www.backblaze.com/blog/how-backblaze-buys-hard-drives/)

> see `cloud-backup.md#storage-pods`

[What is storage volume? - Definition from WhatIs.com](https://searchstorage.techtarget.com/definition/volume)
[Capabilities and limitations of thin-provisioned capacity](https://searchstorage.techtarget.com/tip/Capabilities-and-limitations-of-thin-provisioned-capacity)

### Interface/Protocol

SAS (serial attached SCSI) and SATA uses the same connector. Its the protocol over the wire that contributes to the different in characteristics. In terms of reliability and error rate SAS disks are much better compared to the old SATA disks.

[SAS and SATA for Server Storage](http://www.tomshardware.co.uk/hdd-enterprise-storage-3.5,review-32244.html) !important
[Understanding the difference between SAS, SATA and Near Line SAS Hard drives to select for servers. | Outsourced IT and Cloud Computing Technology](http://blog.kurtiskent.com/2012/05/understanding-difference-between-sas.html)
[SAS vs Near-line SAS vs SATA - Server Fault](http://serverfault.com/questions/394590/sas-vs-near-line-sas-vs-sata)
[Why is Enterprise Storage so expensive? - Server Fault](http://serverfault.com/questions/263694/why-is-enterprise-storage-so-expensive/)
[[SOLVED] Enterprise SATA vs NL SAS (WD RE drives) - Data Storage - Spiceworks](https://community.spiceworks.com/topic/752371-enterprise-sata-vs-nl-sas-wd-re-drives)

[What is nearline storage? - Definition from WhatIs.com](https://searchstorage.techtarget.com/definition/near-line-storage)

[What is iSCSI (Internet Small Computer System Interface)? - Definition from WhatIs.com](https://searchstorage.techtarget.com/definition/iSCSI)
[What you need to know about improving iSCSI performance](https://searchstorage.techtarget.com/podcast/iSCSI-performance-An-expert-discussion-with-Dennis-Martin)

### Physical Connection

[Performance Characteristics of Common Network Fabrics | Microway](https://www.microway.com/knowledge-center-articles/performance-characteristics-of-common-network-fabrics/)

[NETGEAR_Whitepaper_10_Gigabit.pdf](http://wiki.networksecuritytoolkit.org/nstwiki/images/NETGEAR_Whitepaper_10_Gigabit.pdf) iSCSI/Ethernet

### Storage Types

Block vs File vs Object

DAS = Direct Attached Storage (drives inside a server node)
HBA = host bus adapter (offload network processing from CPU in FC SAN)
JBOD?

[Storage area network - Wikiwand](http://www.wikiwand.com/en/Storage_area_network)
[Network-attached storage - Wikiwand](http://www.wikiwand.com/en/Network-attached_storage)
[Object storage - Wikiwand](http://www.wikiwand.com/en/Object_storage)

[Introduction to Storage Area Networks](https://www.redbooks.ibm.com/redbooks/pdfs/sg245470.pdf) (PDF)
[How to create a high-availability configuration with Synology NAS - Tutorials - Synology - Network Attached Storage (NAS)](https://www.synology.com/en-us/knowledgebase/tutorials/585)

[storage - What is the difference between SAN, NAS and DAS? - Server Fault](http://serverfault.com/questions/81723/what-is-the-difference-between-san-nas-and-das)
[SAN vs NAS - Difference between a Storage Area Network and Network Attached Storage](http://www.slashroot.in/san-vs-nas-difference-between-storage-area-network-and-network-attached-storage)
[SAN vs. NAS architecture: How do the two storage systems compare?](https://searchstorage.techtarget.com/answer/The-difference-between-SAN-and-NAS)
[What is a SAN and how does it differ from NAS? | Network World](https://www.networkworld.com/article/3256312/storage/what-is-a-san-and-how-does-it-differ-from-nas.html)
[SAN Versus NAS: What's the Difference and What Do You Need? - Zadara Storage](https://www.zadarastorage.com/blog/tech-corner/san-versus-nas-whats-the-difference/)
[Nas-San Comparison](http://www.nas-san.com/differ.html)

Unified storage unit supports SAN and NAS, with FC and iSCSI interface
[What is unified storage (multiprotocol storage)? - Definition from WhatIs.com](https://searchstorage.techtarget.com/definition/unified-storage)
[Unified storage architecture: Different approaches, scalability and capacity-saving tools](https://www.computerweekly.com/podcast/Unified-storage-architecture-Different-approaches-scalability-and-capacity-saving-tools)
[Multiprotocol unified storage systems poised for growth](https://searchstorage.techtarget.com/feature/Multiprotocol-unified-storage-systems-poised-for-growth) survey
[What does unified storage really mean?](https://searchstorage.techtarget.com/feature/What-does-unified-storage-really-mean)
[Defining storage-area networks (SANs), network-attached storage (NAS) and unified storage](https://www.computerweekly.com/news/1356285/Defining-storage-area-networks-SANs-network-attached-storage-NAS-and-unified-storage)

### SAN

- provides access to _blocks_
- typically with fiber connection
- use Fiber Channel (possibly over Ethernet) or iSCSI (SCSI over IP) protocol
- servers treat them like DAS (direct attached storage)
- file system is managed by servers
- only one client has access to the resource

[SAN (Storage Area Network) Switches - SearchStorage.com](https://searchstorage.techtarget.com/resources/SAN-technology-and-arrays)
[Storage Area Network School: Table of contents](https://searchstorage.techtarget.com/feature/Storage-Area-Network-School-Table-of-contents)

### NAS

- provides access to _files_
- typically with Ethernet connection (1GbE/10GbE)
- has its own IP address
- server mounts to the NAS
- manages the file system internally (NFS/CIFS/GlusterFS/CephFS)
- multiple clients have access to the resource

[NAS (Network Attached Storage) management news and research - SearchStorage.com](https://searchstorage.techtarget.com/resources/NAS-devices)
[How to buy NAS systems for any organization](https://searchstorage.techtarget.com/buyersguide/How-to-buy-NAS-systems-for-any-organization)
[When purchasing NAS products, look before you leap](https://searchstorage.techtarget.com/tutorial/When-purchasing-NAS-products-look-before-you-leap)
[The ultimate network-attached storage guide](https://searchstorage.techtarget.com/essentialguide/The-ultimate-network-attached-storage-guide)
[Clustered NAS vs traditional NAS solutions](https://www.computerweekly.com/feature/Clustered-NAS-vs-traditional-NAS-solutions)
[NAS tackles enterprise storage](https://searchstorage.techtarget.com/feature/NAS-tackles-enterprise-storage)

[QNAP Storage Performance Best Practice :: Storage ::NAS :: QNAP](https://www.qnap.com/en-us/tutorial/con_show.php?op=showone&cid=172)

### Object Storage

- provides access to _objects_ (files)
- objects are stored in a flat namespace
- objects can be associated with external metadata to provide hierarchy
- optimizations in metadata can cater different use cases

[Object storage resources and information - SearchStorage](https://searchstorage.techtarget.com/resources/Object-storage)
[Why object-oriented storage and interactive apps don't mix](https://searchstorage.techtarget.com/video/Why-object-oriented-storage-and-interactive-apps-dont-mix)

[Object-level storage poised to replace NAS in the enterprise](https://searchstorage.techtarget.com/feature/Object-level-storage-poised-to-replace-NAS-in-the-enterprise)
[Nine reasons object-level storage adoption has increased](https://searchstorage.techtarget.com/tip/Nine-reasons-object-level-storage-adoption-has-increased)

### RAID

[RAID - Wikiwand](http://www.wikiwand.com/en/RAID)
[Standard RAID levels - Wikiwand](https://www.wikiwand.com/en/Standard_RAID_levels)
[Nested RAID levels - Wikiwand](https://www.wikiwand.com/en/Nested_RAID_levels#/RAID_100_.28RAID_10.2B0.29)
[RAID - ArchWiki](https://wiki.archlinux.org/index.php/RAID)

[What is RAID 0, 1, 5, & 10? - YouTube](https://www.youtube.com/watch?v=U-OCdTeZLac)
[RAID levels and benefits explained](https://searchstorage.techtarget.com/answer/RAID-types-and-benefits-explained)
[Understanding RAID Performance at Various Levels - StorageCraft](http://www.storagecraft.com/blog/raid-performance/) !important
[Which Type of RAID Should You Use For Your Servers?](https://www.cloudsavvyit.com/3590/which-type-of-raid-should-you-use-for-your-servers/amp/)

[Why RAID 5 stops working in 2009 | ZDNet](https://www.zdnet.com/article/why-raid-5-stops-working-in-2009/)
[Why RAID 6 stops working in 2019 | ZDNet](http://www.zdnet.com/article/why-raid-6-stops-working-in-2019/)
[RAID 5 or RAID 6: Which should you select? - TechRepublic](http://www.techrepublic.com/blog/the-enterprise-cloud/raid-5-or-raid-6-which-should-you-select/)
[RAID 5 and RAID 6 - RAID Types Utilizing Parity](http://www.freeraidrecovery.com/library/raid-5-6.aspx)
[RAID 5 or RAID 6: Which should you select? - TechRepublic](http://www.techrepublic.com/blog/the-enterprise-cloud/raid-5-or-raid-6-which-should-you-select/)
[RAID 5 vs RAID 10: Recommended RAID For Safety and Performance - nixCraft](https://www.cyberciti.biz/tips/raid5-vs-raid-10-safety-performance.html)
[RAID6 or RAID10 - Synology Forum](https://forum.synology.com/enu/viewtopic.php?t=90274#p340196)
[RAID 6 or RAID 1+0: Which should you choose? - TechRepublic](http://www.techrepublic.com/blog/the-enterprise-cloud/raid-6-or-raid-1-plus-0-which-should-you-choose/)
[RAID 6 vs. RAID 10](https://searchdatabackup.techtarget.com/tip/RAID-6-vs-RAID-10)

[Free RAID Calculator - Caclulate RAID Array Capacity and Fault Tolerance.](http://www.raid-calculator.com/default.aspx)
| RAID level | Min. HDD # | Capacity | Description |
|------------|------------|----------|--------------------------------------|
| 0 | 2 | N | striped volume, increase performance |
| 1 | 2 | N/2 | mirror, provides redundancy |
| 5 | 3 | N-1 | 1 parity (single disk failure) |
| 6 | 4 | N-2 | 2 parity (two disks failure) |

[Write-intent bitmap - Linux Raid Wiki](https://raid.wiki.kernel.org/index.php/Write-intent_bitmap) for faster rebuild/recovery

[Five ways to control RAID rebuild times](https://searchstorage.techtarget.com/tip/Five-ways-to-control-RAID-rebuild-times)
[The RAID rebuild process and its impact on customers](https://searchitchannel.techtarget.com/tip/The-RAID-rebuild-process-and-its-impact-on-customers)
[RAID rebuilds: How do RAID rebuilds work and which is fastest?](https://www.computerweekly.com/feature/RAID-rebuilds-How-do-RAID-rebuilds-work-and-which-is-fastest)
[5 Tips To Speed Up Linux Software Raid Rebuilding And Re-syncing - nixCraft](https://www.cyberciti.biz/tips/linux-raid-increase-resync-rebuild-speed.html)

RAID 0、RAID 10、Single 和 JBOD 組態不支援儲存池之擴充

[Unraid | Unleash Your Hardware](https://unraid.net/)

### LUN

[What is logical unit number (LUN)? - Definition from WhatIs.com](https://searchstorage.techtarget.com/definition/logical-unit-number) SCSI identifier for a drive, partition, or RAID array
[LUN storage and its role in SAN management](https://www.computerweekly.com/news/1349805/LUN-storage-and-its-role-in-SAN-management)
[What is a LUN and why do we need storage LUNs?](https://www.computerweekly.com/answer/What-is-a-LUN-and-why-do-we-need-storage-LUNs)
[What is a LUN and why do we need one?](https://searchstorage.techtarget.com/answer/What-is-a-LUN-and-why-do-we-need-one)

[The mystery behind LUN(Logical Unit Number) | Unixbhaskar's Blog](https://unixbhaskar.wordpress.com/2010/11/17/the-mystery-behind-lunlogical-unit-number/)

---

> Modern NAS appliances can provide unified storage (block + file)

## Dell

Dell PS (Equallogic) (stopped) & SC (Compellent)

[Dell EMC Smart IT - Kinetic Infrastructure Webinar](https://novacast.nova.hk/events/dell_emc_20190417/join?ref=index)
Dynamic RAID with granular pages (not whole volume)

Dell EMC SC Series Hybrid Storage Arrays
Dell EMC SC All-flash Storage Arrays

## QNAP

[Tutorial - QNAP](https://www.qnap.com/en/how-to/tutorial/)
[QNAPedia](https://wiki.qnap.com/wiki/Main_Page)
[FAQ - QNAP](https://www.qnap.com/en/how-to/faq/)
[QNAP Helpdesk -](https://helpdesk.qnap.com/index.php?)
[NAS User Manual](https://www.qnap.com/en/support/con_show.php?cid=11)

[QNAP Systems, Inc. - YouTube](https://www.youtube.com/channel/UCoRW41xIvQXqUW4B4QCqPgg)
[QTS 4.3.5 preview: Enhance your storage to maximize performance - YouTube](https://www.youtube.com/watch?v=Za2smaY5q6M)

[Qnap Advanced Support | Advanced Qnap Technical Support](http://qnapsupport.net/)
[QNAP NAS - Elvanör's Technical Wiki](https://wiki.elvanor.net/index.php/QNAP_NAS)

[TS-EC1680U - Features - QNAP](https://www.qnap.com/en/product/ts-ec1680u) dpms-nas1, dpms-nas2

- Core i3-4150 (E3-1200 v3?) 3.5GHz
- 8GB RAM
- 3U rack server
- 16 x 3.5" SATA 6Gb/s
- 2 x internal mSATA cache ports

TS-859U-RP+ msa-nas1

- Atom D525 1.80 GHz
- 1GB RAM
- 2U rack server
- 8 x 3.5" SATA 3Gb/s

[TS-869U-RP - Features - QNAP](https://www.qnap.com/en/product/ts-869u-rp) msa-nas2

- Atom D2701 2.13 GHz
- 2GB RAM
- 2U rack server
- 8 x 3.5" SATA 6Gb/s

[Expansion Units - QNAP](https://www.qnap.com/en/product/series/expansion)
EJ Series Expansion Units
REXP Series Expansion Units
UX Series Expansion Units

Issues:
Extend storage
Connection between EC1680U and Expansion Unit
Data-in-place upgrade? Migrate disk to Expansion Units?

need flexible config

- all disks in single RAID turns out not a good choice
- can only add drives, not remove
- all drives must be of same capacity
- long rebuild time
  Virtualized storage systems (use a much higher number of drives in the volume group) decreases rebuild time and load?
  50 RAID, JBOD, storage pool
  de-duplication

### App store

[App Center :: QNAP](https://www.qnap.com/en/app_center/)
[Qnapclub Store](https://qnapclub.eu/en)

### Common configs

```
/etc/config/uLinux.conf
/etc/exports
/etc/smb.conf
```

### Enable NFSv4

NFSv4 support is behind a flag, to enable it:

```sh
/sbin/setcfg NFS Enable_V4 TRUE
/etc/init.d/nfs restart
```

Ubuntu client probably need this:

```
echo "NEED_IDMAPD=yes" >> /etc/default/nfs-common
```

### File System Check

[Check File System returned "Examination failed (Cannot unmount disk)." - QNAP NAS Community Forum](https://forum.qnap.com/viewtopic.php?t=123461)

```sh
# check file locks
lsof -n /dev/mapper/cachedev1
lsof +f -- /dev/mapper/cachedev1

/etc/init.d/services.sh stop
/etc/init.d/opentftp.sh stop
/etc/init.d/Qthttpd.sh stop
umount /dev/mapper/cachedev1
e2fsck_64 -f -v -C 0 /dev/mapper/cachedev1
mount /dev/mapper/cachedev1
reboot
```
