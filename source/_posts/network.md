---
title: Network
categories:
  - comp
tags:
  - osi
  - ip
  - anycast
  - docker
  - network
toc: true
date: 2016-04-24 16:47:47
---

[OSI model - Wikiwand](https://www.wikiwand.com/en/OSI_model)
[The OSI model explained: How to understand (and remember) the 7 layer network model | Network World](https://www.networkworld.com/article/3239677/lan-wan/the-osi-model-explained-how-to-understand-and-remember-the-7-layer-network-model.html)

[What Is Layer-2 and Why Do We Need It? « ipSpace.net by @ioshints](http://blog.ipspace.net/2015/04/what-is-layer-2-and-why-do-we-need-it.html)

[Bridging and Routing: is there a difference? « ipSpace.net by @ioshints](http://blog.ipspace.net/2010/07/bridging-and-routing-is-there.html)
[Bridging and Routing, Part II « ipSpace.net by @ioshints](http://blog.ipspace.net/2010/07/bridging-and-routing-part-ii.html)

[IP addresses & routing - Julia Evans](https://jvns.ca/blog/2018/07/24/ip-addresses-routing/)

[Lecture OSI and TCP/IP Models - YouTube](https://www.youtube.com/watch?v=Pje0l5r7_lk)
[The OSI Model Demystified - YouTube](https://www.youtube.com/watch?v=HEEnLZV2wGI)

[Here comes 5Gbps networking over standard cables | Ars Technica UK](http://arstechnica.co.uk/gadgets/2016/09/5gbps-ethernet-standard-details-8023bz/)

[科普文：详解音视频直播中的低延时](https://mp.weixin.qq.com/s?__biz=MzUxMzcxMzE5Ng==&mid=2247488746&idx=1&sn=f4e7471c1886347d663f81f97399cd3e&chksm=f951a1a9ce2628bf7d6b48d6a9ca2647cd3d7eb45a335f997ecbfb962c5832b368918fa13d0c&scene=27#wechat_redirect)

[Computer Networks: Crash Course Computer Science #28 - YouTube](https://www.youtube.com/watch?v=3QhU9jd03a0)
[The Internet: Crash Course Computer Science #29 - YouTube](https://www.youtube.com/watch?v=AEaKrq3SpW8)
[The World Wide Web: Crash Course Computer Science #30 - YouTube](https://www.youtube.com/watch?v=guvsH5OFizE)

[Video Notes: Tanenbaum, Wetherall Computer Networks 5e](http://media.pearsoncmg.com/ph/streaming/esm/tanenbaum5e_videonotes/tanenbaum_videoNotes.html)

## IP and Subnet

[RFC 1918 - Address Allocation for Private Internets](https://tools.ietf.org/html/rfc1918)
[RFC 4632 - Classless Inter-domain Routing (CIDR): The Internet Address Assignment and Aggregation Plan](https://tools.ietf.org/html/rfc4632)

[Reserved IP addresses - Wikiwand](https://www.wikiwand.com/en/Reserved_IP_addresses)
[Classless Inter-Domain Routing - Wikiwand](https://www.wikiwand.com/en/Classless_Inter-Domain_Routing)

[What is CIDR Notation?](http://whatismyipaddress.com/cidr)
[What is CIDR (Classless Inter-Domain Routing or supernetting)? - Definition from WhatIs.com](http://searchnetworking.techtarget.com/definition/CIDR)

[ExamPointers.com - Online IPv4 Subnet Mask Calculator](http://ccna.exampointers.com/subnet.phtml)
[CIDR Utility Tool | IP Address Guide](http://www.ipaddressguide.com/cidr)

## DHCP

[Why DHCP's days might be numbered | Network World](https://www.networkworld.com/article/3297800/internet/why-dhcps-days-might-be-numbered.html)

## Routing

[Configuring Multiple Default Routes in Linux | Darien Kindlund's Blog](https://kindlund.wordpress.com/2007/11/19/configuring-multiple-default-routes-in-linux/)
[Two Default Gateways on One System - Thomas-Krenn-Wiki](https://www.thomas-krenn.com/en/wiki/Two_Default_Gateways_on_One_System)
[LiNUX Horizon - Linux Advanced Routing mini HOWTO](http://www.linuxhorizon.ro/iproute2.html)

[linux - Is it possible to have multiple default gateways for outbound connections? - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/345862/is-it-possible-to-have-multiple-default-gateways-for-outbound-connections)
`ip route add` commands can be added with `post-up` directive to `/etc/network/interfaces`

[linux - What is the difference between "route" and "ip route"? - Server Fault](https://serverfault.com/questions/523388/what-is-the-difference-between-route-and-ip-route)

## TCP

[How TCP Sockets Work](https://eklitzke.org/how-tcp-sockets-work)

TCP states
Disconnected but still holding socket
[What Is a Listening Port? | It Still Works](https://itstillworks.com/listening-port-8721837.html)

[TCP 的那些事儿（上） | | 酷 壳 - CoolShell](https://coolshell.cn/articles/11564.html)
[TCP 的那些事儿（下） | | 酷 壳 - CoolShell](https://coolshell.cn/articles/11609.html)

## Anycast

> or "Addressing methods"?

[Anycast - Wikiwand](https://www.wikiwand.com/en/Anycast)
[A Brief Primer on Anycast](https://blog.cloudflare.com/a-brief-anycast-primer/)
[Load Balancing without Load Balancers](https://blog.cloudflare.com/cloudflares-architecture-eliminating-single-p/)
[What is Anycast and How it works](http://www.slashroot.in/what-anycast-and-how-it-works)

## Reliable UDP

[draft-ietf-sigtran-reliable-udp-00 - RELIABLE UDP PROTOCOL](https://tools.ietf.org/html/draft-ietf-sigtran-reliable-udp-00)

[怎么让不可靠的 UDP 可靠？](https://mp.weixin.qq.com/s?__biz=MzIwMzg1ODcwMw==&mid=2247487188&idx=1&sn=2e1280a6a672d66b4f87c036a6c44ca6&chksm=96c9b8b4a1be31a2aca62731912f594f380bf3b4326797a2a013c54e7789095bf5721b5f55f1#rd)
[Reliable UDP (RUDP): The Next Big Streaming Protocol? - Streaming Media Magazine](http://www.streamingmedia.com/Articles/Editorial/Featured-Articles/Reliable-UDP-%28RUDP%29-The-Next-Big-Streaming-Protocol-85316.aspx)

## Router

> see `router.md`

## SDN

[SDN dilemma: Linux kernel networking vs. kernel bypass | InfoWorld](http://www.infoworld.com/article/3189664/networking/sdn-dilemma-linux-kernel-networking-vs-kernel-bypass.html)
[What’s the difference between SDN and NFV? | Network World](http://www.networkworld.com/article/3206709/lan-wan/what-s-the-difference-between-sdn-and-nfv.html)

[What Is SD-WAN & Why You Should Care ? – codeburst](https://codeburst.io/sd-wan-for-business-a-new-wan-is-here-6fe8e198df4d)

## VPN

[WireGuard: fast, modern, secure VPN tunnel](https://www.wireguard.io/) kernel VPN module
[howto/wireguard](https://dn42.net/howto/wireguard)
[FLOSS Weekly 468 WireGuard](https://twit.tv/shows/floss-weekly/episodes/468)

[OpenVPN - Open Source VPN](https://openvpn.net/)
[howto/openvpn](https://dn42.net/howto/openvpn)

[Nyr/openvpn-install: OpenVPN road warrior installer for Debian, Ubuntu and CentOS](https://github.com/Nyr/openvpn-install/)
[How To Create Your Own VPN Server - YouTube](https://www.youtube.com/watch?v=6w3DquIB8yE)

[10 Free Proxy Servers for Anonymous Web Browsing](https://www.fossmint.com/free-proxy-for-anonymous-web-browsing/)

## Firewall

[netfilter/iptables project homepage - Documentation about the netfilter/iptables project](http://netfilter.org/documentation/)

[iptables - ArchWiki](https://wiki.archlinux.org/index.php/Iptables)
[iptables - Debian Wiki](https://wiki.debian.org/iptables)
[An IPTABLES Primer | Daniel Miessler](https://danielmiessler.com/study/iptables/)
[How To Configure iptables Firewall In Linux - LinuxAndUbuntu - Linux News | Apps Reviews | Linux Tutorials HowTo](http://www.linuxandubuntu.com/home/how-to-configure-iptables-firewall-in-linux)

[Uncomplicated Firewall - Wikiwand](https://www.wikiwand.com/en/Uncomplicated_Firewall) Manages `iptables` rules
[UncomplicatedFirewall - Ubuntu Wiki](https://wiki.ubuntu.com/UncomplicatedFirewall)
[Uncomplicated Firewall - ArchWiki](https://wiki.archlinux.org/index.php/Uncomplicated_Firewall)
[Ubuntu Manpage: ufw - program for managing a netfilter firewall](http://manpages.ubuntu.com/manpages/bionic/man8/ufw.8.html)
[How to Configure a Firewall with UFW](https://www.linode.com/docs/security/firewalls/configure-firewall-with-ufw/)
[A Guide to the Uncomplicated Firewall (UFW) for Linux](https://medium.com/@jasonrigden/a-guide-to-the-uncomplicated-firewall-ufw-for-linux-570c3774d7f4)

[Open Port Check Tool - Test Port Forwarding on Your Router](https://www.yougetsignal.com/tools/open-ports/)

## BPF

[BPF · Linux kernel code execution engine](https://facebookmicrosites.github.io/bpf/)
[Berkeley Packet Filter - Wikiwand](https://www.wikiwand.com/en/Berkeley_Packet_Filter)

[A thorough introduction to eBPF [LWN.net]](https://lwn.net/Articles/740157/)
[BPF comes to firewalls [LWN.net]](https://lwn.net/Articles/747551/)
[eBPF: One Small Step](http://www.brendangregg.com/blog/2015-05-15/ebpf-one-small-step.html)
[An intro to using eBPF to filter packets in the Linux kernel | Opensource.com](https://opensource.com/article/17/9/intro-ebpf)
[Dive into BPF: a list of reading material](https://qmonnet.github.io/whirl-offload/2016/09/01/dive-into-bpf/)
[bpfilter » ADMIN Magazine](http://www.admin-magazine.com/Archive/2019/50/Bpfilter-offers-a-new-approach-to-packet-filtering-in-Linux)

[Introduction to Cilium — Cilium documentation](http://docs.cilium.io/en/stable/intro/)
[Why is the kernel community replacing iptables with BPF? — Cilium](https://cilium.io/blog/2018/04/17/why-is-the-kernel-community-replacing-iptables/)
[Linux BPF Superpowers](http://www.brendangregg.com/blog/2016-03-05/linux-bpf-superpowers.html)

[zoidbergwill/awesome-ebpf](https://github.com/zoidbergwill/awesome-ebpf)
[pratyushanand/learn-bpf](https://github.com/pratyushanand/learn-bpf)
[iovisor/bcc: BCC - Tools for BPF-based Linux IO analysis, networking, monitoring, and more](https://github.com/iovisor/bcc)

[The One About eBPF | TechSNAP 388 | Jupiter Broadcasting](https://www.jupiterbroadcasting.com/127741/the-one-about-ebpf-techsnap-388/)

## FTP

[Active FTP vs. Passive FTP, a Definitive Explanation](http://slacksite.com/other/ftp.html)

```sh
curl -T uploadfile -u user:passwd ftp://ftp.upload.com/
# upload as
curl -T uploadfile -u user:passwd ftp://ftp.upload.com/myfile
```

## Speed test

[How to Test Internet Connection Speed From the Terminal](https://www.maketecheasier.com/test-internet-connection-speed-from-terminal/)

[Speedtest by Ookla - The Global Broadband Speed Test](http://www.speedtest.net/run) with region selection
[Internet Speed Test | Fast.com](https://fast.com/en/)by Netflix

[OFCA Broadband Performance Test](http://speedtest.ofca.gov.hk/) web version requires Flash

## Physical layer

[How do internet cables distinguish between no data being sent and 0 bits being sent? - Quora](https://www.quora.com/How-do-internet-cables-distinguish-between-no-data-being-sent-and-0-bits-being-sent)

[Physical layer: signals, waves and transmission types - ICTShore.com](https://www.ictshore.com/free-ccna-course/physical-layer-signals/)
[Phase-locked loop - Wikiwand](https://www.wikiwand.com/en/Phase-locked_loop)
[Unipolar encoding - Wikiwand](https://www.wikiwand.com/en/Unipolar_encoding)

## Scaling

[Dropbox traffic infrastructure: Edge network – Dropbox Tech Blog](https://blogs.dropbox.com/tech/2018/10/dropbox-traffic-infrastructure-edge-network/amp/)
[Optimizing web servers for high throughput and low latency | Dropbox Tech Blog](https://blogs.dropbox.com/tech/2017/09/optimizing-web-servers-for-high-throughput-and-low-latency/)

---

## TODO

[10 Most important open source networking projects | Network World](http://www.networkworld.com/article/3203369/lan-wan/10-most-important-open-source-networking-projects.html)

There's an open source insurgence happening in the networking industry.

Increasing demands on the network to scale to unprecedented levels and at the same time become more customized to specific use cases has led to the emergence of  open source projects to support them.

**MORE AT NETWORK WORLD**: [Top 7 Linux IoT projects](http://www.networkworld.com/article/3200272/internet-of-things/the-top-7-linux-iot-projects.html) +

In many cases networking vendors are using these open source projects as the basis for enterprise networking products. In other cases, they are the core underlying technology for some of the largest networks in the world.

"Network transformation is moving into a phase of production-ready deployments," says Arpit Joshipura, general manager of networking at the Linux Foundation. "As that happens, we believe there's a major disruption happening in open source networking, and it's becoming a fundamental building block for next-generation IT and next-gen networks for carriers."

Here are 10 of the most important open source projects in the networking industry.

**CORD**

The idea behind the Central Office Re-architected as a Data Center (CORD) project is that central offices of telecommunications and service provider environments typically include myriad hardware and software for controlling many different aspects of networks. CORD aims to create a software-defined operating platform for central offices that uses commodity servers, white box switches and open source software.

**[More information on CORD](http://opencord.org/)**

**FD.io**

FD.io stands for Fast Data -- input/output, and it's an open source project made up of various open source libraries all with the goal of accelerating data efficiency in networking. FD.io focuses on ensuring open source networking deployments have the highest throughput, lowest latency and most efficient IO services. There are a handful of focus areas for FD.io, including a Vector Packet Processing (VPP) project donated by Cisco, and others focused on hardware acceleration, programmability and integration with other systems. FD.io components are typically used in conjunction with other projects such as OpenDaylight, OpenNFV, and OpenStack. The components are designed to work on a variety of generic hardware, including x86, ARM and PowerPC. Platinum members of the FD.io project include Cisco, Ericsson and Intel.

**[More information on FD.io](https://fd.io/)**

**Mano**

Mano is meant to be an open source software project for management and orchestration of software-defined networks and network function virtualization. It focuses on core areas such as supporting multi-site deployments, onboarding of NFVs, virtual network funcntions packaging, upgrading and installations on an SDN, creating development environments, service modeling and being platform-aware. The European Telecommunications Standards Institute (ETSI) houses the project.

**[More information on ETSI open source Mano](https://osm.etsi.org/)**

**ONAP**

The Open Networking Automation Platform, or ONAP, is the combination of two projects: ECOMP, which was donated by AT&T, and the Open-O Orchestration platform. ONAP is primarily targeted at providing an open source automation and orchestration platform for service providers, particularly telecommunication vendors, to run SDNs and offer virtual network functions. ONAP's more than 10 million lines of code include processes for onboarding networks and network functions, orchestration, control, inventory and maintaining policy across the network.

**[More information on ONAP](https://www.onap.org/)**

**ONOS**

The Open Networking Operating System (ONOS) describes itself as an open source carrier-grade software defined networking (SDN) operating system. It's geared at service providers who are looking for an open source operating system on which to build or run their SDN software.

**[More information about ONOS](http://onosproject.org/)**

**OpenDaylight **

Founded in 2013, this modular open source software defined networking (SDN) controller is housed within the Linux Foundation. It is fundamentally a series of software packages that users can use bits and parts of -- or the whole thing -- to create software controllers for their virtual networks. Many vendorss use or support the open source code in their commercial SDN controllers, including Brocade, HPE, Ericsson, Serro and Inocybe. The OpenDaylight Foundation, which manages the development of the source code for the Linux Foundation, says there are 27 OpenDaylight User Groups around the world.

[More information about OpenDaylight](https://www.opendaylight.org/)

**OpenFlow**

OpenFlow is credited with being the first standard communications protocol in the software defined networking market. Developed at Stanford University, the communications standards in OpenFlow dictate how the control plane can communicate with the forwarding data plane in SDN environments. While OpenFlow itself is not an open source project, the standards developed by OpenFlow and its organizer the Open Networking Foundation are some of the most important standards in the SDN market. Vendors including Alcatlel-Lucent, Arista, Brocade, Big Switch Networks, Ciena, Cisco, Cumulus, Dell, Ericsson, Extreme Networks, HPE, Huawei, Juniper, Pica8 and many others support OpenFlow standards in at least some of their routers and switches.

**[More information about OpenFlow](https://www.opennetworking.org/sdn-resources/openflow)**

**OpenNFV **

Network Functions Virtualization (NFV) is the idea of replacing networking applications that used to be in dedicated hardware, such as load balancers and firewalls, and implementing them as software. OpenNFV's goal is to create open source NFV components. OpenNFV has created a reference NFV platform for companies to build and deploy NFV components on, with a goal of providing system-level integration. OpenNFV has primarily been used by service providers and telecommunication vendors. AT&T, Cisco, Dell, Ericsson, HPE, Huawei, IBM, Intel, Juniper, Red Hat and SUSE are among the 53 member companies of the OpenNFV project, which is housed within the Linux Foundation.

**[More information about OpenNFV](https://www.opnfv.org/)**

**OpenSwitch **

OpenSwitch is a modular, Linux-based open source network operating system (NOS) hosted in the Linux Foundation. It is a software platform that provides Layer 2 and 3 capabilities. It's meant to run inside hardware, such as switches and routers, that are designed using specifications from the Open Compute Project. Premier members of the OpenSwitch project include Barefoot Networks, Broadcom, Cavium, Dell EMC, Extreme Networks, Hewlett Packard Enterprise, Mellanox and Snaproute.

[More information on OpenSwitch](http://www.openswitch.net/use/usehome)

**OpenvSwitch **

OpenvSwitch, also known as OVS, is a multi-layer open source virtual switch distributed with an Apache license. OpenvSwitch can be used as a virtual, or software implementation of a networking switch in a networking environment. OVS is used to connect virtual machines within a host or virtual machines across hosts. It also supports common networking protocols, such as OpenFlow as well as standard spanning tree architectures, VLAN tagging and port mirroring.

[More information about OpenvSwitch](http://openvswitch.org/)
