---
title: Remote Procedure Call
categories:
  - comp.lang
tags:
  - rpc
  - web-dev
toc: true
date: 2018-08-02 12:02:00
---

# RPC

[Remote procedure call - Wikiwand](http://www.wikiwand.com/en/Remote_procedure_call)
Usually an interface description language ([IDL](#idl)) is used to define the data sent over the wire. The IDL that can usually generate bindings for multiple languages.

Message queues can be used for RPC calls.

> see `message-queue.md`

## zerorpc

[zerorpc](http://www.zerorpc.io/) MessagePack + ZeroMQ
[zerorpc](https://github.com/0rpc) Org

## gRPC

[grpc - grpc.io](http://www.grpc.io/)
[gRPC - Wikiwand](https://www.wikiwand.com/en/GRPC)
[grpc](https://github.com/grpc) Org
A high performance, open source, general RPC framework that puts mobile and HTTP/2 first.

[Take a REST with HTTP-2, Protobufs, and Swaggerquay](https://coreos.com/blog/gRPC-protobufs-swagger.html)
[Google's gRPC: A Lean and Mean Communication Protocol for Microservices - The New Stack](https://thenewstack.io/grpc-lean-mean-communication-protocol-microservices/)

[Intro to gRPC: A Modern Toolkit for Microservice Communication - YouTube](https://www.youtube.com/watch?v=RoXT_Rkg8LA)
[Exploring The gRPC Framework for Building Microservices | Nordic APIs |](https://nordicapis.com/exploring-the-grpc-framework-for-building-microservices/)

[Effectively communicate between Microservices – ITNEXT](https://itnext.io/effectively-communicate-between-microservices-de7252ba2f3c) TL;DR: Use gRPC
[Tensorflow serving: REST vs gRPC – Avidan Eran – Medium](https://medium.com/@avidaneran/tensorflow-serving-rest-vs-grpc-e8cef9d4ff62) REST is faster for small data payload

[bradleyjkemp/grpc-tools: A suite of gRPC debugging tools. Like Fiddler/Charles but for gRPC.](https://github.com/bradleyjkemp/grpc-tools)

[Introducing gRPC Support with NGINX 1.13.10 - NGINX](https://www.nginx.com/blog/nginx-1-13-10-grpc)

### Web

[grpc/grpc-web: gRPC for Web Clients](https://github.com/grpc/grpc-web)
[gRPC-Web: Moving past REST+JSON towards type-safe Web APIs - Improbable](https://improbable.io/games/blog/grpc-web-moving-past-restjson-towards-type-safe-web-apis)
[gRPC-Web is going GA - Cloud Native Computing Foundation](https://www.cncf.io/blog/2018/10/24/grpc-web-is-going-ga/)

[grpc-ecosystem/grpc-gateway: gRPC to JSON proxy generator following the gRPC HTTP spec](https://github.com/grpc-ecosystem/grpc-gateway)

[How to use gRPC-web with React – freeCodeCamp.org](https://medium.freecodecamp.org/how-to-use-grpc-web-with-react-1c93feb691b5)

### Go

[Implementing gRPC service in Golang – Kurio Toolbox](https://toolbox.kurio.co.id/implementing-grpc-service-in-golang-afb9e05c0064)
[[Tutorial, Part 1] How to develop Go gRPC microservice with HTTP/REST endpoint, middleware…](https://medium.com/@amsokol.com/tutorial-how-to-develop-go-grpc-microservice-with-http-rest-endpoint-middleware-kubernetes-daebb36a97e9)
[[Tutorial, Part 2] How to develop Go gRPC microservice with HTTP/REST endpoint, middleware…](https://medium.com/@amsokol.com/tutorial-how-to-develop-go-grpc-microservice-with-http-rest-endpoint-middleware-kubernetes-af1fff81aeb2)
[[Tutorial, Part 3] How to develop Go gRPC microservice with HTTP/REST endpoint, middleware…](https://medium.com/@amsokol.com/tutorial-part-3-how-to-develop-go-grpc-microservice-with-http-rest-endpoint-middleware-739aac8f1d7e)

### Node

[Building gRPC Service Server Note CRUD API with node.js](https://medium.com/@alfianlosari/building-grpc-service-server-note-crud-api-with-node-js-bcc5478d5bdb)

## RSocket

[RSocket](http://rsocket.io/)
[RPC Thunder Dome – Netifi – Medium](https://medium.com/netifi/rpc-thunder-dome-3103e2449957)
[Give REST a Rest with RSocket](https://www.infoq.com/articles/give-rest-a-rest-rsocket)

[RSocket: Reactive Streaming Service Networking with Ryland Degnan - Software Engineering Daily](https://softwareengineeringdaily.com/2019/01/22/rsocket-reactive-streaming-service-networking-with-ryland-degnan/)

## Scuttlebutt

[Secure Scuttlebutt Consortium](https://github.com/ssbc)
[The definitive guide to Secure Scuttlebutt – clebertech-en – Medium](https://medium.com/clebertech-en/the-definitive-guide-to-secure-scuttlebutt-a1b3a3fd73f6)
[Secure Scuttlebutt - Scuttlebot](http://scuttlebot.io/more/protocols/secure-scuttlebutt.html)
[Scuttlebutt Protocol Guide](https://ssbc.github.io/scuttlebutt-protocol-guide/index.html)
[ssbc/scuttlebutt-guide: A collection of links to known resources!](https://github.com/ssbc/scuttlebutt-guide)

[Scuttlebutt · GitBook](https://www.scuttlebutt.nz/) Patchwork client

Patchwork is a user interface for displaying messages from the distributed database (Scuttlebot) to the user, and to allow the user to add new messages. The underlying protocol supports arbitrary message types, Patchwork exposes a UI for interacting with a subset of them. Anyone could write and use other UIs while still contributing to the same database. [Patchbay](https://github.com/ssbc/patchbay) for example is a more developer-centric frontend.

[Scuttlebot peer-to-peer log store](http://scuttlebot.io/) used as a database, identity provider, and messaging system
[dominictarr/sbot-web](https://github.com/dominictarr/sbot-web)

## TARS

[TARS,rpc framework by tencent](https://tars.tencent.com/base/tars_index/en/index.html)
[TarsCloud/Tars: Tars is a highly performance rpc framework based on naming service using tars protocol and provides a semi-automatic operation platform.](https://github.com/TarsCloud/Tars)

## Dubbo

RPC framework created by Alibaba.

[DUBBO](http://dubbo.io/)
[dubbo (@dubbo) on GitBook · GitBook](https://www.gitbook.com/@dubbo)

[alibaba/dubbo: Dubbo is a high-performance, java based, open source RPC framework](https://github.com/alibaba/dubbo)

## ICE

> GPLv2

[Internet Communications Engine - Wikiwand](https://www.wikiwand.com/en/Internet_Communications_Engine)
[ZeroC - Network Your Software](https://zeroc.com/)

## JSON-RPC

[JSON-RPC](https://www.jsonrpc.org/)
[simple is better - JSON-RPC](http://www.simple-is-better.org/rpc/index.html)

---

# IDL

> TODO: merge `Dropbox/caravan/caravan/interchange-format`

## Protocol Buffers

[Protocol Buffers  |  Google Developers](https://developers.google.com/protocol-buffers/)
[Protocol Buffers - Wikiwand](https://www.wikiwand.com/en/Protocol_Buffers)

[Protocol Buffers, Part 1 — Serialization Library for Microservices](https://codeburst.io/protocol-buffers-part-1-serialization-library-for-microservices-37418e72908b)
[Protocol Buffers, Part 2 — The Untold Parts Of Using “Any”](https://codeburst.io/protocol-buffers-part-2-the-untold-parts-of-using-any-6a328560048d)

## MessagePack

## Thrift

[Apache Thrift - Home](https://thrift.apache.org/)
