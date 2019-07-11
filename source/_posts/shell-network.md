---
title: "Shell Tools (Network)"
categories:
  - app
toc: true
date: 2015-09-15 13:55:34
tags:
- netcat
- nmap
- netstat
- tcpdump
- traceroute
- ss
---

Network related shell tools

> see `network.md`
> need to merge?

[7 free networking tools you must have | Network World](https://www.networkworld.com/article/2825879/network-management/7-free-open-source-network-monitoring-tools.html)
[20 quick tips to make Linux networking easier (free PDF) - TechRepublic](https://www.techrepublic.com/resource-library/whitepapers/20-quick-tips-to-make-linux-networking-easier/#ftag=CAD-00-10aag7e)

<!-- more -->

## `iproute2`/`ip`

`iproute2` package deprecates old networking commands in `net-tools` package
[networking:iproute2 [Linux Foundation Wiki]](https://wiki.linuxfoundation.org/networking/iproute2)
[Deprecated Linux networking commands and their replacements | Doug Vitale Tech Blog](https://dougvitale.wordpress.com/2011/12/21/deprecated-linux-networking-commands-and-their-replacements/)

| Deprecated command | Replacement command(s)                                                              |
|--------------------|-------------------------------------------------------------------------------------|
| arp                | ip n (ip neighbor)                                                                  |
| ifconfig           | ip a (ip addr), ip link, ip -s (ip -stats)                                          |
| ipmaddr            | ip maddr                                                                            |
| iptunnel           | ip tunnel                                                                           |
| iwconfig           | iw                                                                                  |
| mii-tool           | ethtool                                                                             |
| nameif             | ip link, ifrename                                                                   |
| netstat            | ss, ip route (for netstat-r), ip -s link (for netstat -i), ip maddr (for netstat-g) |
| route              | ip r (ip route)                                                                     |

[`ip` command cheat sheet](https://access.redhat.com/sites/default/files/attachments/rh_ip_command_cheatsheet_1214_jcs_print.pdf) (PDF)
[How to check your network connections on Linux | Network World](https://www.networkworld.com/article/3262045/linux/checking-your-network-connections-on-linux.html)

### check connection

[Linux – Determine / Find Ethernet Connection Speed](https://www.cyberciti.biz/faq/howto-determine-ethernet-connection-speed/)

```sh
ethtool eno1
```

## `nmap`

[Nmap: the Network Mapper - Free Security Scanner](https://nmap.org/)
[How To Use Nmap to Scan for Open Ports on your VPS | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-nmap-to-scan-for-open-ports-on-your-vps)
[What is Nmap? Why you need this network mapper | Network World](https://www.networkworld.com/article/3296740/lan-wan/what-is-nmap-why-you-need-this-network-mapper.html)

[How to Check Service Running on Specific Port on Linux](https://linoxide.com/linux-how-to/check-service-running-linux-port/)

[Hack Like a Pro: How to Conduct Active Reconnaissance and DOS Attacks with Nmap « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/hack-like-pro-conduct-active-reconnaissance-and-dos-attacks-with-nmap-0146950/)
[Hack Like a Pro: Advanced Nmap for Reconnaissance « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/hack-like-pro-advanced-nmap-for-reconnaissance-0151619/)
[Hack Like a Pro: Using the Nmap Scripting Engine (NSE) for Reconnaissance « Null Byte :: WonderHowTo](https://null-byte.wonderhowto.com/how-to/hack-like-pro-using-nmap-scripting-engine-nse-for-reconnaissance-0158681/)

```sh
# most nmap commands require root privileges
sudo su

# scan ports
nmap -O ${host}
# check port at host
nmap -p 443 192.168.2.254
# check TLS ciphers
nmap -p 443 --script ssl-enum-ciphers ${host}
```

## `netcat`

> `nc` or `ncat` in different distros

[Netcat: the TCP/IP swiss army](http://nc110.sourceforge.net/)
[A Unix Utility You Should Know About: Netcat - good coders code, great coders reuse](http://www.catonmat.net/blog/unix-utilities-netcat/)
[Using netcat as an intercepting proxy | Hawk Host Blog](http://blog.hawkhost.com/2009/12/12/using-netcat-as-an-intercepting-proxy/)
[Netcat – a couple of useful examples | G-Loaded Journal](http://www.g-loaded.eu/2006/11/06/netcat-a-couple-of-useful-examples/)
[Netcat – The Admin’s Best Friend » ADMIN Magazine](http://www.admin-magazine.com/Articles/Netcat-The-Admin-s-Best-Friend)
[Hack Like a Pro: How to Use Netcat, the Swiss Army Knife of Hacking Tools « Null Byte](http://null-byte.wonderhowto.com/how-to/hack-like-pro-use-netcat-swiss-army-knife-hacking-tools-0148657/)
[Linux and Unix Port Scanning With netcat [nc] Command - nixCraft](https://www.cyberciti.biz/faq/linux-port-scanning/)

```sh
# hostA, listen for UDP packet at port 5060
nc -u -l 5060
# hostB, connect to hostA's UDP 5060
# -z test connection only
nc -vzu hostA 5060
```

[Wireshark vs. Netcat for Network Protocol Analysis](https://www.upguard.com/articles/wireshark-vs.-netcat-for-network-protocol-analysis)

## Network Sniffing

[TCPDUMP/LIBPCAP public repository](http://www.tcpdump.org/)
[caesar0301/awesome-pcaptools: A collection of tools developed by other researchers in the Computer Science area to process network traces. All the right reserved for the original authors.](https://github.com/caesar0301/awesome-pcaptools)

[tcpdump - man page - ManKier](https://www.mankier.com/1/tcpdump)
[tcpdump101.com - Build packet capture syntax online](https://tcpdump101.com/)
[Packet Analyzer: 15 TCPDUMP Command Examples](https://www.thegeekstuff.com/2010/08/tcpdump-command-examples)
[Tcpdump 101 | Jacques DALBERA's IT world](https://itworldjd.wordpress.com/2014/02/07/tcpdump/)
[A Quick and Practical Reference for tcpdump | Benjamin Cane](https://bencane.com/2014/10/13/quick-and-practical-reference-for-tcpdump/)
[Masterclass – Tcpdump – Expressions - Packet Pushers](https://packetpushers.net/masterclass-tcpdump-expressions/)

```sh
# dump traffic
sudo tcpdump -vvv -s 0 -nni <interface> -w <file> host <host> and port <port> &
```

```sh
# monitor ARP traffic
sudo tcpdump -i enp3s0 -l -n arp
```

[nicolaka/netshoot: a Docker network troubleshooting swiss-army container](https://github.com/nicolaka/netshoot)

```sh
docker run --net host nicolaka/netshoot ngrep -tpd enp3s0 HTTP
```

### Wireshark

Wireshark can open many dump formats (e.g. `.cap`/`.pcap` from `tcpdump`)

[Wireshark · Go Deep.](https://www.wireshark.org/)
[Track Down Network Problems With Wireshark | PCWorld](http://www.pcworld.com/article/186871/track_down_network_problems_with_wireshark.html)

## `ss`

[Probe Your Linux Sockets With ss | Linux.com | The source for Linux information](https://www.linux.com/learn/intro-to-linux/2017/4/probe-your-linux-sockets-ss)

## `traceroute`

[traceroute - man page - ManKier](https://www.mankier.com/8/traceroute)

[How Does Traceroute Work and Example's of using traceroute command](http://www.slashroot.in/how-does-traceroute-work-and-examples-using-traceroute-command)

## network monitor

[18 commands to monitor network bandwidth on Linux server – BinaryTides](https://www.binarytides.com/linux-commands-monitor-network/)

[bmon - A Powerful Network Bandwidth Monitoring and Debugging Tool for Linux](https://www.tecmint.com/bmon-network-bandwidth-monitoring-debugging-linux/)

```
nload
iftop
```

## `scapy`

[Scapy](https://scapy.net/)

[Data Harvest » Linux Magazine](http://www.linuxpromagazine.com/Online/Features/Packet-Analysis-with-Scapy)

## `netstat`

```sh
# list listening TCP ports
netstat -antlp
lsof -i udp:24000
lsof -i tcp:80
```

[oh-my-zsh/systemadmin.plugin.zsh at master · robbyrussell/oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh/blob/master/plugins/systemadmin/systemadmin.plugin.zsh)

## ethr

[Microsoft/ethr: Ethr is a Network Performance Measurement Tool for TCP, UDP & HTTP.](https://github.com/Microsoft/Ethr)
