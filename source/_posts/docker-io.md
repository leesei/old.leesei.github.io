---
title: "Docker.io"
date: 2014-12-11 17:38:50
categories:
- container
tags:
- shell-tool
- docker
- devops
- web-deploy
---

[Container Orchestration with Docker and Swarm](http://container.training/swarm-selfpaced.yml.html#1) !important
[Docker Swarm Workshop](http://vfarcic.github.io/docker-swarm/#/cover)

[Docker Playground](http://labs.play-with-docker.com/)
[Play with Docker Classroom](http://training.play-with-docker.com/) [all](http://training.play-with-docker.com/alacart/)

[Reference Architectures - Docker, Inc.](https://success.docker.com/Architecture) !important
[Docker Reference Architecture: Designing Scalable, Portable Docker Container Networks - Docker, Inc.](https://success.docker.com/Architecture/Docker_Reference_Architecture%3A_Designing_Scalable%2C_Portable_Docker_Container_Networks)
[Deploy and scale containers with Docker native, open source orchestration PyCon 2017 - YouTube](https://www.youtube.com/watch?v=EuzoEaE6Cqs)

## Docker Compose

Compose is a tool for defining and running multi-containers Docker applications on a *single Docker host* or *cluster using standalone Docker Swarm*.
For multi-hosts deployment on *Swarm mode* use `docker stack` on Docker 1.13+.

Compose file can be [stacked](https://docs.docker.com/compose/extends/) for environment specific settings.

Docker [acquired Orchard](https://blog.docker.com/2014/07/welcoming-the-orchard-and-fig-team/) and used its [Fig](http://www.fig.sh/index.html) as the basis of Docker Compose (released early-2015). See also [decking.io](http://decking.io/).

[Docker Compose | Docker](http://www.docker.com/products/docker-compose)  
[Overview of Docker Compose | Docker Documentation](https://docs.docker.com/compose/overview/)  
[Compose 1.6: New Compose file for defining networks and volumes | Docker Blog](https://blog.docker.com/2016/02/compose-1-6/) [Docker Compose Files Version 2 - YouTube](https://www.youtube.com/watch?v=EReEOMS7gsk)  
[Compose file version 3 reference | Docker Documentation](https://docs.docker.com/compose/compose-file/)  
[Compose file version 2 reference | Docker Documentation](https://docs.docker.com/compose/compose-file/compose-file-v2/)  
[Controlling startup order in Compose | Docker Documentation](https://docs.docker.com/compose/startup-order/) !important, wait for service  

Compose Version 3 added `deploy` key, which is ignored in `docker-compose up` for single node deployment. In swarm mode, `docker stack` (supported in 1.13+) will read the settings in `deploy` key and apply them with `docker service` calls internally.  
[docker.github.io/compose-file.md at 8524552f99e5b58452fcb1403e1c273385988b71 · aanand/docker.github.io](https://github.com/aanand/docker.github.io/blob/8524552f99e5b58452fcb1403e1c273385988b71/compose/compose-file.md)  
[docker service create | Docker Documentation](https://docs.docker.com/engine/reference/commandline/service_create/#create-services-using-templates) Template variables for swarm services

[Docker Tip #60: What Really Happens When You Run docker-compose up? — Nick Janetakis](https://nickjanetakis.com/blog/docker-tip-60-what-really-happens-when-you-run-docker-compose-up)

[A beginner’s guide to Docker — how to create a client/server side with docker-compose](https://medium.freecodecamp.org/a-beginners-guide-to-docker-how-to-create-a-client-server-side-with-docker-compose-12c8cf0ae0aa)
[How we happily dockerized our development environment (part 1/2) — Medium](https://medium.com/@aherve/how-we-happily-dockerized-our-development-environment-part-1-2-b05fd6927a53#.3rev8amcg)  
[Dockerized development environment on steroids (part 2/2) — Medium](https://medium.com/@aherve/dockerized-development-environment-on-steroids-part-2-2-b800a65d0462#.21qoaievq)

[Introduction to Docker Compose Tool for Multi-Container Applications | Linux.com | The source for Linux information](https://www.linux.com/learn/introduction-docker-compose-tool-multi-container-applications)  
[Docker Volumes and Networks with Compose | Linux.com | The source for Linux information](https://www.linux.com/learn/docker-volumes-and-networks-compose)  
[Docker tutorial: Get started with Docker Compose | InfoWorld](https://www.infoworld.com/article/3254689/devops/docker-tutorial-get-started-with-docker-compose.html)

[使用docker-compose进行python开发 | YL Notes](http://yunlzheng.github.io/2015/06/06/dev-python-with-docker-compose/)  
[Dockerizing Flask with Compose and Machine - from localhost to the cloud - Real Python](https://realpython.com/blog/python/dockerizing-flask-with-compose-and-machine-from-localhost-to-the-cloud/) [realpython/orchestrating-docker](https://github.com/realpython/orchestrating-docker)  

[Docker Compose Tutorial: Orchestrate Containers for Development | Codeship | via @codeship](https://blog.codeship.com/orchestrate-containers-for-development-with-docker-compose/)  
[Orchestrate Containers for Development with Docker Compose | via @codeship](https://blog.codeship.com/orchestrate-containers-for-development-with-docker-compose/)  
[A Docker Container Pattern - Compose Configuration - Levvel](http://blog.levvel.io/blog-post/a-docker-container-pattern-compose-configuration/)  
[Beyond Docker Compose](http://blog.xebialabs.com/2016/04/11/beyond-docker-compose/)  
[Easy deploy a nodejs app to prod and staging with docker](https://medium.com/@theotow/easy-deploy-a-nodejs-app-to-prod-and-staging-with-docker-f7e6ff406b69) cascading Compose files  

[Docker Compose UI by Francesco Uliana](http://francescou.github.io/docker-compose-ui/)

### Examples

[bitnami-docker/subrion.md at master · bitnami/bitnami-docker](https://github.com/bitnami/bitnami-docker/blob/master/tutorials/subrion.md)
[bitnami-docker/redmine.md at master · bitnami/bitnami-docker](https://github.com/bitnami/bitnami-docker/blob/master/tutorials/redmine.md)
https://raw.githubusercontent.com/sameersbn/docker-redmine/master/docker-compose.yml
https://raw.githubusercontent.com/sameersbn/docker-gitlab/master/docker-compose.yml

## Docker Swarm (standalone)

Docker Swarm is native clustering for Docker Engines. Exposes Docker Remote API to be utilized by standard Docker tools and other tools. Swarm comes with a default scheduler, but it can be replaced by others (e.g. Aurora, Kubernetes).

Swarm, unlike Kubernetes, is not declarative.

Docker [acquired](https://blog.docker.com/2016/03/docker-welcomes-aurora-project-creators/) [Conductant](http://www.infoworld.com/article/3040743/application-virtualization/docker-snaps-up-apache-aurora-devs-for-swarm-team.html) (founded by the creators of Aurora) in March 2016. We're probably going to see Aurora features in Swarm.

> see `#docker-swarm-mode`

[Docker Swarm | Docker](http://www.docker.com/products/docker-swarm)
[Swarm Overview](https://docs.docker.com/swarm/overview/)

[Docker Tutorial 11 - Docker Swarm - YouTube](https://www.youtube.com/watch?v=zTKGfPfhg78) with hosted discovery
[Libswarm (in a nutshell) · Container42](http://www.container42.com/2014/07/03/libswarm/)
[Have Docker, Will Swarm — On Docker — Medium](https://medium.com/on-docker/have-docker-will-swarm-eafae7b58461) setup Swarm in a SINGLE machine

[#SwarmWeek: It’s a Wrap – Thanks Y’all! | Docker Blog](https://blog.docker.com/2016/03/swarm-week-roundup-docker-swarm/)
[#SwarmWeek – Video Tutorials to Join Your First Docker Swarm Cluster | Docker Blog](https://blog.docker.com/2016/03/swarmweek-join-your-first-swarm/)
[Docker Swarm - YouTube](https://www.youtube.com/playlist?list=PLkA60AVN3hh8lmRdhPKzsNJvZxJ8dpj4t)
[ScaleSwarm: Auto-scaling a swarm cluster - YouTube](https://www.youtube.com/watch?v=fE0qVTGC6MA)
[Sentient Clusters: Micro-services, Atlassian products, and the Docker Swarm - Nicola Paolucci - YouTube](https://www.youtube.com/watch?v=Pmh5m9eczsE) 30 minutes walk-through

[Docker Machine, Compose & Swarm Tutorials | Codeship | via @codeship](https://blog.codeship.com/docker-machine-compose-and-swarm-how-they-work-together/)
[Running Services within a Docker Swarm - via @codeship | via @codeship](https://blog.codeship.com/running-services-within-docker-swarm/) !important
[linux - how to create docker overlay network between multi hosts? - Stack Overflow](http://stackoverflow.com/questions/34365604/how-to-create-docker-overlay-network-between-multi-hosts/34434948#34434948)
[Levvel Blog - Running a Distributed Docker Swarm on AWS](http://www.levvel.io/blog-post/running-distributed-docker-swarm-on-aws/)
[NGINX as a Reverse Proxy for Docker Swarm Clusters | via @codeship](https://blog.codeship.com/nginx-reverse-proxy-docker-swarm-clusters/)
[Review: Docker Swarm soars, and the sky's the limit | InfoWorld](http://www.infoworld.com/article/2913636/linux/first-look-docker-clustering-with-docker-swarm.html)
[Deploying Containers with Docker Swarm and Docker Networking | Technology Conversations](http://technologyconversations.com/2015/11/25/deploying-containers-with-docker-swarm-and-docker-networking/) [code](https://github.com/vfarcic/docker-swarm-networking)
[Docker Austin: How Do I Even Swarm? | Carina by Rackspace](https://getcarina.com/blog/docker-austin-how-do-i-even-swarm/)
[Distributed Data Analysis with Docker Swarm | via @codeship](https://blog.codeship.com/distributed-data-analysis-with-docker-swarm/) naive map-reduce with Docker Swarm
[Evaluating Container Platforms at Scale — On Docker — Medium](https://medium.com/on-docker/evaluating-container-platforms-at-scale-5e7b44d93f2c)
[Docker Swarm: Flat File Engine Discovery — On Docker — Medium](https://medium.com/on-docker/docker-swarm-flat-file-engine-discovery-2b23516c71d4)
[Rescheduling containers on node failures with Docker Swarm 1.1 - Container Solutions](http://container-solutions.com/rescheduling-containers-on-node-failures-with-docker-swarm-1-1/)
[Couchbase Cluster on Docker Swarm using Docker Compose and Docker Machine](http://blog.couchbase.com/2016/may/couchbase-cluster-docker-swarm-compose-machine)
[Deploy Docker Swarm cluster on one host | Nan Xiao's Blog](http://nanxiao.me/en/deploy-docker-swarm-cluster-on-one-host/)

[Docker Swarm Exceeds Kubernetes Performance at Scale | Docker Blog](https://blog.docker.com/2016/03/swarmweek-docker-swarm-exceeds-kubernetes-scale/)
[Docker Swarm beats Kubernetes? Not so fast | InfoWorld](http://www.infoworld.com/article/3042573/application-virtualization/docker-swarm-beats-kubernetes-not-so-fast.html)

### Scaling To Infinity with Docker Swarm, Docker Compose and Consul

[Scaling To Infinity: The Quest For Fully Automated, Scalable, Self-Healing System With Zero-Downtime](http://vfarcic.github.io/scaling/#/cover)

[Scaling To Infinity with Docker Swarm, Docker Compose and Consul (Part 1/4) – A Taste of What Is To Come | Technology Conversations](http://technologyconversations.com/2015/07/02/scaling-to-infinity-with-docker-swarm-docker-compose-and-consul-part-14-a-taste-of-what-is-to-come/)
[Scaling To Infinity with Docker Swarm, Docker Compose and Consul (Part 2/4) – Manually Deploying Services | Technology Conversations](http://technologyconversations.com/2015/07/02/scaling-to-infinity-with-docker-swarm-docker-compose-and-consul-part-24-manually-deploying-services/)
[Scaling To Infinity with Docker Swarm, Docker Compose and Consul (Part 3/4) – Blue-Green Deployment, Automation and Self-Healing Procedure | Technology Conversations](http://technologyconversations.com/2015/07/02/scaling-to-infinity-with-docker-swarm-docker-compose-and-consul-part-34-blue-green-deployment-automation-and-self-healing-procedure/)
[Scaling To Infinity with Docker Swarm, Docker Compose and Consul (Part 4/4) – Scaling Individual Services | Technology Conversations](http://technologyconversations.com/2015/07/02/scaling-to-infinity-with-docker-swarm-docker-compose-and-consul-part-44-scaling-individual-services/)

[vfarcic/docker-swarm](https://github.com/vfarcic/docker-swarm)

## Docker Swarm mode

Docker 1.12 (June 2016) included *Swarm mode* (via SwarmKit) for Swarm capability without Docker Swarm standalone.
[Docker 1.12: Now with Built-in Orchestration! | Docker Blog](https://blog.docker.com/2016/06/docker-1-12-built-in-orchestration/)
[DockerCon 2016: What's New in Docker - Docker 1.12 | via @codeship](https://blog.codeship.com/whats-new-docker/)
[Comparing Swarm, Swarmkit and Swarm Mode | Sreenivas Makam's Blog](https://sreeninet.wordpress.com/2016/07/14/comparing-swarm-swarmkit-and-swarm-mode/)
[swarm/README.md at master · docker/swarm](https://github.com/docker/swarm/blob/master/README.md#swarm-disambiguation)
[Docker tutorial: Get started with Docker swarm mode | InfoWorld](https://www.infoworld.com/article/3259872/containers/docker-tutorial-get-started-with-docker-swarm-mode.html)
[Container Orchestration with Docker and Swarm](http://container.training/swarm-selfpaced.yml.html)

[Overview - User Guide| Alibaba Cloud Documentation Center](https://www.alibabacloud.com/help/doc-detail/52580.htm) Docker Swarm standalone vs Swarm mode
[Docker Swarm vs Swarm Mode | Neil Cresswell | Pulse | LinkedIn](https://www.linkedin.com/pulse/docker-swarm-vs-mode-neil-cresswell/)

[It's 2018, Is Swarm Dead? Answered by a Docker Captain.](https://www.bretfisher.com/is-swarm-dead-answered-by-a-docker-captain/) TL;DR: NO
[Future of Docker Swarm in 2018 on Built-in Container Orchestration](https://www.bretfisher.com/the-future-of-docker-swarm/)
[Docker Swarm Firewall Ports](https://www.bretfisher.com/docker-swarm-firewall-ports/)

[Swarm mode overview](https://docs.docker.com/engine/swarm/)
[Getting started with swarm mode | Docker Documentation](https://docs.docker.com/engine/swarm/swarm-tutorial/)
[Setting up a Docker Swarm cluster using Docker in Docker | Callista Enterprise](http://callistaenterprise.se/blogg/teknik/2017/12/18/docker-in-swarm-mode-on-docker-in-docker/)
[Docker Swarm Mode - YouTube](https://www.youtube.com/playlist?list=PLkA60AVN3hh-jd4zGpRWHG8LIQUpBXBsM)

[Swarm mode key concepts | Docker Documentation](https://docs.docker.com/engine/swarm/key-concepts/)
Task: A Docker container and the commands to run inside the container. It is the atomic scheduling unit of swarm.  
Service: definition of the tasks to execute on the worker nodes.  
Stack: a collection of services that make up an application in a specific environment.  

[How nodes work | Docker Documentation](https://docs.docker.com/engine/swarm/how-swarm-mode-works/nodes/)
[How services work | Docker Documentation](https://docs.docker.com/engine/swarm/how-swarm-mode-works/services/)

[Docker Operations - Docker Training](https://training.docker.com/docker-operations)
[Getting Started With Swarm Mode | Docker Orchestration | Katacoda](https://www.katacoda.com/courses/docker-orchestration/getting-started-with-swarm-mode)
[Learn Docker in Production using Interactive Browser-Based Labs | Katacoda](https://www.katacoda.com/courses/docker-production)
[Learn Docker Security using Interactive Browser-Based Labs | Katacoda](https://www.katacoda.com/courses/docker-security)

[docker/swarmkit: A toolkit for orchestrating distributed systems at any scale. It includes primitives for node discovery, raft-based consensus, task scheduling and more.](https://github.com/docker/swarmkit)

[swarmzilla/swarm3k: SwarmZilla 3000 Collaborative Project](https://github.com/swarmzilla/swarm3k)
[Docker Swarm Lessons from Swarm3K](https://sematext.com/blog/docker-swarm-lessons-from-swarm3k/)
[Taming SwarmZilla: 150k Containers in 3K+ Docker Swarm Nodes](https://sematext.com/blog/docker-swarm-swarm3k/)

[swarm - alex ellis' blog](https://blog.alexellis.io/tag/swarm/)
[Top 5 of Docker Swarm](https://blog.alexellis.io/top-5-docker-swarm/)

[Running 1,000 Containers in Docker Swarm - via @codeship | via @codeship](https://blog.codeship.com/running-1000-containers-in-docker-swarm/) !important, kernel tuning
[Introduction to Docker Swarm Orchestration - UpCloud](https://www.upcloud.com/support/docker-swarm-orchestration/)
[Massively Scalable with Docker SwarmKit — Medium](https://medium.com/@chanwit/massively-scalable-with-docker-swarmkit-879541caff86)
[Trying the new docker 1.12 swarm mode locally using machine – Mantika – Bringing latest research in Machine Learning to industry](http://blog.mantika.io/docker-1.12-swarm/)
[All Hail the New Docker Swarm - Container Solutions](http://container-solutions.com/hail-new-docker-swarm/)
[Docker Swarm Is Dead. Long Live Docker Swarm.](https://www.infoq.com/news/2016/06/dockercon-docker-swarm)
[Running Services within a Docker Swarm - via @codeship | via @codeship](https://blog.codeship.com/running-services-within-docker-swarm/)

[One-shot containers with Docker Swarm](https://blog.alexellis.io/containers-on-swarm/)

```sh
docker service create --restart-policy=none --name crawler1 -e url=http://blog.alexellis.io -d crawl_site alexellis2/href-counter
```

### Limitation

The number of connections to ingress loadbalancer (using kernel's IPVS) is bound by the number of available ports per source IP. So high concurrency access will result in connections waiting.

[IPVS Software - Advanced Layer-4 Switching](http://www.linuxvirtualserver.org/software/ipvs.html)
[IPVS - LVSKB](http://kb.linuxvirtualserver.org/wiki/IPVS)

[[SWARM] Very poor performance for ingress network with lots of parallel requests · Issue #35082 · moby/moby](https://github.com/moby/moby/issues/35082)
[Pauses/delays with overlay network on swarm · Issue #31746 · moby/moby](https://github.com/moby/moby/issues/31746)

### attachable network

[Docker Stacks and Attachable networks](https://blog.alexellis.io/docker-stacks-attachable-networks/)

```sh
docker network create --driver=overlay --attachable attachable-overlay
docker service create --publish 80:80 --network=attachable-overlay --name nginx nginx
docker run --network=attachable-overlay -ti alpine:latest sh
```

When using with `stack deploy`, define the network as external.

```yaml
networks:
  attachable-overlay:
    external: true
```

### swarm network

[How Docker Swarm Container Networking Works - Under the Hood](https://neuvector.com/network-security/docker-swarm-container-networking/)

[Service Discovery and Load balancing Internals in Docker 1.12 – Sreenivas Makam's Blog](https://sreeninet.wordpress.com/2016/07/29/service-discovery-and-load-balancing-internals-in-docker-1-12/amp/) DNS strategy explained with Docker Swarm
[Use swarm mode routing mesh | Docker Documentation](https://docs.docker.com/engine/swarm/ingress/)
[Solving the routing mess for services using Docker – Luis Herrera Benítez – Medium](https://medium.com/@lherrera/solving-the-routing-mess-for-services-in-docker-73492c37b335)
[Load Balancing Docker Swarm Mode - UpCloud](https://www.upcloud.com/support/load-balancing-docker-swarm-mode/)
[Docker 1.12 swarm mode - round robin inside and out](http://blog.scottlogic.com/2016/08/30/docker-1-12-swarm-mode-round-robin.html)

Ingress for Swarm
[Home - Docker Flow Proxy](https://proxy.dockerflow.com/)

### `docker service`

[docker service | Docker Documentation](https://docs.docker.com/engine/reference/commandline/service/#usage)
[docker service create | Docker Documentation](https://docs.docker.com/engine/reference/commandline/service_create/)
[docker service update | Docker Documentation](https://docs.docker.com/engine/reference/commandline/service_update/#options)

A service is defined by an image plus its scheduling options. It is only applicable in Swarm mode.
The containers will be automatically prefixed with the service name.
`service ps` list the containers and nodes they are running on.
[Deploy services to a swarm | Docker Documentation](https://docs.docker.com/engine/swarm/services/)
[docker service create | Docker Documentation](https://docs.docker.com/engine/reference/commandline/service_create/#add-bind-mounts-volumes-or-memory-filesystems)

`--mount` option for `docker service`
[Give a service access to volumes or bind mounts | Docker Documentation](https://docs.docker.com/engine/swarm/services/#give-a-service-access-to-volumes-or-bind-mounts)
[Add bind-mounts or volumes | Docker Documentation](https://docs.docker.com/engine/reference/commandline/service_create/#add-bind-mounts-or-volumes)

|       Key       |                              Value                              |
|:---------------:|:---------------------------------------------------------------:|
| `type`          | `mount` (default), `bind`, `tmpfs`                              |
| `src`           | host path if `type`== `mount`; volume name if `type`== `volume` |
| `dst`/`target`  | container path                                                  |
| `volume-driver` | `local` (default), `flocker`, `glusterfs`, `ceph`               |
| `volume-label`  | volume label                                                    |
| `volume-opt`    | volume option                                                   |

`--mount` can specify driver and create volume, `--volume` (of `docker run`) can only bind existing volume

[Create services using templates | Docker Documentation](https://docs.docker.com/engine/reference/commandline/service_create/#create-services-using-templates) some values can be set with variables templates

Default host name is container id.
Container name is `{{.Service.Name}}.{{.Task.Slot}}.{{.Task.ID}}`

### `docker stack`

[docker stack | Docker Documentation](https://docs.docker.com/engine/reference/commandline/stack/)
[Get Started, Part 5: Stacks | Docker Documentation](https://docs.docker.com/get-started/part5/#persist-the-data)
[Deploy a stack to a swarm | Docker Documentation](https://docs.docker.com/engine/swarm/stack-deploy/)

A stack is a collection of services defined in Compose Version 3. It is only applicable in Swarm mode. A stack gets its own overlay network (as in `docker-compose`).
The services, containers and network will be automatically prefixed with the stack name.

> The docker stack deploy command is effectively the equivalent of Docker Compose (a Python app) re-written in Golang.

[play-with-docker/stacks: Docker stacks samples](https://github.com/play-with-docker/stacks)

[Docker and Swarm Mode – Part 1 | Gabriel Schenker's Blog](https://lostechies.com/gabrielschenker/2016/09/05/docker-and-swarm-mode-part-1/)
[Docker and Swarm Mode – Part 2 | Gabriel Schenker's Blog](https://lostechies.com/gabrielschenker/2016/09/11/docker-and-swarm-mode-part-2/)

[Docker Compose from development to production – Basilio Vera – Medium](https://medium.com/@basi/docker-compose-from-development-to-production-88000124a57c)
[Deploy Docker Compose (v3) to Swarm (mode) Cluster - Codefresh](https://codefresh.io/blog/deploy-docker-compose-v3-swarm-mode-cluster/)
[Deploy Swarm Services with the new docker `stack` and a compose file!](http://jmkhael.io/deploy-swarm-services-with-the-new-docker-stack-and-a-compose-file-2/)

### secrets/config

[Manage sensitive data with Docker secrets | Docker Documentation](https://docs.docker.com/engine/swarm/secrets/)
[Use Secrets in Compose](https://docs.docker.com/engine/swarm/secrets/#use-secrets-in-compose)
[Compose file version 3 reference - secrets | Docker Documentation](https://docs.docker.com/compose/compose-file/#secrets)

[Store configuration data using Docker Configs | Docker Documentation](https://docs.docker.com/engine/swarm/configs/#about-configs)
[Compose file version 3 reference - configs | Docker Documentation](https://docs.docker.com/compose/compose-file/#configs)

[The Definitive Cheatsheet for Docker Secrets](https://firepress.org/blog/the-definitive-cheatsheet-for-docker-secrets/)

### vs Kubernetes

[Docker Inevitably Embraces Kubernetes Container Orchestration](https://www.nextplatform.com/2018/04/17/docker-inevitably-embraces-kubernetes-container-orchestration/)
[Docker Clustering Tools Compared: Kubernetes vs Docker Swarm | Technology Conversations](https://technologyconversations.com/2015/11/04/docker-clustering-tools-compared-kubernetes-vs-docker-swarm/)

### CLI

* [swarm init](https://docs.docker.com/engine/reference/commandline/swarm_init/)
* [swarm join](https://docs.docker.com/engine/reference/commandline/swarm_join/)
* [service create](https://docs.docker.com/engine/reference/commandline/service_create/)
* [service inspect](https://docs.docker.com/engine/reference/commandline/service_inspect/)
* [service ls](https://docs.docker.com/engine/reference/commandline/service_ls/)
* [service rm](https://docs.docker.com/engine/reference/commandline/service_rm/)
* [service scale](https://docs.docker.com/engine/reference/commandline/service_scale/)
* [service ps](https://docs.docker.com/engine/reference/commandline/service_ps/)
* [service update](https://docs.docker.com/engine/reference/commandline/service_update/)

#### Logging into container of a stack

```sh
# get unique container token
CONTAINER_TOKEN=$(docker service ps  -f 'name=STACK_SERVICE.1' STACK_SERVICE -f desired-state=running -q --no-trunc )
docker exec -ti STACK_SERVICE.1.${CONTAINER_TOKEN} bash
```

Script for distributed use case with `docker-machine` (from [this post](https://stackoverflow.com/a/42955871/665507)):

```sh
#! /bin/bash

set -e

exec_task=$1
exec_instance=$2

strindex() {
  x="${1%%$2*}"
  [[ "$x" = "$1" ]] && echo -1 || echo "${#x}"
}

parse_node() {
  read title
  id_start=0
  name_start=`strindex "$title" NAME`
  image_start=`strindex "$title" IMAGE`
  node_start=`strindex "$title" NODE`
  dstate_start=`strindex "$title" DESIRED`
  id_length=name_start
  name_length=`expr $image_start - $name_start`
  node_length=`expr $dstate_start - $node_start`

  read line
  id=${line:$id_start:$id_length}
  name=${line:$name_start:$name_length}
  name=$(echo $name)
  node=${line:$node_start:$node_length}
  echo $name.$id
  echo $node
}

if true; then
   read fn
   docker_fullname=$fn
   read nn
   docker_node=$nn
fi < <( docker service ps -f name=$exec_task.$exec_instance --no-trunc -f desired-state=running $exec_task | parse_node )

echo "Executing in $docker_node $docker_fullname"

eval `docker-machine env $docker_node`

docker exec -ti $docker_fullname /bin/bash
```

## Docker Machine

You can use Docker Machine to:
- Provision and manage [supported infrastructures](https://docs.docker.com/machine/drivers/)
- Provision Swarm clusters

[Machine Overview](https://docs.docker.com/machine/overview/)
[Machine concepts and help](https://docs.docker.com/machine/concepts/)

Configs (usually certs) are stored in `.docker/machine`.
Do note that `generic` driver will change the hostname and [(re)install docker](https://github.com/docker/machine/issues/1357) on the host to Docker service will be restarted/

[Java Magazine, January/February 2016, (72)](http://www.javamagazine.mozaicreader.com/JanFeb2016#&pageSet=72&page=0&contentItem=0)

[Docker Swarm and Docker Compose with Ben Firshman, Product Manager at Docker, Inc. - YouTube](https://www.youtube.com/watch?v=Ad3g7rjwAyo?t=575) (little bit out-dated)

### Provision

[docker-machine create | Docker Documentation](https://docs.docker.com/machine/reference/create/)
[Machine drivers | Docker Documentation](https://docs.docker.com/machine/drivers/)

Use `--engine-install-url` with [Rancher's install script](http://rancher.com/docs/rancher/latest/en/hosts/#supported-docker-versions) to install a particular version of Docker on the nodes.

```sh
--engine-install-url=https://get.docker.com/
--engine-install-url=https://test.docker.com/
--engine-install-url=https://releases.rancher.com/install-docker/1.13.sh
--engine-install-url=https://releases.rancher.com/install-docker/17.05.sh
```

### Operation

```sh
# assuming a node `node1` is provisioned
docker-machine ls

# set and under Docker environment
eval $(docker-machine env node1)
eval $(docker-machine env -u)

docker-machine ssh node1
docker-machine inspect node1 -f {{ .Driver.IPAddress }} # `node_ip`
docker run -d -p 8000:80 --name webserver nginx:alpine
# visit http://<node_ip>:8080
docker rm -f $(docker ps -ql)

docker-machine stop node1
docker-machine rm node1
```

[Experimenting with Native Docker tooling · Container42](http://www.container42.com/2015/09/15/experimenting-with-native-docker-tooling/) deploy on Digital Ocean

#### AWS

[Amazon Web Services (AWS) EC2 example | Docker Documentation](https://docs.docker.com/machine/examples/aws/)

Create IAM account and generate access key pair.
Save to `~/.aws/credentials`:
```
[default]
aws_access_key_id = AKID1234567890
aws_secret_access_key = MY-SECRET-KEY
```

```sh
docker-machine create --driver amazonec2 --amazonec2-region us-west-2 node1
# us-west-1a is sometime full, cannot allocate subnet
```

[Amazon Web Services | Docker Documentation](https://docs.docker.com/machine/drivers/aws/#options)

#### Digital Ocean

[Digital Ocean example | Docker Documentation](https://docs.docker.com/machine/examples/ocean/#step-2-generate-a-personal-access-token)

Create API token
```sh
docker-machine create --driver digitalocean --digitalocean-access-token xxxxx node1
```

[Digital Ocean | Docker Documentation](https://docs.docker.com/machine/drivers/digital-ocean/#options)
