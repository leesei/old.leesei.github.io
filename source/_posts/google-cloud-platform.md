---
title: Google Cloud Platform
categories:
  - web
tags:
  - null
toc: true
date: 2017-02-11 10:35:04
---

[Cloud Computing Services | Google Cloud](https://cloud.google.com/)
[Google Cloud Platform](https://github.com/GoogleCloudPlatform) GitHub org

[How to get started with GCP | Google Cloud Platform](https://cloud.google.com/getting-started/)
[Google Cloud tutorial: Get started with Google Cloud Platform (GCP) | InfoWorld](https://www.infoworld.com/article/3267929/google-cloud-tutorial-get-started-with-google-cloud.html)

[GCP Free Tier - Free Extended Trials and Always Free | Google Cloud](https://cloud.google.com/free/) [details](https://cloud.google.com/free/docs/gcp-free-tier#always-free)

## Learning

[Navigating Google Cloud Platform: A Guide for new GCP Users (Google I/O '17) - YouTube](https://www.youtube.com/watch?v=RynMOvYdsCg)
[Google Cloud Platform (GCP) service guide: The right tools for the job | InfoWorld](https://www.infoworld.com/article/3254749/cloud-computing/google-cloud-platform-services-guide-the-right-tools-for-the-job.html)

[Google Codelabs](https://codelabs.developers.google.com/?cat=Cloud)
[GCP Education Series](https://codelabs.developers.google.com/gcp-edu)
[Google Cloud | Coursera](https://www.coursera.org/googlecloud)
[Developing Applications with Google Cloud Platform | Coursera](https://www.coursera.org/specializations/developing-apps-gcp)
[Google Cloud Platform Fundamentals: Core Infrastructure | Coursera](https://www.coursera.org/learn/gcp-fundamentals) !important, 20% GCP, 80% general knowledge
[Google Cloud Platform - YouTube](https://www.youtube.com/googlecloudplatform)

[Cloud_OnBoard_TrainingManual](https://lp.google-mkto.com/rs/248-TPC-286/images/Cloud_OnBoard_TrainingManual.pdf)

[How to Use Google Cloud Platform | Solutions Gallery | Google Cloud](https://cloud.google.com/docs/tutorials)
[Interactive Tutorials - GCP](https://console.cloud.google.com/getting-started?tutorial=toc)

## `gcloud` CLI

Install `google-cloud-sdk`, or `docker pull google/cloud-sdk:alpine`.
[gcloud | Cloud SDK | Google Cloud Platform](https://cloud.google.com/sdk/gcloud/reference/)
[google/cloud-sdk - Docker Hub](https://hub.docker.com/r/google/cloud-sdk/)

```sh
gcloud init
gcloud config configurations  # manage configurations
gcloud config configurations list # list configurations
gcloud config                 # manage active configuration
```

---

# Compute

[Cloud Computing Products at Scale | Cloud Compute Products | Google Cloud](https://cloud.google.com/products/compute/)

## Google Compute Engine (GCE)

[Google Cloud Platform Blog: IAM best practice guides available now](https://cloudplatform.googleblog.com/2016/03/IAM-best-practice-guides-available-now.html)
[Always Free Usage Limits | Google Cloud Platform Free Tier | Google Cloud Platform](https://cloud.google.com/free/docs/always-free-usage-limits)

[Storing and Retrieving Instance Metadata | Compute Engine Documentation | Google Cloud](https://cloud.google.com/compute/docs/storing-retrieving-metadata)

## Google Kubernetes Engine (GKE)

[Google Kubernetes Engine | Kubernetes Engine | Google Cloud](https://cloud.google.com/kubernetes-engine/)
[Kubernetes to Cloud Native: Jumpstart your journey developing on GKE](https://inthecloud.withgoogle.com/gke-ebook-21/dl-cd.html)

[Scalable Node.js with Kubernetes and Google Kubernetes Engine](https://nodesource.com/blog/scalable-nodejs-with-kubernetes-and-google-kubernetes-engine/)
[GKE tutorial: Get started with Google Kubernetes Engine | InfoWorld](https://www.infoworld.com/article/3292637/cloud-computing/gke-tutorial-get-started-with-google-kubernetes-engine.html)
[Architecting with Google Kubernetes Engine | Coursera](https://www.coursera.org/specializations/architecting-google-kubernetes-engine)
[Best practices for creating a highly available GKE cluster | Google Cloud Blog](https://cloud.google.com/blog/products/containers-kubernetes/best-practices-for-creating-a-highly-available-gke-cluster)

[Traffic Director supports proxyless gRPC | Google Cloud Blog](https://cloud.google.com/blog/products/networking/traffic-director-supports-proxyless-grpc)

[Kubernetes The Easy Way! (For Developers In 2018) - YouTube](https://www.youtube.com/watch?v=kOa_llowQ1c) CI/CD over GKE, deployment configs are all repos, git push/tag triggers commit/PR

## Google App Engine (GAE)

> `~/caravan/cloud-providers/gae`

```sh
gcloud components install app-engine-python
gcloud components install app-engine-python-extras
```

Use `gcloud app` subcommand to manage GAE applications.

[Managing Cloud Platform Projects, App Engine Applications, and Billing | App Engine standard environment for Python | Google Cloud Platform](https://cloud.google.com/appengine/docs/python/console/)
[google app engine - `gcloud app deploy` vs. `appcfg.py` - Stack Overflow](http://stackoverflow.com/questions/39280666/gcloud-app-deploy-vs-appcfg-py)

[Google App Engine Documentation | App Engine Documentation | Google Cloud](https://cloud.google.com/appengine/docs/)
[Sample Applications | App Engine standard environment for Python | Google Cloud](https://cloud.google.com/appengine/docs/standard/python/samples)
[GAE Cupboard](http://www.gaecupboard.com/) Ingredients for your Google App Engine recipes
[h5bp/server-configs-gae: Google App Engine (GAE) app boilerplate config](https://github.com/h5bp/server-configs-gae)

[bslatkin/mirrorrr: Web proxy for App Engine](https://github.com/bslatkin/mirrorrr)
[systempuntoout/stackprinter: StackPrinter: The Stack Exchange Printer Friendly Suite](https://github.com/systempuntoout/stackprinter)
[potatolondon/getfavicon: Google App Engine app that retrieves the relevant favicon for a URL, or returns a default icon should it not be able to find it.](https://github.com/potatolondon/getfavicon)

[Python Web Applications: Deploy Your Script as a Flask App – Real Python](https://realpython.com/python-web-applications/)

### Groovy

[10 years of App Engine with a Groovy twist -- Guillaume Laforge's Blog](http://glaforge.appspot.com/article/10-years-of-app-engine-with-a-groovy-twist)

[Glide - Home](http://glide-gae.appspot.com/)

[Welcome -- Gaelyk - a lightweight Groovy toolkit for Google App Engine Java](http://gaelyk.appspot.com/)
[Google I/O 2009 - Groovy and Grails in App Engine - YouTube](https://www.youtube.com/watch?v=NEnniZTdOYk)
[Groovy and Grails in Google App Engine](https://www.slideshare.net/glaforge/groovy-and-grails-in-google-app-engine)

## Google Cloud Run

> Function as a Service

[Google Cloud Run — Deploying Containerized Applications to a Serverles:-s Environment ⚡](https://medium.com/@timtech4u/deploy-serverless-container-google-cloud-run-68d716af7716)

# Storage

[Cloud Storage Options | Storage Products | Google Cloud](https://cloud.google.com/products/storage/)

## Google Cloud Storage

[Cloud Storage - Online Data Storage | Cloud Storage | Google Cloud](https://cloud.google.com/storage/)

# Database

[GCP Databases | Google Cloud](https://cloud.google.com/products/databases/)

## Cloud SQL

[Cloud SQL - MySQL & PostgreSQL Relational Database Service | Cloud SQL | Google Cloud](https://cloud.google.com/sql/)

## Firebase

Google bought Firebase in 2014 and migrated its Google Cloud Messaging to Firebase Cloud Messaging.
Also provides static hosting and FaaS.

[Firebase](https://firebase.google.com/)
[Firebase - Wikiwand](http://www.wikiwand.com/en/Firebase)
[Firebase Products](https://firebase.google.com/products-build)
[Firebase Authentication | Simple, free multi-platform sign-in](https://firebase.google.com/products/auth)
[Firebase Realtime Database | Store and sync data in real time](https://firebase.google.com/products/realtime-database/)
[Cloud Firestore | Store and sync app data at global scale | Firebase](https://firebase.google.com/products/firestore)
[Documentation | Firebase](https://firebase.google.com/docs/)
[Firebase Pricing](https://firebase.google.com/pricing)

[What is Firebase? The complete story, abridged. | by Doug Stevenson | Firebase Developers | Medium](https://medium.com/firebase-developers/what-is-firebase-the-complete-story-abridged-bcc730c5f2c0) !important
[Lessons from a small Firebase project. – ITNEXT](https://itnext.io/lessons-from-a-long-week-with-firebase-b433ce8ee49e)
[Why Frontend Developers Should Learn Firebase in 2022 - DEV Community](https://dev.to/javinpaul/why-frontend-developers-should-learn-firebase-in-2022-1kga)

[Firebase Open Source](https://firebaseopensource.com/)

[Add Firebase to your JavaScript project | Firebase Documentation](https://firebase.google.com/docs/web/setup)
[Add Firebase to your Flutter app](https://firebase.google.com/docs/flutter/setup?platform=ios)
[Add the Firebase Admin SDK to your server | Firebase Documentation](https://firebase.google.com/docs/admin/setup)
[firebase/firebaseui-web: FirebaseUI is an open-source JavaScript library for Web that provides simple, customizable UI bindings on top of Firebase SDKs to eliminate boilerplate code and promote best practices.](https://github.com/firebase/firebaseui-web)

[Building an API with Firebase - DEV Community 👩‍💻👨‍💻](https://dev.to/andrewevans0102/building-an-api-with-firebase-3h7e)

[Building a Real-Time Chat App with React and Firebase | CSS-Tricks](https://css-tricks.com/building-a-real-time-chat-app-with-react-and-firebase/)
[Getting started with react-redux-firebase - LogRocket Blog](https://blog.logrocket.com/getting-started-react-redux-firebase/)

## Bigtable

[Bigtable - Scalable NoSQL Database Service | Cloud Bigtable | Google Cloud](https://cloud.google.com/bigtable/)

## Cloud Spanner

[Cloud Spanner | Automatic Sharding with Transactional Consistency at Scale | Cloud Spanner | Google Cloud](https://cloud.google.com/spanner/)

Scalable SQL

# AI

[Cloud AI | Google Cloud](https://cloud.google.com/products/ai/)
