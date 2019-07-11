---
title: Elastic Beats
categories:
  - web
toc: true
date: 2015-08-03 13:22:02
tags:
  - elastic-stack
---

## Beats

[Beats | Elastic](https://www.elastic.co/products/beats)
[Beats Platform Reference | Elastic](https://www.elastic.co/guide/en/beats/libbeat/current/index.html)

[Beats 5.3.0 released | Elastic](https://www.elastic.co/blog/beats-5-3-0-released)
[Filebeat modules, access logs and Elasticsearch storage requirements | Elastic](https://www.elastic.co/blog/filebeat-modiles-access-logs-and-elasticsearch-storage-requirements) tuning to save storage
[Structured logging with Filebeat | Elastic](https://www.elastic.co/blog/structured-logging-filebeat)

### Index template

Each beat should have a corresponding template for index creation, see `elastic-elasticsearch#index-creation-mapping`.
Elasticsearch can auto detect the schema but we can be more specific by adding the index template specific to the beat.

```sh
# get all indices
http -b http://elasticsearch:9200/_cat/indices?pretty
# get all index templates
http -b http://elasticsearch:9200/_template?pretty

curl -XPUT 'http://elasticsearch:9200/_template/filebeat' -d@filebeat/filebeat.template.json
curl -XPUT 'http://elasticsearch:9200/_template/dockbeat' -d@dockbeat/dockbeat.template.json
```

### Official beats

[elastic/beats: Beats - Lightweight shippers for Elasticsearch & Logstash](https://github.com/elastic/beats)

[Filebeat | Elastic](https://www.elastic.co/products/beats/filebeat) !important
[Filebeat Reference | Elastic](https://www.elastic.co/guide/en/beats/filebeat/current/index.html)
[beats/filebeat at master · elastic/beats](https://github.com/elastic/beats/tree/master/filebeat)
[Filebeat vs. Logstash -- The Evolution of a Log Shipper - Logz.io](https://logz.io/blog/filebeat-vs-logstash/)

[Metricbeat | Elastic](https://www.elastic.co/downloads/beats/metricbeat)
[Metricbeat Reference | Elastic](https://www.elastic.co/guide/en/beats/metricbeat/current/index.html)
[beats/metricbeat at master · elastic/beats](https://github.com/elastic/beats/tree/master/metricbeat)

[Packetbeat | Elastic](https://www.elastic.co/products/beats/packetbeat)
[Packetbeat Reference | Elastic](https://www.elastic.co/guide/en/beats/packetbeat/current/index.html)
[beats/packetbeat at master · elastic/beats](https://github.com/elastic/beats/tree/master/packetbeat)

[Topbeat | Elastic](https://www.elastic.co/products/beats/topbeat) (legacy)
[Topbeat Reference | Elastic](https://www.elastic.co/guide/en/beats/topbeat/current/index.html)

### Community Beats

[Community Beats | Beats Platform Reference | Elastic](https://www.elastic.co/guide/en/beats/libbeat/master/community-beats.html)

[Ingensi/dockbeat: Dockbeat - the elastic Beat for docker daemon monitoring](https://github.com/Ingensi/dockbeat)
[YaSuenag/hsbeat: Beat for Java HotSpot VM](https://github.com/YaSuenag/hsbeat)
[PhaedrusTheGreek/nagioscheckbeat: An Elastic Beat for all the Nagios checks](https://github.com/PhaedrusTheGreek/nagioscheckbeat)
[christiangalsterer/httpbeat: Elastic Beat to call HTTP endpoints](https://github.com/christiangalsterer/httpbeat) different from Logstash's `http_poller` as this works in local LAN and push to Logstash
[mheese/journalbeat: Journalbeat is a log shipper from systemd/journald to Logstash/Elasticsearch](https://github.com/mheese/journalbeat)
