---
title: "Cloud Providers"
categories:
  - web
tags:
  - web-deploy
toc: false
date: 2015-06-17 11:32:04
---

[The history of cloud: a fairy tale | Network World](http://www.networkworld.com/article/3217325/cloud-computing/the-history-of-cloud-a-fairy-tale.html)

## PaaS

A PAAS that supports autoscaling and database.

[Now: realtime global deployments](https://zeit.co/now#faq)

## Azure

http://azure.microsoft.com/en-us/pricing/details/websites/
http://azure.microsoft.com/en-us/pricing/details/sql-database/

Basic Tier
3 VM + 250GB SQL + Auto Scale = \$71
(plus bandwidth fees)

Supports C#, Java, Node, PHP, Python in SDK
It seems the "Websites" is the PAAS
But pricing page also indicates VM instances (IAAS)
Supports dynamic scaling out of the box, higher tier support more advances scaling algorithm

[Overview of the Azure CLI | Microsoft Docs](https://docs.microsoft.com/en-us/cli/azure/)

## Google App Engine

https://cloud.google.com/appengine/pricing
https://cloud.google.com/appengine/docs/quotas

Supports Python, Java, PHP, Go in SDK
Supports any language with Google Cloud VMs (IAAS)
Supports dynamic scaling out of the box

1 frontend + 1GB Datastore = Free

1 frontend + 64GB Datastore + Auto Scale = \$11.52
(plus extra frontend, bandwidth, read/write operation fees)

## Heroku

https://www.heroku.com/pricing

Supports any language with buildpacks
Plenty of add-ons

1 dyno + 10K row Postgres = Free

1 dynos + 64GB Postgres + [Adept Scale](https://addons.heroku.com/adept-scale#skiff) = \$68
(plus extra frontend, bandwidth fees)

# IaaS

[AWS vs. Azure vs. Google Cloud: Which free tier is best? | InfoWorld](http://www.infoworld.com/article/3179785/cloud-computing/aws-vs-azure-vs-google-cloud-which-free-tier-is-best.html)
[Cloud review: Amazon, Microsoft, Google, IBM, and Joyent | InfoWorld](http://www.infoworld.com/article/3057586/cloud-computing/cloud-review-amazon-microsoft-google-ibm-and-joyent-compared.html)
[Cloud compute: AWS, Azure, Google, SoftLayer compared | InfoWorld](http://www.infoworld.com/article/3150205/cloud-computing/cloud-compute-aws-azure-google-softlayer-compared.html)
[Kubernetes: AWS vs GCP vs Azure vs DigitalOcean – Andrei Dascalu – Medium](https://medium.com/@andreidascalu/kubernetes-aws-vs-gcp-vs-azure-vs-digitalocean-24d71067c795)[Google Cloud Platform for AWS Professionals  |  Google Cloud Platform for AWS Professionals  |  Google Cloud Platform](https://cloud.google.com/docs/compare/aws/)

[Apache Libcloud is a standard Python library that abstracts away differences among multiple cloud provider APIs | Apache Libcloud](https://libcloud.apache.org/)
[Apache Libcloud documentation](https://libcloud.readthedocs.io/en/latest/)
[islamgulov/libcloud.rest: REST Interface for Libcloud](https://github.com/islamgulov/libcloud.rest)
[pkgcloud/pkgcloud: pkgcloud is a standard library for node.js that abstracts away differences among multiple cloud providers.](https://github.com/pkgcloud/pkgcloud)
[apcera/libretto: Libretto is a Golang library to create Virtual Machines (VMs) on any cloud and Virtual Machine hosting platforms such as AWS, Azure, OpenStack, vSphere, or VirtualBox.](https://github.com/apcera/libretto)

> see `vps-hosting.md`

## Amazon Web Service

> see `aws.md`

## Google Cloud Platform

> see `google-cloud-platform.md`

## Rackspace

[Rackspace: Managed Dedicated & Cloud Computing Services](https://www.rackspace.com/)
