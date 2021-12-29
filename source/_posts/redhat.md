---
title: Redhat
categories:
  - linux
tags:
  - desktop
  - redhat
  - fedora
  - centos
toc: true
date: 2016-04-24 23:25:51
---

[Red Hat Enterprise Linux operating system](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)
[Fedora](https://getfedora.org/) is the official open source version of RHEL, test ground for RHEL features.
[CentOS Project](https://www.centos.org/) is an community fork of RHEL, no Redhat support.
[Korora Project](https://kororaproject.org/) [discontinued](https://kororaproject.org/about/news/time-for-a-break)

## Fedora

Package Management: RPM (`dnf` after 22)

[Fedora (operating system) - Wikiwand](https://www.wikiwand.com/en/Fedora_%28operating_system%29)
[FedoraProject](https://fedoraproject.org/wiki/Fedora_Project_Wiki)

[The relationship between Fedora and Red Hat Enterprise Linux | Red Hat](https://www.redhat.com/en/technologies/linux-platforms/articles/relationship-between-fedora-and-rhel)
[Fedora 21 rolls three versions of Linux into one OS | InfoWorld](http://www.infoworld.com/article/2842575/linux/fedora-21-three-flavors-of-linux-one-os.html)
[Fedora 25 stakes out leading edge, not bleeding edge | InfoWorld](http://www.infoworld.com/article/3143141/linux/fedora-25-stakes-out-leading-edge-not-bleeding-edge.html)

Rawhide is the Fedora's rolling release
[Releases/Rawhide - FedoraProject](https://fedoraproject.org/wiki/Releases/Rawhide?rd=Rawhide)

## CentOS

### Firewall

[CentOS Linux 7 以 firewalld 指令設定防火牆規則教學 - G. T. Wang](https://blog.gtwang.org/linux/centos-7-firewalld-command-setup-tutorial/)
[How To Open A Port In CentOS / RHEL 7 – The Geek Diary](https://www.thegeekdiary.com/how-to-open-a-ports-in-centos-rhel-7/)

[5.3. Viewing the Current Status and Settings of firewalld Red Hat Enterprise Linux 7 | Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/security_guide/sec-viewing_current_status_and_settings_of_firewalld)
[Open firewall port on CentOS 7 - Stack Overflow](https://stackoverflow.com/questions/24729024/open-firewall-port-on-centos-7)

## Package manager

[DNF Package Manager For RPM-Based Linux Distributions - LinuxAndUbuntu - Linux News | Apps Reviews | Linux Tutorials HowTo](http://www.linuxandubuntu.com/home/dnf-package-manager-for-rpm-based-linux-distributions)
[what is different between DNF and yum [Quick review] - Eldernode](https://blog.eldernode.com/what-is-different-between-dnf-and-yum/)

[DNF command on CentOS 8 - what is DNF command - DNF tutorial](https://blog.eldernode.com/dnf-command-on-centos-8/)

EPEL: AUR for CentOS
[Top 8 YUM ThirdParty Repositories for CentOS and RHEL](https://www.tecmint.com/yum-thirdparty-repositories-for-centos-rhel/amp/)

### Copr

[Category:Copr - FedoraProject](https://fedoraproject.org/wiki/Category:Copr)
[Copr Plugin | DNF](http://dnf.baseurl.org/2014/03/19/copr-plugin/)

[Fedora Hosted](https://fedorahosted.org) is Fedora's equivalent of AUR or PPA, it hosts many Copr (Cool Other Package Repo).
[FAQs - Fedora Hosted](https://fedorahosted.org/web/faq)

[UserDocs – copr](https://fedorahosted.org/copr/wiki/UserDocs)
[HowToEnableRepo – copr](https://fedorahosted.org/copr/wiki/HowToEnableRepo)

```sh
sudo dnf copr enable <reponame>
# for remix such as Korora, specify Fedora base
sudo dnf copr enable <reponame> fedora-23-x86_64
```

### Fedy

[Fedy - Tweak your Fedora](http://folkswithhats.org/)
[folkswithhats/fedy: Fedy lets you install multimedia codecs and additional software that Fedora doesn't want to ship, like mp3 support, Adobe Flash, Oracle Java etc., and much more with just a few clicks.](https://github.com/folkswithhats/fedy)
