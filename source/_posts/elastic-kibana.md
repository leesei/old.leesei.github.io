---
title: Elastic Stack
categories:
  - web
toc: true
date: 2015-08-03 13:22:02
tags:
  - database
  - visualization
  - elastic-stack
---

## Kibana

[Kibana: Explore, Visualize, Discover Data | Elastic](https://www.elastic.co/products/kibana)
[Kibana User Guide | Elastic](https://www.elastic.co/guide/en/kibana/current/index.html)
[Elasticsearch Graph | Elastic](https://www.elastic.co/guide/en/graph/current/index.html)
[elastic/kibana: Kibana analytics and search dashboard for Elasticsearch](https://github.com/elastic/kibana)

Visualizations are saved as Panels, a Dashboard is comprised of Panels.

[Importing Existing Beat Dashboards | Beats Platform Reference | Elastic](https://www.elastic.co/guide/en/beats/libbeat/current/import-dashboards.html)

[Tag that Cloud | Elastic](https://www.elastic.co/blog/tag-that-cloud-a-new-visualization-in-kibana) 5.1
[New Kibana Visualizations: Heatmap and Point Series | Elastic](https://www.elastic.co/blog/awesome-new-kibana-visualizations-heatmap-and-point-series) 5.4
[Kibana under the hood: object persistence | Elastic](https://www.elastic.co/blog/kibana-under-the-hood-object-persistence)

[Sense](https://www.elastic.co/guide/en/sense/current/index.html) is an interactive UI for Elastic search. It was ported as [Console Plugin](https://www.elastic.co/guide/en/kibana/5.0/console-kibana.html) in Kibana 5 and later integrated as part of Kibana.

[sivasamyk/logtrail: Kibana plugin to view, search & live tail log events](https://github.com/sivasamyk/logtrail)
[wardviaene/kibana-logtrail - Docker Hub](https://hub.docker.com/r/wardviaene/kibana-logtrail/)

[Creating Custom Kibana Visualizations: A How-To Guide](https://logz.io/blog/kibana-visualizations/)
[Componentizing the Kibana UI, part 1: CSS that Scales | Elastic](https://www.elastic.co/blog/componentizing-the-kibana-ui-css-that-scales)
[Componentizing the Kibana UI, part 2: JavaScript with React | Elastic](https://www.elastic.co/blog/componentizing-the-kibana-ui-writing-javascript-with-react)
[Thousands of Color-coded Visualizations in React | Elastic](https://www.elastic.co/blog/color-coded-visualizations-react)

[How To Use Kibana Dashboards and Visualizations | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-kibana-dashboards-and-visualizations)

### Internals

[Kibana under the hood: object persistence | Elastic](https://www.elastic.co/blog/kibana-under-the-hood-object-persistence)

[kibana create index pattern api - Google Search](https://www.google.com.hk/search?newwindow=1&q=kibana+create+index+pattern+api&oq=kibana+add+index+pattern+curl&gs_l=psy-ab.3.1.0i71k1l4.0.0.0.3975.0.0.0.0.0.0.0.0..0.0....0...1..64.psy-ab..0.0.0.Df3C3GI4j1g)
[Create Indices pattern through commnadline - Kibana - Discuss the Elastic Stack](https://discuss.elastic.co/t/create-indices-pattern-through-commnadline/54180)

### Timeseries

[Timelion: The time series composer for Kibana | Elastic](https://www.elastic.co/blog/timelion-timeline)
[Computation near the visualization layer | Elastic](https://www.elastic.co/blog/computation-near-the-visualization-layer)
[Normalizing sparse time series with Timelion | Elastic](https://www.elastic.co/blog/sparse-timeseries-and-timelion)
[Getting Started with Time Series Analysis in Kibana | Elastic](https://www.elastic.co/blog/timelion-tutorial-from-zero-to-hero)
[Kibana Time Series Visual Builder | Elastic](https://www.elastic.co/blog/master-time-with-kibanas-new-time-series-visual-builder)
[Kibana's New Time Series Visual Builder - Part 2 | Elastic](https://www.elastic.co/blog/kibanas-new-time-series-visual-builder-part-2)
[Mining Earthquake Data with Kibana 5 and Timelion | Elastic](https://www.elastic.co/blog/mining-earthquake-data-with-kibana-5-and-timelion)

### Index pattern

We have to register index pattern in Kibana before we can visualize it.
We do this by directly adding to the `.kibana` index in Elasticsearch.
[Index pattern creation API · Issue #3709 · elastic/kibana](https://github.com/elastic/kibana/issues/3709#issuecomment-324877479)
[Load dashboards from filesystem · Issue #2310 · elastic/kibana](https://github.com/elastic/kibana/issues/2310)
[Create an Ingest API by Bargs · Pull Request #5213 · elastic/kibana](https://github.com/elastic/kibana/pull/5213)

```sh
http -b http://elasticsearch:9200/.kibana/index-pattern

curl -XPOST -H 'Content-Type: application/json' 'http://elasticsearch:9200/.kibana/index-pattern/filebeat-*' -d'{"title":"filebeat-*","timeFieldName":"@timestamp","notExpandable":true}'

http --print HhBb POST "http://elasticsearch:9200/.kibana/index-pattern/dockbeat-*" << EOF
{"title":"dockbeat-*","timeFieldName":"@timestamp","notExpandable":true}
EOF
```

For kibana 6.0 using curl and jq:

```sh
url="http://localhost:5601"
index_pattern="logstash-*"
time_field="@timestamp"
# Create index pattern and get the created id
# curl -f to fail on error
id=$(curl -f -XPOST -H "Content-Type: application/json" -H "kbn-xsrf: anything" \
  "$url/api/saved_objects/index-pattern" \
  -d"{\"attributes\":{\"title\":\"$index_pattern\",\"timeFieldName\":\"$time_field\"}}" \
  | jq -r '.id')
# Create the default index
curl -XPOST -H "Content-Type: application/json" -H "kbn-xsrf: anything" \
  "$url/api/kibana/settings/defaultIndex" \
  -d"{\"value\":\"$id\"}"
```

## Alternative

[Reactivesearch - React and React Native UI components for Elasticsearch](https://opensource.appbase.io/reactivesearch/)
[Reactive Manual - React components for building Search UIs](https://opensource.appbase.io/reactive-manual/)
[How to Build an E-commerce Search UI with React and Elasticsearch](https://codeburst.io/how-to-build-an-e-commerce-search-ui-with-react-and-elasticsearch-a581c823b2c3)
[Components - InnerSearch : Vue.js components for ElasticSearch](https://innersearch.github.io/vue-innersearch/#/)
