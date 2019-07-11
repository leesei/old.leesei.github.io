---
title: Mesos
categories:
  - web
tags:
  - web-deploy
toc: true
date: 2016-03-21 18:48:23
---

# Mesos

[Apache Mesos](http://mesos.apache.org/) [Github](https://github.com/mesos)
[Apache Mesos - Wikiwand](http://www.wikiwand.com/en/Apache_Mesos)

Apache Mesos is inspired by the Google's paper of their Borg system. It abstracts CPU, memory, storage, and other compute resources away from machines (physical or virtual), enabling fault-tolerant and elastic distributed systems to easily be built and run effectively. Twitter have been using it since 2007.
Mesos provides the low level API. It usually requires a "framework" (scheduler) to tell it what to do and on which node to execute the task.

It uses Zookeeper underneath for leader election. Non-responsive node will be removed, replace by new node; if the old node response later on the response will be disposed and it will be killed to prevent duplication.

Mesos is best run on bare metal or on VM.

[A tale of two clusters: Mesos and YARN - O'Reilly Media](https://www.oreilly.com/ideas/a-tale-of-two-clusters-mesos-and-yarn)

> Mesos is low-level infrastructure; it needs frameworks like Aurora to give it something to do. As David Messina, VP of marketing for Docker, put it in an email, "Aurora is intended for humans to interact with and perform high-level tasks like 'run 100 instances of my service', while Mesos is a toolkit that programmers interact with to build other systems."

<!-- more -->

## Video

[Building Distributed Frameworks on Mesos - YouTube](https://www.youtube.com/watch?v=n5GT7OFSh58)
[How Airbnb Simplifies with Mesos - YouTube](https://www.youtube.com/watch?v=GfpGmhZwaoM)
[Running Mesos at Atlassian - YouTube](https://www.youtube.com/watch?v=Itufcu8Z-Bc)
[Simplifying with Mesos and Marathon - YouTube](https://www.youtube.com/watch?v=OgVaQPYEsVo)
[Operating Apache Aurora and Mesos at Twitter - YouTube](https://www.youtube.com/watch?v=E4lxX6epM_U)
[Run Any App on Mesos on Any Infrastructure Using Docker - YouTube](https://www.youtube.com/watch?v=u5jd9YT9EsY)
[Running YARN Alongside Mesos - YouTube](https://www.youtube.com/watch?v=d7vZWm_xS9c)

## Mini-Mesos

[minimesos.org - Testing infrastructure for Mesos frameworks](https://minimesos.org/)
[Mini-Mesos: What’s a Nice XPer Doing in a Company Like This? - The New Stack](http://thenewstack.io/mini-mesos/)

## Mesosphere

[Introducing The Mesosphere Datacenter Operating System](https://mesosphere.com/) [Github](https://github.com/mesosphere)
[Blog - Mesosphere](https://mesosphere.com/blog/)

[Mesosphere OS manages entire data centers with one click | InfoWorld](http://www.infoworld.com/article/2933324/data-center/mesosphere-os-manages-entire-data-centers-with-one-click.html)
[Taking Mesos to the next level with DC/OS](https://mesosphere.com/blog/2016/04/19/hindman-mesos-dcos/)

## Marathon

[Marathon: A cluster-wide init and control system for services in cgroups or Docker containers](https://mesosphere.github.io/marathon/)
[mesosphere/marathon: Deploy and manage containers (including Docker) on top of Apache Mesos at scale.](https://github.com/mesosphere/marathon)
Marathon is used for long running services.

[Mesosphere Marathon for production container environments](https://mesosphere.com/blog/2016/02/17/marathon-production-ready-containers/)

## Chronos

[Chronos: Fault tolerant job scheduler for Mesos](http://mesos.github.io/chronos/)
[mesos/chronos: Fault tolerant job scheduler for Mesos which handles dependencies and ISO8601 based schedules](https://github.com/mesos/chronos)
Chronos is used to execute services at particular time, like cron, for batch processing.

## Aurora

[Apache Aurora](http://aurora.apache.org/) [Github](https://github.com/apache/aurora)
Aurora is a Mesos framework for long-running services and batch jobs. It is build by Twitter and the creator Bill Farner joined Docker Inc.

[Introduction to Apache Aurora - YouTube](https://www.youtube.com/watch?v=asd_h6VzaJc)
[mesos - Marathon vs Aurora and their purposes - Stack Overflow](http://stackoverflow.com/questions/28651922/marathon-vs-aurora-and-their-purposes)

