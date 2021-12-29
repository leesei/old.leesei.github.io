---
title: Elasticsearch
categories:
  - web
toc: true
date: 2015-08-03 13:22:02
tags:
  - database
  - elastic-stack
---

## Elasticsearch

[Elasticsearch | Elastic](https://www.elastic.co/products/elasticsearch)
[Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
[Elasticsearch Clients | Elastic](https://www.elastic.co/guide/en/elasticsearch/client/index.html)
[Elasticsearch Plugins and Integrations | Elastic](https://www.elastic.co/guide/en/elasticsearch/plugins/current/index.html)
[Elasticsearch: The Definitive Guide | Elastic](https://www.elastic.co/guide/en/elasticsearch/guide/current/index.html) For 2.x

[Open Distro for Elasticsearch | Open Distro](https://opendistro.github.io/for-elasticsearch/) AWS's distro after Elasticsearch.co's license change

[A Practical Introduction to Elasticsearch | Elastic](https://www.elastic.co/blog/a-practical-introduction-to-elasticsearch)
[Elasticsearch 5.0.0 GA released | Elastic](https://www.elastic.co/blog/elasticsearch-5-0-0-released)
[Six Ways to Crash Elasticsearch | Elastic](https://www.elastic.co/blog/found-crash-elasticsearch)
[Monitoring Kafka with Elastic Stack: Filebeat | Elastic](https://www.elastic.co/blog/monitoring-kafka-with-elastic-stack-1-filebeat) uses 5.0 ingest pipeline
[Setting Up Elasticsearch for a Blog | Elastic](https://www.elastic.co/blog/setting-up-elasticsearch-for-a-blog) create index, mapping via API, 2.x
[Elasticsearch as a NoSQL Database | Elastic](https://www.elastic.co/blog/found-elasticsearch-as-nosql)
[Reindex is coming! | Elastic](https://www.elastic.co/blog/reindex-is-coming)

[Elasticsearch by Example: Part 1 – codeburst](https://codeburst.io/elasticsearch-by-example-part-1-a4a38cd97f55)
[Elasticsearch by Example: Part 2 – codeburst](https://codeburst.io/elasticsearch-by-example-part-2-73f9816f5404)
[Elasticsearch by Example: Part 3 – codeburst](https://codeburst.io/elasticsearch-by-example-part-3-2ec44d99892d)
[Elasticsearch by Example: Part 4 – codeburst](https://codeburst.io/elasticsearch-by-example-part-4-cd11928a579e)
[Elasticsearch by Example: Part 5 – codeburst](https://codeburst.io/elasticsearch-by-example-part-5-6495f69f3797)

[Get data from Elasticsearch by id using http from @wfbutton on @eggheadio](https://egghead.io/courses/get-started-with-elasticsearch)
[Using Elasticsearch as the Primary Data Store](https://vlkan.com/blog/post/2018/11/14/elasticsearch-primary-data-store/)
[rekibnikufesin/elasticsearch-intro](https://github.com/rekibnikufesin/elasticsearch-intro)
[dwyl/learn-elasticsearch: Learn how to use ElasticSearch to power a great search experience for your project/product/website.](https://github.com/dwyl/learn-elasticsearch)

[Elasticsearch Cheat Sheet for developers](http://elasticsearch-cheatsheet.jolicode.com/)
[A Useful Elasticsearch Cheat Sheet in Times of Trouble](https://logz.io/blog/elasticsearch-cheat-sheet/)
[Elasticsearch Developer Cheat Sheet](https://sematext.com/elasticsearch-developer-cheat-sheet/)
[Elasticsearch Devops Cheat Sheet and Snippets](https://sematext.com/elasticsearch-devops-cheat-sheet/)

[Getting started with Elasticsearch and Node.js - Part 1](https://www.compose.com/articles/getting-started-with-elasticsearch-and-node/)
[Getting started with Elasticsearch and Node.js - Part 2](https://www.compose.com/articles/elasticsearch-and-node-part-ii/)
[Getting started with Elasticsearch and Node.js - Part 3](https://www.compose.com/articles/getting-started-with-elasticsearch-and-node-js-part-3/)

### CLI API

```sh
# create index
http PUT http://elasticsearch:9200/INDEX
# get index
http -b http://elasticsearch:9200/INDEX?pretty
# get all indices
http -b http://elasticsearch:9200/_cat/indices?pretty
# get all index templates
http -b http://elasticsearch:9200/_template?pretty

# _reindex
curl -XPOST elasticsearch:9200/_reindex?pretty -d'{
  "source": {
    "index": "src",
    "query": {
      "match": {
        "tags": "bananas"
      }
    }
  },
  "dest": {
    "index": "dest"
  }
}'
http -b POST http://elasticsearch:9200/_reindex?pretty << EOF
{
  "source": {
    "index": "src",
    "query": {
      "match": {
        "tags": "bananas"
      }
    }
  },
  "dest": {
    "index": "dest"
  }
}
EOF

# performance, stats
## show on-going tasks
http "http://elasticsearch:9200/_tasks?pretty&detailed&actions=*reindex,*byquery"

# insert document
http -b POST http://elasticsearch:9200/INDEX/TYPE?pretty << EOF
{
  "userId": 10,
  "name": {
    "first": "Katherine",
    "last": "Jones"
  },
  "tags": ["trick manager", "restaurant manager"]
}
EOF

# get mapping
http http://elasticsearch:9200/INDEX/TYPE/_mapping?pretty
{
  "name" : {
    "properties" : {
      "name" : {
        "properties" : {
          "first" : {
            "type" : "string"
          },
          "last" : {
            "type" : "string"
          }
        }
      },
      "tags" : {
        "type" : "string"
      },
      "userId" : {
        "type" : "long"
      }
    }
  }
}
```

[taskrabbit/elasticsearch-dump: Import and export tools for elasticsearch](https://github.com/taskrabbit/elasticsearch-dump)
[ElasticSearchCLITools/esTail: ElasticSearch CLI Tail - This application simulate the tail command against a index which has a @timestamp](https://github.com/ElasticSearchCLITools/esTail)

[API Conventions | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/api-conventions.html)
[Document APIs | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs.html)
[Search APIs | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/search.html)
[Indices APIs | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/indices.html) vs [Document's index API](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-index_.html)?
[cat APIs | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/cat.html) return data in tabulated forms

### Internals

[Elasticsearch from the Bottom Up, Part 1 | Elastic](https://www.elastic.co/blog/found-elasticsearch-from-the-bottom-up) !important, Lucent links
[Elasticsearch from the Top Down | Elastic](https://www.elastic.co/blog/found-elasticsearch-top-down)
[Elasticsearch in Production | Elastic](https://www.elastic.co/blog/found-elasticsearch-in-production) !important, network partition, profiling endpoints
[Elasticsearch Internals - Tracking in-sync shard copies | Elastic](https://www.elastic.co/blog/tracking-in-sync-shard-copies)
[Elasticsearch Hot Warm Architecture | Elastic](https://www.elastic.co/blog/hot-warm-architecture-in-elasticsearch-5-x)

An index is stored in a set of shards, which are themselves Lucene indices consisting of segments. Search happens on segments. Documents marked deleted will be removed when segments are merges.
Elasticsearch creates 5 shards per index by default.

[Where are my documents?Refreshing news... | Elastic](https://www.elastic.co/blog/refreshing_news)
[Disk-Based Field Data a.k.a. Doc Values | Elastic](https://www.elastic.co/blog/disk-based-field-data-a-k-a-doc-values) inverted index
[Sparse versus dense document values with Apache Lucene | Elastic](https://www.elastic.co/blog/sparse-versus-dense-document-values-with-apache-lucene)

### Index Creation/Mapping

[index template](https://www.elastic.co/guide/en/elasticsearch/reference/current/indices-templates.html) to control how the daily index is generated
Mapping will be generated dynamically but it:

- may detect field types incorrectly
- produce duplicate fields ([`_source`](https://www.elastic.co/guide/en/elasticsearch/reference/current/mapping-source-field.html) and [`_all`](https://www.elastic.co/guide/en/elasticsearch/reference/current/mapping-all-field.html)
- always use [standard analyzer](https://www.elastic.co/guide/en/elasticsearch/reference/current/analysis-standard-analyzer.html) which tokenizes strings
- all keys in the documents will end up in the index's mapping

[Mapping | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/mapping.html)
[An Introduction to Elasticsearch Mapping | Elastic](https://www.elastic.co/blog/found-elasticsearch-mapping-introduction) !important
The schema in Elasticsearch is a mapping that describes the the fields in the JSON documents along with their data type, as well as how they should be indexed in the Lucene indexes that lie under the hood. Because of this, in Elasticsearch terms, we usually call this schema a “mapping”.
"Mapping type" (keys at root level of mapping) is the name of type in index, see below.
An field can be of "multi-field" type to support multiple way of indexing (or not at all).
[Index vs. Type | Elastic](https://www.elastic.co/blog/index-vs-type)
In the past we tried to make elasticsearch easier to understand by building an analogy with relational databases: indices would be like a database, and types like a table in a database. This was a mistake. Types are being [phased out](https://github.com/elastic/elasticsearch/issues/15613) since 5.x.
[A Data Exploration Workflow for Mappings | Elastic](https://www.elastic.co/blog/found-mapping-workflow) insert a document and reference the dynamically generated mapping
[Managing Relations Inside Elasticsearch | Elastic](https://www.elastic.co/blog/managing-relations-inside-elasticsearch)
Elasticsearch has a concept of "query time" joining with [parent/child-relations](https://www.elastic.co/guide/reference/mapping/parent-field) and "index time" joining with [nested types](https://www.elastic.co/guide/reference/mapping/nested-type).
[Indices, types, and parent / child: current status and upcoming changes in Elasticsearch | Elastic](https://www.elastic.co/blog/index-type-parent-child-join-now-future-in-elasticsearch)
[And the big one said "Rollover" — Managing Elasticsearch time-based indices efficiently | Elastic](https://www.elastic.co/blog/managing-time-based-indices-efficiently) introduces Rollover template
[Removal of mapping types in Elasticsearch 6.0 | Elastic](https://www.elastic.co/blog/removal-of-mapping-types-elasticsearch)

### Data types

[Elasticsearch replaces string type with two new types text and keyword. | Elastic](https://www.elastic.co/blog/strings-are-dead-long-live-strings) `text` vs `keyword` (full text vs exact match)
[Numeric and Date Ranges...Just Another Brick in the Wall | Elastic](https://www.elastic.co/blog/numeric-and-date-ranges-in-elasticsearch-just-another-brick-in-the-wall)
[Searching numb3rs in 5.0 | Elastic](https://www.elastic.co/blog/searching-numb3rs-in-5.0)

### Ingest

Elastic search gained the power to ingest logs in 5.0. Consider it a little cousin of Logstash.

[Writing Your Own Ingest Processor for Elasticsearch | Elastic](https://www.elastic.co/blog/writing-your-own-ingest-processor-for-elasticsearch)
[A New Way To Ingest - Part 1 | Elastic](https://www.elastic.co/blog/new-way-to-ingest-part-1)
[A New Way To Ingest - Part 2 | Elastic](https://www.elastic.co/blog/new-way-to-ingest-part-2)
[Elastic Ingest Node: A Client's Perspective | Elastic](https://www.elastic.co/blog/ingest-node-a-clients-perspective)

### Text Analyzer

[All About Analyzers, Part One | Elastic](https://www.elastic.co/blog/found-text-analysis-part-1)
[All About Analyzers, Part Two | Elastic](https://www.elastic.co/blog/found-text-analysis-part-2)

_Match query_ also went through [standard analyzer](https://www.elastic.co/guide/en/elasticsearch/reference/current/analysis-standard-analyzer.html) and _term query_ looks for exact match.

### Query

Elasticsearch is powered by Apache Lucene query language.

[Query DSL | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html)

[Troubleshooting Elasticsearch searches, for Beginners | Elastic](https://www.elastic.co/blog/found-beginner-troubleshooting) !important
[Painless Scripting Language | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-scripting-painless.html)
[Lucene Expressions Language | Elasticsearch Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-scripting-expression.html)

[Painless: A New Scripting Language | Elastic](https://www.elastic.co/blog/painless-a-new-scripting-language)
[Using Painless in Kibana scripted fields | Elastic](https://www.elastic.co/blog/using-painless-kibana-scripted-fields)
[A Profile a Day Keeps the Doctor Away: The Elasticsearch Search Profiler | Elastic](https://www.elastic.co/blog/a-profile-a-day-keeps-the-doctor-away-the-elasticsearch-search-profiler)
[In which order are my Elasticsearch queries/filters executed? | Elastic](https://www.elastic.co/blog/elasticsearch-query-execution-order)
[The Great Query Refactoring: Thou shalt only parse once | Elastic](https://www.elastic.co/blog/the-great-query-refactoring-thou-shalt-only-parse-once)
[Instant Aggregations: Rewriting Queries for fun and profit | Elastic](https://www.elastic.co/blog/instant-aggregations-rewriting-queries-for-fun-and-profit)
[Monitoring the Search Queries | Elastic](https://www.elastic.co/blog/monitoring-the-search-queries) monitoring production Elasticsearch with Packetbeats

[Elasticsearch.pm - Part 4: Querying and Search Options](https://www.compose.com/articles/elasticsearch-pm-part-4-querying-and-search-options/)

> set `explain` to `true` on search object

#### SQL

[An Introduction to Elasticsearch SQL with Practical Examples - Part 1 | Elastic](https://www.elastic.co/blog/an-introduction-to-elasticsearch-sql-with-practical-examples-part-1)
[SQL Access | Elasticsearch Reference [6.3] | Elastic](https://www.elastic.co/guide/en/elasticsearch/reference/current/xpack-sql.html)

#### Lucene

[Apache Lucene - Apache Lucene Core](http://lucene.apache.org/core/)
[org.apache.lucene.queryparser.classic (Lucene 6.4.1 API)](http://lucene.apache.org/core/6_4_1/queryparser/org/apache/lucene/queryparser/classic/package-summary.html#package.description)
[Welcome to Lucene Tutorial.com - Lucene Tutorial.com](http://www.lucenetutorial.com/index.html)

### Aggregation

[Elasticsearch's New Aggregations | Elastic](https://www.elastic.co/blog/found-elasticsearch-aggregations)

Aggregation groups documents into buckets of documents; replaces facets since 1.0

### Scaling

[Sizing Elasticsearch | Elastic](https://www.elastic.co/blog/found-sizing-elasticsearch) scaling Elasticsearch, shard and index, inverted index
[Every Shard deserves a home. | Elastic](https://www.elastic.co/blog/every-shard-deserves-a-home)
[Scaling Elasticsearch, Kibana, Beats, and Logstash | Elastic](https://www.elastic.co/blog/small-medium-or-large-scaling-elasticsearch-and-evolving-the-elastic-stack-to-fit) Architecture, 5.x
[Elasticsearch Hot Warm Architecture | Elastic](https://www.elastic.co/blog/hot-warm-architecture-in-elasticsearch-5-x)

### Securing Elasticsearch

[Securing Elasticsearch and Kibana | X-Pack for the Elastic Stack | Elastic](https://www.elastic.co/guide/en/x-pack/current/xpack-security.html)
[Getting Started with Elasticsearch and SSL & Native Authentication | Elastic](https://www.elastic.co/blog/getting-started-with-elasticsearch-ssl-native-authentication)
[Getting Started with Shield’s Document Level Security in Elasticsearch | Elastic](https://www.elastic.co/blog/getting-started-with-shield-document-level-security-in-elasticsearch)

### Discovery

[github/elasticsearch-srv-discovery: Elasticsearch discovery with SRV records](https://github.com/github/elasticsearch-srv-discovery)
[lithiumtech/elasticsearch-consul-discovery: Consul based node discovery plugin for elasticsearch](https://github.com/lithiumtech/elasticsearch-consul-discovery)

## Curator

[elastic/curator: Curator: Tending your Elasticsearch indices](https://github.com/elastic/curator)
[Curator Reference | Elastic](https://www.elastic.co/guide/en/elasticsearch/client/curator/current/index.html)
