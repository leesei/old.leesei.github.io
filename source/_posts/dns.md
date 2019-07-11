---
title: DNS
categories:
  - web
toc: true
date: 2015-07-25 22:59:34
tags:
---

[Domain name - Wikiwand](https://www.wikiwand.com/en/Domain_name)
[Domain Name System - Wikiwand](https://www.wikiwand.com/en/Domain_Name_System)
[DNS for Rocket Scientists - Contents](http://www.zytrax.com/books/dns/)
[A Comparison of DNS Server Types: How To Choose the Right DNS Configuration | DigitalOcean](https://www.digitalocean.com/community/tutorials/a-comparison-of-dns-server-types-how-to-choose-the-right-dns-configuration)

[RFC 1034 - Domain names - concepts and facilities](https://tools.ietf.org/html/rfc1034)
[RFC 1035 - Domain names - implementation and specification](https://tools.ietf.org/html/rfc1035)
[RFC 2136 - Dynamic Updates in the Domain Name System (DNS UPDATE)](https://tools.ietf.org/html/rfc2136)

[An Introduction to Managing DNS | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-managing-dns)
[Domains and DNS :: DigitalOcean Product Documentation](https://www.digitalocean.com/docs/networking/dns/)
[An Introduction to DNS Terminology, Components, and Concepts | DigitalOcean](https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts)
[DNS Concepts - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/dns/dns-concepts)
[DNS Zones and Records overview - Azure DNS | Microsoft Docs](https://docs.microsoft.com/en-us/azure/dns/dns-zones-records)
[An Introduction to Learning and Using DNS Records - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/an-introduction-to-learning-and-using-dns-records--cms-24704)
[DNS Explained – How Your Browser Finds Websites | Scotch](https://scotch.io/tutorials/dns-explained-how-your-browser-finds-websites)
[Anatomy of a Linux DNS Lookup – Part I – zwischenzugs](https://zwischenzugs.com/2018/06/08/anatomy-of-a-linux-dns-lookup-part-i/)
[Anatomy of a Linux DNS Lookup – Part II – zwischenzugs](https://zwischenzugs.com/2018/06/18/anatomy-of-a-linux-dns-lookup-part-ii/)

DNS resolution:
Browser cache
Recursive Name Servers (Name Servers in OS's network setting, `/etc/resolv.conf`)
Root Name Server
TLD (gTLD, ccTLD)
Authoritative Name Servers (SOA record)
Secondary Name Server (NS record) for second level domains and sub-domains

[domain name system - Why does DNS work the way it does? - Server Fault](https://serverfault.com/questions/355887/why-does-dns-work-the-way-it-does)
[domain name system - Should we host our own nameservers? - Server Fault](https://serverfault.com/questions/23744/should-we-host-our-own-nameservers)
[How (and Why) I Run My Own DNS Servers – zwischenzugs](https://zwischenzugs.com/2018/01/26/how-and-why-i-run-my-own-dns-servers/)

[DNS in the cloud: Why and why not | Network World](https://www.networkworld.com/article/3273891/hybrid-cloud/dns-in-the-cloud-why-and-why-not.html)
[CloudFlare DNS is simple, fast and flexible](https://blog.cloudflare.com/cloudflare-dns-is-simple-fast-and-flexible/)
[How to Launch a 65Gbps DDoS, and How to Stop One](https://blog.cloudflare.com/65gbps-ddos-no-problem/)

> see `network.md#anycast`

## DNS Records

These are the records stored in Authoritative Name Servers

[How to: Edit DNS records (A, AAAA, CNAME, MX, TXT, SRV) – Hover Help Center](https://help.hover.com/hc/en-us/articles/217282457-How-to-Edit-DNS-records-A-CNAME-MX-TXT-and-SRV-Updated-Aug-2015-)
[CName VS A Record - YouTube](https://www.youtube.com/watch?v=WqhgGpv4cKY)
Use CNAME and subdomain to redirect your domain name to an URL
[REDIRECT.CENTER](http://redirect.center/)

A
AAAA
CNAME
MX
TXT
SRV

[SOA](https://www.wikiwand.com/en/SOA_record) Start of Authority
NS Name Server

### Glue Records

Glue record is used to resolve NS record under the same zone to prevent circular dependencies, they are stored in parent level

[domain name system - What is a glue record? - Server Fault](https://serverfault.com/questions/309622/what-is-a-glue-record)
[Glue Records and Dedicated DNS](https://ns1.com/blog/glue-records-and-dedicated-dns)

## Verifying Domain Name Resolution

```sh
# this should show new name server
whois yourdomainname.com
# might show info from old name server due to caching
dig -t NS yourdomainname.com
dig yourdomainname.com NS
# explicitly use new Domain Nameservers
dig -t NS yourdomainname.com @dnserver
# should have yourdomainname in "ANSWER SECTION"

nslookup google.com
host -v google.com
drill google.com
```

[An Introduction to Managing DNS | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-managing-dns) (Series)
[How To Set Up a Host Name with DigitalOcean | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-host-name-with-digitalocean)

## Registrars

[Hover - domain name and email management made simple](https://www.hover.com/)
[Namecheap.com • Cheap Domain Name Registration & Web Hosting](https://www.namecheap.com/)

[Freenom - A Name for Everyone](https://www.freenom.com/en/index.html?lang=en) many TLDs, at most one year
[Dot TK - Find a new FREE domain](http://www.dot.tk/en/index.html) under Freenom

[gTLD Extensions | Discover Your Next Domain - GoDaddy](https://www.godaddy.com/tlds/gtld.aspx)
[Domain name registrar and VPS cloud hosting - Gandi.net](http://www.gandi.net/)
[Domain Names | Search and Register New Domains, Web Hosting, Website Builder, SSL Certificates | Name.com](https://www.name.com/)
[DNSPod-免费智能 DNS 解析服务商-电信*网通*教育网,智能 DNS](https://www.dnspod.cn/)

[FreeDNS - Free DNS - Dynamic DNS - Static DNS subdomain and domain hosting](http://freedns.afraid.org/)
[Free DNS hosting with freedns.afraid.org](https://coolaj86.com/articles/free-dns-hosting-with-freedns-afraid-org.html)
[JS.ORG | DNS](https://dns.js.org/)

[Namechk | Username, Domain & Trademark Search](https://namechk.com/)

### DDNS

[Free Dynamic DNS - No-IP.com - Managed DNS Services](http://www.noip.com/free)
[5 Best Dynamic DNS Providers You Can Lookup for Free Today](http://www.makeuseof.com/tag/5-best-dynamic-dns-providers-can-lookup-free-today/)
[花生壳官网|动态域名|免费域名建站|DDNS|向日葵远程控制|蒲公英路由器-Oray 开放的互联网应用服务引领者](http://www.oray.com/)

[xip.io: wildcard DNS for everyone](http://xip.io/) resolves `[*.]<IP>.xip.io` to `<IP>`.

## Private DNS Server

> integrating Let's Encrypt client into a private DNS server is cool

[Linux DNS Server - How To Set Up Static or Dynamic DNS for Your Internet Servers](http://www.aboutdebian.com/dns.htm)

[BIND 9 Open Source DNS Server | Internet Systems Consortium](https://www.isc.org/downloads/bind/)
[BIND - Wikiwand](https://www.wikiwand.com/en/BIND)
[Deploying a DNS Server using Docker - SAMEER NAIK](http://www.damagehead.com/blog/2015/04/28/deploying-a-dns-server-using-docker/)
[sameersbn/docker-bind: Dockerize BIND DNS server with webmin for DNS administration](https://github.com/sameersbn/docker-bind)

[miekg/coredns: CoreDNS is a DNS server that runs middleware](https://github.com/miekg/coredns)

[Dnsmasq - network services for small networks.](http://thekelleys.org.uk/dnsmasq/doc.html)

### DNS clients

[nsupdate(8): Dynamic DNS update utility - Linux man page](https://linux.die.net/man/8/nsupdate)
[Dynamic DNS - ArchWiki](https://wiki.archlinux.org/index.php/Dynamic_DNS)

## Secure DNS

[Check if your browser uses Secure DNS, DNSSEC, TLS 1.3, and Encrypted SNI - gHacks Tech News](https://www.ghacks.net/2019/04/29/check-if-your-browser-uses-secure-dns-dnssec-tls-1-3-and-encrypted-sni/)

### DNS over HTTPS (DoH)/DNS over TLSs (DoT)

> use HTTPS/TLS connection for DNS resolution to prevent eavesdropping and tempering from MITM

[DNS over HTTPS is coming whether ISPs and governments like it or not – Naked Security](https://nakedsecurity.sophos.com/2019/04/24/dns-over-https-is-coming-whether-isps-and-governments-like-it-or-not/amp/)

[RFC 7626 - DNS Privacy Considerations](https://tools.ietf.org/html/rfc7626)
[RFC 7858 - Specification for DNS over Transport Layer Security (TLS)](https://tools.ietf.org/html/rfc7858)
[RFC 8310 - Usage Profiles for DNS over TLS and DNS over DTLS](https://tools.ietf.org/html/rfc8310)

### DNSSEC

> ensure the authoritative name servers can be trusted, preventing cache-poisoning attack

[Domain Name System Security Extensions - Wikiwand](https://www.wikiwand.com/en/Domain_Name_System_Security_Extensions)
[How DNSSEC Works | Cloudflare](https://www.cloudflare.com/dns/dnssec/how-dnssec-works/)
[DNSSEC – What Is It and Why Is It Important? - ICANN](https://www.icann.org/resources/pages/dnssec-what-is-it-why-important-2019-03-05-en)

[RFC 4033 - DNS Security Introduction and Requirements](https://tools.ietf.org/html/rfc4033)
[RFC 4034 - Resource Records for the DNS Security Extensions](https://tools.ietf.org/html/rfc4034)
[RFC 4035 - Protocol Modifications for the DNS Security Extensions](https://tools.ietf.org/html/rfc4035)

---

## Public DNS

### Google DNS

[Public DNS  |  Google Developers](https://developers.google.com/speed/public-dns/)

```
8.8.8.8
8.8.4.4
```

### Cloudflare DNS

[1.1.1.1 — the Internet’s Fastest, Privacy-First DNS Resolver](https://1.1.1.1/)
[Announcing 1.1.1.1: the fastest, privacy-first consumer DNS service](https://blog.cloudflare.com/announcing-1111/)

```
1.1.1.1
```

### OpenDNS

[Home Internet Security | OpenDNS](https://www.opendns.com/home-internet-security/)
[OpenDNS > System (also available at http://208.69.38.170/)](http://208.69.38.170/)
Allows you to link IPs to your predefined filters.

```
208.67.222.222
208.67.220.220
```

### Freenom

```
80.80.80.80
80.80.81.81
```
