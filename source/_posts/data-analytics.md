---
title: Data Analytics
categories:
  - big-data
tags:
  - null
toc: true
date: 2016-09-21 23:05:16
---

> see `devops.md`
> see `database.md`, `elastic-stack.md`, `elastic-kibana.md`

[Analytics - Wikiwand](http://www.wikiwand.com/en/Analytics)

[Software analytics - Wikiwand](http://www.wikiwand.com/en/Software_analytics)
[Web analytics - Wikiwand](https://www.wikiwand.com/en/Web_analytics)
[IT operations analytics - Wikiwand](http://www.wikiwand.com/en/IT_operations_analytics)
[Session (web analytics) - Wikiwand](http://www.wikiwand.com/en/Session_(web_analytics%29)

[Behavioral analytics - Wikiwand](https://www.wikiwand.com/en/Behavioral_analytics)
not to be confused with User Behavioral Analytics, used in security context for threat detection
[Business intelligence - Wikiwand](https://www.wikiwand.com/en/Business_intelligence)
[Cohort analysis - Wikiwand](https://www.wikiwand.com/en/Cohort_analysis)
[10 Steps To Get You Started With Behavioral Analytics](https://amplitude.com/blog/2016/06/14/10-steps-behavioral-analytics/)
[Six Ways to Create Better Customer Behavior Analytics | Datameer](https://www.datameer.com/blog/six-ways-create-better-customer-behavior-analytics/)

[What is Operational Analytics? - Definition from Techopedia](https://www.techopedia.com/definition/29495/operational-analytics)
[Operations Analytics | Coursera](https://www.coursera.org/learn/wharton-operations-analytics)

[Business analytics - Wikiwand](https://www.wikiwand.com/en/Business_analytics)

First data, logs or events triggered by applications and services, must be collected and store on some data store.

[Data Series - Microsoft Virtual Academy](https://mva.microsoft.com/search/SearchResults.aspx#!q="Data Series%3A"&lang=1033)

[Introducing Application Insights Analytics | Brian Harry's blog](https://blogs.msdn.microsoft.com/bharry/2016/03/28/introducing-application-analytics/)

[Apache Hadoop Ecosystem and Open Source Big Data Projects | Hortonworks](https://hortonworks.com/ecosystems/) !important

[Prefect Docs](https://docs.prefect.io/)

## Use cases

[OLTP vs. OLAP](http://datawarehouse4u.info/OLTP-vs-OLAP.html)

[Online transaction processing - Wikiwand](https://www.wikiwand.com/en/Online_transaction_processing) OLTP
[What is OLTP (online transaction processing)? - Definition from WhatIs.com](https://searchdatacenter.techtarget.com/definition/OLTP)
[Online analytical processing - Wikiwand](https://www.wikiwand.com/en/Online_analytical_processing) OLAP
[What is OLAP (online analytical processing)? - Definition from WhatIs.com](https://searchdatamanagement.techtarget.com/definition/OLAP)
[Hybrid transactional/analytical processing (HTAP) - Wikiwand](http://www.wikiwand.com/en/Hybrid_transactional/analytical_processing_(HTAP%29) NoSQL/NewSQL database can serve this purpose
RTA
[Data warehouse - Wikiwand](https://www.wikiwand.com/en/Data_warehouse)
[Extract, transform, load - Wikiwand](https://www.wikiwand.com/en/Extract,_transform,_load)
[ETL](http://datawarehouse4u.info/ETL-process.html)

[A good nudge trumps a good prediction - O'Reilly Radar](http://radar.oreilly.com/2014/07/a-good-nudge-trumps-a-good-prediction.html)

> Whether prediction should be user friendly or business friendly

## Stream Architecture

[What is Stream Processing? - data Artisans](https://data-artisans.com/what-is-stream-processing)
[How a Stream Works - DZone Big Data](https://dzone.com/articles/how-a-stream-works)

Streaming pipeline:

| Type           | Example       | Usage                                                 |
| -------------- | ------------- | ----------------------------------------------------- |
| Message bus    | Redis, Kafka  | low latency data ingest                               |
| Datalake       | S3/HDFS       | high capacity low cost long term storage              |
| Data warehouse | Elasticsearch | data structuring and indexing, fast interactive query |

[Apache Flink vs. Apache Spark - DZone Big Data](https://dzone.com/articles/apache-flink-vs-apache-spark-brewing-codes)
[Apache Flink: Does the world need another streaming engine? | ZDNet](https://www.zdnet.com/article/apache-flink-does-the-world-need-another-streaming-engine/)
[Choose your real-time weapon: Storm or Spark? | InfoWorld](https://www.infoworld.com/article/2854894/application-development/spark-and-storm-for-real-time-computation.html)

[Streaming Architecture with Ted Dunning | Software Engineering Daily](https://softwareengineeringdaily.com/2018/02/19/streaming-architecture-with-ted-dunning/)
Spark: Batch first, then stream; ELT job, working set in memory
Flink: Stream first, then batch; exactly one event processing

[Apache Flink: Scalable Stream and Batch Data Processing](https://flink.apache.org/)
[How Netflix Optimized Flink for Massive Scale on AWS](https://www.datanami.com/2018/04/30/how-netflix-optimized-flink-for-massive-scale-on-aws/)
[Why Apache Flink - data Artisans](https://data-artisans.com/why-apache-flink)

[Apache Kafka](https://kafka.apache.org/)
[Apache Kafka - Hortonworks](https://hortonworks.com/apache/kafka/)
[Kafka Design Patterns with Gwen Shapira | Software Engineering Daily](https://softwareengineeringdaily.com/2018/02/20/kafka-design-patterns-with-gwen-shapira/)
[Best Practices for Apache Kafka® in Production: Confluent Online Talk Series - Confluent](https://www.confluent.io/online-talk/best-practices-for-apache-kafka-in-production-confluent-online-talk-series)

[Apache NiFi](https://nifi.apache.org/)
[Apache NiFi - Hortonworks](https://hortonworks.com/apache/nifi/)

[Apache Storm](http://storm.apache.org/)
[Apache Storm - Hortonworks](https://hortonworks.com/apache/storm/)
[Apache Storm: Architecture - DZone Big Data](https://dzone.com/articles/apache-storm-architecture)

[Apache Spark™ - Unified Analytics Engine for Big Data](https://spark.apache.org/)
[Apache Spark - Hortonworks](https://hortonworks.com/apache/spark/)
[Spark and Streaming with Matei Zaharia | Software Engineering Daily](https://softwareengineeringdaily.com/2018/02/26/spark-and-streaming-with-matei-zaharia/)
[Apache Spark Tutorials - Frank Kane - YouTube](https://www.youtube.com/playlist?list=PL6cactdCCnTJ2XZYIQYIwLperpbKB86jv)
[Apache Spark 2 using Python 3 - YouTube](https://www.youtube.com/playlist?list=PLf0swTFhTI8qtIYxVoPOjA2fYzBFiNMue)
[Spark SQL: An Introductory Guide - DZone Big Data](https://dzone.com/articles/spark-sql-an-introductory-guide-for-beginners)
[We interrupt this revolution: Apache Spark changes the rules of the game | ZDNet](https://www.zdnet.com/article/we-interrupt-this-revolution-apache-spark-changes-the-rules-of-the-game/)

[Cloud Dataflow - Stream & Batch Data Processing  |  Google Cloud](https://cloud.google.com/dataflow/)
[Hadoop and Spark: A tale of two cities | ZDNet](https://www.zdnet.com/article/hadoop-and-spark-a-tale-of-two-cities/)

[Apache Beam](https://beam.apache.org/)
[Apache Beam - Wikiwand](https://www.wikiwand.com/en/Apache_Beam)
stream API to abstract streaming warehouse, abstracts Flink, Spark, Dataflow  
Beam is introducing a framework through which APIs in languages other than Java can be supported, and Python is the first one.

## Batch Architecture

[Apache Hadoop](https://hadoop.apache.org/)
[Big Data: What is Hadoop - An Easy Explanation For Absolutely Anyone](https://www.bernardmarr.com/default.asp?contentID=1080)

[Is Hadoop Officially Dead?](https://www.datanami.com/2018/10/18/is-hadoop-officially-dead/)
[Why is Hadoop dying? | Packt Hub](https://hub.packtpub.com/why-is-hadoop-dying/)

## Big data

[onurakpolat/awesome-bigdata: A curated list of awesome big data frameworks, ressources and other awesomeness.](https://github.com/onurakpolat/awesome-bigdata)

[Fueling the Gold Rush: The Greatest Public Datasets for AI](https://medium.com/startup-grind/fueling-the-ai-gold-rush-7ae438505bc2)
[Dataset Search](https://toolbox.google.com/datasetsearch)

[The Data Science Venn Diagram — Drew Conway](http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram)
[The Third Wave Data Scientist – Towards Data Science](https://towardsdatascience.com/the-third-wave-data-scientist-1421df7433c9)

[Data Skeptic](https://dataskeptic.com/)
[A data cleaner's cookbook - About](https://www.polydesmida.info/cookbook/index.html)
[Chris Albon](https://chrisalbon.com/)

[Pachyderm - Scalable, Reproducible Data Science](http://www.pachyderm.io/)
[Containerized data analytics at scale, with Minio and Pachyderm](https://blog.minio.io/containerized-data-analytics-at-scale-with-minio-and-pachyderm-1b9256c86c5b)

[Data Science eBook by Analyticbridge - 2nd Edition - Data Science Central](https://www.datasciencecentral.com/profiles/blogs/data-science-ebook-2nd-edition-table-of-content)

[Extracting value from the IoT - O'Reilly Radar](http://radar.oreilly.com/2014/06/extracting-value-from-the-iot.html)

> Collecting data and loading it into a data warehouse is not sufficient. You also need capabilities for accessing, modeling, and analyzing your data.

[Awesome Data Science Repository - Data Science Central](http://www.datasciencecentral.com/group/research/forum/topics/awesome-data-science-repository)

[PredictionIO Open Source Machine Learning Server](https://prediction.io/)

[The Art and Science of Data-Driven Journalism](http://towcenter.gitbooks.io/the-art-and-science-of-data-driven-journalism/content/)

[Comparison of top data science libraries for Python, R and Scala [Infographic] - Data Science Central](https://www.datasciencecentral.com/profiles/blogs/comparison-of-top-data-science-libraries-for-python-r-and-scala)

[Kaggle: Your Home for Data Science](https://www.kaggle.com/)
[Introduction to Data Science](http://www.infoq.com/presentations/introduction-data-science)
[Explore Your Data: The Fundamentals of Network Analysis](http://www.infoq.com/presentations/network-analysis)

[Design vs. Data: Enemies or Friends?](http://www.infoq.com/presentations/design-data) how to evolve and extent a code base.

[Cathy O'Neil on Weapons of Math Destruction | EconTalk | Library of Economics and Liberty](http://www.econtalk.org/archives/2016/10/cathy_oneil_on_1.html) crucial decision made based on machine learn statistics is unreliable as no one really know how the algorithm works

[An expert's guide to big data storage architecture](https://searchstorage.techtarget.com/essentialguide/An-experts-guide-to-big-data-storage-architecture)
[Big data tutorial: Everything you need to know](https://searchstorage.techtarget.com/essentialguide/Big-data-tutorial-Everything-you-need-to-know)

### HDF

[HDFGroup Documentation](https://portal.hdfgroup.org/display/support/Documentation)
https://support.hdfgroup.org/HDF5/docNewFeatures/SWMR/Design-HDF5-FileLocking.pdf

[Parallel I/O – Why, How, and Where to? - The HDF Group](https://www.hdfgroup.org/2015/04/parallel-io-why-how-and-where-to-hdf5/)

[Cyrille Rossant - Moving away from HDF5](https://cyrille.rossant.net/moving-away-hdf5/)
[Cyrille Rossant - Should you use HDF5?](https://cyrille.rossant.net/should-you-use-hdf5/)
[On HDF5 and the future of data management](http://blog.khinsen.net/posts/2016/01/07/on-hdf5-and-the-future-of-data-management/)

### Jupyter

[Project Jupyter | Home](http://jupyter.org/)
[Jupyter and the future of IPython — IPython](http://ipython.org/index.html) Jupyter was formerly [IPython Notebook](http://ipython.org/notebook.html)

[Jupyter Notebook: An Introduction – Real Python](https://realpython.com/jupyter-notebook-introduction/)
[Basics of Jupyter Notebook and Python | Packt Hub](https://hub.packtpub.com/basics-jupyter-notebook-python/)
[28 Jupyter Notebook tips, tricks and shortcuts](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/)

[A gallery of interesting Jupyter Notebooks · jupyter/jupyter Wiki](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks)
[JupyterLab Documentation](https://jupyterlab.readthedocs.io/en/stable/)
[Hello, Colaboratory - Colaboratory](https://colab.research.google.com/notebooks/welcome.ipynb#recent=true)
[Microsoft Azure Notebooks](https://notebooks.azure.com/)

[scrapbook documentation](https://nteract-scrapbook.readthedocs.io/en/latest/) a library for recording a notebook’s data values and generated visual content as "scraps"
[papermill documentation](https://papermill.readthedocs.io/en/latest/) tool for parameterizing and executing Jupyter Notebooks

[Project Jupyter](https://github.com/jupyter)
[The Jupyter Notebook — Jupyter Notebook documentation](https://jupyter-notebook.readthedocs.io/en/stable/)
[nbviewer](https://nbviewer.jupyter.org/) [FAQ](https://nbviewer.jupyter.org/faq)
[jupyter/nbconvert: Jupyter Notebook Conversion](https://github.com/jupyter/nbconvert)
[Binder (beta)](https://mybinder.org/) executable notebooks

[JupyterLab](https://github.com/jupyterlab)
[JupyterLab Documentation — JupyterLab documentation](https://jupyterlab.readthedocs.io/en/stable/)

[JupyterHub](https://github.com/jupyterhub)
[JupyterHub — JupyterHub documentation](https://jupyterhub.readthedocs.io/en/stable/)

[ipywidgets — Jupyter Widgets documentation](https://ipywidgets.readthedocs.io/en/stable/index.html)
[A very simple demo of interactive controls on Jupyter notebook](https://towardsdatascience.com/a-very-simple-demo-of-interactive-controls-on-jupyter-notebook-4429cf46aabd)

[jupyter-repo2docker — repo2docker documentation](https://repo2docker.readthedocs.io/en/latest/)
[Docker Without the Hassle – Towards Data Science](https://towardsdatascience.com/docker-without-the-hassle-b98447caedd8)

[neuron - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=neuron.neuron-IPE)
[Data Science in Visual Studio Code using Neuron, a new VS Code extension – Microsoft Faculty Connection](https://blogs.msdn.microsoft.com/uk_faculty_connection/2018/10/29/data-science-in-visual-studio-code-using-neuron-a-new-vs-code-extension/)

### CUDA

> see `docker-nvidia.md`

[CUDA - Wikiwand](https://www.wikiwand.com/en/CUDA)
[Programming Guide :: CUDA Toolkit Documentation](https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html)

[Intro to Parallel Programming CUDA - Udacity 458 - YouTube](https://www.youtube.com/playlist?list=PLGvfHSgImk4aweyWlhBXNF6XISY3um82_)

[Home - CUDA Tutorial](https://cuda-tutorial.readthedocs.io/en/latest/)

[NVIDIA Collective Communications Library (NCCL) | NVIDIA Developer](https://developer.nvidia.com/nccl)  multi-GPU and multi-node collective communication primitives 

## Business Analytics

### Commercial

[Big Data Integration and Analytics | Hitachi Vantara](https://www.hitachivantara.com/en-us/products/big-data-integration-analytics.html)
[Business Intelligence and Analytics | Tableau Software](https://www.tableau.com/)

[The 5 best self-service BI tools compared | CIO](https://www.cio.com/article/3281372/business-intelligence/the-5-best-self-service-bi-tools-compared.html)

### Open source

[Apache Superset (incubating) — Apache Superset documentation](http://superset.apache.org/)
[Redash helps you make sense of your data | Redash](https://redash.io/)
[Metabase](https://www.metabase.com/)

---

## Data Processing

[Tabula: Extract Tables from PDFs](https://tabula.technology/)
[香港地址解析器 Hong Kong Address Parser](https://g0vhk-io.github.io/HKAddressParser/#/)

[資料一線通 | DATA.GOV.HK](https://data.gov.hk/tc/)
[Open Data Hong Kong - 香港開放數據 | Hong Kong's Open Data community](https://www.opendatahk.com/)
[g0vhk.io - Home | Facebook](https://www.facebook.com/g0vhk.io)

## Python

> see `data-analytics-python.md`

## JavaScript

[Crossfilter](http://square.github.io/crossfilter/) Pandas for JavaScript
[How to Create an Interactive Dashboard with Crossfilter and Dc.Js](https://blog.sicara.com/interactive-dashboard-crossfilter-dcjs-tutorial-7f3a3ea584c2)
