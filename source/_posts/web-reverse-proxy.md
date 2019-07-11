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
[What is a Reverse Proxy vs. Load Balancer? - NGINX](https://www.nginx.com/resources/glossary/reverse-proxy-vs-load-balancer/)
[webserver - Difference between proxy server and reverse proxy server - Stack Overflow](https://stackoverflow.com/questions/224664/difference-between-proxy-server-and-reverse-proxy-server?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)

[Load Balancing and B2 Cloud Storage](https://www.backblaze.com/blog/load-balancing-and-b2-cloud-storage/)
[Load Balancer Administration - Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html-single/load_balancer_administration/)

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

## Caddy

> sole developer of Caddy is making decisions against the community
> this lead to the fork [WedgeServer/wedge](https://github.com/WedgeServer/wedge), but it's not actively developed
> [Put A Fork In Caddy; It's Done](https://neflabs.com/blog/caddy-server/)

[Caddy - The HTTP/2 Web Server with Fully Managed SSL](https://caddyserver.com/)
[mholt/caddy: Fast, cross-platform HTTP/2 web server with automatic HTTPS](https://github.com/mholt/caddy)
[ZZROTDesign/alpine-caddy: Alpine Linux Docker Container running Caddyserver](https://github.com/ZZROTDesign/alpine-caddy)

[Simply Secure » Linux Magazine](http://www.linux-magazine.com/Issues/2018/213/Caddy)
[Today I became a Go developer, with vim and Caddy](https://coolaj86.com/articles/today-i-became-a-golang-dev-with-vim-and-caddy/)
[A Look Inside Caddy, a Web Server Written in Go](https://blog.gopheracademy.com/caddy-a-look-inside/)

[Caddy User Guide](https://caddyserver.com/docs)
[Command Line Interface - Caddy](https://caddyserver.com/docs/cli)
[caddy/dist/init/linux-systemd at master · mholt/caddy](https://github.com/mholt/caddy/tree/master/dist/init/linux-systemd)
[caddyserver/examples: Simple guided examples of how to use Caddy](https://github.com/caddyserver/examples)
[Add WSGI directive for serving Python apps · Issue #176 · mholt/caddy](https://github.com/mholt/caddy/issues/176)

```sh
curl https://getcaddy.com | bash -s personal http.cors,http.expires,http.filemanager,http.filter,http.forwardproxy,http.git,http.hugo,http.jwt,http.locale,http.login,http.minify

mkdir caddy; cd caddy
wget https://caddyserver.com/download/linux/amd64 -O caddy_linux_amd64.tar.gz
tar xzf caddy_linux_amd64.tar.gz

./caddy browse -log ./log -port 80 -root <WWW_ROOT>
```

### Videos

[Provo Linux User Group - 2/16/16 - Matt Holt - "Caddy" - YouTube](https://www.youtube.com/watch?v=ZyVA9tuif4s)
[Caddy server Git add-on tutorial. - YouTube](https://www.youtube.com/watch?v=dmat1MUT0fc)

## Phusion Passenger

[Fast web server & app server, Ruby Python Node.js - Phusion Passenger](https://www.phusionpassenger.com/)
[Passenger Library](https://www.phusionpassenger.com/library/)
[Phusion Passenger Design and Architecture](https://www.phusionpassenger.com/documentation/Design and Architecture.html)

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

## Keepalived

[Keepalived for Linux](http://www.keepalived.org/)

[Chapter 2. Keepalived Overview - Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/load_balancer_administration/ch-keepalived-overview-vsa)
[How To Set Up Highly Available Web Servers with Keepalived and Floating IPs on Ubuntu 14.04 | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-highly-available-web-servers-with-keepalived-and-floating-ips-on-ubuntu-14-04)
