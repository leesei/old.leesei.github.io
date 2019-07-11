---
title: "Container Orchestration"
date: 2014-12-11 17:37:50
categories:
- container
tags:
- devops
- web-deploy
---

# Container Orchestration

> see `docker-io.md`
> see `kubernetes.md`
> see `rancher.md`
> see `openshift.md`
> see `mesos.md`

As of 2017, Kubernetes became the tool of choice for container orchestration.
See projects under [Cloud Native Computing Foundation](https://www.cncf.io/projects/).
[micahhausler/container-transform: Transforms docker-compose, ECS, and Marathon configurations](https://github.com/micahhausler/container-transform)
[The Docker Ecosystem: Scheduling and Orchestration | DigitalOcean](https://www.digitalocean.com/community/tutorials/the-docker-ecosystem-scheduling-and-orchestration)

## Comparison

[Container Orchestration Wars (2017) - YouTube](https://www.youtube.com/watch?v=NRZ6N4e-Mko)  
[Kubernetes vs Docker Swarm: A comparison of cloud container tools](https://www.cbronline.com/in-depth/kubernetes-vs-docker-container-tools) 2018-02  
[Docker Swarm Management: A Quick Overview of Rancher, Portainer and Shipyard](https://www.servethehome.com/docker-swarm-management-a-quick-overview-of-rancher-portainer-and-shipyard/) 2017-02  
[Kubernetes, Mesos, and Swarm: Comparing the Rancher Orchestration Engine Options | Rancher Labs](http://rancher.com/comparing-rancher-orchestration-engine-options/) 2016-10 !important  
[Docker Orchestrations Compared: Kubernetes vs Amazon ECS vs Docker Cloud / Swarm / EE / Cloud (PART I)](https://sematext.com/blog/2017/04/24/docker-orchestration-poll-kubernetes-swarm-amazon-ecs/) 2017-04  
[Choosing the Right Containerization and Cluster Management Tool](https://blog.kublr.com/choosing-the-right-containerization-and-cluster-management-tool-fdfcec5700df) 2017-02  
[Container Orchestration Wars - YouTube](https://www.youtube.com/watch?v=C_u4_l84ED8) 2016-07  

[Containers, Configuration Management, and The Right Tool for the Right Job | the agile admin](http://theagileadmin.com/2015/11/10/containers-configuration-management-and-the-right-tool-for-the-right-job/) 2015-11  
[Docker and the Future of Configuration Management – Coming In November! | the agile admin](http://theagileadmin.com/2015/10/29/docker-and-the-future-of-configuration-management-coming-in-november/) 2015-10  
[Swarm v. Fleet v. Kubernetes v. Mesos - O'Reilly Media](https://www.oreilly.com/ideas/swarm-v-fleet-v-kubernetes-v-mesos) 2015-10  
[Docker Clustering Tools Compared: Kubernetes vs Docker Swarm | Technology Conversations](http://technologyconversations.com/2015/11/04/docker-clustering-tools-compared-kubernetes-vs-docker-swarm/) 2015-11  
[cluster computing - Docker-Swarm, Kubernetes, Mesos & Core-OS Fleet - Stack Overflow](http://stackoverflow.com/questions/27640633/docker-swarm-kubernetes-mesos-core-os-fleet)  
[5 Next-Gen Cloud Technologies You Should Know | Linux.com | The source for Linux information](https://www.linux.com/news/5-next-gen-cloud-technologies-you-should-know)  
[8 Container Orchestration Tools to Know | Linux.com | The source for Linux information](https://www.linux.com/news/8-open-source-container-orchestration-tools-know)  
[Docker Swarm与Apache Mesos的区别](http://www.infoq.com/cn/articles/difference-between-swarm-docker-and-mesos-apache)  
[Mesos, Kubernetes, and Infrastructure of the Future with Dharmesh Kakadia | Software Engineering Daily](https://softwareengineeringdaily.com/2016/12/14/mesos-kubernetes-and-infrastructure-of-the-future-with-dharmesh-kakadia/)  
[Docker Clustering Tools Compared: Kubernetes vs Docker Swarm | Technology Conversations](https://technologyconversations.com/2015/11/04/docker-clustering-tools-compared-kubernetes-vs-docker-swarm/) 2015-11  
[A Brief Comparison of Mesos and Kubernetes - The New Stack](http://thenewstack.io/a-brief-comparison-of-mesos-and-kubernetes/)  

[Kubernetes vs Rancher vs Docker Swarm (Pros & Cons) | StackShare](https://stackshare.io/stackups/kubernetes-vs-rancher-vs-docker-swarm)

[Docker's new orchestration tools: Any container to any cloud | InfoWorld](http://www.infoworld.com/article/2889317/application-virtualization/dockers-new-orchestration-tools-any-container-to-any-cloud.html)  
[Docker and the Future of Configuration Management | the agile admin](http://theagileadmin.com/tag/dockercmroundup/)

[garywiz/chaperone: Lightweight process-tree manager for Docker-like containers](https://github.com/garywiz/chaperone)

[Microservices Workshop](http://vfarcic.github.io/ms-workshop/#/cover)

## Apcera

[Open Source | Apcera The Trusted Cloud Platform](https://www.apcera.com/open-source)

[Apcera](https://github.com/apcera) GitHub org
[Apcera Community Edition Webinar - Docker and Persistent Storage - YouTube](https://www.youtube.com/watch?v=WYETUXP_C5M)
[Apcera Developer Portal - The Trusted Cloud Platform](https://developer.apcera.com/)
[The Apcera Cloud Platform: Community Edition | Trusted Cloud](https://www.apcera.com/community-edition)
[NATS - Cloud Native, Open Source, High Performance Messaging](http://nats.io/)
[Kurma - Extensible and flexible container engine for a cloud native world.](http://kurma.io/)

APCFS: NFSv4 compatible file system for persistent storage

## Docker For AWS

[Docker Public Beta](https://beta.docker.com/)

[Docker for AWS Public Beta - Docker Blog](https://blog.docker.com/2016/11/docker-aws-public-beta/)
[Docker for AWS: Who's it really for? | InfoWorld](http://www.infoworld.com/article/3145696/application-development/docker-for-aws-whos-it-really-for.html)

## Vagrant

> see `hashicorp.md`

Vagrant has a Docker driver since 1.6. But Docker Machine is enough for me.

[Vagrant 1.6 Feature Preview: Docker-Based Development Environments - HashiCorp](https://www.hashicorp.com/blog/feature-preview-vagrant-1-6-docker-dev-environments.html)

## Spotify

[spotify/helios: Docker container orchestration platform](https://github.com/spotify/helios)
[helios/user_manual.md at master · spotify/helios](https://github.com/spotify/helios/blob/master/docs/user_manual.md)

[Helios | Docker Blog](https://blog.docker.com/tag/helios/)
Built upon Zookeeper

[helios/helios_solo.md at master · spotify/helios](https://github.com/spotify/helios/blob/master/docs/helios_solo.md)
Docker image for Helios

## CenturyLink Labs

[Projects | CenturyLink Labs](https://labs.ctl.io/projects/)

[Panamax: Docker Management for Humans](http://panamax.io/)

[Zodiac | CenturyLink Labs](https://labs.ctl.io/projects/zodiac/)
[CenturyLinkLabs/zodiac: A lightweight tool for easy deployment and rollback of dockerized applications.](https://github.com/CenturyLinkLabs/zodiac) based on Docker Compose

[Watchtower | CenturyLink Labs](https://labs.ctl.io/projects/watchtower/)
[CenturyLinkLabs/watchtower: Automatically update running Docker containers](https://github.com/CenturyLinkLabs/watchtower)

[Dray | CenturyLink Labs](https://labs.ctl.io/projects/dray/)

## Light Weight

[The Search for a GUI Docker | Linux Journal](https://www.linuxjournal.com/content/search-gui-docker)

[Kontena - The Developer Friendly Container & Microservices Platform](https://www.kontena.io/)

[Portainer | Simple management UI for Docker](https://portainer.io/)
[Portainer documentation](https://portainer.readthedocs.io/en/stable/)

[Swarmpit](https://swarmpit.io/)
[swarmpit/swarmpit: Lightweight Docker Swarm management UI](https://github.com/swarmpit/swarmpit)

[The Imixs-Cloud | imixs-cloud](https://imixs.github.io/imixs-cloud/) uses Portainer, Swarmpit

[Kitematic](https://kitematic.com/)
[Releases · docker/kitematic](https://github.com/docker/kitematic/releases) release for all platforms

[shipyard](http://shipyard-project.com/) built on Swarm
[Using Shipyard To Manage Docker Containers – JGamblin.com](http://jerrygamblin.com/2016/06/10/using-shipyard-to-manage-docker-containers/)

Rancher > Portainer > shipyard

[Cockpit Project](http://cockpit-project.org/) administer your GNU/Linux servers via a web browser
[How to Install Cockpit on Ubuntu 18.04 - Alibaba Cloud Community](https://www.alibabacloud.com/blog/how-to-install-cockpit-on-ubuntu-18-04_594039?spm=a2c65.11461433.0.0.4ee35355t8NTC4)

[Mercateo/dwatch: Manage your docker containers, images and networks in a nice and clean way.](https://github.com/Mercateo/dwatch)
[lirantal/dockly: Immersive terminal interface for managing docker containers and services](https://github.com/lirantal/dockly)

[dockersamples/docker-swarm-visualizer: A visualizer for Docker Swarm Mode using the Docker Remote API, Node.JS, and D3](https://github.com/dockersamples/docker-swarm-visualizer)
[justone/dockviz: Visualizing docker data](https://github.com/justone/dockviz)
