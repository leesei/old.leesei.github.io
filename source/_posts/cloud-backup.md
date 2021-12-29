---
title: "Cloud Backup"
categories:
  - web
tags:
  - null
toc: true
date: 2016-04-02 02:31:56
---

[The Differences Between Cloud Backup, Cloud Storage, and Cloud Sync](https://www.backblaze.com/blog/sync-vs-backup-vs-storage/)
[Object Storage vs. Block Storage Services | DigitalOcean](https://www.digitalocean.com/community/tutorials/object-storage-vs-block-storage-services)
[Is Your Cloud Storage Slow as Shit? – Becoming odrive](https://medium.odrive.com/is-your-cloud-storage-slow-as-shit-f021f5ff5e11)
[Best cloud backup of 2020: Online services to get your data backed up | TechRadar](https://www.techradar.com/best/best-cloud-backup)

## Comparisons

[Carbonite vs. Mozy vs. Backblaze - Best Backup Software](https://www.backblaze.com/best-online-backup-service.html)
[Crashplan vs Backblaze: The Unlimited Cloud Backup Roundup](http://www.cloudwards.net/crashplan-vs-backblaze/)

## Clients

[rclone - rsync for cloud storage](http://rclone.org/)
[RcloneBrowser](https://mmozeiko.github.io/RcloneBrowser/)
[Cyberduck | Libre FTP, SFTP, WebDAV, S3, Backblaze B2 & OpenStack Swift browser for Mac and Windows](https://cyberduck.io/)
[Cyberduck Alternatives and Similar Software - AlternativeTo.net](http://alternativeto.net/software/cyberduck/)
[Duplicacy](https://duplicacy.com/) A new generation cross-platform cloud backup tool
[duplicity: Main](http://duplicity.nongnu.org/)
[andrewgaul/s3proxy: Access other storage backends via the S3 API](https://github.com/andrewgaul/s3proxy)

[Syncthing](https://syncthing.net/) sync between your machines
[Sync files across multiple devices with Syncthing | Opensource.com](https://opensource.com/article/20/1/sync-files-syncthing)
[Control your data with Syncthing: An open source synchronization tool | Opensource.com](https://opensource.com/article/18/9/take-control-your-data-syncthing)
[Synchronize Files Between Multiple Systems With Syncthing - OSTechNix](https://ostechnix.com/synchronize-files-between-multiple-systems-with-syncthing/)
[Linux Fu: Keep In Sync | Hackaday](https://hackaday.com/2020/07/23/linux-fu-keep-in-sync/)

## odrive

[odrive - Sync all cloud storage in one place](https://odrive.com/)
[Setup Your odrive](https://docs.odrive.com/docs)

[odrive Sync Agent](https://docs.odrive.com/docs/odrive-sync-agent)

[odrive CLI](https://docs.odrive.com/docs/odrive-cli)
[Sync CLIent ‘Magic’ – Becoming odrive](https://medium.odrive.com/sync-client-magic-602d858731de)

```sh
odrive-agent &
odrive authentication <TOKEN>

odrive mount ~/odrive
# sync is pulling from cloud to local
# `.cloud` corresponds to a file, `.cloudf` corresponds to a folder
odrive sync ~/odrive/Box.cloudf  # became `~/odrive/Box/`
# sync all folders
find ~/odrive/Box/ -name '*.cloudf' -print0 | xargs -0 -n1 -P$(nproc) odrive sync

# refresh is syncing changes/updates
# sync per folder
find ~/odrive/Box/ -type d -print0 | xargs -0 -n1 -P$(nproc) odrive refresh
# sync deleted files
odrive emptytrash
```

## Backblaze

Backblaze uses consumer grade HDDs and publish [Hard Drive Test Data](https://www.backblaze.com/b2/hard-drive-test-data.html) quarterly.

### Storage Pods

[Backblaze Storage Pod](https://www.backblaze.com/b2/storage-pod.html)
[The Evolution and Future of Cloud Storage Pods](https://www.backblaze.com/blog/storage-pod-evolution/)
[Agile Development for Hardware Design - A Case Study](https://www.backblaze.com/blog/designing-the-next-storage-pod/)
[Backblaze Vaults: Zettabyte-Scale Cloud Storage Architecture](https://www.backblaze.com/blog/vault-cloud-storage-architecture/)

### Personal Backup

[Cloud Backup: Easy, Secure Online Backup - Backblaze](https://www.backblaze.com/cloud-backup)
personal unlimited backup for Mac and Windows at $5/mo

### B2

[B2 Cloud Storage: The Lowest Priced Online File Storage](https://www.backblaze.com/b2/cloud-storage.html)
[Backblaze B2: The World’s Lowest Cost Cloud Storage](https://www.backblaze.com/blog/b2-cloud-storage-provider/)
[Introducing Backblaze B2 Lifecycle Rules](https://www.backblaze.com/blog/backblaze-b2-lifecycle-rules/)
[Backblaze B2 and the S3 Compatible API on Cloudflare](https://blog.cloudflare.com/backblaze-b2-and-the-s3-compatible-api-on-cloudflare/amp/)

S3 alternative. The first 10 GB of storage and the first 1GB of download each day is free. 1TB is $5/mo

[How to Backup Linux With Duplicity and Restic](https://www.backblaze.com/blog/backing-linux-backblaze-b2-duplicity-restic/)

[Amazon S3 vs Microsoft Azure vs. B2 Cloud Storage Pricing](https://www.backblaze.com/b2/cloud-storage-providers.html)

#### B2 Clients

Since B2 provides HTTP RESTful API, we can easily write our own client.

[Get the Command-Line Tool](https://www.backblaze.com/b2/docs/quick_command_line.html) [source](https://github.com/Backblaze/B2_Command_Line_Tool)
[B2 Python Pusher](https://www.backblaze.com/b2/docs/b2-python-pusher.html)
[b2sync - like rsync but for B2](https://www.backblaze.com/b2/docs/b2sync.html)

## Digital Ocean Spaces

[An Introduction to DigitalOcean Spaces | DigitalOcean](https://www.digitalocean.com/community/tutorials/an-introduction-to-digitalocean-spaces) S3 compatible object store
[How to Manage DigitalOcean Spaces with s3cmd | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-manage-digitalocean-spaces-with-s3cmd)
[How To Configure s3cmd 2.x To Manage DigitalOcean Spaces | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-configure-s3cmd-2-x-to-manage-digitalocean-spaces)

## Dropbox

[Install Dropbox](https://www.dropbox.com/install)
[Developers - Dropbox](https://www.dropbox.com/developers)
[Reference Guide - Developers - Dropbox](https://www.dropbox.com/developers/reference)

[Re: Dropbox icon stuck on starting - Dropbox Community - 331778](https://www.dropboxforum.com/t5/Files-folders/Dropbox-icon-stuck-on-starting/m-p/331937/highlight/true#M49822)
Beta: xx.3.xx
Stable: xx.4.xx

[Dropbox stuck on indexing / syncing in Windows 10 : dropbox](https://www.reddit.com/r/dropbox/comments/8rae7h/dropbox_stuck_on_indexing_syncing_in_windows_10/)
[Troubleshoot Issues with Selective Sync & Indexing | Dropbox Help](https://help.dropbox.com/installs-integrations/sync-uploads/select-files-to-sync)
[Dropbox Sync Issues | Dropbox Help](https://help.dropbox.com/installs-integrations/sync-uploads/files-not-syncing)

## Google

> add Google Drive

[Here's how Google is overhauling its cloud storage offerings | InfoWorld](http://www.infoworld.com/article/3133344/cloud-computing/heres-how-google-is-overhauling-its-cloud-storage-offerings.html6)

## Mega

[MEGA](https://mega.nz/)
[Megatools - command line client for Mega.nz](https://megatools.megous.com/)
[Mega Cloud Sync in Command Line on Arch Linux | DominicMDominicM](http://dominicm.com/mega-cloud-sync-command-line-arch-linux/)

## Memstore

[Object Storage | Memset](https://www.memset.com/services/object-storage/)
5GB Free Tier, 50GB at £2.01/mo

## CrashPlan

[Online Data Backup - Offsite, Onsite, & Cloud - CrashPlan Backup Software](https://www.code42.com/crashplan/)

## Carbonite

[Cloud backup solutions for home and business | Carbonite](https://www.carbonite.com/)

## SpiderOak

[SpiderOak Secure Software | SpiderOak](https://spideroak.com/)

## FreeFileSync

[#Quick Start - FreeFileSync](https://freefilesync.org/manual.php) also sync locally

---

# Private Cloud Solution

[8 Self-Hosted Cloud Storage Solutions -PCQuest](http://www.pcquest.com/8-self-hosted-cloud-storage-solutions-2/)

[Syncthing](https://syncthing.net/)
[SparkleShare - Self hosted, instant, secure file sync](http://sparkleshare.org/)
[Syncany - Secure file sync software for arbitrary storage backends](https://www.syncany.org/)

[Home | NAS4Free - The Free Network Attached Storage Project](http://www.nas4free.org/)
[ZFSguru.com](http://zfsguru.com/)

[The ZFS NAS Box Thread - Ars Technica OpenForum](http://arstechnica.com/civis/viewtopic.php?p=28752381)

[FileRun - Selfhosted File Sync and Share](https://filerun.com/)

## ownCloud/Nextcloud

[ownCloud.org](https://owncloud.org/)
The founders of the project are dissatisfied with ownCloud.com's management, IP strategy and direction over the project. So they forked the project and created Nextcloud.

[Nextcloud](https://nextcloud.com/)
[Nextcloud](https://github.com/nextcloud) GitHub org

[ownCloud Statement concerning nextcloud](https://owncloud.com/owncloud-statement-concerning-formation-nextcloud-frank-karlitschek/)
[​OwnCloud closes US office, blames Nextcloud | ZDNet](http://www.zdnet.com/article/owncloud-closes-us-office/)
[OwnCloud Has Been Forked By Former Developers, Founder - Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=OwnCloud-Forked-To-NextCloud)
[Speculations on why ownCloud's founder forked its popular product into Nextcloud - TechRepublic](http://www.techrepublic.com/article/owncloud-founder-has-forked-their-product-into-nextcloud/)

## OpenMediaVault

[OpenMediaVault - The open network attached storage solution](http://www.openmediavault.org/)
[Build your own NAS with OpenMediaVault](https://www.howtoforge.com/tutorial/install-open-media-vault-nas/)
[omv-extras.org Joomla](http://omv-extras.org/joomla/)
[omv-extras.org Simple](http://omv-extras.org/simple/)

## FreeNAS

[FreeNAS Storage Operating System | Open Source - FreeNAS - Open Source Storage Operating System](http://www.freenas.org/)
[The Ars NAS distribution shootout: FreeNAS vs NAS4Free | Ars Technica](http://arstechnica.com/information-technology/2014/06/the-ars-nas-distribution-shootout-freenas-vs-nas4free/)
[How-To: Set up a home file server using FreeNAS](http://www.engadget.com/2012/02/01/how-to-set-up-a-home-file-server-using-freenas/)
