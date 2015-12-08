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

[File:Ssl handshake with two way authentication with certificates.png - Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Ssl_handshake_with_two_way_authentication_with_certificates.png)

[ImperialViolet - Overclocking SSL](https://www.imperialviolet.org/2010/06/25/overclocking-ssl.html)
[ImperialViolet - Public key pinning](https://www.imperialviolet.org/2011/05/04/pinning.html)
[Survival Guide - TLS/SSL and SSL (X.509) Certificates (CA-signed and Self-Signed)](http://www.zytrax.com/tech/survival/ssl.html)
[Is TLS Fast Yet?](https://istlsfastyet.com/)
[BetterCrypto⋅org](https://bettercrypto.org/)
[Rolling out Public Key Pinning with HPKP Reporting — Google Web Updates](https://developers.google.com/web/updates/2015/09/HPKP-reporting-with-chrome-46)
[The SSL/TLS Handshake: an Overview – SSL Information and FAQ](https://info.ssl.com/tls-handshake/)

[How the NSA (may have) put a backdoor in RSA’s cryptography: A technical primer | Ars Technica](http://arstechnica.com/security/2014/01/how-the-nsa-may-have-put-a-backdoor-in-rsas-cryptography-a-technical-primer/)
[Critics slam SSL authority for minting certificate for impersonating sites | Ars Technica](http://arstechnica.com/business/2012/02/critics-slam-ssl-authority-for-minting-cert-used-to-impersonate-sites/)

[How to obtain and install an SSL/TLS certificate, for free | Ars Technica](http://arstechnica.com/security/2009/12/how-to-get-set-with-a-secure-sertificate-for-free/)
[Web served, part 2: Securing things with SSL/TLS | Ars Technica](http://arstechnica.com/information-technology/2012/11/securing-your-web-server-with-ssltls/#p4)

[HTTP Strict Transport Security - Wikiwand](http://www.wikiwand.com/en/HTTP_Strict_Transport_Security): always use HTTPS

[Qualys SSL Labs](https://www.ssllabs.com/) run tests for your server.

## The Issue: CA

As it turns out, CA are not trust worthy at all. There are many instances of CA issuing fraudulent certificates (willingly or being hacked).

[How the Comodo certificate fraud calls CA trust into question | Ars Technica](http://arstechnica.com/security/2011/03/how-the-comodo-certificate-fraud-calls-ca-trust-into-question/)

[Google warns of unauthorized TLS certificates trusted by almost all OSes [Updated] | Ars Technica](http://arstechnica.com/security/2015/03/google-warns-of-unauthorized-tls-certificates-trusted-by-almost-all-oses/)
[Google Chrome will banish Chinese certificate authority for breach of trust | Ars Technica](http://arstechnica.com/security/2015/04/google-chrome-will-banish-chinese-certificate-authority-for-breach-of-trust/)

[Another fraudulent certificate raises the same old questions about certificate authorities | Ars Technica](http://arstechnica.com/security/2011/08/earlier-this-year-an-iranian/)

http://arstechnica.com/search/?ie=UTF-8&q=+Certificate+Authorities

## Let's Encrypt

[Let's Encrypt](https://letsencrypt.org/)
[How It Works](https://letsencrypt.org/howitworks/)
[Technology](https://letsencrypt.org/howitworks/technology/)

[letsencrypt](https://github.com/letsencrypt/)
[Let's Encrypt Demo - YouTube](https://www.youtube.com/watch?v=Gas_sSB-5SU)

[Let's Encrypt with HAProxy](https://coolaj86.com/articles/lets-encrypt-with-haproxy/)
[Let's Encrypt on Raspberry Pi](https://coolaj86.com/articles/lets-encrypt-on-raspberry-pi/)
[adventures in haproxy: tcp, tls, https, ssh, openvpn](https://coolaj86.com/articles/adventures-in-haproxy-tcp-tls-https-ssh-openvpn/)

## Standards

[RFC 2986 - PKCS #10: Certification Request Syntax Specification Version 1.7](http://tools.ietf.org/html/rfc2986)
[RFC 3447 - Public-Key Cryptography Standards (PKCS) #1: RSA Cryptography Specifications Version 2.1](http://tools.ietf.org/html/rfc3447)
[RFC 5958 - Asymmetric Key Packages](http://tools.ietf.org/html/rfc5958)
[RFC 6101 - The Secure Sockets Layer (SSL) Protocol Version 3.0](http://tools.ietf.org/html/rfc6101)
[RFC 7525 - Recommendations for Secure Use of Transport Layer Security (TLS) and Datagram Transport Layer Security (DTLS)](https://tools.ietf.org/html/rfc7525)
[RFC 7292 - PKCS #12: Personal Information Exchange Syntax v1.1](http://tools.ietf.org/html/rfc7292)
