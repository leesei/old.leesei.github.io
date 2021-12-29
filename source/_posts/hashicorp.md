---
title: HashiCorp
categories:
  - web
tags:
  - devops
  - web-deploy
toc: true
date: 2016-03-19 15:14:33
---

# HashiCorp

[HashiCorp Products](https://www.hashicorp.com/#overview)
[HashiCorp Learn](https://learn.hashicorp.com/)

[Tao of HashiCorp | HashiCorp](https://www.hashicorp.com/tao-of-hashicorp/)
[The Tao of HashiCorp | HashiCorp](https://www.hashicorp.com/blog/the-tao-of-hashicorp/)

[#180: Otto, Vagrant, and Automation with Mitchell Hashimoto - The Changelog](https://changelog.com/180/)

## Vagrant

> see `vagrant.md`

## Packer

[Packer by HashiCorp](https://www.packer.io/)
Packer is a free and open source tool for creating golden images for multiple platforms from a single source configuration.

[Packer Curriculum - HashiCorp Learn](https://learn.hashicorp.com/packer)
[Documentation - Packer by HashiCorp](https://packer.io/docs/index.html)

[Docker? VMs? EC2? Yes! With Packer.io](http://www.kevinclarke.info/slides/c4l15/#/)

[Developing with Packer and Docker | Sam Thursfield's Blog](https://samthursfield.wordpress.com/2014/10/20/developing-with-packer-and-docker/)
[linux - Packer,Dockramp vs Dockerfile - Stack Overflow](http://stackoverflow.com/questions/31778106/packer-dockramp-vs-dockerfile)
[Packer Build - Create and Build Packer Templates and Images for AWS](https://www.middlewareinventory.com/blog/build-packer-aws-image-example/)
[Why Docker made me love Packer | Home](http://datafundamentals.com/content/why-docker-made-me-love-packer)
[Provision Infrastructure with Packer | Terraform - HashiCorp Learn](https://learn.hashicorp.com/tutorials/terraform/packer?in=terraform/provision)
[Docker and Packer playing nice: Part 1 | Home](http://datafundamentals.com/content/docker-and-packer-playing-nice-part-1)

## Serf

[Serf by HashiCorp](https://www.serfdom.io/)
Serf is a decentralized solution for cluster membership, failure detection, and orchestration. Lightweight and highly available.

[Internals - Serf by HashiCorp](https://www.serfdom.io/docs/internals/index.html)

## Consul

[Consul by HashiCorp](https://www.consul.io/)
Service discovery and configuration made easy. Distributed, highly available, and datacenter-aware. Built upon Serf.

Underlying health checks are AP
States (KV store and discovery) are CP

[Introduction - Consul by HashiCorp](https://www.consul.io/intro/)
[Consul Curriculum - HashiCorp Learn](https://learn.hashicorp.com/consul)
[Documentation - Consul by HashiCorp](https://www.consul.io/docs/index.html)

[Official Consul Docker Image - HashiCorp](https://www.hashicorp.com/blog/official-consul-docker-image.html)
[Why is service discovery important? (And what is Consul?) - O'Reilly Media](https://www.oreilly.com/learning/why-is-service-discovery-important-and-what-is-consul)

[Presentation: Service discovery in a microservice architecture | Smartjava.org](http://www.smartjava.org/content/presentation-service-discovery-microservice-architecture) [code](https://github.com/josdirksen/next-build-consul)
[Service Discovery with Docker and Consul: part 1 | Smartjava.org](http://www.smartjava.org/content/service-discovery-docker-and-consul-part-1)
[Service Discovery with Docker and Consul: part 2 | Smartjava.org](http://www.smartjava.org/content/service-discovery-docker-and-consul-part-2)
[GrassInWind2019/gRPCwithConsul: Use gRPC + Consul to do service discovery and RPC.](https://github.com/GrassInWind2019/gRPCwithConsul)

### Consul Template

[Introducing Consul Template - HashiCorp](https://www.hashicorp.com/blog/introducing-consul-template.html)
[hashicorp/consul-template: Generic template rendering and notifications with Consul](https://github.com/hashicorp/consul-template)

### Consul Connect

[Connect (Service Segmentation) - Consul by HashiCorp](https://www.consul.io/docs/connect/index.html)
[Connect Services - Service Mesh | Consul - HashiCorp Learn](https://learn.hashicorp.com/consul/getting-started/connect)

### Containers

Consul is often used to power load balancing of containers.

[Load-balancing Docker containers with Nginx and Consul-Template - Belly Card Engineering](https://tech.bellycard.com/blog/load-balancing-docker-containers-with-nginx-and-consul-template/)

[progrium/embassy: Easy, distributed discovery and routing mesh for Docker powered by Consul](https://github.com/progrium/embassy)

[gliderlabs/registrator: Service registry bridge for Docker with pluggable adapters](https://github.com/gliderlabs/registrator)

[Scalable Architecture DR CoN: Docker, Registrator, Consul, Consul Template and Nginx](http://www.maori.geek.nz/scalable_architecture_dr_con_docker_registrator_consul_nginx/)

[Where are my containers? Dockerized service discovery with Consul – Development the way it should be](https://jlordiales.me/2015/01/23/docker-consul/)
[Automatic container registration with Consul and Registrator – Development the way it should be](https://jlordiales.me/2015/02/03/registrator/)
[Consul Template for transparent load balancing of containers – Development the way it should be](https://jlordiales.me/2015/04/01/consul-template/)

## Terraform

[Terraform by HashiCorp](https://www.terraform.io/)
Build, Combine, and Launch Infrastructure
[Understand Terraform (infra-as-code) in 5 minutes - Je suis un dev](https://www.jesuisundev.com/en/understand-terraform-infra-as-code-in-5-minutes/)

[Terraform Curriculum - HashiCorp Learn](https://learn.hashicorp.com/terraform)
[Documentation - Terraform by HashiCorp](https://www.terraform.io/docs/index.html)

Declarative: define desired state, not steps

- only way to scale, computer can find more efficient strategy to reach the end state
  Output Plan before execution
  Provides scheduler, can use external one

[Manage AWS Infrastracture as Code with Terraform - M.Labouardy](http://www.blog.labouardy.com/manage-aws-infrastracture-as-code-with-terraform/)
[Manage AWS VPC as Infrastructure as Code with Terraform - M.Labouardy](http://www.blog.labouardy.com/manage-aws-vpc-as-infrastructure-as-code-with-terraform/)
[Setup Docker Swarm on AWS using Ansible & Terraform](https://hackernoon.com/setup-docker-swarm-on-aws-using-ansible-terraform-daa1eabbc27d)
[Why Terraform exceeds Chef, Puppet, Ansible, SaltStack, or CloudFormation - Level UpLevel Up](https://www.level-up.one/why-terraform-exceeds-chef-puppet-ansible-saltstack-or-cloudformation)
[Infrastructure as Code with Terraform » ADMIN Magazine](http://www.admin-magazine.com/Archive/2018/46/Infrastructure-as-Code-with-Terraform)

## Vault

[Vault by HashiCorp](https://www.vaultproject.io/)
A tool for managing secrets.

[Vault Curriculum - HashiCorp Learn](https://learn.hashicorp.com/vault)
[Documentation | Vault by HashiCorp](https://www.vaultproject.io/docs/)

[Introduction to Vault • Seth Vargo - YouTube](https://www.youtube.com/watch?v=yvImdLP3LEA)
[The Changelog #239: Managing Secrets Using Vault with Seth Vargo | Changelog](https://changelog.com/podcast/239)

## Nomad

[Nomad by HashiCorp](https://www.nomadproject.io/)
[Nomad by HashiCorp](https://www.nomadproject.io/use-cases/simple-container-orchestration)
A Distributed, Highly Available, Datacenter-Aware Scheduler

[Conductor: Why We Migrated from Kubernetes to Nomad – The New Stack](https://thenewstack.io/conductor-why-we-migrated-from-kubernetes-to-nomad/)

[Nomad Curriculum - HashiCorp Learn](https://learn.hashicorp.com/nomad)
[Documentation - Nomad by HashiCorp](https://www.nomadproject.io/docs/index.html)

## Otto

[Otto by HashiCorp](https://www.ottoproject.io/)
[The Successor to Vagrant - Otto by HashiCorp](https://www.ottoproject.io/intro/vagrant-successor.html)

Zero config development environment prepared by experts in the field.
Designed for production.
