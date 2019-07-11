---
title: "Container Ecosystem"
date: 2014-12-11 17:37:50
categories:
  - container
tags:
  - shell-tool
  - devops
  - web-deploy
---

> rename to `cloud-native`? separate `Containers` from it

# Container Ecosystem

> see `container-orchestration.md`
> see `container-arm.md`

[CNCF Cloud Native Interactive Landscape](https://landscape.cncf.io/) [source](https://github.com/cncf/landscape)
[The Beginner’s Guide to the CNCF Landscape - Cloud Native Computing Foundation](https://www.cncf.io/blog/2018/11/05/34097/)
[What is cloud-native? The modern way to develop applications | InfoWorld](https://www.infoworld.com/article/3281046/what-is-cloud-native-the-modern-way-to-develop-software.html)
[Towards a Kubernetes native Future – CloudARK – Medium](https://medium.com/@cloudark/towards-a-kubernetes-native-future-3e75d7eb9d42)

[Inside the Linux Container Ecosystem - Online Edition](https://www.sdxcentral.com/reports/linux-container-ecosystem/)
[The Docker Ecosystem | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/the-docker-ecosystem) !important, 2015-01
[Sysdig | The Container Ecosystem Project](https://sysdig.com/blog/the-container-ecosystem-project/) 2015-10
[Docker Ecosystem Rosetta Stones – zwischenzugs](https://zwischenzugs.com/2015/12/22/docker-ecosystem-rosetta-stones/) 2015-12
[Open Container Ecosystem - MindMeister Mind Map](https://www.mindmeister.com/389671722/docker-ecosystem)
[Understanding the Docker Ecosystem - via @codeship | via @codeship](http://blog.codeship.com/understanding-the-docker-ecosystem/)
[Codenvy Market Map (Spring 2016)](https://codenvy.com/docs/Codenvy-Market-Map-Spring-2016.pdf) (PDF)
[eBooks Series: The Docker and Container Ecosystem - The New Stack](http://thenewstack.io/ebookseries/)
[Basics - Docker, Containers, Hypervisors, CoreOS - EtherealMind](http://etherealmind.com/basics-docker-containers-hypervisors-coreos/)
[Codeship Webinar Video: An Introduction to Web Apps with Docker](http://resources.codeship.com/webinars/thank-you-video-an-introduction-to-web-apps-with-docker)
[解读 2017 之容器篇：后 Kubernetes 时代](https://mp.weixin.qq.com/s?__biz=MzIzNjUxMzk2NQ==&mid=2247488689&idx=1&sn=00fe79c0156d62f7db6d8ef2447457b2&=41#wechat_redirect)
[The Docker Ecosystem: An Introduction to Common Components | DigitalOcean](https://www.digitalocean.com/community/tutorials/the-docker-ecosystem-an-introduction-to-common-components) 2015-02

[Fundamentals of Containers, Kubernetes, and Red Hat OpenShift | edX](https://www.edx.org/course/fundamentals-containers-kubernetes-red-hat-do081x)
[50+ Useful Docker Tools | Caylent](http://caylent.com/50-useful-docker-tools/)

[NodeUp: ninetyeight - A Docker Show #2](http://nodeup.com/ninetyeight)

## Containers

[Linux Containers](https://linuxcontainers.org/) [Linux Container (LXC) Introduction - YouTube](https://www.youtube.com/watch?v=_KnmRdK69qM)
[Linux Containers - LXC - Getting started](https://linuxcontainers.org/lxc/getting-started/)
[Linux Containers - LXD - Introduction](https://linuxcontainers.org/lxd/introduction/) This is the Docker Engine equivalent
[LXC 1.0: Blog post series [0/10] | Stéphane Graber's website](https://www.stgraber.org/2013/12/20/lxc-1-0-blog-post-series/)
[LXC - Wikiwand](http://www.wikiwand.com/en/LXC)
[LXC vs Docker comparison criteria deep dive - Robin Systems](https://robinsystems.com/blog/containers-deep-dive-lxc-vs-docker-comparison/)

[How to easily run graphics-accelerated GUI apps in LXD containers on your Ubuntu desktop – Mi blog lah!](https://blog.simos.info/how-to-easily-run-graphics-accelerated-gui-apps-in-lxd-containers-on-your-ubuntu-desktop/)

[A Brief History of Containers: From 1970s chroot to Docker 2016](http://blog.aquasec.com/a-brief-history-of-containers-from-1970s-chroot-to-docker-2016)
[What is Docker? Linux containers explained | InfoWorld](http://www.infoworld.com/article/3204171/linux/what-is-docker-linux-containers-explained.html)
[From dotCloud to Docker](http://jpetazzo.github.io/2017/02/24/from-dotcloud-to-docker/)
[5 Years at Docker · KenCochrane.net](https://www.kencochrane.net/2017/03/24/5-years-at-docker/)
[Container Defense in Depth - The New Stack](http://thenewstack.io/container-defense-depth/)
[A Practical Introduction to Container Terminology - RHD Blog](https://developers.redhat.com/blog/2018/02/22/container-terminology-practical-introduction/)
[Containers for all - are we there yet? • DEVCLASS](https://devclass.com/2018/12/21/containers-for-all-are-we-there-yet/)

Houses vs apartments
[Virtual Machines vs Docker Containers - Dive Into Docker - YouTube](https://www.youtube.com/watch?v=TvnZTi_gaNc)
[Containers and VMs - A Practical Comparison - YouTube](https://www.youtube.com/watch?v=L1ie8negCjc)
[Lightboard VMs vs. Containers: Advanced Deep Dive - YouTube](https://www.youtube.com/watch?v=PoiXuVnSxfE)

[[Podcast] PodCTL #3 - Making Sense of Container Standards – OpenShift Blog](https://blog.openshift.com/podcast-podctl-3-making-sense-of-container-standards/)
[A Comparison of Linux Container Images - Crunch Tools](http://crunchtools.com/comparison-linux-container-images/)
[Containers are Linux](https://www.redhat.com/en/blog/containers-are-linux)

Containers is implemented with these Linux kernel features:

- CGroup (control group)
- [Namespace](http://man7.org/linux/man-pages/man7/user_namespaces.7.html) ([unshare(2)](https://linux.die.net/man/2/unshare), [setns(2)](https://linux.die.net/man/2/setns))
- [Capability Filter](https://linux.die.net/man/7/capabilities)
  [Docker security](https://docs.docker.com/engine/security/security/)
  Solaris's Zone and BSD's Jail are similar implementation in non-Linux kernels.

[Everything You Need to Know about Linux Containers, Part I: Linux Control Groups and Process Isolation | Linux Journal](https://www.linuxjournal.com/content/everything-you-need-know-about-linux-containers-part-i-linux-control-groups-and-process)
[Everything You Need to Know about Linux Containers, Part II: Working with Linux Containers (LXC) | Linux Journal](https://www.linuxjournal.com/content/everything-you-need-know-about-linux-containers-part-ii-working-linux-containers-lxc)
[Everything You Need to Know about Containers, Part III: Orchestration with Kubernetes | Linux Journal](https://www.linuxjournal.com/content/everything-you-need-know-about-containers-part-iii-orchestration-kubernetes)

[Linux Container Internals (Part I) – Rabbit Stack](https://rabbitstack.github.io/operating systems/containers/linux-containers-internals-part-i/)
[Linux Container Internals (Part II) – Rabbit Stack](https://rabbitstack.github.io/operating systems/containers/linux-container-internals-part-ii/)
[The History of Pets vs Cattle and How to Use the Analogy Properly | Cloudscaling](http://cloudscaling.com/blog/cloud-computing/the-history-of-pets-vs-cattle/)
The crux of Pets is indispensability, statefulness does not implies being Pets

[Containers from Scratch | posts](https://ericchiang.github.io/post/containers-from-scratch/)

[Containers and VMs - A Practical Comparison - YouTube](https://www.youtube.com/watch?v=L1ie8negCjc)

```sh
# check PID of containerized process *on host*, 29840
$ sudo ls -l /proc/29840/ns
total 0
lrwxrwxrwx. 1 root root 0 Oct 15 17:31 ipc -> 'ipc:[4026531839]'
lrwxrwxrwx. 1 root root 0 Oct 15 17:31 mnt -> 'mnt:[4026532434]'
lrwxrwxrwx. 1 root root 0 Oct 15 17:31 net -> 'net:[4026531969]'
lrwxrwxrwx. 1 root root 0 Oct 15 17:31 pid -> 'pid:[4026532446]'
lrwxrwxrwx. 1 root root 0 Oct 15 17:31 user -> 'user:[4026531837]'
lrwxrwxrwx. 1 root root 0 Oct 15 17:31 uts -> 'uts:[4026531838]'
# use nsenter to join the namespace
$ sudo nsenter --pid=/proc/29840/ns/pid \
    unshare -f --mount-proc=$PWD/rootfs/proc \
    chroot rootfs /bin/bash
root@localhost:/# ps aux
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.0  20272  3064 ?        S+   00:25   0:00 /bin/bash
root         5  0.0  0.0  20276  3248 ?        S    00:29   0:00 /bin/bash
root         6  0.0  0.0  17504  1984 ?        R+   00:30   0:00 ps aux
```

[Namespaces in operation, index [LWN.net]](https://lwn.net/Articles/531114/#series_index)
[Cgroups, namespaces, and beyond: what are containers made from? - YouTube](https://www.youtube.com/watch?v=sK5i-N34im8)
[What Have Namespaces Done for You Lately? - YouTube](https://www.youtube.com/watch?v=MHv6cWjvQjM)

[Containers 101: Linux containers and Docker explained | InfoWorld](http://www.infoworld.com/article/3072929/linux/containers-101-linux-containers-and-docker-explained.html)
[Docker 基础技术：Linux CGroup | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17049.html)
[Docker 基础技术：Linux Namespace（上） | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17010.html)
[Docker 基础技术：Linux Namespace（下） | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17029.html)
[Docker 基础技术：AUFS | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17061.html)
[Docker 基础技术：DeviceMapper | | 酷 壳 - CoolShell](https://coolshell.cn/articles/17200.html)

[OpenVZ Virtuozzo Containers Wiki](http://openvz.org/Main_Page)

> see `docker.md`
> see `rocket.md`

[Bryan Cantrill on FreeBSD Jails and Solaris Zones - YouTube](https://www.youtube.com/watch?v=hgN8pCMLI2U)

[Welcome to Vagga’s documentation! — Vagga documentation](http://vagga.readthedocs.org/en/latest/)

[Docker vs LXC](https://www.upguard.com/articles/docker-vs-lxc)
[Flockport - LXC vs Docker](https://www.flockport.com/lxc-vs-docker/)
[Flockport - LXC vs LXD vs Docker - Making sense of the rapidly evolving container ecosystem](https://www.flockport.com/lxc-vs-lxd-vs-docker-making-sense-of-the-rapidly-evolving-container-ecosystem/)
[Flockport - Sleepwalking into a Monoculture and Lock-in with Linux Containers](https://www.flockport.com/sleepwalking-into-a-monoculture-lock-in-with-linux-containers/)
[Basics - Docker, Containers, Hypervisors, CoreOS - EtherealMind](http://etherealmind.com/basics-docker-containers-hypervisors-coreos/)

### OCI

[Open Container Initiative](https://www.opencontainers.org/) [GitHub](https://github.com/opencontainers)
[App Container](https://github.com/appc)

[Making Sense of Container Standards and Foundations: OCI, CNCF, appc and rkt](https://coreos.com/blog/making-sense-of-standards/)

[OCIv2 | Cyphar](https://www.cyphar.com/blog/tag/ociv2-images/)

#### runC

Evolution:
[lmctfy - Let Me Contain That For You](http://lmctfy.io/) ([PDF](http://www.linuxplumbersconf.org/2013/ocw//system/presentations/1239/original/lmctfy%20%281%29.pdf)) (merged to libcontainer)
[docker/libcontainer](https://github.com/docker/libcontainer)(donated to OCI as part of runC)

[Open Container Project](http://runc.io/)
[opencontainers/runc](https://github.com/opencontainers/runc)
[Introducing runC: a lightweight universal container runtime | Docker Blog](https://blog.docker.com/2015/06/runc/)
[4 reasons why Docker's libcontainer is a big deal | InfoWorld](http://www.infoworld.com/article/2607966/application-virtualization/4-reasons-why-docker-s-libcontainer-is-a-big-deal.html)
[Jessie Frazelle's Blog: Runc Containers on the Desktop](https://blog.jessfraz.com/post/runc-containers-on-the-desktop/) from Docker to RunC
[jfrazelle/containers: runc configs for containers.](https://github.com/jfrazelle/containers)

[Docker 背后的容器管理——Libcontainer 深度解析](http://www.infoq.com/cn/articles/docker-container-management-libcontainer-depth-analysis)
[Docker 背后的标准化容器执行引擎——runC](http://www.infoq.com/cn/articles/docker-standard-container-execution-engine-runc)

#### containerd

[Containerd Project](https://containerd.tools/)
[docker/containerd: A daemon to control runC](https://github.com/docker/containerd)
Containerd was released to public in 2015-12, integrated to Docker Engine 1.11 in 2016-04
[Docker containerd integration | Docker Blog](https://blog.docker.com/2016/04/docker-containerd-integration)

[containerd Deep Dive: Intro to containerd · Container42](https://container42.com/2017/10/14/containerd-deep-dive-intro/)
[containerd Deep Dive // Speaker Deck](https://speakerdeck.com/stevvooe/containerd-deep-dive)

[Docker 1.11 et plus: Engine is now built on runC and containerd — Medium](https://medium.com/@tiffanyfayj/docker-1-11-et-plus-engine-is-now-built-on-runc-and-containerd-a6d06d7e80ef)
Compared to the Docker Engine, containerd exposes essentially a CRUD interface around containers, using gRPC; while the Engine exposes not only containers, but also images, volumes, networks, builds, etc. using a full-blown HTTP API.

[Open Container Initiative Launches a Container Image Format Spec - The New Stack](http://thenewstack.io/open-container-initiative-launches-container-image-format-spec/)  
[Containerd 1.0 Release Becomes the Public Face of Containers - The New Stack](https://thenewstack.io/containerd-1-0-release/)  
[Docker components explained](http://alexander.holbreich.org/docker-components-explained/)

### Docker in Windows

[Windows Containers Documentation](https://msdn.microsoft.com/virtualization/windowscontainers/containers_welcome)
[Windows Container on Windows 10](https://msdn.microsoft.com/virtualization/windowscontainers/quick_start/quick_start_windows_10)
[How to build a Node.js Nano Server Docker base image](http://stefanscherer.github.io/how-to-build-nodejs-nanoserver-image/)
[What you need to know about Docker in Windows | InfoWorld](http://www.infoworld.com/article/3163257/application-development/what-you-need-to-know-about-docker-in-windows.html)
[The Similarities and Differences Between Windows and Linux Containers | Rancher Labs](https://rancher.com/the-similarities-and-differences-between-windows-and-linux-containers/)

### Eric Hansen@Linux.org

[Linux Containers: Part 1, The Intro | Linux.org](http://www.linux.org/threads/linux-containers-part-1-the-intro.4379/)
[Linux Containers: Part 2, Creating Stopping and Connecting | Linux.org](http://www.linux.org/threads/linux-containers-part-2-creating-stopping-and-connecting.4399/)
[Linux Containers: Part 3, Tools of the Trade | Linux.org](http://www.linux.org/threads/linux-containers-part-3-tools-of-the-trade.4402/)
[Linux Containers: Part 4, Getting to the Universe (Ping Google.com) | Linux.org](http://www.linux.org/threads/linux-containers-part-4-getting-to-the-universe-ping-google-com.4428/)
[Linux Containers: Part 5, Creating Your Own VPN | Linux.org](http://www.linux.org/threads/linux-containers-part-5-creating-your-own-vpn.4431/)
[Linux Containers: Part 6, Additional VPN Security | Linux.org](http://www.linux.org/threads/linux-containers-part-6-additional-vpn-security.4459/)
[Linux Containers: Part 7, HTTP and HTTPS Routing | Linux.org](http://www.linux.org/threads/linux-containers-part-7-http-and-https-routing.4544/)

## Security

> see `linux-security.md`

[Docker security](https://docs.docker.com/engine/security/security/)
[Understanding Docker Security and Best Practices | Docker Blog](https://blog.docker.com/2015/05/understanding-docker-security-and-best-practices/)
[Docker Engine 1.10 Security Improvements | Docker Blog](https://blog.docker.com/2016/02/docker-engine-1-10-security/)

[Bitnami Engineering Portal: Why non-root containers are important for security](https://engineering.bitnami.com/articles/why-non-root-containers-are-important-for-security.html)

[A House of Cards: An Exploration of Security When Building Docker Containers | Heroku](https://blog.heroku.com/exploration-of-security-when-building-docker-containers)

[New Docker Security Features and What They Mean: Seccomp Profiles](http://blog.aquasec.com/new-docker-security-features-and-what-they-mean-seccomp-profiles)
[Docker 1.10 Security Features, part 2: Authorization Plug-In](http://blog.aquasec.com/docker-1.10-security-features-part-2-authorization-plug-in)
[Docker 1.10 Security Features, Part 3: User Namespace](http://blog.aquasec.com/docker-1.10-user-namespace)
[Docker 1.11 and CIS Benchmark: What’s New in Security?](http://blog.aquasec.com/docker-1.11-and-cis-benchmark-whats-new-in-security)

[Introducing Peekr™, Scalock’s Free Security Scanner for Container Images](http://blog.aquasec.com/introducing-peekr-scalocks-free-security-scanner-for-container-images)
[Anchore Open Source - Analysis and Policy Management for Containers](https://anchore.com/opensource/)
[Automated Container Security » ADMIN Magazine](http://www.admin-magazine.com/Articles/Securing-containers-with-Anchore)
[The known knowns - the importance of ongoing security scans for containers](http://blog.aquasec.com/the-known-unknowns-the-importance-of-ongoing-security-scans-for-containers)

[Tech N' Talk: Ten Layers of Container Security with Red Hat's Kirsten Newcomer – Red Hat OpenShift Blog](https://blog.openshift.com/tech-n-talk-ten-layers-of-container-security-with-red-hats-kirsten-newcomer/)
[Container Security 20170802](https://www.redhat.com/en/engage/container-security-20170802) 0 layers of container security

[A Field Guide to Docker Security Measures – zwischenzugs](https://zwischenzugs.com/2015/05/21/a-field-guide-to-docker-security-measures/)

[The Evolution of Docker Container Security: Part I](http://www.itprotoday.com/cloud-data-center/evolution-docker-container-security-part-1)

[Docker - Introduction to User Namespaces in Docker Engine](https://success.docker.com/KBase/Introduction_to_User_Namespaces_in_Docker_Engine)
[Docker Security: Best Practices for your Vessel & Containers](http://linux-audit.com/docker-security-best-practices-for-your-vessel-and-containers/)
[Five Docker Security Best Practices - The New Stack](https://thenewstack.io/5-docker-security-best-practices/)
[Containers have arrived -- and no one knows how to secure them | InfoWorld](http://www.infoworld.com/article/2923852/security/containers-have-arrived-and-no-one-knows-how-to-secure-them.html)
[5 keys to conquering container security | InfoWorld](http://www.infoworld.com/article/3104030/security/5-keys-to-docker-container-security.html)
[8 Docker security rules to live by | InfoWorld](http://www.infoworld.com/article/3154711/security/8-docker-security-rules-to-live-by.html)
[7 container security tools to lock down Docker and Kubernetes | InfoWorld](https://www.infoworld.com/article/3234671/containers/7-container-security-tools-to-lock-down-docker-and-kubernetes.html)

`docker daemon` with `--userns-remap`
[User Namespaces Demo - asciinema](https://asciinema.org/a/5uyrknsjg7u2fad6ii0wgizd4?speed=3)

[Docker security Part 1 | Opensource.com](https://opensource.com/business/14/7/docker-security-selinux)
[Docker security Part 2 | Opensource.com](https://opensource.com/business/14/9/security-for-docker)

[Docker Security Nathan McCauley and Diogo Mónica - YouTube](https://www.youtube.com/watch?v=8mUm0x1uy7c&list=PLkA60AVN3hh94tm0_6_rGxamkuHOLr30l&index=10) [slide](https://www.slideshare.net/Docker/docker-security-for-slide)

[Free eBook - Docker Security - Using Containers Safely in Production](https://www.openshift.com/promotions/docker-security.html)
[Introduction to Container Security](https://d3oypxn00j2a10.cloudfront.net/assets/img/Docker%20Security/WP_Intro_to_container_security_03.20.2015.pdf) (PDF)

[Container Defense in Depth - The New Stack](http://thenewstack.io/container-defense-depth/)

[Container Myths Debunked (Redux) - Crunch Tools](http://crunchtools.com/container-myths-redux/)
[Securing Docker Containers with sVirt and Trusted Sources - Crunch Tools](http://crunchtools.com/securing-docker-svirt/)

[Containing an Attack with Linux Containers and AppArmor/SELinux : Jay Beale : Free Download & Streaming : Internet Archive](https://archive.org/details/Containing_An_Attack_With_Linux_Containers)

[docker/docker-bench-security: The Docker Bench for Security is a script that checks for dozens of common best-practices around deploying Docker containers in production. https://dockerbench.com](https://github.com/docker/docker-bench-security)

[coreos/clair: Container Vulnerability Analysis Service](https://github.com/coreos/clair)
[CoreOS takes on software security for containers | InfoWorld](http://www.infoworld.com/article/3045345/virtualization/coreos-takes-on-software-security-for-containers.html)

[CONTAINERS AND SECURITY](https://www.socallinuxexpo.org/sites/default/files/presentations/cameron_containers_and_security_scale14x.pdf) (PDF)
[User Namespaces - ContainerCon 2015](https://events.linuxfoundation.org/sites/events/files/slides/User Namespaces - ContainerCon 2015 - 16-9-final_0.pdf) (PDF)

## Service Discovery

> see `coreos.md`

### Consul

> see `hashicorp.md#consul`

## PaaS

[gliderlabs/herokuish: Utility for emulating Heroku build and runtime tasks in containers](https://github.com/gliderlabs/herokuish)
[progrium/cedarish: Heroku Cedar-ish Base Image for Docker](https://github.com/progrium/cedarish)

### Deis

[Deis | The Kubernetes Company](https://deis.com/)

[Deis Workflow | Open Source Kubernetes PaaS](https://deis.com/workflow/) v2 PaaS
[deis/workflow: The open source PaaS for Kubernetes.](https://github.com/deis/workflow)

[deis/deis: Your PaaS. Your Rules.](https://github.com/deis/deis/) v1 PaaS

### Flynn

[Flynn – The product that ops provides to developers](https://flynn.io/)
[flynn/flynn: A next generation open source platform as a service (PaaS)](https://github.com/flynn/flynn)

### Dokku

[dokku/dokku: A docker-powered PaaS that helps you build and manage the lifecycle of applications](https://github.com/dokku/dokku)
[Dokku - The smallest PaaS implementation you've ever seen](http://dokku.viewdocs.io/dokku/)

[Dokku Tutorials | DigitalOcean](https://www.digitalocean.com/community/tags/dokku)
[How to Get Started with Dokku Debian 8 - UpCloud](https://www.upcloud.com/support/get-started-dokku-debian/)
[Digital Ocean + Dokku = 10\$ Heroku](http://beletsky.net/2013/08/digitalocean-plus-dokku-equals-10-heroku.html)
[PaaS in Your Pocket with Dokku](http://beletsky.net/2013/09/paas-in-your-pocket-with-dokku.html)

[sehrope/dokku-logging-supervisord: Individual app logs and supervisord for Dokku](https://github.com/sehrope/dokku-logging-supervisord)

## State Management

[Containerizing stateful applications | InfoWorld](http://www.infoworld.com/article/3106416/cloud-computing/containerizing-stateful-applications.html)
[Solving the Stateful Service Problem in Container Orchestration](http://blog.traintracks.io/solving-the-stateful-service-problem-in-container-orchestration/)

## Secret Management

[How to keep container secrets secret | InfoWorld](http://www.infoworld.com/article/3211285/containers/how-to-keep-container-secrets-secret.html)

## Cloud Native Application Bundles (CNAB)

[CNAB: Cloud Native Application Bundles](https://cnab.io/)

[Docker App and CNAB - Docker Blog](https://blog.docker.com/2018/12/docker-app-and-cnab/)
[docker/app: Make your Docker Compose applications reusable, and share them on Docker Hub](https://github.com/docker/app)

[Bitnami Engineering Portal: Production Ready Packaging with CNAB and Bitnami Kubernetes Production Runtime (BKPR)](https://engineering.bitnami.com/articles/production-ready-packaging-with-cnab-and-bitnami-kubernetes-production-runtime-bkpr.html)

## Cloud Native Buildpacks (CNB)

[Cloud Native Buildpack Documentation · Cloud Native Buildpack Documentation](https://buildpacks.io/)
[Turn Your Code into Docker Images with Cloud Native Buildpacks | Heroku](https://blog.heroku.com/docker-images-with-buildpacks)

[Cloud Native Buildpacks](https://github.com/buildpack)
[buildpack/samples: Samples for buildpack creators](https://github.com/buildpack/samples)

## Monitoring

> see `devops.md#Prometheus`

[Building A Central Logging Service In-House — Smashing Magazine](https://www.smashingmagazine.com/2018/05/building-central-logging-service/)
[4 Common Kubernetes-Monitoring Traps to Avoid - The New Stack](https://thenewstack.io/4-common-kubernetes-monitoring-traps-to-avoid/)

[Dockers Monitoring Tools -](https://www.level-up.one/dockers-monitoring-tools/)
[Deep Dive into Docker Logging - Level UpLevel Up](https://www.level-up.one/deep-dive-into-docker-logging/)
[ctop](https://ctop.sh/) [bcicen/ctop: Top-like interface for container metrics](https://github.com/bcicen/ctop)
[Monitoring Docker Containers - docker stats, cAdvisor, Universal Control Plane](http://blog.couchbase.com/2016/april/monitoring-docker-containers-docker-stats-cadvisor-universal-control-plane)
[Gathering container metrics](http://jpetazzo.github.io/2013/10/08/docker-containers-metrics/)
[Adventures in GELF](http://jpetazzo.github.io/2017/01/20/docker-logging-gelf/)

[Auditing Docker Containers in a DevOps Environment » ADMIN Magazine](http://www.admin-magazine.com/Archive/2018/43/Auditing-Docker-Containers-in-a-DevOps-Environment) with `auditd`

[Monitoring Kubernetes, part 1: the challenges + data sources - Cloud Native Computing Foundation](https://www.cncf.io/blog/2019/01/09/monitoring-kubernetes-part-1-the-challenges-data-sources/)

[Container Monitoring: Top Docker Metrics to Watch](https://sematext.com/blog/2016/06/28/top-docker-metrics-to-watch/)
[Open Source Docker Monitoring & Logging](https://sematext.com/blog/2016/07/19/open-source-docker-monitoring-logging/)

[Monitoring Docker with docker-scout](http://blog.scoutapp.com/articles/2015/03/16/monitoring-docker)
[Collect all Logs From a Docker Swarm Cluster](http://jmkhael.hopto.org/collect-all-logs-from-a-docker-swarm-cluster/)
[Multiple Docker containers logging to a single syslog](http://jpetazzo.github.io/2014/08/24/syslog-docker/)

[A monitoring solution for Docker hosts, containers and containerized services](https://stefanprodan.com/2016/a-monitoring-solution-for-docker-hosts-containers-and-containerized-services/) Prometheus, Grafana, cAdvisor, NodeExporter and AlertManager
[Monitor your applications with Prometheus](https://blog.alexellis.io/prometheus-monitoring/) Prometheus, NodeExporter

[#SwarmWeek: Realtime Cluster Monitoring with Docker Swarm and Riemann | Docker Blog](https://blog.docker.com/2016/03/realtime-cluster-monitoring-docker-swarm-riemann/)
[Monitoring Metrics for Docker Containers](https://www.infoq.com/news/2016/07/containermetrics)
[How Docker changes application monitoring | InfoWorld](http://www.infoworld.com/article/3138035/data-center/how-docker-changes-application-monitoring.html)

[An Overview of the Logging Ecosystem in 2017 - via @codeship | via @codeship](https://blog.codeship.com/an-overview-of-the-logging-ecosystem-in-2017/)
[Monitoring Docker Containers with Elasticsearch and cAdvisor | via @codeship](https://blog.codeship.com/monitoring-docker-containers-with-elasticsearch-and-cadvisor/) ELK 2.x + cAdvisor
[Monitoring Docker Containers: docker stats, cAdvisor... | via @codeship](https://blog.codeship.com/monitoring-docker-containers/) Prometheus + InfluxDB + cAdvisor

[Kubernetes Monitoring: Best Practices on Vimeo](https://vimeo.com/285843343)

[google/cadvisor: Analyzes resource usage and performance characteristics of running containers.](https://github.com/google/cadvisor)
[Sysdig | Wiki | Getting Started](http://www.sysdig.org/wiki/getting-started/)

### sematext

[Reference Architecture: Monitoring and Logging for Docker Datacenter](https://sematext.com/docker-datacenter-monitoring-and-logging/)

[Docker “Swarm Mode”: Full Cluster Monitoring & Logging with 1 Command](https://sematext.com/blog/2016/09/19/docker-swarm-mode-full-cluster-monitoring-logging-with-1-command/)

### logspout

[gliderlabs/logspout: Log routing for Docker container logs](https://github.com/gliderlabs/logspout)
[looplab/logspout-logstash: A minimalistic adapter for github.com/gliderlabs/logspout to write to Logstash UDP](https://github.com/looplab/logspout-logstash)
[rtoma/logspout-redis-logstash: Logspout adapter for writing Docker container logs to Redis in Logstash jsonevent layout](https://github.com/rtoma/logspout-redis-logstash)

## Docker Flow

[Docker Flow: Blue-Green Deployment and Relative Scaling | Technology Conversations](http://technologyconversations.com/2016/03/07/docker-flow-blue-green-deployment-and-relative-scaling/)
[vfarcic/docker-flow: Docker Flow: Blue-Green Deployment and Relative Scaling](https://github.com/vfarcic/docker-flow)

### Docker Flow: Proxy

[vfarcic/docker-flow-proxy](https://github.com/vfarcic/docker-flow-proxy) HAProxy + Consul
[Docker Flow: Proxy – On-Demand HAProxy Service Discovery and Reconfiguration | Technology Conversations](http://technologyconversations.com/2016/03/21/docker-flow-proxy-on-demand-haproxy-service-discovery-and-reconfiguration/)

## azk

[azk](http://www.azk.io/) Orchestrate dev environment with Docker
[Introduction | azk Docs Gitbook](http://docs.azk.io/en/index.html)

## Bitnami

[Bitnami Kubernetes - Application Packaging and Deployment for Kubernetes](https://bitnami.com/kubernetes)

[Bitnami Kubernetes Production Runtime](https://kubeprod.io/)
[Bitnami Engineering Portal: Announcing the Bitnami Kubernetes Production Runtime (BKPR)](https://engineering.bitnami.com/articles/announcing-the-bitnami-kubernetes-production-runtime-bkpr.html)

## Crane

[michaelsauter/crane: Crane - Lift containers with ease](https://github.com/michaelsauter/crane)
[Lifting Docker containers with Crane](http://www.ivoverberk.nl/lifting-docker-containers-with-crane/)

## Packer

> see `hashicorp.md#packer`

## Rancher

> see `rancher.md`

## Pachyderm

Distributed system for data science

[Pachyderm - Scalable, Reproducible Data Science](https://pachyderm.io/)
[Pachyderm Developer Documentation — Pachyderm documentation](https://pachyderm.readthedocs.io/en/latest/)

## Node.js

[Create a Node.js Container image for Windows](https://stefanscherer.github.io/create-an-io-js-container-image-for-windows/)
[Minimal Docker Containers for Node.js | @RisingStack](https://blog.risingstack.com/minimal-docker-containers-for-node-js/)
[StrongLoop | Containerizing Node.js Apps with Docker and StrongLoop](https://strongloop.com/strongblog/containerizing-node-js-apps-with-docker-and-strongloop/)
[Containerizing a Node.js Application for Development With Compose | DigitalOcean](https://www.digitalocean.com/community/tutorials/containerizing-a-node-js-application-for-development-with-docker-compose)
[Dockerizing a Node.js Web Application - Semaphore](https://semaphoreci.com/community/tutorials/dockerizing-a-node-js-web-application)
[danawoodman/docker-node-hello-world](https://github.com/danawoodman/docker-node-hello-world)
[Running a MEAN web application in Docker containers on AWS | via @codeship](http://blog.codeship.com/running-mean-web-application-docker-containers-aws/)

## nearForm

[mcollina/docker-loghose: Collect all the logs from all docker containers](https://github.com/mcollina/docker-loghose)

[apparatus/fuge](https://github.com/apparatus/fuge)
[nearForm releases fuge for microservices - nearForm](http://www.nearform.com/nodecrunch/release-fuge-microservices/)
[apparatus/fuge-runner: Process and container runner and watcher for the fuge tool](https://github.com/apparatus/fuge-runner)

[nodezoo/nodezoo-workshop: A microservices workshop for the Seneca framework.](https://github.com/nodezoo/nodezoo-workshop)
[nodezoo/nodezoo-system: A preconfigured set of scripts to run nodezoo via fuge](https://github.com/nodezoo/nodezoo-system)

[nscale](http://nscale.nearform.com/)
[nScale – microservices deployer for Node.js - nearForm](http://www.nearform.com/tool-nscale/)
[Introducing nscale for deployment - nearForm](http://www.nearform.com/nodecrunch/introducing-nscale-deployment/)
[nearform/nscale-docs: Documentation for nscale](https://github.com/nearform/nscale-docs/)0
[nscale-docs/tutorials at master · nearform/nscale-docs](https://github.com/nearform/nscale-docs/tree/master/tutorials)

## CloudFoundary

[bosh](https://bosh.io/) BOSH is an open source tool for release engineering, deployment, lifecycle management, and monitoring of distributed systems.

[cloudfoundry-incubator/diego-release: BOSH Release for Diego](https://github.com/cloudfoundry-incubator/diego-release)
[Diego Architecture | Cloud Foundry Docs](https://docs.cloudfoundry.org/concepts/diego/diego-architecture.html#architecture)

[Cloud Foundry stages a comeback | InfoWorld](http://www.infoworld.com/article/3082062/paas/cloud-foundry-stages-a-comeback.html)
[Are Diego and Docker Really Good Friends? - Blog on All Things Cloud Foundry](http://blog.altoros.com/are-diego-and-docker-really-good-friends.html)

## IaaS

[RackHD](https://rackhd.github.io/)
[RackHD Archives - {code}](https://blog.thecodeteam.com/tag/RackHD/)

## FaaS

[Serverless - The Serverless Application Framework powered by AWS Lambda, API Gateway, and more](https://serverless.com/)
[The Leading Open Source Serverless Solutions for Kubernetes](https://gravitational.com/blog/serverless-on-kubernetes/)
[CNCF Cloud Native Interactive Landscape serverless](https://landscape.cncf.io/format=serverless)

[Open source serverless computing: Fission, Fn, Kubeless, and OpenWhisk | InfoWorld](https://www.infoworld.com/article/3279781/application-development/open-source-serverless-fission-fn-kubeless-and-openwhisk.html)
[Demystifying Serverless & OpenFaas – Collabnix](http://collabnix.com/demystifying-openfaas-simplifying-serverless-computing/)

[gloo](https://gloo.solo.io/) Function gateway for microservice, monolithic, and serverless applications

[Functions as a Service (FaaS)](https://blog.alexellis.io/functions-as-a-service/)
[alexellis/faas: Functions as a Service - a serverless framework for Docker](https://github.com/alexellis/faas)
[iron-io/functions: IronFunctions - the serverless microservices platform by](https://github.com/iron-io/functions)

[metrue/fx: fx is a framework to help you do Function as a Service with painless on your own servers](https://github.com/metrue/fx)

[Kubeless](https://kubeless.io/)
[Serverless Functions for Kubernetes - Fission](https://fission.io/)
[funktionio/funktion: a CLI tool for working with funktion](https://github.com/funktionio/funktion/)

[One-shot containers with Docker Swarm](https://blog.alexellis.io/containers-on-swarm/)
[alexellis/jaas: CLI to run tasks / batch jobs / ah-hoc containers on Docker Swarm](https://github.com/alexellis/jaas)

[A crash course on Serverless APIs with Express and MongoDB](https://hackernoon.com/a-crash-course-on-serverless-apis-with-express-and-mongodb-77774f7730fe)

### Knative

> Knative is a project to create a standard set of building blocks for Kubernetes to enable serverless development patterns. It’s not a complete serverless framework.

[Knative  |  Google Cloud](https://cloud.google.com/knative/)
[docs/README.md at master · knative/docs](https://github.com/knative/docs/blob/master/README.md)
[Knative: bringing serverless to Kubernetes everywhere | Google Cloud Blog](https://cloud.google.com/blog/products/containers-kubernetes/knative-bringing-serverless-to-kubernetes-everywhere)
[How Knative Can Unite Kubernetes and Serverless - The New Stack](https://thenewstack.io/how-knative-can-unite-kubernetes-and-serverless/)

[knative/build: A Kubernetes-native Build resource.](https://github.com/knative/build)
[First look at knative build for OpenFaaS functions](https://blog.alexellis.io/first-look-at-knative-build-for-openfaas-functions/)

[Introduction to Knative – Paul Czarkowski – Medium](https://medium.com/@pczarkowski/introduction-to-knative-b93a0b9aeeef)
[Using the Knative Build system by itself – Paul Czarkowski – Medium](https://medium.com/@pczarkowski/using-the-knative-build-system-by-itself-cf215ce01524)
[ko: fast Kubernetes microservice development in Go – Knative – Medium](https://medium.com/knative/ko-fast-kubernetes-microservice-development-in-go-f94a934a7240)
[How to use Knative on Kubernetes to deploy a Serverless Application](https://itnext.io/how-to-use-knative-on-kubernetes-to-deploy-a-serverless-application-582d62fa2a9f)
[Deploying serverless apps with Knative](https://cloud.ibm.com/docs/containers?topic=containers-serverless-apps-knative)
[redhat-developer-demos/knative-tutorial: A pratical guide to get started with knative. Knative concepts are explained simple and easy way with lots of demos and exercises.](https://github.com/redhat-developer-demos/knative-tutorial)

[Part 1: Introduction to Serverless with Knative | Red Hat Developer](https://developers.redhat.com/coderland/serverless/serverless-knative-intro/)
[Part 2: Building a Serverless Service | Red Hat Developer](https://developers.redhat.com/coderland/serverless/building-a-serverless-service/)
[Part 3: Deploying a Serverless Service to Knative | Red Hat Developer](https://developers.redhat.com/coderland/serverless/deploying-serverless-knative/)

[Knative 系列（一）：基本概念和原理解读](https://www.infoq.cn/article/PEOIcPk4lZRg-fAwry8H)
[Knative系列（二）：兵马未动粮草先行之Build篇](https://www.infoq.cn/article/D489mKhQ96dGwfj*w05E)
[Knative 系列（三）：Serving篇](https://www.infoq.cn/article/PYGUCS*yWxhLM5Rok9vF)
[Knative系列（四）：Eventing 篇](https://www.infoq.cn/article/FkKfwsvpVdC_60DfxMMg)

### OpenWhisk

[Apache OpenWhisk is a serverless, open source cloud platform](https://openwhisk.apache.org/)
[Debugging Node.js OpenWhisk Actions - James Thomas](http://jamesthom.as/blog/2018/07/10/debugging-node-dot-js-openwhisk-actions/)

### OpenFaaS

[OpenFaaS - Serverless Functions Made Simple](https://www.openfaas.com/)
[Morning coffee with the OpenFaaS CLI](https://blog.alexellis.io/quickstart-openfaas-cli/)

### KEDA

[Announcing KEDA: bringing event-driven containers and functions to Kubernetes - Open Source blog](https://cloudblogs.microsoft.com/opensource/2019/05/06/announcing-keda-kubernetes-event-driven-autoscaling-containers/)
[kedacore/keda: KEDA is a Kubernetes-based Event Driven Autoscaling component. It provides event driven scale for any container running in Kubernetes](https://github.com/kedacore/keda)
[Build Event-Driven Containers | Microsoft Azure](https://info.microsoft.com/ww-registration-Build-Event-Driven-Containers-with-Azure-Functions-on-Kubernetes.html)

## OS

There are several aspects

1. Lightweight user-land to be used as base image of container
2. Micro OS/Container OS designed to run on infrastructure to run containers

[From CoreOS to Nano: Micro OSes strip down for containers | InfoWorld](http://www.infoworld.com/article/2942721/linux/from-coreos-to-nano-micro-oses-strip-down-for-containers.html)
[Review: The best Linux distros for Docker and containers | InfoWorld](https://www.infoworld.com/article/3235229/linux/review-the-best-linux-distros-for-docker-and-containers.html)
[Container OS comparison | via @codeship](https://blog.codeship.com/container-os-comparison/)

### Alphine Linux

[Alpine Linux | Alpine Linux](http://alpinelinux.org/)
[Alpine Linux wiki](http://wiki.alpinelinux.org/wiki/Main_Page)

[docker-alpine :: viewdocs.io](http://gliderlabs.viewdocs.io/docker-alpine/)
[Docker Official Images are Moving to Alpine Linux](https://www.brianchristner.io/docker-is-moving-to-alpine-linux/)
[Flockport - A quick introduction to Alpine Linux](https://www.flockport.com/a-quick-introduction-to-alpine-linux/)
[Alpine Based Docker Images Make a Difference in Real World Apps - Nick Janetakis](http://nickjanetakis.com/blog/alpine-based-docker-images-make-a-difference-in-real-world-apps)
[Super small Docker image based on Alpine Linux | Hacker News](https://news.ycombinator.com/item?id=10782897)
[Review: Alpine Linux is made for Docker | InfoWorld](https://www.infoworld.com/article/3206644/linux/review-alpine-linux-is-made-for-docker.html)

[\_/alpine/](https://hub.docker.com/_/alpine/)
[u/iron/](https://hub.docker.com/u/iron/) built with Alpine
[envygeeks/alpine/](https://hub.docker.com/r/envygeeks/alpine/)

[Alpine Linux and Docker Nautilus Protect Crate Images | Crate.IO](https://crate.io/a/alpine-linux-and-dock er-nautilus-protect-crate/)

[Alpine Linux package management - Alpine Linux](http://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management)
[Alpine packages](https://pkgs.alpinelinux.org/packages)

### RancherOS

[RancherOS | Rancher Labs](http://rancher.com/rancher-os/) OS built out of Docker containers.
Linux kernel hands of to `system-docker` (running as PID1), all processes it spawn are containerized.

[Rancher Documentation](http://docs.rancher.com/os/)
[RancherOS: A simpler Linux for Docker lovers | InfoWorld](https://www.infoworld.com/article/3216524/linux/rancheros-a-simpler-linux-for-docker-lovers.html)

### KurmaOS

[Kurma - Extensible and flexible container engine for a cloud native world.](http://kurma.io/)
[apcera/kurmaos: KurmaOS - Containerized operating system](https://github.com/apcera/kurmaos)

[Apcera The Trusted Cloud Platform | Innovation, Meet Trust.](https://www.apcera.com/)
[Apcera](https://github.com/apcera) GitHub org

[Resource Library | Apcera The Trusted Cloud Platform](https://www.apcera.com/multi-cloud-resources)

### Snappy Ubuntu Core

[Snappy Ubuntu Core | Cloud | Ubuntu](http://www.ubuntu.com/cloud/snappy)
[Core | Ubuntu developer portal](https://developer.ubuntu.com/en/snappy/#tour)

## VM to run containers

[It doesn't work with Docker, K8s right now, but everyone's going nuts anyway for AWS's Firecracker microVMs • The Register](https://www.theregister.co.uk/AMP/2018/11/27/aws_sets_firecracker/)

### LinuxKit

[Announcing LinuxKit: A Toolkit for building Secure, Lean and Portable Linux Subsystems - Docker Blog](https://blog.docker.com/2017/04/introducing-linuxkit-container-os-toolkit/)
[OK, I give up. Is Docker now Moby? And what is LinuxKit?](https://www.mirantis.com/blog/ok-i-give-up-is-docker-now-moby-and-what-is-linuxkit/)
[Top 10 Reasons why LinuxKit is better than the traditional OS distribution – Collabnix](http://collabnix.com/top-10-reasons-why-linuxkit-is-better-than-the-traditional-os-distribution/)
[LinuxKit Deep Dive](https://www.slideshare.net/Docker/linuxkit-deep-dive)

### Kata Containers

[Kata Containers - The speed of containers, the security of VMs](https://katacontainers.io/)
Kata Containers combines technology from Intel Clear Containers and Hyper runV. It used a CRI compatible extremely lightweight VM to run the container to archive better isolation.
[Kata Containers » ADMIN Magazine](http://www.admin-magazine.com/Articles/Isolate-workloads-from-Docker-and-Kubernetes-with-Kata-Containers?utm_source=ADMIN+Newsletter&utm_campaign=ADMIN_Update_195%3A_Kata_Containers_2019-27-03&utm_medium=email)

[kubernetes/frakti: The hypervisor-based container runtime for Kubernetes.](https://github.com/kubernetes/frakti)

[Intel® Clear Containers: Now part of Kata Containers | Clear Linux\* Project](https://clearlinux.org/containers)
[Intel takes on CoreOS with its own container-based Linux | InfoWorld](http://www.infoworld.com/article/2925038/linux/intel-takes-on-coreos-with-its-own-container-based-linux.html)

[An introduction to Clear Containers [LWN.net]](http://lwn.net/Articles/644675/)
[Intel's Clear Containers Address Security Concerns - The New Stack](http://thenewstack.io/securing-containers-intels-clear-containers/)
