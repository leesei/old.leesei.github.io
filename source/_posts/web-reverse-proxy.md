---
title: Reverse Proxy
categories:
  - web
tags:
  - web-deploy
toc: false
date: 2015-06-17 11:32:04
---

[Reverse proxy - Wikiwand](https://www.wikiwand.com/en/Reverse_proxy)
[What is a Reverse Proxy Server? | NGINX](https://www.nginx.com/resources/glossary/reverse-proxy-server/)

[Proxy vs. Reverse Proxy (Explained by Example) - YouTube](https://www.youtube.com/watch?v=ozhe__GdWC8)
[webserver - Difference between proxy server and reverse proxy server - Stack Overflow](https://stackoverflow.com/questions/224664/difference-between-proxy-server-and-reverse-proxy-server?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)

[Load balancing in Layer 4 vs Layer 7 with HAPROXY Examples - YouTube](https://www.youtube.com/watch?v=aKMLgFVxZYk)

[Load Balancer vs Reverse Proxy (Explained by Example) - YouTube](https://www.youtube.com/watch?v=S8J2fkN2FeI)
[What is a Reverse Proxy vs. Load Balancer? - NGINX](https://www.nginx.com/resources/glossary/reverse-proxy-vs-load-balancer/)
Load balancer is an application of reverse proxy

[Load Balancing and B2 Cloud Storage](https://www.backblaze.com/blog/load-balancing-and-b2-cloud-storage/)
[Load Balancer Administration - Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html-single/load_balancer_administration/)

[The "subfolder problem", OR, "why can't I reverse proxy my app into a subfolder?" - Wiki - Caddy Community](https://caddy.community/t/the-subfolder-problem-or-why-cant-i-reverse-proxy-my-app-into-a-subfolder/8575)

[10 Top Open Source Caching Tools for Linux in 2020](https://www.tecmint.com/open-source-caching-tools-for-linux/amp/)
[PageSpeed Modules](https://www.modpagespeed.com/)

## Preserving client IP address

[Unable to retrieve user's IP address in docker swarm mode · Issue #25526 · moby/moby](https://github.com/moby/moby/issues/25526)
[Preserve Source IP Address Despite Reverse Proxies - HAProxy Technologies](https://www.haproxy.com/blog/preserve-source-ip-address-despite-reverse-proxies/)

---

# Software solutions

> see `apache.md`
> see `nginx.md`

[Pow: Zero-configuration Rack server for Mac OS X](http://pow.cx/)

[jweslley/bam](https://github.com/jweslley/bam) (uses Procfile)
[Prax](http://ysbaddaden.github.io/prax/)
[Invoker - A Process Manager](http://invoker.codemancers.com/)
[pyromaniac/hoof](https://github.com/pyromaniac/hoof/) (no longer maintained)
[vulcand/vulcand: Programmatic load balancer backed by Etcd](https://github.com/vulcand/vulcand)

[squid : Optimising Web Delivery](http://www.squid-cache.org/)

[Armor - Uncomplicated, modern HTTP server](https://armor.labstack.com/)

[Ultra Monkey:](http://www.ultramonkey.org/) uses IPVS

[mitmproxy - an interactive HTTPS proxy](https://mitmproxy.org/)

[micro/go-proxy: A proxy library for micro services](https://github.com/micro/go-proxy)

[Node.js process load balance performance: comparing cluster module, iptables and Nginx — Medium](https://medium.com/@fermads/node-js-process-load-balancing-comparing-cluster-iptables-and-nginx-6746aaf38272#.92b5q68t4)

[Poor man’s load balancing with Docker — Medium](https://medium.com/@lherrera/poor-mans-load-balancing-with-docker-2be014983e5)
[HAProxy vs Nginx - what's in your wallet? - The Matrix has you...](https://distinctplace.com/2017/04/20/haproxy-vs-nginx/)

[Beam: A Distributed Knowledge Graph Store](https://www.ebayinc.com/stories/blogs/tech/beam-a-distributed-knowledge-graph-store/)

## Linux Kernel

Used by Docker SwarmKit

[IPVS Software - Advanced Layer-4 Switching](http://www.linuxvirtualserver.org/software/ipvs.html)
[IPVS - LVSKB](http://kb.linuxvirtualserver.org/wiki/IPVS)
[Ipvsadm - LVSKB](http://kb.linuxvirtualserver.org/wiki/Ipvsadm)
[Ultra Monkey: The Linux Virtual Server](http://www.ultramonkey.org/3/lvs.html)
[Linux Virtual Server Tutorial](http://www.ultramonkey.org/papers/lvs_tutorial/html/)

## GitHub Load Balancer

[Introducing the GitHub Load Balancer - GitHub Engineering](http://githubengineering.com/introducing-glb/)
[GLB: GitHub’s open source load balancer | GitHub Engineering](https://githubengineering.com/glb-director-open-source-load-balancer/)
[GitHub open-sources internal load-balancing software | InfoWorld](http://www.infoworld.com/article/3124547/data-center/github-to-open-up-its-load-balancing-software.html)

## HAProxy

[HAProxy - Wikiwand](https://www.wikiwand.com/en/HAProxy)
[HAProxy - The Reliable, High Performance TCP/HTTP Load Balancer](http://www.haproxy.org/)

[observing/haproxy: HAProxy management and orchestration](https://github.com/observing/haproxy) Node.js driver
[jiangwenyuan/nuster: A caching proxy server based on HAProxy](https://github.com/jiangwenyuan/nuster)

[An Introduction to HAProxy and Load Balancing Concepts | DigitalOcean](https://www.digitalocean.com/community/tutorials/an-introduction-to-haproxy-and-load-balancing-concepts)
[How To Use HAProxy As A Layer 7 Load Balancer For WordPress and Nginx On Ubuntu 14.04 | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-haproxy-as-a-layer-7-load-balancer-for-wordpress-and-nginx-on-ubuntu-14-04)
[How To Use HAProxy to Set Up HTTP Load Balancing on an Ubuntu VPS | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-haproxy-to-set-up-http-load-balancing-on-an-ubuntu-vps)
[Load Balancing with HAProxy - Servers for Hackers](https://serversforhackers.com/load-balancing-with-haproxy)
[HAProxy Failover using Keepalived in AWS EC2 - DevOpsTech Solutions](http://www.devopstech.com/haproxy-failover-keepalived-aws-ec2/)

[HAProxy with HTTPS (TLS/SSL)](https://coolaj86.com/articles/haproxy-with-https-tls-ssl/)
[How To Implement SSL Termination With HAProxy on Ubuntu 14.04 | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-implement-ssl-termination-with-haproxy-on-ubuntu-14-04)
[Let's Encrypt with HAProxy](https://coolaj86.com/articles/lets-encrypt-with-haproxy/)

[Load Balancing for Docker Containers with HA Proxy](http://rgardler.github.io/2015/09/10/container_load_balancing_with_haproxy)
[True Zero Downtime HAProxy Reloads](http://engineeringblog.yelp.com/2015/04/true-zero-downtime-haproxy-reloads.html)

## H2O

[H2O - the optimized HTTP/2 server](https://h2o.examp1e.net/)
[h2o/h2o: H2O - the optimized HTTP/1, HTTP/2 server](https://github.com/h2o/h2o)

## Algernon

[xyproto/algernon: HTTP/2 web/application server with Lua support](https://github.com/xyproto/algernon)
[Algernon](http://algernon.roboticoverlords.org/)

```sh
go get github.com/xyproto/algernon
```

## LiteSpeed

[LiteSpeed Web Server - Apache Alternative - LiteSpeed Technologies](https://www.litespeedtech.com/products/litespeed-web-server) compatible with Apache conf, supports HTTP/2, HTTP/3, event driven
[LiteSpeed Technologies - YouTube](https://www.youtube.com/channel/UC2gbIbGhz3PR6N_U_MJLrzg)

[Get OpenLiteSpeed!](https://openlitespeed.org/)
[Easily Install OpenLiteSpeed in 1 Click! • OpenLiteSpeed](https://openlitespeed.org/kb/1-click-install/)

## LiteSpeed Cache

[What is LiteSpeed Cache? | LiteSpeed Documentation](https://docs.litespeedtech.com/lscache/)
[Overview | LiteSpeed Cache Without a Plugin | LiteSpeed Documentation](https://docs.litespeedtech.com/lscache/noplugin/)

[Overview | LSCache for WordPress | LiteSpeed Documentation](https://docs.litespeedtech.com/lscache/lscwp/)
[LiteSpeed Cache for WordPress - LiteSpeed Technologies](https://www.litespeedtech.com/products/cache-plugins/wordpress-acceleration)

[Overview | LiteSpeed Cache for Joomla! | LiteSpeed Documentation](https://docs.litespeedtech.com/lscache/lscjoomla/)
[LiteSpeed Cache for Joomla - LiteSpeed Technologies](https://www.litespeedtech.com/products/cache-plugins/joomla-acceleration)
[Configuration | LiteSpeed Cache for Joomla! | LiteSpeed Documentation](https://docs.litespeedtech.com/lscache/lscjoomla/settings/)

### ESI

[Edge Side Includes Caching for WordPress ⋆ LiteSpeed Blog](https://blog.litespeedtech.com/2017/09/06/wpw-esi-and-litespeed-cache/)
[Guide to Using ESI in Joomla with LSCache ⋆ LiteSpeed Blog](https://blog.litespeedtech.com/2018/07/10/using-esi-in-joomla/)

## Caddy

> Caddy used to add Sponsor header and use different license for pre-built binaries
> https://www.reddit.com/r/golang/comments/bgz0cd/announcing_caddy_10_caddy_2_and_caddy_enterprise/
> Version 2.0 was released in May 2020, seems to have better community support

> TODO: remove v1 docs (prior to May 2020)

[Caddy - The HTTP/2 Web Server with Fully Managed SSL](https://caddyserver.com/)
prebuild librabry from download page are [licensed differently](https://caddy.community/t/caddy-server-its-free-for-live-server/3371)
[caddyserver/caddy: Fast, multi-platform web server with automatic HTTPS](https://github.com/caddyserver/caddy)
[caddyserver/caddy-docker: Source for the official Caddy v2 Docker Image](https://github.com/caddyserver/caddy-docker)
[caddyserver/dist: Resources for packaging and distributing Caddy](https://github.com/caddyserver/dist) systemd unit file

```dockerfile
FROM caddy:2-builder-alpine AS builder

RUN xcaddy build \
	--with github.com/greenpau/caddy-auth-jwt \
	--with github.com/greenpau/caddy-auth-portal \
	--with github.com/aksdb/caddy-cgi \
	--with github.com/abiosoft/caddy-json-parse \
	--with github.com/greenpau/caddy-trace \
	--with github.com/RussellLuo/caddy-ext/ratelimit \
	--with github.com/chukmunnlee/caddy-openapi \
	--with github.com/lucaslorentz/caddy-docker-proxy/plugin \
	--with github.com/casbin/caddy-authz \
	--with github.com/mholt/caddy-l4 \
	--with github.com/mholt/caddy-ratelimit

FROM caddy:2-alpine

# overwrites caddy with my custom build
COPY --from=builder /usr/bin/caddy /usr/bin/caddy
```

```
https://caddyserver.com/download?\
  package=github.com%2Fgreenpau%2Fcaddy-auth-jwt&\
  package=github.com%2Fgreenpau%2Fcaddy-auth-portal&\
  package=github.com%2Faksdb%2Fcaddy-cgi%2Fv2&\
  package=github.com%2Fabiosoft%2Fcaddy-json-parse&\
  package=github.com%2Fgreenpau%2Fcaddy-trace&\
  package=github.com%2FRussellLuo%2Fcaddy-ext%2Fratelimit&\
  package=github.com%2Fchukmunnlee%2Fcaddy-openapi&\
  package=github.com%2Flucaslorentz%2Fcaddy-docker-proxy%2Fplugin%2Fv2&\
  package=github.com%2Fcasbin%2Fcaddy-authz%2Fv2&\
  package=github.com%2Fmholt%2Fcaddy-l4&\
  package=github.com%2Fmholt%2Fcaddy-ratelimit
```

[Welcome — Caddy Documentation](https://caddyserver.com/docs/)
[Getting Started — Caddy Documentation](https://caddyserver.com/docs/getting-started)
[Upgrading to Caddy 2 — Caddy Documentation](https://caddyserver.com/docs/v2-upgrade)
[Caddy Community](https://caddy.community/)
[Top Wiki topics - Caddy Community](https://caddy.community/c/wiki/13)

[Anyone else dislike v2? - Help - Caddy Community](https://caddy.community/t/anyone-else-dislike-v2/8191/10)
[For Mastodon Caddy Setting file. (Based on official Nginx configuration example) [Last Update: May 16, 2020]](https://gist.github.com/ehlxr/37764950fcb4d68d3a00b5f0000823e7) v1 -> v2
[Upgrading to Caddy 2 — Caddy Documentation](https://caddyserver.com/docs/v2-upgrade)

[Caddy offers TLS, HTTPS, and more in one dependency-free Go Web server – Ars Technica](https://arstechnica.com/gadgets/2020/05/caddy-offers-tls-https-and-more-in-one-dependency-free-go-web-server/?amp=1)

### v1

[Command Line Interface - Caddy](https://caddyserver.com/docs/cli) v1
[caddyserver/examples: Simple guided examples of how to use Caddy](https://github.com/caddyserver/examples) v1

[abiosoft/caddy](https://hub.docker.com/r/abiosoft/caddy/tags)
[zzrot/alpine-caddy](https://hub.docker.com/r/zzrot/alpine-caddy)

[Simply Secure » Linux Magazine](http://www.linux-magazine.com/Issues/2018/213/Caddy)
[Today I became a Go developer, with vim and Caddy](https://coolaj86.com/articles/today-i-became-a-golang-dev-with-vim-and-caddy/)
[A Look Inside Caddy, a Web Server Written in Go](https://blog.gopheracademy.com/caddy-a-look-inside/)

```sh
# OBSOLETE v1 instructions
curl https://getcaddy.com | bash -s personal http.cors,http.expires,http.filemanager,http.filter,http.forwardproxy,http.git,http.hugo,http.jwt,http.locale,http.login,http.minify

mkdir caddy; cd caddy
wget https://caddyserver.com/download/linux/amd64 -O caddy_linux_amd64.tar.gz
tar xzf caddy_linux_amd64.tar.gz

./caddy browse -log ./log -port 80 -root <WWW_ROOT>
```

### Config

[Caddyfile Quick-start — Caddy Documentation](https://caddyserver.com/docs/quick-starts/caddyfile)
[Caddyfile Tutorial — Caddy Documentation](https://caddyserver.com/docs/caddyfile-tutorial)
[The Caddyfile — Caddy Documentation](https://caddyserver.com/docs/caddyfile)

[API Quick-start — Caddy Documentation](https://caddyserver.com/docs/quick-starts/api)
[API — Caddy Documentation](https://caddyserver.com/docs/api)

[JSON Config Structure - Caddy Documentation](https://caddyserver.com/docs/json/)

[Command Line — Caddy Documentation](https://caddyserver.com/docs/command-line)

```sh
caddy run --config /path/to/Caddyfile
caddy start --config /path/to/Caddyfile  # in background
caddy file-server browse
```

[Top Wiki topics - Caddy Community](https://caddy.community/c/wiki/13)
[So You Want to Write a Caddyfile - Wiki - Caddy Community](https://caddy.community/t/so-you-want-to-write-a-caddyfile/8205)
[Composing in the Caddyfile - Wiki - Caddy Community](https://caddy.community/t/composing-in-the-caddyfile/8291)

#### CORS

[Caddy v2.1 CORS whitelist](https://gist.github.com/ryanburnette/d13575c9ced201e73f8169d3a793c1a3) use `import` directive
[Implementing CORS whitelist in Caddy v2 - Help - Caddy Community](https://caddy.community/t/implementing-cors-whitelist-in-caddy-v2/8590) including 2.0 solution

### Videos

[Provo Linux User Group - 2/16/16 - Matt Holt - "Caddy" - YouTube](https://www.youtube.com/watch?v=ZyVA9tuif4s)
[Caddy server Git add-on tutorial. - YouTube](https://www.youtube.com/watch?v=dmat1MUT0fc)

### Module/Plugin

[Extending Caddy — Caddy Documentation](https://caddyserver.com/docs/extending-caddy)

[Modules - Caddy Documentation](https://caddyserver.com/docs/modules/) built-in modules
[Download Caddy](https://caddyserver.com/download) select bundled modules
[caddyserver/xcaddy: Build Caddy with plugins](https://github.com/caddyserver/xcaddy)

[mholt/caddy-l4: Layer 4 (TCP/UDP) app for Caddy](https://github.com/mholt/caddy-l4)

[abiosoft/caddy-git: git middleware for Caddy](https://github.com/abiosoft/caddy-git) for deployment

[mholt/caddy-ratelimit: HTTP rate limiting module for Caddy 2](https://github.com/mholt/caddy-ratelimit)
[caddy-ext/ratelimit at master · RussellLuo/caddy-ext](https://github.com/RussellLuo/caddy-ext/tree/master/ratelimit)
[greenpau/caddy-auth-portal: Authentication Plugin for Caddy v2 implementing Form-Based, Basic, Local, LDAP, OpenID Connect, OAuth 2.0 (Github, Google, Facebook, Okta, etc.), SAML Authentication](https://github.com/greenpau/caddy-auth-portal)
[greenpau/caddy-auth-jwt: JWT Authorization Plugin for Caddy v2](https://github.com/greenpau/caddy-auth-jwt)
[lucaslorentz/caddy-docker-proxy: Caddy as a reverse proxy for Docker](https://github.com/lucaslorentz/caddy-docker-proxy)

[casbin/caddy-authz: Caddy-authz is a middleware for Caddy that blocks or allows requests based on access control policies.](https://github.com/casbin/caddy-authz)
[casbin/casbin: An authorization library that supports access control models like ACL, RBAC, ABAC in Golang](https://github.com/casbin/casbin)

[How to use DNS provider modules in Caddy 2 - Wiki - Caddy Community](https://caddy.community/t/how-to-use-dns-provider-modules-in-caddy-2/8148)
[caddy-dns](https://github.com/caddy-dns)
[mholt/caddy-dynamicdns: Caddy app that keeps your DNS records (A/AAAA) pointed at itself.](https://github.com/mholt/caddy-dynamicdns)

## lighttpd

[lighttpd - ArchWiki](https://wiki.archlinux.org/title/Lighttpd)

## Phusion Passenger

[Fast web server & app server, Ruby Python Node.js - Phusion Passenger](https://www.phusionpassenger.com/)
[Passenger Library](https://www.phusionpassenger.com/library/)
[Phusion Passenger Design and Architecture](https://www.phusionpassenger.com/documentation/Design and Architecture.html)
[phusion/passenger: A fast and robust web server and application server for Ruby, Python and Node.js](https://github.com/phusion/passenger)

[What's new in Passenger 5 part 1: performance and HTTP JSON API](https://blog.phusion.nl/2015/03/04/whats-new-in-passenger-5-part-1-performance-and-http-json-api/)
[What's new in Passenger 5 part 2: better logging, better restarting, better WebSockets and more](https://blog.phusion.nl/2015/03/04/whats-new-in-passenger-5-part-2-better-logging-better-restarting-better-websockets-and-more/)

[How we've made Phusion Passenger 5 ("Raptor") up to 4x faster than Unicorn, up to 2x faster than Puma, Torquebox](http://www.rubyraptor.org/how-we-made-raptor-up-to-4x-faster-than-unicorn-and-up-to-2x-faster-than-puma-torquebox/)
[Pointer tagging, linked string hash tables, turbocaching and other Phusion Passenger 5 optimizations](http://www.rubyraptor.org/pointer-tagging-linked-string-hash-tables-turbocaching-and-other-raptor-optimizations/#turbocaching)

[Phusion Passenger Standalone users guide](https://www.phusionpassenger.com/documentation/Users%20guide%20Standalone.html) (obsolete)

## Netflix Zuul

[The Netflix Tech Blog: Announcing Zuul: Edge Service in the Cloud](http://techblog.netflix.com/2013/06/announcing-zuul-edge-service-in-cloud.html)
[Using Netflix Zuul to Proxy your Microservices | Heroku](https://blog.heroku.com/archives/2016/3/2/using_netflix_zuul_to_proxy_your_microservices)

[Open Sourcing Zuul 2 – Netflix TechBlog – Medium](https://medium.com/netflix-techblog/open-sourcing-zuul-2-82ea476cb2b3)
[Netflix/zuul: Zuul is a gateway service that provides dynamic routing, monitoring, resiliency, security, and more.](https://github.com/netflix/zuul/)

Depends on Zookeeper

## Træfɪk

[Træfɪk](https://traefik.io/)
[Traefik Tutorial: Traefik Reverse Proxy with LetsEncrypt for Docker Media Server](https://www.smarthomebeginner.com/traefik-reverse-proxy-tutorial-for-docker/amp/)

Auto load-balancing, supports multiple service registries (Docker, Kubernetes, Mesos/Marathon, Consul, Etcd, and more to come)

[Let's Encrypt - Træfik](https://docs.traefik.io/configuration/acme/)
[Let's Encrypt & Docker - Træfik](https://docs.traefik.io/user-guide/docker-and-lets-encrypt/)
[Swarm Mode Cluster - Træfik](https://docs.traefik.io/user-guide/swarm-mode/)

[Nginx to Caddy to Traefik](https://sean.thenewells.us/nginx-to-caddy-to-traefik/) Compose, user network, multiple container
[Enabling HTTPS termination in Traefik](https://niels.nu/blog/2017/traefik-https-letsencrypt.html)
[Traefik - a Modern HTTP Reverse Proxy and Load Balancer for Microservices such as Docker](https://sysadmins.co.za/traefik-a-modern-http-reverse-proxy-and-load-balancer-for-microservices-such-as-docker/)
[Quick & Easy HTTPS For Local Development - via @codeship | via @codeship](https://blog.codeship.com/quick-easy-https-for-local-development/)
[Traefik a Reverse Proxy alternative to Nginx - YouTube](https://www.youtube.com/watch?v=GsBXAunkPWg)
[Running Traefik on Worker Nodes More Securely – mikesir87's blog](https://blog.mikesir87.io/2019/08/running-traefik-on-worker-nodes-more-securely/)

## Keepalived

[Keepalived for Linux](http://www.keepalived.org/)

[Chapter 2. Keepalived Overview - Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/load_balancer_administration/ch-keepalived-overview-vsa)
[How To Set Up Highly Available Web Servers with Keepalived and Floating IPs on Ubuntu 14.04 | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-highly-available-web-servers-with-keepalived-and-floating-ips-on-ubuntu-14-04)
