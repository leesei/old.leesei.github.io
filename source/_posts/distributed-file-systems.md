---
title: "Distributed File Systems"
date: 2015-05-20 12:15:46
categories:
  - linux
tags:
  - file-system
  - storage
toc: true
---

# Distributed Storage

> see `enterprise-server.md#storage`

[Clustered file system - Wikiwand](https://www.wikiwand.com/en/Clustered_file_system#/Distributed_file_systems)
[List of Distributed file systems - Wikiwand](https://www.wikiwand.com/en/List_of_file_systems#/Distributed_file_systems)
[Comparison of distributed file systems - Wikiwand](https://www.wikiwand.com/en/Comparison_of_distributed_file_systems)

[n1trux/awesome-sysadmin: Distributed Filesystems](https://github.com/n1trux/awesome-sysadmin#distributed-filesystems)

[Distributed Storage: Picking The Right Tool For The Job | SolidFire | Blog](http://www.solidfire.com/blog/distributed-storage-picking-the-right-tool-for-the-job/)
[Distributed Storage Tech Preview [with video] - VMware vSphere Blog - VMware Blogs](https://blogs.vmware.com/vsphere/2012/09/distributed-storage-tech-preview-with-video.html) (2012)
[File storage, block storage, or object storage?](https://www.redhat.com/en/topics/data-storage/file-block-object-storage)
[Distributed File System SBFAQ](http://pl.atyp.us/2015-05-dfs-sbfaq.html)

[Distributed Replicated Block Device - Wikiwand](https://www.wikiwand.com/en/Distributed_Replicated_Block_Device)

[filesystems - Distributed File Systems: GridFS vs. GlusterFS vs Ceph vs HekaFS Benchmarks - Stack Overflow](http://stackoverflow.com/questions/17425153/distributed-file-systems-gridfs-vs-glusterfs-vs-ceph-vs-hekafs-benchmarks)
[Ceph at CERN: A Year in the Life of a Petabyte-Scale Block Storage Service » OpenStack Open Source Cloud Computing Software](https://www.openstack.org/summit/vancouver-2015/summit-videos/presentation/ceph-at-cern-a-year-in-the-life-of-a-petabyte-scale-block-storage-service)

[Testing of several distributed file-systems (HDFS, Ceph and GlusterFS) for supporting the HEP experiments analysis - IOPscience](http://iopscience.iop.org/article/10.1088/1742-6596/513/4/042014/meta) [PDF](http://iopscience.iop.org/article/10.1088/1742-6596/513/4/042014/pdf)
[Performance comparison of distributed file systems, Marian Marinov (1H Ltd) on Vimeo](https://vimeo.com/album/2920922/video/98428204)
[[Linux.conf.au 2013] - grand distributed storage debate glusterfs and ceph going head head - YouTube](https://www.youtube.com/watch?v=JfRqpdgoiRQ)
[Ceph at CERN: A Year in the Life of a Petabyte-Scale Block Storage Service - YouTube](https://www.youtube.com/watch?v=OopRMUYiY5E)

[Performance comparison of Distributed File Systems on 1Gbit networks](http://www.slideshare.net/azilian/performance-comparison)

[Global File System 2 - Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html-single/global_file_system_2/)
[Hortonworks Data Platform - Hortonworks Data Platform](http://docs.hortonworks.com/HDPDocuments/HDP2/HDP-2.3.0/bk_installing_manually_book/content/index.html)

## Ceph

[Ceph (software) - Wikiwand](https://www.wikiwand.com/en/Ceph_%28software%29)
[ceph.com](http://ceph.com/)
Ceph is a flexible object storage system, with four access methods: Amazon S3 RESTful API, CephFS, Rados Block Device and iSCSI gateway.

> Note that ceph has several aspects: `rados` is the underlying object-storage, quite solid and libraries for most languages; `radosgw` is an S3/Swift compatible system; `rbd` is a shared-block-storage (similar to iSCSI, supported by KVM, OpenStack, and others); CephFS is the POSIX-compliant mountable filesystem.

[5 Ceph storage questions answered and explained](https://searchstorage.techtarget.com/feature/5-Ceph-storage-questions-answered-and-explained)
[GlusterFS vs. Ceph: Weighing the open source combatants](https://searchstorage.techtarget.com/tip/GlusterFS-vs-Ceph-Weighing-the-open-source-combatants) The foundation of Ceph is object storage, that of GlusterFS is a file system.

[Red Hat Ceph Storage | Red Hat](http://www.redhat.com/en/technologies/storage/ceph)

[Bootstrap your Ceph cluster in Docker](http://ceph.com/planet/bootstrap-your-ceph-cluster-in-docker/)
[ceph/ceph-docker: Docker files and images to run Ceph in containers](https://github.com/ceph/ceph-docker)

> use Rook

[Ceph Intro and Architectural Overview by Ross Turk - YouTube](https://www.youtube.com/watch?v=OyH1C0C4HzM)
[Ceph Intro & Architectural Overview - YouTube](https://www.youtube.com/watch?v=7I9uxoEhUdY)
[Fundamentals of Ceph by Greg Farnum - YouTube](https://www.youtube.com/watch?v=lG6eeUNw9iI)
[Storage Tutorial - Learning Ceph - YouTube](https://www.youtube.com/watch?v=8GbUaAnOnwo)

## Rook

[Rook.io](https://rook.io/)  
File, Block, and Object Storage Services for your Cloud-Native Environments
Kubernetes Operator for Ceph (and many others)

[Rook’s Framework for Cloud-Native Storage Orchestration](https://blog.rook.io/rooks-framework-for-cloud-native-storage-orchestration-c66278014df7)
[Why you should master Rook for Ceph storage on Kubernetes - Superuser](https://superuser.openstack.org/articles/rook-ceph-kubernetes-quickstart/)
[Ceph storage with Rook Running Ceph on Kubernetes - YouTube](https://www.youtube.com/watch?v=cfwIcHU604Y)
[YVR18-114:Auto-deployment of Ceph cluster with Rook on top of Kubernetes - YouTube](https://www.youtube.com/watch?v=SFG_MYFv6C4) Strong accent
[Auto-Deployment of Ceph Cluster With Rook on Top of Kubernetes - Dennis Chen, Arm - YouTube](https://www.youtube.com/watch?v=gLA9PwclpCA) English interpretation

## GlusterFS

[GlusterFS - Wikiwand](http://www.wikiwand.com/en/GlusterFS)
[Storage for your Cloud. — Gluster](http://www.gluster.org/)
[Gluster Docs](https://docs.gluster.org/en/latest/)
[Architecture - Gluster Docs](https://docs.gluster.org/en/latest/Quick-Start-Guide/Architecture/)

[Red Hat Gluster Storage (formerly Red Hat Storage Server) | Red Hat](http://www.redhat.com/en/technologies/storage/gluster)
[Red Hat Gluster Storage architecture | Red Hat](http://www.redhat.com/en/resources/red-hat-gluster-storage-architecture)

[LAMP Cluster — Distributed filesystem • Websites, Hosting and Friends](http://blog.lavoie.sl/2013/04/lamp-cluster-distributed-filesystem.html)
[GlusterFS performance on different frameworks • Websites, Hosting and Friends](http://blog.lavoie.sl/2013/12/glusterfs-performance-on-different-frameworks.html)

[Demystifying Gluster - GlusterFS For SysAdmins - YouTube](https://www.youtube.com/watch?v=HkBndZOcEA0)

[GlusterFS – JamesCoyle.net](http://www.jamescoyle.net/tag/glusterfs)

## Block Storage

### LINSTOR/DRDB

[LINSTOR | LINBIT-Creates, Removes, & Manages storage volumes](https://www.linbit.com/en/linstor/)
[Distributed Replicated Block Device - Wikiwand](https://www.wikiwand.com/en/Distributed_Replicated_Block_Device)
[DRBD - Linux-HA](http://www.linux-ha.org/wiki/DRBD)

[Linbit Docs – Docs LINBIT](https://docs.linbit.com/docs/users-guide-9.0/)

### iSCSI

Most NAS can expose storage pool as iSCSI LUN over IP.

iSCSI Target: An iSCSI storage server. In this tutorial the target is your NAS.
iSCSI initiator: An iSCSI client. Initiators connect to targets and use their storage.
iSCSI LUN: a portion of storage space that can be utilized by initiators by connecting it to a target. LUNs can be block-based or file-based, though block-based is recommended as it supports more features.

> Warning: Connecting more than one initiator to the same target might result in data loss or damage to the NAS disks.

[How to create and use the iSCSI target service on a QNAP NAS - QNAP (AU)](https://www.qnap.com/en-au/how-to/tutorial/article/how-to-create-and-use-the-iscsi-target-service-on-a-qnap-nas/)

## Object Storage

> see `aws.md#s3`

[kahing/goofys: a high-performance, POSIX-ish Amazon S3 file system written in Go](https://github.com/kahing/goofys)
[s3fs-fuse/s3fs-fuse: FUSE-based file system backed by Amazon S3](https://github.com/s3fs-fuse/s3fs-fuse)

### Minio

[Minio: Private cloud storage](https://minio.io/) self-hosted S3-compatible object storage
[Minio Docs](https://docs.minio.io/)

[The complete guide to attach a Docker volume with Minio on your Docker Swarm Cluster](https://firepress.org/blog/the-complete-guide-to-attach-a-docker-volume-with-minio-on-your-docker-swarm-cluster/)

## OrangeFS

[OrangeFS - Wikiwand](https://www.wikiwand.com/en/OrangeFS)
[OrangeFS](http://orangefs.com/) more info than [orangefs.org](http://www.orangefs.org/)

An open source FS by EMC, the one behind
[EMC Isilon - Wikiwand](http://www.wikiwand.com/en/EMC_Isilon)

## Stratis

[Stratis Storage](https://stratis-storage.github.io/)

[Stratis: Easy local storage management for Linux [LWN.net]](https://lwn.net/Articles/755454/)

## Lustre File system

[Lustre (file system) - Wikiwand](https://www.wikiwand.com/en/Lustre_(file_system%29)
[Lustre](http://lustre.org/)

[The Lustre Distributed Filesystem | Linux Journal](https://www.linuxjournal.com/content/lustre-distributed-filesystem)
[Lustre® File System | OpenSFS: The Lustre File System Community](http://opensfs.org/lustre/)

White papers:  
[Inside The Lustre File System](https://www.seagate.com/files/www-content/solutions-content/cloud-systems-and-solutions/high-performance-computing/_shared/docs/clusterstor-inside-the-lustre-file-system-ti.pdf) by Seagate
[Lustre File System](http://www.csee.ogi.edu/~zak/cs506-pslc/lustrefilesystem.pdf) bu Sum

[Lustre File System - YouTube](https://www.youtube.com/watch?v=oNeYpRDbB2M)

## XtreemFS

[XtreemFS - Wikiwand](http://www.wikiwand.com/en/XtreemFS)
[XtreemFS - Fault-Tolerant Distributed File System](http://www.xtreemfs.org/)

> I tested XtreemFS and found that it does not work well. There are problems like data corruption ([#359][#359]), read errors in degraded mode ([#357][#357]/[#235][#235]), crippled read-only mode ([#358][#358]) etc.; build system is a mess plus XtreemFS depends on old (not updated since 2007) non-free JAR ([#309][#309], [#173][#173]) so XtreemFS is in violation of DFSG and not distributable in Debian. Also I'm not happy about how devs respond to bugs. Finally XtreemFS is written in poor language notorious for inefficient memory management so naturally XtreemFS can't stand against GfarmFS and LizardFS in performance comparison.

[#173]: https://github.com/xtreemfs/xtreemfs/issues/173
[#235]: https://github.com/xtreemfs/xtreemfs/issues/235
[#309]: https://github.com/xtreemfs/xtreemfs/issues/309
[#357]: https://github.com/xtreemfs/xtreemfs/issues/357
[#358]: https://github.com/xtreemfs/xtreemfs/issues/358
[#359]: https://github.com/xtreemfs/xtreemfs/issues/359

## HDFS

## LizardFS

[LizardFS](https://lizardfs.com/)

## seaweedfs

[chrislusf/seaweedfs: SeaweedFS is a simple and highly scalable distributed file system.](https://github.com/chrislusf/seaweedfs)

## OpenEBS

[OpenEBS](https://www.openebs.io/) block storage
[Welcome to OpenEBS Documentation ·](https://docs.openebs.io/)

[OpenEBS · GitHub](https://github.com/openebs)
[Using OpenEBS as a Kubernetes persistent volume – openebs](https://blog.openebs.io/using-openebs-as-kubernetes-persistent-volume-daccae4bdce2)

## Longhorn

[rancher/longhorn-manager: Millions and millions of volumes orchestrated](https://github.com/rancher/longhorn-manager)
[rancher/longhorn: Distributed block storage for Kubernetes](https://github.com/rancher/longhorn)

---

## Resumable HTTP Upload

[Performing a Resumable Upload  |  Drive REST API  |  Google Developers](https://developers.google.com/drive/api/v3/resumable-upload)

[Amazon S3: Multipart Upload | AWS News Blog](https://aws.amazon.com/blogs/aws/amazon-s3-multipart-upload/)
[Amazon S3 Multipart Upload CLI](https://aws.amazon.com/premiumsupport/knowledge-center/s3-multipart-upload-cli/)
[Using the REST API for Multipart Upload - Amazon Simple Storage Service](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingRESTAPImpUpload.html)
[S3 Lifecycle Management Update – Support for Multipart Uploads and Delete Markers | AWS News Blog](https://aws.amazon.com/blogs/aws/s3-lifecycle-management-update-support-for-multipart-uploads-and-delete-markers/)

[Uploading a Large File to Amazon S3](https://www.jtouzi.net/uploading-a-large-file-to-amazon-web-services-s3/)
[Signing Multipart Uploads to S3 Buckets from Scratch](https://medium.com/workday-engineering/signing-multipart-uploads-to-s3-buckets-from-scratch-9df181885b2)
[Security and S3 Multipart Upload | Mingle](https://www.thoughtworks.com/mingle/infrastructure/2015/06/15/security-and-s3-multipart-upload.html)
