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
[Chapter 8. Network File System (NFS)](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Storage_Administration_Guide/ch-nfs.html)

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

[Linux Home Server HOWTO - Network File System](http://www.brennan.id.au/19-Network_File_System.html)
[SettingUpNFSHowTo - Community Help Wiki](https://help.ubuntu.com/community/SettingUpNFSHowTo)
[Linux NFS-HOWTO](http://nfs.sourceforge.net/nfs-howto/)

## Samba

[Samba - opening windows to a wider world](https://www.samba.org/samba/)
[Using Samba](https://www.samba.org/samba/docs/using_samba/toc.html)
[smb.conf](https://www.samba.org/samba/docs/man/manpages/smb.conf.5.html)

### follow symlink

```ini
[global]
follow symlinks = yes
wide links = yes
unix extensions = no
```

```sh
sudo service smbd restart
```
