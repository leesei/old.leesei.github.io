---
title: Web Deployment
categories:
  - web
tags:
  - web-deploy
toc: true
date: 2016-02-05 13:42:41
---

[毛記電視網站是怎樣練成的？| Gap 撈 Tech](http://blog.gaplotech.com/how-tvmost-is-built/)
[tech@TVB – Medium](https://medium.com/techattvb)
[知乎已读服务架构如何实现高可用、高扩展、去并发？](https://www.infoq.cn/article/1jFqOKBkgCY5W*F30lzq)
[蚂蚁金服面对亿级并发场景的组件体系设计](https://www.infoq.cn/article/VTXJgETSN9IkxTqi-uiQ)
[This is My Architecture - YouTube](https://www.youtube.com/playlist?list=PLhr1KZpdzukdeX8mQ2qO73bg6UKQHYsHb)

[Concurrent Programming for Scalable Web Architectures](http://berb.github.io/diploma-thesis/index.html)
[The Architecture of Open Source Applications (Volume 2): Scalable Web Architecture and Distributed Systems](http://aosabook.org/en/distsys.html)

> see `web-reverse-proxy`

## Simple HTTP server

[Big list of http static server one-liners](https://gist.github.com/willurd/5720255)

[m3ng9i/ran: a simple static web server written in Go](https://github.com/m3ng9i/ran)
[TheWaWaR/simple-http-server: Simple http server in Rust (Windows/Mac/Linux)](https://github.com/TheWaWaR/simple-http-server)
[Caddy - The HTTP/2 Web Server with Automatic HTTPS](https://caddyserver.com/)

[Fenix Web Server | Static Web Servers for the Desktop](https://fenixwebserver.com/)
[live-server - npm](https://www.npmjs.com/package/live-server)

[TinyWeb Server on Windows](https://ccm.net/faq/2568-tinyweb-server-on-windows)

## Firewall Transversal

[ngrok - secure introspectable tunnels to localhost](https://ngrok.com/)

## Benchmarking

[ab - Apache HTTP server benchmarking tool - Apache HTTP Server](https://httpd.apache.org/docs/current/programs/ab.html)
Use `ab -k` (keepalive) to avoid testing connections (kernel responsibility)
[Simultaneously benchmark many URLs with ApacheBench and GNU parallel · Simon Holywell](https://www.simonholywell.com/post/2015/06/parallel-benchmark-many-urls-with-apachebench/)

[brianfrankcooper/YCSB: Yahoo! Cloud Serving Benchmark](https://github.com/brianfrankcooper/YCSB)

[wg/wrk: Modern HTTP benchmarking tool](https://github.com/wg/wrk)
[giltene/wrk2: A constant throughput, correct latency recording variant of wrk](https://github.com/giltene/wrk2)
[rakyll/hey: HTTP load generator, ApacheBench (ab) replacement, formerly known as rakyll/boom](https://github.com/rakyll/hey)

[k6.io - Performance testing for developers, like unit-testing, for performance](https://k6.io/)

[Stresstests with Gatling by Niko Köbler - YouTube](https://www.youtube.com/watch?v=gOZvtBYzIVc)
[Stéphane Landelle - Load Testing Done Right with Gatling - YouTube](https://www.youtube.com/watch?v=VUPTaPms210)

[Siege Home](https://www.joedog.org/siege-home/)

[Locust - A modern load testing framework](https://locust.io/) in Python

[mcollina/autocannon: fast HTTP/1.1 benchmarking tool written in Node.js](https://github.com/mcollina/autocannon)
[alexfernandez/loadtest: Runs a load test on the selected URL. Easy to extend minimally for your own ends.](https://github.com/alexfernandez/loadtest)

[SmokePing - About SmokePing](http://oss.oetiker.ch/smokeping/index.en.html)
[Smokeping on Nginx](http://tomoconnor.eu/blogish/smokeping-nginx/#.VvbNZGF96_5)

### Gatling

[Gatling Project, Stress Tool](http://gatling.io/#/)
[Gatling Load and Performance testing - Open-source load and performance testing](https://gatling.io/docs/current/)
[52-technologies-in-2016/10-gatling](https://github.com/shekhargulati/52-technologies-in-2016/blob/master/10-gatling/README.md)

```scala
import io.gatling.core.Predef._
import io.gatling.http.Predef._
import scala.concurrent.duration._

class ParameterizedSimulation extends Simulation {
  val url = System.getenv("GATLING_URL")
  val requests = Integer.parseInt(System.getenv("GATLING_REQUESTS"))
  val users = Integer.parseInt(System.getenv("GATLING_USERS"))
  val reqs_per_user = requests / users
  val rampTime = Integer.parseInt(System.getenv("GATLING_RAMP_TIME"))
  val scn = scenario("My scenario").repeat(reqs_per_user) {
    exec(
      http("Dinosaur")
        .get(url)
        .check(status.in(Seq(200,304)))
    )
  }

  setUp(scn.inject(rampUsers(users) over (rampTime seconds)))
}
```

```sh
./gatling.sh -s <class> -on <result-basename> -rd <description>
```

## Storage

[Object Storage versus Block Storage: Understanding the Technology Differences - Druva](http://www.druva.com/blog/object-storage-versus-block-storage-understanding-technology-differences/)
[Block vs. file storage to support virtual server environments - Storage Technology Magazine](http://searchstorage.techtarget.com/magazineContent/Block-vs-file-storage-to-support-virtual-server-environments)
[How an object store differs from file and block storage](http://searchcloudstorage.techtarget.com/feature/How-an-object-store-differs-from-file-and-block-storage)

## ops stuff

> `~/caravan/devops`, `devops.md`
