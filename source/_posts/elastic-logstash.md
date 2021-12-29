---
title: Elastic Logstash
categories:
  - web
toc: true
date: 2015-08-03 13:22:02
tags:
  - elastic-stack
---

## Logstash

[Logstash | Elastic](https://www.elastic.co/products/logstash)
[Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/index.html)
[Input plugins | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/input-plugins.html)
[elastic/logstash: logstash - transport and process your logs, events, or other data](https://github.com/elastic/logstash)

[How Logstash Works | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/pipeline.html)
The Logstash event processing pipeline has three stages: inputs → filters → outputs. Inputs generate events, filters modify them, and outputs ship them elsewhere. Inputs and outputs support codecs that enable you to encode or decode the data as it enters or exits the pipeline without having to use a separate filter.

[Introduction to Logstash: Getting Started | Cybera](https://www.cybera.ca/news-and-events/tech-radar/introduction-to-logstash-getting-started/)

[A Practical Introduction to Logstash | Elastic](https://www.elastic.co/blog/a-practical-introduction-to-logstash)
[The evolving story about the Logstash File Input | Elastic](https://www.elastic.co/blog/the-evolving-story-about-the-logstash-file-input)
[A History of Logstash Output Workers | Elastic](https://www.elastic.co/blog/a-history-of-logstash-output-workers)
[Logstash Persistent Queue | Elastic](https://www.elastic.co/blog/logstash-persistent-queue) ditched the need for Redis
[Just Enough Redis for Logstash | Elastic](https://www.elastic.co/blog/just_enough_redis_for_logstash)
[Little Logstash Lessons: Handling Duplicates | Elastic](https://www.elastic.co/blog/logstash-lessons-handling-duplicates) custom IDs
[The future of Log4j input in Logstash | Elastic](https://www.elastic.co/blog/log4j-input-logstash) write to local file and use Filebeat instead
[Archiving your event stream with Logstash | Elastic](https://www.elastic.co/blog/archiving-your-event-stream-with-logstash) archive log to S3
[Little Logstash Lessons - Part I: Using grok and mutate to type your data | Elastic](https://www.elastic.co/blog/little-logstash-lessons-part-using-grok-mutate-type-data)
[​Little Logstash Lessons: Using Logstash to help create an Elasticsearch mapping template | Elastic](https://www.elastic.co/blog/logstash_lesson_elasticsearch_mapping)
[Introducing Logstash Dissect | Elastic](https://www.elastic.co/blog/logstash-dude-wheres-my-chainsaw-i-need-to-dissect-my-logs)
[Do you grok Grok? | Elastic](https://www.elastic.co/blog/do-you-grok-grok)

[Questions about Self Monitoring Systems blog post - Beats - Discuss the Elastic Stack](https://discuss.elastic.co/t/questions-about-self-monitoring-systems-blog-post/43542/6) Configuring Logstash as a monitoring system

## Install and run

Logstash is easy to install and run in command line. This is very useful when trying out filters.

```sh
export LOGSTASH_PACKAGE=logstash-5.5.1.tar.gz
curl -O https://artifacts.elastic.co/downloads/logstash/${LOGSTASH_PACKAGE}
tar xzf ${LOGSTASH_PACKAGE}
```

See [elk-docker/Dockerfile at master · spujadas/elk-docker](https://github.com/spujadas/elk-docker/blob/master/Dockerfile)

```sh
bin/logstash -e 'input { stdin { } } output { stdout { codec => rubydebug } }'
bin/logstash -f config.conf
```

Parse nginx log from `stdin` or beat:

```logstash
input {
    stdin { }
    beats { port => "5043" }
}
filter {
  if [type] == "nginx-access" {
    grok {
      match => { "message" => "%{HTTPD_COMBINEDLOG}" }
    }
    geoip {
        source => "clientip"
    }
  }
}

output {
    stdout { codec => rubydebug }
}
```

Heartbeat and ES with credentials:

```logstash
input {
  heartbeat {
    interval => 5
    message  => 'Hello from Logstash 💓'
  }
}

output {
  elasticsearch {
    hosts    => [ 'elasticsearch' ]
    user     => 'elastic'
    password => 'changeme'
  }
}
```

## Plugins

[Working with plugins | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/working-with-plugins.html)
[Logstash Plugins](https://github.com/logstash-plugins)

[Input plugins | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/input-plugins.html)
[Output plugins | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/output-plugins.html)
[Codec plugins | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/codec-plugins.html)

## Filters Plugins

[Filter plugins | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/filter-plugins.html)
[Date filter plugin | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/plugins-filters-date.html)

### Grok

[Grok filter plugin | Logstash Reference | Elastic](https://www.elastic.co/guide/en/logstash/current/plugins-filters-grok.html)
[Grok Debugger](https://grokdebug.herokuapp.com/)
[Grok Constructor](http://grokconstructor.appspot.com/)

The syntax for a grok pattern is `%{SYNTAX:SEMANTIC}`.

`SYNTAX` are [regular expressions](https://www.elastic.co/guide/en/logstash/current/plugins-filters-grok.html#_regular_expressions) supported by [Oniguruma](https://github.com/kkos/oniguruma/blob/master/doc/RE). You can define your own patterns by putting it in `patterns_dir`.

Logstash provides a bunch of patterns by default: see [logstash-patterns-core/patterns](https://github.com/logstash-plugins/logstash-patterns-core/tree/master/patterns).

Examples:

```
%{NGINXACCESS}
%{SYSLOGBASE} %{DATA:message}
```

Search with `tags:_grokparsefailure` to look for filed logs.

## Docker

```sh
docker run -it --rm logstash logstash -e 'input { stdin { } }
filter {
  grok { match => {
    "message" => "%{IP:client} %{WORD:method} %{URIPATHPARAM:request} %{NUMBER:bytes} %{NUMBER:duration}"
  } }
}
output { stdout { codec => rubydebug } }'
```

```
55.3.244.1 GET /index.html 15824 0.043

{
      "duration" => "0.043",
       "request" => "/index.html",
    "@timestamp" => 2017-08-22T04:23:42.127Z,
        "method" => "GET",
         "bytes" => "15824",
      "@version" => "1",
          "host" => "kylee-arch",
        "client" => "55.3.244.1",
       "message" => "55.3.244.1 GET /index.html 15824 0.043"
}
```
