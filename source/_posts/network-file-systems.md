---
title: "Network File Systems"
date: 2015-05-20 12:15:46
categories:
  - linux
tags:
  - file-system
  - storage
toc: true
---

# Network File System

[Network File System - Wikiwand](https://www.wikiwand.com/en/Network_File_System)  
[Server Message Block - Wikiwand](https://www.wikiwand.com/en/Server_Message_Block)
[Chapter 8. Network File System (NFS)](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Storage_Administration_Guide/ch-nfs.html)

[Network share: Performance differences between NFS & SMB](https://ferhatakgun.com/network-share-performance-differences-between-nfs-smb/)
[Comparison of NFS vs. others - Linux NFS](http://wiki.linux-nfs.org/wiki/index.php/Comparison_of_NFS_vs._others)

SMB2 > AFP ~ CIFS

[Shared Storage with NFS and SSHFS » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/Shared-Storage-with-NFS-and-SSHFS)
[Optimizing Your NFS Filesystem » ADMIN Magazine](http://www.admin-magazine.com/HPC/Articles/Useful-NFS-Options-for-Tuning-and-Management)

[Why You Should Never Again Utter The Word, "CIFS" - Stephen Foskett, Pack Rat](http://blog.fosketts.net/2012/02/16/cifs-smb/)
[From LAN Manager and SMB to CIFS: The Evolution of Prehistoric PC Network Protocols - Stephen Foskett, Pack Rat](http://blog.fosketts.net/2012/03/22/lan-manager-smb-cifs-history/)
[A Fairy Tale of Two Storage Protocols - Stephen Foskett, Pack Rat](http://blog.fosketts.net/2014/09/23/fairy-tale-storage-protocols/)
[vSphere 6: NFS 4.1 Finally Has a Use? - Stephen Foskett, Pack Rat](http://blog.fosketts.net/2015/02/03/vsphere-6-nfs-41-finally/)
[Using NFS to Share Data Between UNIX and Mac OS X - Stephen Foskett, Pack Rat](http://blog.fosketts.net/2015/03/20/using-nfs-to-share-data-between-unix-and-mac-os-x/)

[ServeTheHome: Server, Storage, Networking, and Software Reviews](https://www.servethehome.com/)
[Linux Home Server HOWTO - Network File System](http://www.brennan.id.au/19-Network_File_System.html)
[SettingUpNFSHowTo - Community Help Wiki](https://help.ubuntu.com/community/SettingUpNFSHowTo)
[Linux NFS-HOWTO](http://nfs.sourceforge.net/nfs-howto/)

[NAS / 路由器 / 網絡相關 - YouTube](https://www.youtube.com/playlist?list=PLXvhiMRRLHkN5LwW18zKryt22UbQza4i3) Mostly for Synology products

## FreeNAS/TrueNAS

[TrueNAS](https://www.truenas.com/)

[FreeNAS is Dead Long Live TrueNAS CORE | ServeTheHome](https://www.servethehome.com/freenas-is-dead-long-live-truenas-core/)
[TrueNAS Core will soon replace FreeNAS—and we test the beta – Ars Technica](https://arstechnica.com/gadgets/2020/07/an-easy-mode-for-zfs-we-test-the-truenas-core-12-0-beta/?amp=1)

[What did you DO?? - The "Jellyfish Fryer" All-SSD Server - YouTube](https://www.youtube.com/watch?v=zeAce9pofvk)

## Samba/CIFS/Windows Share Folder

[Samba - ArchWiki](https://wiki.archlinux.org/index.php/Samba)
[Samba - opening windows to a wider world](https://www.samba.org/samba/)
[Using Samba](https://www.samba.org/samba/docs/using_samba/toc.html)
[smb.conf](https://www.samba.org/samba/docs/man/manpages/smb.conf.5.html)
[Samba Troubleshooting » ADMIN Magazine](http://www.admin-magazine.com/Articles/Samba-pitfalls-in-daily-operation)
[Samba Cheatsheet | Programster's Blog](https://blog.programster.org/samba-cheatsheet)

```sh
# samba.service is for AD domain controller
# use this to control the samba share on Linux server
sudo systemctl start nmb.service
```

[linux - Mount cifs Network Drive: write permissions and chown - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/68079/mount-cifs-network-drive-write-permissions-and-chown) Must specify `uid` and `gid` mount option

```sh
sudo mount -t cifs -o rw,username=$USER,password=$PWD,uid=$(id -u),forceuid,gid=$(id -g),forcegid \
    $SAMBA_PATH $TARGET_FOLDER
```

```sh
smbclient $SAMBA_PATH --user $USER
```

### Clearing credentials on Windows

[clear out windows 10 network credentials without rebooting - Super User](https://superuser.com/questions/1069475/clear-out-windows-10-network-credentials-without-rebooting)
[How to Clear Saved Credentials for Network Share or Remote Desktop Connection | Password Recovery](https://www.top-password.com/blog/clear-saved-credentials-for-network-share-or-remote-desktop/)

```
net use \\server\share /delete
klist purge
```

### follow symlink

```ini
[global]
follow symlinks = yes
wide links = yes
unix extensions = no
```

---

[NitroShare](https://nitroshare.net/)
