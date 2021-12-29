---
title: "Virtualization"
date: 2015-05-10 17:03:12
categories:
  - linux
tags:
  - virtualbox
toc: true
---

---

[Virtualization - Wikiwand](http://www.wikiwand.com/en/Virtualization)

[OSBoxes - Virtual Machines for VirtualBox & VMware](https://www.osboxes.org/)

[Performance Tuning on Virtual Machines | Learning Tree Blog](https://blog.learningtree.com/performance-tuning-on-virtual-machines/)

# Hypervisor

A Hypervisor is also called as a Virtual Machine Monitor (VMM).

[Hypervisor 101: Understanding the Virtualization Market](http://www.datacenterknowledge.com/archives/2012/08/01/hypervisor-101-a-look-hypervisor-market/)

Type 1 hypervisors run directly on the system hardware ("native" or "bare metal" or "embedded").
Type 2 hypervisors run on a host operating system. Most client side VM software contains this kind of hypervisor.
Intel's VTx technology improved the performance of visualization (rendering binary translation and paravirtualization obsolete) and allowed for KVM to be implemented. More importantly, it negated most of the differences between “type-1” and “type-2” hypervisors.

[Ben Armstrong’s Virtualization Blog | Hyper-V Program Manager](https://blogs.msdn.microsoft.com/virtual_pc_guy/)

[Comparison of platform virtualization software - Wikiwand](https://www.wikiwand.com/en/Comparison_of_platform_virtualization_software)
[A Performance Comparison of Hypervisors - VMWare](https://www.vmware.com/pdf/hypervisor_performance.pdf) (PDF)
[Performance Comparison of KVM, VMware and XenServer using a Large Telecommunication Application](https://www.thinkmind.org/download.php?articleid=cloud_computing_2014_5_20_20101) (PDF)
[Will Containers Replace Hypervisors? Almost Certainly! | Cloudscaling](http://cloudscaling.com/blog/cloud-computing/will-containers-replace-hypervisors-almost-certainly/)

## CPU Modes

[Protection ring - Wikiwand](https://www.wikiwand.com/en/Protection_ring)
[Real mode - Wikiwand](https://www.wikiwand.com/en/Real_mode)
[Protected mode - Wikiwand](https://www.wikiwand.com/en/Protected_mode)
[x86 virtualization - Wikiwand](https://www.wikiwand.com/en/X86_virtualization)

## KVM

[Documents - KVM](https://www.linux-kvm.org/page/Documents)
[How to Install Kvm on Ubuntu 20.04 | Linuxize](https://linuxize.com/post/how-to-install-kvm-on-ubuntu-20-04/)

[How to Use Virtualbox VMs on KVM In Linux](https://www.tecmint.com/migrate-virtualbox-vms-into-kvm-vms/amp/)

## Xen

[The Xen Project, the powerful open source industry standard for virtualization.](http://www.xenproject.org/)
[Hypervisor x86 & ARM](http://www.xenproject.org/developers/teams/hypervisor.html)
[Xen & Docker: Made for Each Other! | Xen Project Blog](https://blog.xenproject.org/2014/09/08/xen-docker-made-for-each-other/)

Xen only check handle three things: memory, CPU and interrupts

## VMWare vSphere

[Free VMware vSphere Hypervisor, Free Virtualization (ESXi) | United States](https://www.vmware.com/products/vsphere-hypervisor)

## Hyper-V

[Hyper-V - Wikiwand](https://www.wikiwand.com/en/Hyper-V)
[What Is Hyper-V & How Do You Use It? A Beginner's Guide](https://www.cloudwards.net/hyper-v/)
[Introduction to Hyper-V on Windows 10 | Microsoft Docs](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/)
[Enable Hyper-V on Windows 10 | Microsoft Docs](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v)
[Run virtual machines on Windows 8.1 with Client Hyper‑V: A quick how-to | ZDNet](http://www.zdnet.com/pictures/run-virtual-machines-on-windows-8-1-with-client-hyper-v-a-quick-how-to/)

## QEMU

[QEMU - ArchWiki](https://wiki.archlinux.org/title/QEMU)

[QEMU](https://www.qemu.org/)
[wimpysworld/quickemu: Quickly create and run optimised Windows, macOS and Linux desktop virtual machines.](https://github.com/wimpysworld/quickemu)

[GPU Passthrough with QEMU on Arch Linux | DominicM](http://dominicm.com/gpu-passthrough-qemu-arch-linux/)

## VirtualBox

[VirtualBox - ArchWiki](https://wiki.archlinux.org/index.php/VirtualBox)

[Downloads – Oracle VM VirtualBox](https://www.virtualbox.org/wiki/Downloads)
[Oracle® VM VirtualBox®](https://www.virtualbox.org/manual/)

Also download the extension packs (PUEL, non-commercial only).

### Shared Folder

Requires Guest Additions

[Chapter 4. Guest Additions](https://www.virtualbox.org/manual/ch04.html#sharedfolders)
[Mounting VirtualBox shared folders on Ubuntu Server 16.04 LTS](https://gist.github.com/estorgio/1d679f962e8209f8a9232f7593683265)
[What does "auto-mount" do in VirtualBox shared folder setup? - Super User](https://superuser.com/questions/252257/what-does-auto-mount-do-in-virtualbox-shared-folder-setup)

```sh
sudo usermod -aG vboxsf
```

### Enable 64-bit support

> [virtualbox.org • View topic - I have a 64bit host, but can't install 64bit guests](https://forums.virtualbox.org/viewtopic.php?f=1&t=62339)

To enable 64bit guests, run through the following checklist:

1. Note your exact CPU model or part number, then go online and check its capabilities. The CPU must have 64bit capability and support either Intel or AMD virtualization technologies: VT-x or AMD-v.

2. You usually need to enable VT-x/AMD-v in the host PC BIOS. You need to check with your PC manual or support forum to find out how to boot into the BIOS screen. This is not something we here at the forums can help you with. Once you get there you need to look for something buried in a menu, perhaps in the security category. The option may be called something like "Enable Virtualization Technology". If you see "Virtual Directed I/O" then that is a different thing. Remember to reboot your host OS after making BIOS changes - in this case a full restart from power off is required, just resuming from a hibernated state may not do the job.

3. If (1) and (2) are already taken care of, then make sure that no other host apps are already using VT-x/AMD-v. The usual culprits are system level debuggers, other VM platforms, and some resident anti-virus applications. This has become a particular issue with 64bit Windows desktop and server hosts - especially Win8/Win2k12/Win10, since these may enable Microsoft's Hyper-v VM platform by default: this grabs ownership of VT-x and won't play nice with VirtualBox.

4. When creating a VM, make sure you choose the 64-bit version of the guest OS template in <VM Settings> | General | Basic | Version, e.g. choose "Ubuntu (64 bit)" and not "Ubuntu" or "Ubuntu (32bit)". This has become more important since VirtualBox 4.3.x, because choosing the correct template also allows other modern processor features to be visible to the guest - it's not just about 64bit capability any more.

## Gaming

{% asset_img virtualbox-win7.png %}

Tips for the Guest Windows 7:

- Install Guest Additions
- Switching off Hibernation
- Switching off System Restore ("System protection")
- Reducing the size of the PagingFile ("Advanced system settings")
- Run "Turn Windows features on or off"
- [Trimming down an already installed Win 7.](http://www.overclock.net/t/1198847/trimming-down-an-already-installed-win-7)
- [Sean's Windows 7 Install & Optimization Guide for SSDs & HDDs](http://www.overclock.net/t/1156654/seans-windows-7-install-optimization-guide-for-ssds-hdds)

[Using ESXI for Virtualized Gaming - Justin-Tech Blog](https://blog.justin-tech.com/using-esxi-for-virtualized-gaming/)

[Fixing Audio in Linux Guests | VirtualBox - Without The Sarcasm](https://www.withoutthesarcasm.com/fixing-audio-in-linux-guests-virtualbox/)

---

# The Battle

[Hypervisor "versus" Linux Containers with Docker !](http://www.slideshare.net/fasgoncalves/hypervisor-versus-linux-containers)
[Linux containers vs. VMs: A security comparison | InfoWorld](http://www.infoworld.com/article/3071679/linux/linux-containers-vs-vms-a-security-comparison.html)
[Why Containers Instead of Hypervisors?](http://blog.smartbear.com/web-monitoring/why-containers-instead-of-hypervisors/)
[Containers vs. virtual machines: How to tell which is the right choice for your enterprise | InfoWorld](http://www.infoworld.com/article/3068183/cloud-storage/containers-vs-virtual-machines-how-to-tell-which-is-the-right-choice-for-your-enterprise.html)
[Difference between Hypervisor Virtualization and Container Virtualization](http://www.slashroot.in/difference-between-hypervisor-virtualization-and-container-virtualization)
[What is Docker and why is it so darn popular? | ZDNet](http://www.zdnet.com/article/what-is-docker-and-why-is-it-so-darn-popular/)
[Will Containers Replace Hypervisors? Almost Certainly! | Cloudscaling](http://cloudscaling.com/blog/cloud-computing/will-containers-replace-hypervisors-almost-certainly/)

[Docker vs. VMWare: How Do They Stack Up?](https://www.upguard.com/articles/docker-vs.-vmware-how-do-they-stack-up)
[[Infographic] Docker vs. Vagrant](https://www.upguard.com/articles/docker-vs-vagrant)
[The Difference: Docker vs. Virtualization — munz & more](http://www.munzandmore.com/2015/cc/docker-container-vs-virtualization)

[Containers are not VMs | Docker Blog](https://blog.docker.com/2016/03/containers-are-not-vms/)
[There’s Application Virtualization and There’s Docker | Docker Blog](https://blog.docker.com/2016/04/app-virtualization-docker/)
[So, when do you use a Container or VM? | Docker Blog](https://blog.docker.com/2016/05/vm-or-containers/)

[Containers vs Hypervisors: The Battle Has Just Begun | Linux.com](https://www.linux.com/news/enterprise/cloud-computing/785769-containers-vs-hypervisors-the-battle-has-just-begun)
It's too early so say Containers have won and Hypervisors are obsolete.

---

# Infrastructure

[OpenStack Open Source Cloud Computing Software](http://www.openstack.org/)
[OpenStack Wiki](https://wiki.openstack.org/wiki/Main_Page)

---

# Container

[Docker features and tools by Tom Verelst - YouTube](https://www.youtube.com/watch?v=heBI7oQvHZU)

http://blog.docker.com/2016/02/containers-as-a-service-caas/
https://blog.docker.com/2016/01/webinar-qa-docker-networking/
http://blog.docker.com/2015/12/containerd-daemon-to-control-runc/

[Microcontainers: Iron.io's New Hack to Shrink Docker Containers - The New Stack](http://thenewstack.io/microcontainers-iron-ios-new-hack-shrink-docker-containers/)

[DockerCon EU 2015 - YouTube](https://www.youtube.com/playlist?list=PLkA60AVN3hh87OoVra6MHf2L4UR9xwJkv)

[Docker: Sorry, you're just going to have to learn about it. Today we begin • The Register](http://www.theregister.co.uk/2014/11/28/docker_part_1_the_history_of_docker/)
[Docker, Part 2: Whoa! Spontaneous industry standard! How did they do THAT? • The Register](http://www.theregister.co.uk/2014/12/01/docker_part_2_the_libcontainer_evolution/)
[Part 3: Docker vs hypervisor in tech tussle SMACKDOWN • The Register](http://www.theregister.co.uk/2014/12/02/docker_part_3_containers_versus_hypervisors/)
[Docker part 4: Microsoft CAN'T ignore it. Aux armes, citoyens! • The Register](http://www.theregister.co.uk/2014/12/04/docker_part_4_prognostication_microsoft_and_the_red_wedding/)

---

# Container OS

Runs Docker image in a minimal kernel
Solves the [PID 1 zombie reaping problem](https://blog.phusion.nl/2015/01/20/docker-and-the-pid-1-zombie-reaping-problem/)

[Hyper - Make VM run like Container](https://hyper.sh/)
[About Hyper | About Hyper](https://docs.hyper.sh/)
[Hyper, a Hypervisor-Agnostic Docker Engine - The New Stack](http://thenewstack.io/hyper-a-hypervisor-agnostic-docker-engine/)
Borrow concepts from Kubernetes

[Photon OS™ by VMware®](http://vmware.github.io/photon/) Minimal LXC host
[Photon OS FAQ](http://vmware.github.io/photon/assets/files/photon_faqs.pdf) (PDF)

[CoreOS is Linux for Massive Server Deployments](https://coreos.com/)
[Running Kubernetes on CoreOS](https://coreos.com/kubernetes/docs/latest/)
