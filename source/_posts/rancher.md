---
title: "Rancher"
date: 2014-12-11 18:38:50
categories:
  - container
tags:
  - shell-tool
  - docker
  - devops
  - rancher
  - web-deploy
---

# Rancher

[Your Enterprise Kubernetes Platform | Rancher Labs](https://rancher.com/)
[Rancher | 全栈化容器管理平台](http://www.cnrancher.com/)
[What-is-rancher | Rancher Labs](https://rancher.com/what-is-rancher/)
[Rancher](https://github.com/rancher/) GitHub org

Rancher 2 rebased on Kubernetes and become [GA on 2018-05](https://forums.rancher.com/t/rancher-release-v2-0-0/10239).
[FAQ | Rancher Labs](https://rancher.com/docs/rancher/v2.x/en/faq/)

- dropped Rancher Compose
- dropped Cattle
- dropped environments (replaced with k8s cluster)
  [2.0 Docs | Rancher Labs](https://rancher.com/docs/rancher/v2.x/en/)

[rancher/rancher: Platform for operating Docker in production](https://github.com/rancher/rancher)
[jmreicha/awesome-rancher: Curated list of Rancher resources](https://github.com/jmreicha/awesome-rancher)

[Painless Container Management with Rancher 2.0, Kubernetes, and IBM Cloud](https://medium.com/ibm-watson-data-lab/painless-container-management-with-rancher-2-0-kubernetes-and-ibm-cloud-5a14ac2d4ccc)

1.6 Specific:
[Understanding Cattle, Swarm and Kubernetes in Rancher | Rancher Labs](http://rancher.com/cattle-swarm-kubernetes-side-side/)
[Kubernetes, Mesos, and Swarm: Comparing the Rancher Orchestration Engine Options | Rancher Labs](http://rancher.com/comparing-rancher-orchestration-engine-options/)
[Comparing Kubernetes and Docker Swarm | Rancher Labs](https://rancher.com/comparing-kubernetes-and-docker-swarm/)

## Installation

[Quick Start Guide | Rancher Labs](https://rancher.com/docs/rancher/v2.x/en/quick-start-guide/)

[joshuacox/ansibleplaybook-rancher: Ansible playbook to keep a Rancher container running on a docker host](https://github.com/joshuacox/ansibleplaybook-rancher)

## Resources

[A Primer on the Kubernetes Landscape | Rancher Labs](http://rancher.com/primer-kubernetes-landscape/)
[Container Ecosystem Trends You Need to Know | Rancher Labs](http://rancher.com/container-ecosystem-trends-need-know/)

[Focus on Services, Not on Containers | Rancher Labs](http://rancher.com/focus-services-not-containers/)
[Using Containers for a More Cost-Effective Cloud | Rancher Labs](http://rancher.com/using-containers-cost-effective-cloud/)
[Do Microservices Make SOA Irrelevant? | Rancher Labs](http://rancher.com/microservices-make-soa-irrelevant/)
[Running Serverless Applications on Rancher | Rancher Labs](http://rancher.com/running-serverless-applications-rancher/)

[Understanding Authentication & Authorization in Rancher 2.0 | Rancher Labs](https://rancher.com/blog/2018/2018-05-04-authentication-authorization-rancher2/)

2016:  
[Getting Microservices Deployments on Kubernetes with Rancher | Rancher Labs](http://rancher.com/getting-micro-services-production-kubernetes/)
[Creating Microservices Deployments on Kubernetes with Rancher - Part 2 | Rancher Labs](https://rancher.com/creating-microservices-deployments-on-kubernetes-with-rancher-part-2/)

### Storage

[Block Storage, Object Storage, and File Systems: What They Mean for Containers | Rancher Labs](http://rancher.com/block-object-file-storage-containers/)
[Rancher Introduces Persistent Storage for Docker | Rancher Labs](http://rancher.com/how-rancher-storage-services-unleash-the-power-of-software-defined-storage/) !important

### Monitoring

[Containers and Real-Time Resource Monitoring | Rancher Labs](http://rancher.com/containers-real-time-resource-monitoring/)

### Service

[How to Run GitLab in Rancher](http://rancher.com/how-to-run-gitlab-in-rancher-1/)
[How to Run GitLab in Rancher - Part 2 | Rancher Labs](http://rancher.com/run-gitlab-rancher-2/)

### Catalog

> obsolete in 2.0? Use Helm instead?

[Rancher Catalog](https://rancher.com/docs/rancher/v1.6/en/catalog/)
[rancher/rancher-catalog](https://github.com/rancher/rancher-catalog/)
[rancher/community-catalog: Catalog entries contributed by the community](https://github.com/rancher/community-catalog)
[rancher/catalog-dockerfiles: Dockerfiles for Rancher Catalog containers](https://github.com/rancher/catalog-dockerfiles)

[Rancher catalog, GlusterFS, how to choose where bricks get created? - Convoy - Rancher Forums](https://forums.rancher.com/t/rancher-catalog-glusterfs-how-to-choose-where-bricks-get-created/2103) parameterize variables

### Video

[Rancher and Kubernetes Training - YouTube](https://www.youtube.com/playlist?list=PLfAoTEAPazb4fQQwOxY3uXsO_UBK3fEPG)
[Intro to Kubernetes on Rancher 2.0 | Rancher Labs](https://rancher.com/events/training/2018-training-25/)

[Online Meetups and Webinars - YouTube](https://www.youtube.com/playlist?list=PLfAoTEAPazb5Q1eQcbdHqW4eJcDDdn9RF)
Storage, Volume, Network, Load Balancing, HA, Monitor, Logging, DaaS

[2017 Training: Docker containers and Rancher - YouTube](https://www.youtube.com/watch?v=8K14A_CZFdI) !important

[Demo: launching and using Kubernetes within Rancher - YouTube](https://www.youtube.com/watch?v=kbsbZHCNfrg)
[2017 Online Training: Using Kubernetes - YouTube](https://www.youtube.com/watch?v=YRmUu2YXj7w)

## k3s/k3OS

[k3s - Lightweight Kubernetes | k3s](https://k3s.io/)
[rancher/k3s: Lightweight Kubernetes. 5 less than k8s.](https://github.com/rancher/k3s)

[The First Kubernetes OS | k3OS | k3os](https://www.k3os.io/)
[Announcing k3OS: A Kubernetes Operating System](https://rancher.com/blog/2019/announcing-k3os-kubernetes-operating-system/)

[May 2019 Online Meetup: Introducing k3OS - YouTube](https://www.youtube.com/watch?v=cmKCYfvRGL8) [slide](https://info.rancher.com/e2t/c/*W2v_-9D5BGqnvW48QkRS3S-F8t0/*W7ch8pC5WQ3YjW6nH9S147GPX10/5/f18dQhb0S1V22RwkM_LZMS_CQS34W1H8tCW1cTS9DW5k02jz4M2vQ0W30Fmlf7Q3SF1W1_Mg4R3Gf54jW88Z7Jk6FXpgyW2FXCYD2dxt5SW8Y783w8XQgDjW2sQCNy8CsG0SMW7QV1Lf3W8W8HLjvz95L5mmW6w-b5h6xH3_4V9HfcS2F6_t1W6R4SpS3VZKVMVk3CM06ttx10N5f-0BVCzyqcW7X9S0R7gzpRnW1Xfd9m6dcK3nW8sP7jJ6dcmqrN6Tb5T61zcdRW7RWsy77Rq5HSW8J9BFD4DZh-JW6mJxcH38Z-wnVW55F82hcfGQW53qxHH2ZcGwFN5DMnQ28h7PXW68h8LJ1RM_v3W47c0rT1nrgTkVt6w863P7BBCW6060td5LyC-XW6j2SsX2l2KH4Mx1d99gzVwxW6p7t8z1zP5wcW1168qL63kd9lVTDHNJ8Qd6f2W4kXG1-16CmklW2FNv068KF_D_W1Hgcw921hWmSW9bwH_r11tstYW8PZC5S54MVTFW79r1br69rjR6W3sXQN_4VyfJXV_JYkX3XTrFnVdPK1x7QB1_LW3SbzC271mSybW5GMXJz7-5PxHW8mPshD5641BDW2jPKp32W6nfDW97dJdj80rZRGW9l_bRc97vk0yW2sZlrH1pmPrxf5VHnxs04)

[rancher/k3d: Little helper to run Rancher Lab's k3s in Docker](https://github.com/rancher/k3d)
[k3d - A fast kubernetes dev environment](https://blog.zeerorg.site/post/k3d-kubernetes-dev-env)

[Setup a private registry on K3s – ITNEXT](https://itnext.io/setup-a-private-registry-on-k3s-f30404f8e4d3)

## Rio

[Rio - Containers At Their Best](https://rio.io/)
[Introducing Rio - Containers at Their Best](https://rancher.com/blog/2019/introducing-rio)
