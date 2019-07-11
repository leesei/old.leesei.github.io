---
title: Google Cloud Platform
categories:
  - web
tags:
  - null
toc: true
date: 2017-02-11 10:35:04
---

[Cloud Computing Services  |  Google Cloud](https://cloud.google.com/)
[Google Codelabs](https://codelabs.developers.google.com/?cat=Cloud)
[GCP Education Series](https://codelabs.developers.google.com/gcp-edu)
[Google Cloud | Coursera](https://www.coursera.org/googlecloud)
[Developing Applications with Google Cloud Platform | Coursera](https://www.coursera.org/specializations/developing-apps-gcp)
[Google Cloud Platform Fundamentals: Core Infrastructure | Coursera](https://www.coursera.org/learn/gcp-fundamentals) !important, 20% GCP, 80% general knowledge

[Cloud_OnBoard_TrainingManual](https://lp.google-mkto.com/rs/248-TPC-286/images/Cloud_OnBoard_TrainingManual.pdf)

[Interactive Tutorials - GCP](https://console.cloud.google.com/getting-started?tutorial=toc)
[Google Cloud Platform](https://github.com/GoogleCloudPlatform) GitHub org

[How to get started with GCP  |  Google Cloud Platform](https://cloud.google.com/getting-started/)
[GCP Free Tier - Free Extended Trials and Always Free  |  Google Cloud](https://cloud.google.com/free/) [details](https://cloud.google.com/free/docs/gcp-free-tier#always-free)
[How to Use Google Cloud Platform  |  Documentation  |  Google Cloud](https://cloud.google.com/docs/tutorials)
[Google Cloud Platform (GCP) service guide: The right tools for the job | InfoWorld](https://www.infoworld.com/article/3254749/cloud-computing/google-cloud-platform-services-guide-the-right-tools-for-the-job.html)
[Google Cloud tutorial: Get started with Google Cloud Platform (GCP) | InfoWorld](https://www.infoworld.com/article/3267929/google-cloud-tutorial-get-started-with-google-cloud.html)

[Google Cloud Platform - YouTube](https://www.youtube.com/googlecloudplatform)
[Navigating Google Cloud Platform: A Guide for new GCP Users (Google I/O '17) - YouTube](https://www.youtube.com/watch?v=RynMOvYdsCg)

Install `google-cloud-sdk`, or `docker pull google/cloud-sdk:alpine`.
[gcloud  |  Cloud SDK  |  Google Cloud Platform](https://cloud.google.com/sdk/gcloud/reference/)
[google/cloud-sdk - Docker Hub](https://hub.docker.com/r/google/cloud-sdk/)

```sh
gcloud init
gcloud config configurations  # manage configurations
gcloud config configurations list # list configurations
gcloud config                 # manage active configuration
```

## Google Compute Engine (GCE)

[Google Cloud Platform Blog: IAM best practice guides available now](https://cloudplatform.googleblog.com/2016/03/IAM-best-practice-guides-available-now.html)
[Always Free Usage Limits  |  Google Cloud Platform Free Tier  |  Google Cloud Platform](https://cloud.google.com/free/docs/always-free-usage-limits)

[Storing and Retrieving Instance Metadata  |  Compute Engine Documentation  |  Google Cloud](https://cloud.google.com/compute/docs/storing-retrieving-metadata)

## Google Kubernetes Engine (GKE)

[Google Kubernetes Engine  |  Google Cloud](https://cloud.google.com/kubernetes-engine/)

[Scalable Node.js with Kubernetes and Google Kubernetes Engine](https://nodesource.com/blog/scalable-nodejs-with-kubernetes-and-google-kubernetes-engine/)
[GKE tutorial: Get started with Google Kubernetes Engine | InfoWorld](https://www.infoworld.com/article/3292637/cloud-computing/gke-tutorial-get-started-with-google-kubernetes-engine.html)

[Kubernetes The Easy Way! (For Developers In 2018) - YouTube](https://www.youtube.com/watch?v=kOa_llowQ1c) CI/CD over GKE, deployment configs are all repos, git push/tag triggers commit/PR

## Google App Engine (GAE)

> `~/caravan/cloud-providers/gae`

```sh
gcloud components install app-engine-python
gcloud components install app-engine-python-extras
```

Use `gcloud app` subcommand to manage GAE applications.

[Managing Cloud Platform Projects, App Engine Applications, and Billing  |  App Engine standard environment for Python  |  Google Cloud Platform](https://cloud.google.com/appengine/docs/python/console/)
[google app engine - `gcloud app deploy` vs. `appcfg.py` - Stack Overflow](http://stackoverflow.com/questions/39280666/gcloud-app-deploy-vs-appcfg-py)

[Google App Engine Documentation  |  App Engine Documentation  |  Google Cloud](https://cloud.google.com/appengine/docs/)
[Sample Applications  |  App Engine standard environment for Python  |  Google Cloud](https://cloud.google.com/appengine/docs/standard/python/samples)
[GAE Cupboard](http://www.gaecupboard.com/) Ingredients for your Google App Engine recipes
[h5bp/server-configs-gae: Google App Engine (GAE) app boilerplate config](https://github.com/h5bp/server-configs-gae)

[bslatkin/mirrorrr: Web proxy for App Engine](https://github.com/bslatkin/mirrorrr)
[systempuntoout/stackprinter: StackPrinter: The Stack Exchange Printer Friendly Suite](https://github.com/systempuntoout/stackprinter)
[potatolondon/getfavicon: Google App Engine app that retrieves the relevant favicon for a URL, or returns a default icon should it not be able to find it.](https://github.com/potatolondon/getfavicon)

### Groovy

[10 years of App Engine with a Groovy twist -- Guillaume Laforge's Blog](http://glaforge.appspot.com/article/10-years-of-app-engine-with-a-groovy-twist)

[Glide - Home](http://glide-gae.appspot.com/)

[Welcome -- Gaelyk - a lightweight Groovy toolkit for Google App Engine Java](http://gaelyk.appspot.com/)
[Google I/O 2009 - Groovy and Grails in App Engine - YouTube](https://www.youtube.com/watch?v=NEnniZTdOYk)
[Groovy and Grails in Google App Engine](https://www.slideshare.net/glaforge/groovy-and-grails-in-google-app-engine)

## Google Cloud Run

> Function as a Service

[Google Cloud Run — Deploying Containerized Applications to a Serverles:-s Environment ⚡](https://medium.com/@timtech4u/deploy-serverless-container-google-cloud-run-68d716af7716)

## Firebase

Google bought Firebase in 2014 and migrated its Google Cloud Messaging to Firebase Cloud Messaging.

[Firebase - Wikiwand](http://www.wikiwand.com/en/Firebase)
[Documentation  |  Firebase](https://firebase.google.com/docs/?authuser=0)

[Lessons from a small Firebase project. – ITNEXT](https://itnext.io/lessons-from-a-long-week-with-firebase-b433ce8ee49e)
