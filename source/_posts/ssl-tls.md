---
title: "SSL/TLS"
date: 2015-04-02 16:21:24
categories:
  - web
tags:
  - ssl
  - tls
  - security
toc: true
---

[Transport Layer Security](http://www.wikiwand.com/en/Transport_Layer_Security) (TLS) and its predecessor, [Secure Sockets Layer](https://www.digicert.com/ssl.htm) (SSL), are cryptographic protocols designed to provide communications security over a computer network.

The authentication relied on Certificate Authorities (CA) and a public key infrastructure using [X.509](http://www.wikiwand.com/en/X.509) certificates.
The server register with a CA and sign its public key with the key of CA for a fee. The client, after receiving the public key from server, verifies it with the CA.

[Creating Secure Web Apps: What Every Developer Needs to Know About HTTPS Today | Heroku](https://www.heroku.com/tech-sessions/creating-secure-web-apps)
[Exploring HTTPS With Python – Real Python](https://realpython.com/python-https/)
[What are SSL/TLS Certificates? Why do we Need them? and How do they Work? - YouTube](https://www.youtube.com/watch?v=r1nJT63BFQ0)

[The SSL/TLS Handshake: an Overview – SSL Information and FAQ](https://info.ssl.com/tls-handshake/)
[File:Ssl handshake with two way authentication with certificates.png - Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Ssl_handshake_with_two_way_authentication_with_certificates.png)
[TLS 1.3 » ADMIN Magazine](http://www.admin-magazine.com/Articles/TLS-1.3-and-the-return-of-common-sense)

[HTTPS: an awesome, secure tale (pt 1) | by Omer Goldberg | Bits and Pieces](https://blog.bitsrc.io/https-an-awesome-secure-tale-pt-1-32d2ba5ac0c1)

[ESNI: A Privacy-Protecting Upgrade to HTTPS | Electronic Frontier Foundation](https://www.eff.org/deeplinks/2018/09/esni-privacy-protecting-upgrade-https)
[Server Name Indication - Wikiwand](https://www.wikiwand.com/en/Server_Name_Indication) multi-tenant on the same IP

OpenSSL is a toolkit for the TLS and SSL.

> see `openssl.md`

[HTTPS Is Easy!](https://httpsiseasy.com/)
[Is TLS Fast Yet?](https://istlsfastyet.com/)
[ImperialViolet - Overclocking SSL](https://www.imperialviolet.org/2010/06/25/overclocking-ssl.html) HTTPS is fast since 2010
[ImperialViolet - Public key pinning](https://www.imperialviolet.org/2011/05/04/pinning.html)
[Survival Guide - TLS/SSL and SSL (X.509) Certificates (CA-signed and Self-Signed)](http://www.zytrax.com/tech/survival/ssl.html)
[Rolling out Public Key Pinning with HPKP Reporting — Google Web Updates](https://developers.google.com/web/updates/2015/09/HPKP-reporting-with-chrome-46)
[SSL: it’s hard to do right | The Recompiler](https://recompilermag.com/issues/issue-1/ssl-its-hard-to-do-right/)
[Nick Craver - HTTPS on Stack Overflow: The End of a Long Road](https://nickcraver.com/blog/2017/05/22/https-on-stack-overflow/)

[How the NSA (may have) put a backdoor in RSA’s cryptography: A technical primer | Ars Technica](http://arstechnica.com/security/2014/01/how-the-nsa-may-have-put-a-backdoor-in-rsas-cryptography-a-technical-primer/)
[Critics slam SSL authority for minting certificate for impersonating sites | Ars Technica](http://arstechnica.com/business/2012/02/critics-slam-ssl-authority-for-minting-cert-used-to-impersonate-sites/)

obsolete?
[How to obtain and install an SSL/TLS certificate, for free | Ars Technica](http://arstechnica.com/security/2009/12/how-to-get-set-with-a-secure-sertificate-for-free/)
[Web served, part 2: Securing things with SSL/TLS | Ars Technica](http://arstechnica.com/information-technology/2012/11/securing-your-web-server-with-ssltls/#p4)

[BetterCrypto⋅org](https://bettercrypto.org/)
[Cipherli.st - Strong Ciphers for Apache, nginx and Lighttpd](https://cipherli.st/)
[Generate Mozilla Security Recommended Web Server Configuration Files](https://mozilla.github.io/server-side-tls/ssl-config-generator/)

[Deploying HTTPS: The Green Lock and Beyond (Chrome Dev Summit 2015) - YouTube](https://www.youtube.com/watch?v=9WuP4KcDBpI)
[Mythbusting HTTPS: Squashing security’s urban legends - Google I/O 2016 - YouTube](https://www.youtube.com/watch?v=YMfW1bfyGSY)
[Roland Bracewell Shoemaker: Let's Encrypt -- What launching a free CA looks like - YouTube](https://www.youtube.com/watch?v=g2_wbp5vxNs)
[Let's Encrypt with J.C. Jones - YouTube](https://www.youtube.com/watch?v=S7CIHwrroec)

## HSTS

[HTTP Strict Transport Security - Wikiwand](http://www.wikiwand.com/en/HTTP_Strict_Transport_Security): always use HTTPS
[HSTS Preload List Submission](https://hstspreload.appspot.com/)

## Mutual TLS/mTLS

[A Kubernetes engineer's guide to mTLS](https://buoyant.io/mtls-guide/)

## SSL checkers

[Qualys SSL Labs](https://www.ssllabs.com/)
[SSL Certificate Checker - Diagnostic Tool | DigiCert.com](https://www.digicert.com/help/)

[trimstray/htrace.sh: My simple Swiss Army knife for http/https troubleshooting and profiling.](https://github.com/trimstray/htrace.sh)

## Attacks

[Monsters in the Middleboxes: Introducing Two New Tools for Detecting HTTPS Interception](https://blog.cloudflare.com/monsters-in-the-middleboxes/amp/)

## TLS fingerprinting

[Fighting TLS fingerprinting with Node.js | HTTP Toolkit](https://httptoolkit.tech/blog/tls-fingerprinting-node-js/)

## Perfect Forward Secrecy (PFS)

[SSL Enabling Forward Secrecy | DigiCert.com](https://www.digicert.com/ssl-support/ssl-enabling-perfect-forward-secrecy.htm)

## Issues

### CA

As it turns out, CA may not be trust-worthy after all. There are many instances of CA issuing fraudulent certificates (willingly or being hacked).

[How the Comodo certificate fraud calls CA trust into question | Ars Technica](http://arstechnica.com/security/2011/03/how-the-comodo-certificate-fraud-calls-ca-trust-into-question/)

[Google warns of unauthorized TLS certificates trusted by almost all OSes [Updated] | Ars Technica](http://arstechnica.com/security/2015/03/google-warns-of-unauthorized-tls-certificates-trusted-by-almost-all-oses/)
[Google Chrome will banish Chinese certificate authority for breach of trust | Ars Technica](http://arstechnica.com/security/2015/04/google-chrome-will-banish-chinese-certificate-authority-for-breach-of-trust/)

[Another fraudulent certificate raises the same old questions about certificate authorities | Ars Technica](http://arstechnica.com/security/2011/08/earlier-this-year-an-iranian/)

[Trust issues: Know the limits of SSL certificates | InfoWorld](http://www.infoworld.com/article/3187174/internet/trust-issues-know-the-limits-of-ssl-certificates.html)
[Free public certificate authorities: Nice idea, big flaw | InfoWorld](http://www.infoworld.com/article/3185484/security/free-public-certificate-authorities-nice-idea-big-flaw.html)

http://arstechnica.com/search/?ie=UTF-8&q=+Certificate+Authorities

### Heartbleed (2014)

> see `web-security.md#heartbleed`

### Renegotiation Gap (2009)

[Truth in SOA: Really Understanding the SSL/TLS Vulnerability (Part 1)](http://soatruth.blogspot.hk/2009/12/really-understanding-ssltls.html)

## Localhost certs

[FiloSottile/mkcert: A simple zero-config tool to make locally-trusted development certificates with any names you'd like.](https://github.com/FiloSottile/mkcert)

## Free SSL Certs

[SSL For Free - Free SSL Certificates in Minutes](https://www.sslforfree.com/)
[Let's Encrypt](https://letsencrypt.org/)

[How To Get A Trusted SSL Certificate for FREE (Works 2020) - YouTube](https://www.youtube.com/watch?v=K90RxdQp9OE)
[How to Install Free SSL From Let’s Encrypt on Shared Hosting](https://www.hostinger.com/tutorials/ssl/how-to-install-free-ssl-from-lets-encypt-on-shared-hosting)

### Let's Encrypt

[Let's Encrypt](https://letsencrypt.org/)
[How It Works](https://letsencrypt.org/howitworks/)
[Technology](https://letsencrypt.org/howitworks/technology/)
[letsencrypt](https://github.com/letsencrypt/)
[Let's Encrypt Status](https://letsencrypt.status.io/)

[The CA's Role in Fighting Phishing and Malware - Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/2015/10/29/phishing-and-malware.html)

[Automatic HTTPS — Caddy Documentation](https://caddyserver.com/docs/automatic-https#acme-challenges)

[Rate Limits - Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/docs/rate-limits/)
[Staging Environment - Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/docs/staging-environment/)
`https://acme-staging-v02.api.letsencrypt.org/directory`

[The Changelog #243: Let's Encrypt the Web with Jacob Hoffman-Andrews | Changelog](https://changelog.com/podcast/243)

[Let's Encrypt Demo - YouTube](https://www.youtube.com/watch?v=Gas_sSB-5SU)
[Let’s Encrypt Your Docker Dan’s Trial & Errno](https://blog.danivovich.com/2016/01/28/lets-encrypt-your-docker/)
[Docker, Nginx & Letsencrypt: Easy & Secure Reverse Proxy](https://medium.com/@ksiig/docker-nginx-letsencrypt-easy-secure-reverse-proxy-40165ba3aee2)
[How to setup your website for that sweet, sweet HTTPS with Docker, Nginx, and letsencrypt](https://medium.freecodecamp.org/docker-compose-nginx-and-letsencrypt-setting-up-website-to-do-all-the-things-for-that-https-7cb0bf774b7e)
[SSL with Docker Swarm, Let's Encrypt and Nginx](https://finnian.io/blog/ssl-with-docker-swarm-lets-encrypt-and-nginx/)
[Nginx and Let’s Encrypt with Docker in Less Than 5 Minutes](https://medium.com/@pentacent/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71)
[How To Secure a Containerized Node Application with Let's Encrypt | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-secure-a-containerized-node-js-application-with-nginx-let-s-encrypt-and-docker-compose)
[Enabling HTTPS with Let's Encrypt on Docker - BROS - Medium](https://medium.com/bros/enabling-https-with-lets-encrypt-over-docker-9cad06bdb82b)
[Generate free SSL certificates with Docker and LetsEncrypt | Tit Petrič](https://scene-si.org/2016/01/23/generate-free-ssl-certificates-with-docker-and-letsencrypt/)
[How to Set Up Free SSL Certificates from Let's Encrypt using Docker and Nginx](https://www.humankode.com/ssl/how-to-set-up-free-ssl-certificates-from-lets-encrypt-using-docker-and-nginx)

[certbot-docker/certbot-docker: Source files for Certbot's Docker images](https://github.com/certbot-docker/certbot-docker)
[JrCs/docker-letsencrypt-nginx-proxy-companion: LetsEncrypt companion container for nginx-proxy](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion)
[linuxserver/docker-letsencrypt](https://github.com/linuxserver/docker-letsencrypt)
[staticfloat/docker-nginx-certbot: Create and renew website certificates using the Letsencrypt free certificate authority.](https://github.com/staticfloat/docker-nginx-certbot)

[Two domains on one droplet with one SSL certificate | DigitalOcean](https://www.digitalocean.com/community/questions/two-domains-on-one-droplet-with-one-ssl-certificate)
[How To Secure Nginx with Let's Encrypt on Ubuntu 16.04 | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-16-04)

[Let's Encrypt with HAProxy](https://coolaj86.com/articles/lets-encrypt-with-haproxy/)
[Let's Encrypt on Raspberry Pi](https://coolaj86.com/articles/lets-encrypt-on-raspberry-pi/)
[adventures in haproxy: tcp, tls, https, ssh, openvpn](https://coolaj86.com/articles/adventures-in-haproxy-tcp-tls-https-ssh-openvpn/)
[Setting up HTTPS on Nginx using Let’s Encrypt – Frederik Banke – Medium](https://medium.com/@frederikbanke/setting-up-https-on-nginx-using-lets-encrypt-b5eb78cd689d) with Docker and certbot
[How to configure Nginx with free Let’s Encrypt SSL certificate on Debian or Ubuntu Linux](http://www.cyberciti.biz/faq/how-to-configure-nginx-with-free-lets-encrypt-ssl-certificate-on-debian-or-ubuntu-linux/)

## Clients

> integrating Let's Encrypt client into a private DNS server is cool

[ACME Client Implementations - Let's Encrypt](https://letsencrypt.org/docs/client-options/)

[Certbot](https://certbot.eff.org/) [docs](https://certbot.eff.org/docs/) previously `letsencrypt`/`letsencrypt-auto`
[User Guide — Certbot.documentation](https://certbot.eff.org/docs/using.html)
[如何免费的让网站启用 HTTPS | | 酷 壳 - CoolShell](https://coolshell.cn/articles/18094.html)
[Complete guide to configure SSL on Nginx with Let's Encrypt (Ubuntu/Centos/RHEL) - LinuxTechLab](https://linuxtechlab.com/complete-guide-to-configure-ssl-on-nginx-with-lets-encrypt-ubuntu-centos-rhel/)

[diafygi/acme-tiny: A tiny script to issue and renew TLS certs from Let's Encrypt](https://github.com/diafygi/acme-tiny)

[xenolf/lego: Let's Encrypt client and ACME library written in Go](https://github.com/xenolf/lego) Used in Caddy

[Daplie/node-letsencrypt: letsencrypt for node.js](https://github.com/Daplie/node-letsencrypt)
[DylanPiercey/auto-sni: Free, automated HTTPS for NodeJS made easy.](https://github.com/DylanPiercey/auto-sni)

### acme-client

[kelunik/acme-client: Let's Encrypt / ACME client written in PHP for the CLI.](https://github.com/kelunik/acme-client)

[Enabling free SSL on Hostinger shared hosting | Kenrick's Notes](https://blog.kenrick95.org/2016/07/enabling-free-ssl-on-hostinger-shared-hosting/)
[iamshreeram/php-ssl-installer: Installing SSL certificate in hostinger](https://github.com/iamshreeram/php-ssl-installer)

```sh
php bin/acme issue --domains [colon-separated domain names] --path [colon-separated full path to domain root]
```

### acme.sh

[acmesh-official/acme.sh: A pure Unix shell script implementing ACME client protocol](https://github.com/acmesh-official/acme.sh)
[LetsEncrypt SSL cert on GoDaddy Shared Hosting with No Root and No nc](https://tryingtobeawesome.com/encryptdaddy/) `--deploy`, then add cron jobs

```sh
acme.sh --issue -d $DOMAIN -w /home/wwwroot/$DOMAIN
# acme.sh --deploy -d example.com --deploy-hook cpanel_uapi
~/.acme.sh/$DOMAIN/$DOMAIN.cer  # cert
~/.acme.sh/$DOMAIN/$DOMAIN.key  # private key
```

```sh
~/.acme.sh/acme.sh --cron --home ~/.acme.sh --force 2>&1 >> ~/.acme.sh/cronlog.txt
```

### Cloudflare

[How to Get a FREE SSL Certificate with Hostinger - YouTube](https://www.youtube.com/watch?v=gsELqvQfAyM)

- create Cloudflare account
- point to a domain with records
- enable Let's Encrypt

CloudFlare Protection on Hostinger
For 1 CloudFlare Protection plan, you can only use it for 1 website/domain and all its subdomains as long as the domain/website is pointed to us.
We use Cloudflare’s free plan here at Hostinger. It does provide you with these features:

- DDoS attack mitigation
- Global Content Delivery Network (CDN)

The main differences between using Cloudflare with Hostinger directly with and Cloudflare.com are:

- DNS zone can be fully managed from Hostinger side – so you don’t need to worry about updating DNS Records in different places: all of your domain’s DNS management will be in one place
- All main setting of Cloudflare can be found in hPanel – so changing security level will only take a few clicks
- One time activation fee – and Cloudflare will secure your domain and all of your subdomains as long as your domain is hosted with us 💜

### SSL for Free

[SSL For Free - Free SSL Certificates in Minutes](https://www.sslforfree.com/)

### Heroku

[Announcing Heroku Free SSL Beta and Flexible Dyno Hours | Heroku](https://blog.heroku.com/archives/2016/5/18/announcing_heroku_free_ssl_beta_and_flexible_dyno_hours)
[Let's Encrypt and Heroku [Solved] - Server - Let's Encrypt Community Support](https://community.letsencrypt.org/t/lets-encrypt-and-heroku-solved/4272/18)
[Let's Encrypt with a Rails app on Heroku // Collective Idea | Crafting web and mobile software based in Holland, Michigan](http://collectiveidea.com/blog/archives/2016/01/12/lets-encrypt-with-a-rails-app-on-heroku/)
[Use Let’s Encrypt TLS certificate on Heroku — Sikachu’s Blog — Medium](https://sikac.hu/use-let-s-encrypt-tls-certificate-on-heroku-65f853870d90#.ut542pcuk)
[SSL Endpoint | Heroku Dev Center](https://devcenter.heroku.com/articles/ssl-endpoint)
[Set up CloudFlare's free SSL on Heroku](https://robots.thoughtbot.com/set-up-cloudflare-free-ssl-on-heroku)

## Standards

[RFC 2986 - PKCS #10: Certification Request Syntax Specification Version 1.7](http://tools.ietf.org/html/rfc2986)
[RFC 3447 - Public-Key Cryptography Standards (PKCS) #1: RSA Cryptography Specifications Version 2.1](http://tools.ietf.org/html/rfc3447)
[RFC 5958 - Asymmetric Key Packages](http://tools.ietf.org/html/rfc5958)
[RFC 6101 - The Secure Sockets Layer (SSL) Protocol Version 3.0](http://tools.ietf.org/html/rfc6101)
[RFC 7525 - Recommendations for Secure Use of Transport Layer Security (TLS) and Datagram Transport Layer Security (DTLS)](https://tools.ietf.org/html/rfc7525)
[RFC 7292 - PKCS #12: Personal Information Exchange Syntax v1.1](http://tools.ietf.org/html/rfc7292)
