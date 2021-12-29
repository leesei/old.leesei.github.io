---
title: DNS
categories:
  - web
toc: true
date: 2015-07-25 22:59:34
tags:
---

[Domain Name System - Wikiwand](https://www.wikiwand.com/en/Domain_Name_System)
[DNS for Rocket Scientists - Contents](http://www.zytrax.com/books/dns/)
[A Comparison of DNS Server Types: How To Choose the Right DNS Configuration | DigitalOcean](https://www.digitalocean.com/community/tutorials/a-comparison-of-dns-server-types-how-to-choose-the-right-dns-configuration)

[DNS Checker - DNS Propagation Check & DNS Lookup](https://www.whatsmydns.net/) check DNS propagation status
[How to Flush DNS Cache in Microsoft Windows, Linux, and Mac OS](https://www.hostinger.com/tutorials/how-to-flush-dns)

[What Happens When Your Domain Expires?](https://www.forbes.com/sites/forbesbusinesscouncil/2020/07/07/what-happens-when-your-domain-expires/)
[What happens when a domain expires? | Hostinger Help Center](https://support.hostinger.com/en/articles/3004042-what-happens-when-a-domain-expires)
[The states of domain expiration and redemption – Hover Help Center](https://help.hover.com/hc/en-us/articles/217282387-The-states-of-domain-expiration-and-redemption)

[RFC 1034 - Domain names - concepts and facilities](https://tools.ietf.org/html/rfc1034)
[RFC 1035 - Domain names - implementation and specification](https://tools.ietf.org/html/rfc1035)
[RFC 2136 - Dynamic Updates in the Domain Name System (DNS UPDATE)](https://tools.ietf.org/html/rfc2136)

[An Introduction to Managing DNS | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-managing-dns)
[Domains and DNS :: DigitalOcean Product Documentation](https://www.digitalocean.com/docs/networking/dns/)
[An Introduction to DNS Terminology, Components, and Concepts | DigitalOcean](https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts)
[What are the differences between Subdomain, Parked Domain and Add-on Domain? | Hostinger Help Center](https://support.hostinger.com/en/articles/1583424-what-are-the-differences-between-subdomain-parked-domain-and-add-on-domain)
[DNS Concepts - Windows applications | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/dns/dns-concepts)
[DNS Zones and Records overview - Azure DNS | Microsoft Docs](https://docs.microsoft.com/en-us/azure/dns/dns-zones-records)
[An Introduction to Learning and Using DNS Records - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/an-introduction-to-learning-and-using-dns-records--cms-24704)
[DNS Explained – How Your Browser Finds Websites | Scotch](https://scotch.io/tutorials/dns-explained-how-your-browser-finds-websites)
[Anatomy of a Linux DNS Lookup – Part I – zwischenzugs](https://zwischenzugs.com/2018/06/08/anatomy-of-a-linux-dns-lookup-part-i/)
[Anatomy of a Linux DNS Lookup – Part II – zwischenzugs](https://zwischenzugs.com/2018/06/18/anatomy-of-a-linux-dns-lookup-part-ii/)
[Hostinger DNS Zone Editor: A Complete Guide for 2021](https://www.hostinger.com/tutorials/how-to-use-hostinger-dns-zone-editor)

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

## Domain Name

[Domain name - Wikiwand](https://www.wikiwand.com/en/Domain_name)
[New TLDs, five years in - Domain Name Wire | Domain Name News](https://domainnamewire.com/2019/02/28/new-tlds-five-years-in/)

## CDN

### Cloudflare

Provides free TLS and CDN service

[How to manage DNS Zone at Cloudflare | Hostinger Help Center](https://support.hostinger.com/en/articles/4410549-how-to-manage-dns-zone-at-cloudflare)
[Managing DNS records in Cloudflare – Cloudflare Help Center](https://support.cloudflare.com/hc/en-us/articles/360019093151-Managing-DNS-records-in-Cloudflare)

Nameservers

```
alexa.ns.cloudflare.com
kevin.ns.cloudflare.com
```

## Price Controls

[Top Stories: Domain name price controls - Domain Name Wire | Domain Name News](https://domainnamewire.com/2020/01/02/top-stories-domain-name-price-controls/)
[Breaking: ICANN and Verisign agree to .com extension with 7% price hikes - Domain Name Wire | Domain Name News](https://domainnamewire.com/2020/03/27/breaking-icann-and-verisign-agree-to-com-extension-with-7-price-hikes/)

## DNS Records

These are the records stored in Authoritative Name Servers

[How to: Edit DNS records (A, AAAA, CNAME, MX, TXT, SRV) – Hover Help Center](https://help.hover.com/hc/en-us/articles/217282457-How-to-Edit-DNS-records-A-CNAME-MX-TXT-and-SRV-Updated-Aug-2015-)
[CName VS A Record - YouTube](https://www.youtube.com/watch?v=WqhgGpv4cKY)
Use CNAME and subdomain to redirect your domain name to an URL
[REDIRECT.CENTER](http://redirect.center/)
[DNS records Types - YouTube](https://www.youtube.com/watch?v=iktrnk3Nd2E)
[DNS Record Types - CompTIA Network+ N10-007 - 1.8 - YouTube](https://www.youtube.com/watch?v=D37RhTJ0ALY)

A
AAAA for IPv6
CNAME
MX
[TXT record - Wikiwand](https://www.wikiwand.com/en/TXT_record)
[SRV record - Wikiwand](https://www.wikiwand.com/en/SRV_record)

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

[DiG HOWTO](https://www.madboa.com/geek/dig/)

[dog — command-line utility in Rust // Lib.rs](https://lib.rs/gh/ogham/dog/dog)

## SNI

Server Name Identification (SNI), a technology used by servers hosting multiple HTTPS websites. SNI sends the domain name during the TLS ‘handshake’ that allows an HTTPS connection to be established, during which the domain name is sent in the clear.

## Resolving domain

[Chris's Wiki :: blog/linux/SystemdResolvedNotes](https://utcc.utoronto.ca/~cks/space/blog/linux/SystemdResolvedNotes)
[nss(5) - Linux manual page](http://man7.org/linux/man-pages/man5/nss.5.html)

## Registrars

[Hover - domain name and email management made simple](https://www.hover.com/)
[Namecheap.com • Cheap Domain Name Registration & Web Hosting](https://www.namecheap.com/)
[香港域名註冊有限公司](https://www.hkdnr.hk/zho/home-zho/)

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

[AnalogJ/lexicon: Manipulate DNS records on various DNS providers in a standardized way.](https://github.com/AnalogJ/lexicon)

### DDNS

[Free Dynamic DNS - No-IP.com - Managed DNS Services](http://www.noip.com/free)
[5 Best Dynamic DNS Providers You Can Lookup for Free Today](http://www.makeuseof.com/tag/5-best-dynamic-dns-providers-can-lookup-free-today/)
[花生壳官网|动态域名|免费域名建站|DDNS|向日葵远程控制|蒲公英路由器-Oray 开放的互联网应用服务引领者](http://www.oray.com/)

[xip.io: wildcard DNS for everyone](http://xip.io/) resolves `[*.]<IP>.xip.io` to `<IP>`.

[Duck DNS](https://www.duckdns.org/)

[DDNS - Debian Wiki](https://wiki.debian.org/DDNS)
[Linux-Fu: Your Own Dynamic DNS | Hackaday](https://hackaday.com/2020/08/25/linux-fu-your-own-dynamic-dns/)

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
[DNS Security and Privacy — Choosing the right provider](https://medium.com/@nykolas.z/dns-security-and-privacy-choosing-the-right-provider-61fc6d54b986)

### DNS over HTTPS (DoH)/DNS over TLSs (DoT)

> use HTTPS/TLS connection for DNS resolution to prevent eavesdropping and tempering from MITM

[DNS over HTTPS is coming whether ISPs and governments like it or not – Naked Security](https://nakedsecurity.sophos.com/2019/04/24/dns-over-https-is-coming-whether-isps-and-governments-like-it-or-not/amp/)
[DNS Over HTTPS Proxy | DOH Proxy](https://facebookexperimental.github.io/doh-proxy/)
[How to enable DNS-over-HTTPS (DoH) in Firefox | ZDNet](https://www.zdnet.com/article/how-to-enable-dns-over-https-doh-in-firefox/)
[DNS-over-HTTPS (DoH) | Public DNS | Google Developers](https://developers.google.com/speed/public-dns/docs/doh/)
[Configuring DNS-Over-HTTPS on Pi-hole - Pi-hole documentation](https://docs.pi-hole.net/guides/dns-over-https/)

[Using NGINX as a DoT or DoH Gateway - NGINX](https://www.nginx.com/blog/using-nginx-as-dot-doh-gateway/amp/)

[LINUX Unplugged 309: The Future is Open](https://linuxunplugged.com/309)

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

[Public DNS | Google Developers](https://developers.google.com/speed/public-dns/)

```
8.8.8.8
8.8.4.4
```

### Cloudflare DNS

[1.1.1.1 — the Internet’s Fastest, Privacy-First DNS Resolver](https://1.1.1.1/)
[Announcing 1.1.1.1: the fastest, privacy-first consumer DNS service](https://blog.cloudflare.com/announcing-1111/)
[CloudFlare DNS is simple, fast and flexible](https://blog.cloudflare.com/cloudflare-dns-is-simple-fast-and-flexible/)

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
