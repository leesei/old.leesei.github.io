---
title: DNS
categories:
  - web
toc: true
date: 2015-07-25 22:59:34
tags:
---

[An Introduction to DNS Terminology, Components, and Concepts | DigitalOcean](https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts)
[A Comparison of DNS Server Types: How To Choose the Right DNS Configuration | DigitalOcean](https://www.digitalocean.com/community/tutorials/a-comparison-of-dns-server-types-how-to-choose-the-right-dns-configuration)
[An Introduction to Learning and Using DNS Records - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/an-introduction-to-learning-and-using-dns-records--cms-24704)

## Verifying Registry

```sh
# this should show new name server
whois yourdomainname.com
# might show info from old name server due to caching
dig -t NS yourdomainname.com
# explicitly use new name server
dig -t NS yourdomainname.com @new-nameserver
# should have yourdomainname in "ANSWER SECTION"
```

[An Introduction to Managing DNS | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/an-introduction-to-managing-dns) (Series)
[How To Set Up a Host Name with DigitalOcean | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-host-name-with-digitalocean)

## Registrars

[Hover - domain name and email management made simple](https://www.hover.com/)
[Namecheap.com • Cheap Domain Name Registration & Web Hosting](https://www.namecheap.com/)
[gTLD Extensions | Discover Your Next Domain - GoDaddy](https://www.godaddy.com/tlds/gtld.aspx)
[Domain name registrar and VPS cloud hosting - Gandi.net](http://www.gandi.net/)
[Domain Names | Search and Register New Domains, Web Hosting, Website Builder, SSL Certificates | Name.com](https://www.name.com/)

[FreeDNS - Free DNS - Dynamic DNS - Static DNS subdomain and domain hosting](http://freedns.afraid.org/)
[Free DNS hosting with freedns.afraid.org](https://coolaj86.com/articles/free-dns-hosting-with-freedns-afraid-org.html)
[JS.ORG | DNS](https://dns.js.org/)
