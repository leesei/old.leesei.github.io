---
title: Linux Security
categories:
  - linux
tags:
  - security
toc: true
date: 2016-05-30 14:06:25
---

[CPU.fail](https://cpu.fail/)

[Linux Kernel Security (SELinux vs AppArmor vs Grsecurity)](http://www.cyberciti.biz/tips/selinux-vs-apparmor-vs-grsecurity.html)
[Security face-off: Red Hat's SELinux vs. SUSE AppArmor, others](http://searchenterpriselinux.techtarget.com/tip/Security-face-off-Red-Hats-SELinux-vs-SUSE-AppArmor-others)
[access control - Comparsion Between AppArmor and Selinux - Information Security Stack Exchange](http://security.stackexchange.com/questions/29378/comparsion-between-apparmor-and-selinux)

[Linux hardening: a 15-step checklist for a secure Linux server | Network World](https://www.networkworld.com/article/3143050/linux/linux-hardening-a-15-step-checklist-for-a-secure-linux-server.html#tk.nww-fsb)
[What is PAM? – Information & Technology – Medium](https://medium.com/information-and-technology/wtf-is-pam-99a16c80ac57)

[Blacklisting modules on Linux | Network World](https://www.networkworld.com/article/3270624/linux/blacklisting-modules-on-linux.html)
[22 essential Linux security commands | Network World](https://www.networkworld.com/article/3272286/open-source-tools/22-essential-security-commands-for-linux.html)

[carpedm20/awesome-hacking: A curated list of awesome Hacking tutorials, tools and resources](https://github.com/carpedm20/awesome-hacking)
[onlurking/awesome-infosec: A curated list of awesome infosec courses and training resources.](https://github.com/onlurking/awesome-infosec)

[pr4jwal/quick-scripts: A collection of my quick and dirty scripts for vulnerability POC and detections](https://github.com/pr4jwal/quick-scripts)
[CISOfy/lynis: Lynis - Security auditing tool for Linux, macOS, and UNIX-based systems. Assists with compliance testing (HIPAA/ISO27001/PCI DSS) and system hardening. Agentless, and installation optional.](https://github.com/CISOfy/lynis)

[How ASLR protects Linux systems from buffer overflow attacks | Network World](https://www.networkworld.com/article/3331199/linux/what-does-aslr-do-for-linux.amp.html)

[Reverse Shell Cheat Sheet | pentestmonkey](http://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet)

> see `docker-ecosystem.md#security`

## Ubuntu Hardening

[Locking Down Linux: Using Ubuntu as Your Primary OS, Part 1 (Physical Attack Defense) « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/locking-down-linux-using-ubuntu-as-your-primary-os-part-1-physical-attack-defense-0185565/)
[Locking Down Linux: Using Ubuntu as Your Primary OS, Part 2 (Network Attack Defense) « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/locking-down-linux-using-ubuntu-as-your-primary-os-part-2-network-attack-defense-0185709/)
[Locking Down Linux: Using Ubuntu as Your Primary OS, Part 3 (Application Hardening & Sandboxing) « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/locking-down-linux-using-ubuntu-as-your-primary-os-part-3-application-hardening-sandboxing-0185710/)
[Locking Down Linux: Using Ubuntu as Your Primary OS, Part 4 (Auditing, Antivirus & Monitoring) « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/locking-down-linux-using-ubuntu-as-your-primary-os-part-4-auditing-antivirus-monitoring-0185572/)

## SELinux

[SELinux Wiki](https://selinuxproject.org/page/Main_Page)
[Security-Enhanced Linux - Wikiwand](https://www.wikiwand.com/en/Security-Enhanced_Linux)

[Your visual how-to guide for SELinux policy enforcement | Opensource.com](https://opensource.com/business/13/11/selinux-policy-guide)
http://people.redhat.com/duffy/selinux/selinux-coloring-book_A4-Stapled.pdf

## AppArmor

[AppArmor - Wikiwand](https://www.wikiwand.com/en/AppArmor)
[AppArmor - Ubuntu Wiki](https://wiki.ubuntu.com/AppArmor)
[Documentation · Wiki · AppArmor / apparmor · GitLab](https://gitlab.com/apparmor/apparmor/wikis/Documentation)
[Ubuntu Manpage: AppArmor - kernel enhancement to confine programs to a limited set of resources.](http://manpages.ubuntu.com/manpages/bionic/man7/apparmor.7.html)

[14.4. Introduction to AppArmor](https://debian-handbook.info/browse/stable/sect.apparmor.html)

```sh
sudo apt-get install apparmor-profiles apparmor-utils
sudo aa-enforce /etc/apparmor.d/*
```

[The Comprehensive Guide To AppArmor: Part 1 – Information & Technology – Medium](https://medium.com/information-and-technology/so-what-is-apparmor-64d7ae211ed)
[Linux Apparmor Security Tool](http://landoflinux.com/linux_apparmor_security.html)

## seccomp

[seccomp - Wikiwand](https://www.wikiwand.com/en/Seccomp)

## Namespace

[Introduction to Linux namespaces - Part 1: UTS | Yet another enthusiast blog!](https://blog.yadutaf.fr/2013/12/22/introduction-to-linux-namespaces-part-1-uts/)
[Introduction to Linux namespaces - Part 2: IPC | Yet another enthusiast blog!](https://blog.yadutaf.fr/2013/12/28/introduction-to-linux-namespaces-part-2-ipc/)
[Introduction to Linux namespaces - Part 3: PID | Yet another enthusiast blog!](https://blog.yadutaf.fr/2014/01/05/introduction-to-linux-namespaces-part-3-pid/)
[Introduction to Linux namespaces - Part 4: NS (FS) | Yet another enthusiast blog!](https://blog.yadutaf.fr/2014/01/12/introduction-to-linux-namespaces-part-4-ns-fs/)
[Introduction to Linux namespaces – Part 5: NET | Yet another enthusiast blog!](https://blog.yadutaf.fr/2014/01/19/introduction-to-linux-namespaces-part-5-net/)
[Docker for your users - Introducing user namespace | Yet another enthusiast blog!](https://blog.yadutaf.fr/2016/04/14/docker-for-your-users-introducing-user-namespace/)

[Namespaces in operation, part 1: namespaces overview [LWN.net]](http://lwn.net/Articles/531114/)
[namespaces(7) - Linux manual page](http://man7.org/linux/man-pages/man7/namespaces.7.html)

## Cgroup

Control groups

## Containers

> see `docker-ecosystem.md#runc`
> see `docker-ecosystem.md#security`

Libcontainer exposes a easy interface to lower level Linux security features to "contain" the environment. It accesses five namespaces -- Process, Network, Mount, Hostname, and Shared Memory -- to work with Linux.

[Containers are Linux – OpenShift Blog](https://blog.openshift.com/containers-are-linux/)

[Linux Containers and the Future Cloud](http://media.wix.com/ugd/295986_d5059f95a78e451db5de3d54f711e45d.pdf) (PDF)
[Tutorial: "Namespaces and CGroups, the basis of Linux containers" (Rami Rosen) | Netdev 1.1](http://www.netdevconf.org/1.1/tutorial-namespaces-and-cgroups-basis-linux-containers-rami-rosen.html) [PDF](http://media.wix.com/ugd/295986_d73d8d6087ed430c34c21f90b0b607fd.pdf)
[FOSDEM 2016 - How containers work in Linux](https://fosdem.org/2016/schedule/event/namespaces_and_cgroups/)

## Rowhammer/Drammer/RAMpage

[Drammer: Deterministic Rowhammer Attacks on Mobile Platforms](https://vvdveen.com/publications/drammer.pdf) PDF
[New Drammer Android Hack lets Apps take Full control (root) of your Phone](https://thehackernews.com/2016/10/root-android-phone-exploit.html)
[vusec/drammer: Native binary for testing Android phones for the Rowhammer bug](https://github.com/vusec/drammer)

[RAMPAGE AND GUARDION](https://rampageattack.com/)
[Every Android Device Since 2012 Impacted by RAMpage Vulnerability](https://www.bleepingcomputer.com/news/security/every-android-device-since-2012-impacted-by-rampage-vulnerability/)

## Dirty COW

[Dirty COW (CVE-2016-5195)](https://dirtycow.ninja/)
[Dirty COW - Wikiwand](https://www.wikiwand.com/en/Dirty_COW)

## Meltdown and Spectre

Two major computer processor security bugs, dubbed Meltdown and Spectre, affect nearly every device made in the last 20 years.

[What Is Speculative Execution? - ExtremeTech](https://www.extremetech.com/computing/261792-what-is-speculative-execution)

[Meltdown and Spectre](https://meltdown.help/)
[Spectre & Meltdown - Computerphile - YouTube](https://www.youtube.com/watch?v=I5mRwzVvFGE)
[Meltdown: the latest news on two major CPU security bugs - The Verge](https://www.theverge.com/2018/1/4/16850516/intel-meltdown-spectre-bug-patch-cpu-security-flaw-news)
[Meltdown, Spectre: The password theft bugs at the heart of Intel CPUs • The Register](https://www.theregister.co.uk/2018/01/04/intel_amd_arm_cpu_vulnerability/)

[What are the Meltdown and Spectre exploits? | Network World](https://www.networkworld.com/article/3245813/security/meltdown-and-spectre-exploits-cutting-through-the-fud.html)
[New Spectre derivative bug haunts Intel processors | Network World](https://www.networkworld.com/article/3261087/cpu-processors/new-spectre-derivative-bug-haunts-intel-processors.html)
[Microsoft, Google: We've found a fourth data-leaking Meltdown-Spectre CPU hole • The Register](https://www.theregister.co.uk/2018/05/21/spectre_meltdown_v4_microsoft_google/)

[speed47/spectre-meltdown-checker: Spectre & Meltdown vulnerability/mitigation checker for Linux](https://github.com/speed47/spectre-meltdown-checker)
[IAIK/meltdown: This repository contains several applications, demonstrating the Meltdown bug.](https://github.com/IAIK/meltdown)

## MDS

[RIDL and Fallout: MDS attacks](https://mdsattacks.com/)
[ZombieLoad Attack](https://zombieloadattack.com/)

[Microarchitectural Data Sampling (aka MDS, ZombieLoad, RIDL & Fallout) explained by Red Hat - YouTube](https://www.youtube.com/watch?v=Oeb-O4yKK2c)
[Buffer the Intel flayer: Chipzilla, Microsoft, Linux world, etc emit fixes for yet more data-leaking processor flaws • The Register](https://www.theregister.co.uk/2019/05/14/intel_sidechannel_vulnerability/)
[Intel CPUs impacted by new Zombieload side-channel attack | ZDNet](https://www.zdnet.com/article/intel-cpus-impacted-by-new-zombieload-side-channel-attack/)

[Intel Side Channel Vulnerability MDS](https://www.intel.com/content/www/us/en/architecture-and-technology/mds.html)
[Deep Dive: Intel Analysis of Microarchitectural Data Sampling](https://software.intel.com/security-software-guidance/insights/deep-dive-intel-analysis-microarchitectural-data-sampling)

[RIP Hyper-Threading? ChromeOS axes key Intel CPU feature over data-leak flaws – Microsoft, Apple suggest snub • The Register](https://www.theregister.co.uk/2019/05/14/intel_hyper_threading_mitigations/)
