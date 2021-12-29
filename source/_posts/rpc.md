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
> nanomsg and zeromq's REQREP can also be used for RPC

## zerorpc

[zerorpc](http://www.zerorpc.io/) MessagePack + ZeroMQ
[zerorpc](https://github.com/0rpc) Org
[Build reliable, traceable, distributed systems with ZeroMQ - YouTube](https://www.youtube.com/watch?v=9G6-GksU7Ko)

## gRPC

[grpc - grpc.io](https://www.grpc.io/)
[Guides | gRPC](https://grpc.io/docs/guides/)
[grpc/CONCEPTS.md at master · grpc/grpc](https://github.com/grpc/grpc/blob/master/CONCEPTS.md)

[grpc](https://github.com/grpc) Org
[gRPC - Wikiwand](https://www.wikiwand.com/en/GRPC)
A high performance, open source, general RPC framework that puts mobile and HTTP/2 first.

[gRPC vs REST: Understanding gRPC, OpenAPI and REST and when to use them in API design | Google Cloud Blog](https://cloud.google.com/blog/products/api-management/understanding-grpc-openapi-and-rest-and-when-to-use-them)
[Take a REST with HTTP-2, Protobufs, and Swaggerquay](https://coreos.com/blog/gRPC-protobufs-swagger.html)
[Google's gRPC: A Lean and Mean Communication Protocol for Microservices - The New Stack](https://thenewstack.io/grpc-lean-mean-communication-protocol-microservices/)
[Heres why you should use gRPC for everything » André Snede Kock](https://snede.net/heres-why-you-should-use-grpc-for-everything/)

[gRPC Crash Course - Modes, Examples, Pros & Cons and more - YouTube](https://www.youtube.com/watch?v=Yw4rkaTc0f8) Node.js
[Intro to gRPC: A Modern Toolkit for Microservice Communication - YouTube](https://www.youtube.com/watch?v=RoXT_Rkg8LA)
[Introduction to gRPC: A general RPC framework that puts mobile and HTTP/2 first (M.Atamel, R.Tsang) - YouTube](https://www.youtube.com/watch?v=hNFM2pDGwKI)
[Exploring The gRPC Framework for Building Microservices | Nordic APIs |](https://nordicapis.com/exploring-the-grpc-framework-for-building-microservices/)

[Effectively communicate between Microservices – ITNEXT](https://itnext.io/effectively-communicate-between-microservices-de7252ba2f3c) TL;DR: Use gRPC
[Tensorflow serving: REST vs gRPC – Avidan Eran – Medium](https://medium.com/@avidaneran/tensorflow-serving-rest-vs-grpc-e8cef9d4ff62) REST is faster for small data payload

[hyperium/tonic: A native gRPC client & server implementation with async/await support.](https://github.com/hyperium/tonic)
[Introducing gRPC Support with NGINX 1.13.10 - NGINX](https://www.nginx.com/blog/nginx-1-13-10-grpc)

### Tips and tricks

[bradleyjkemp/grpc-tools: A suite of gRPC debugging tools. Like Fiddler/Charles but for gRPC.](https://github.com/bradleyjkemp/grpc-tools)

[Using gRPC in Production -- connection keepalive | Meng Xuan Xia](https://cs.mcgill.ca/~mxia3/2019/02/23/Using-gRPC-in-Production/)
[Enabling connection keepalive? · Issue #154 · grpc/grpc-node](https://github.com/grpc/grpc-node/issues/154)
[How to test keepalive options? · Issue #706 · grpc/grpc-node](https://github.com/grpc/grpc-node/issues/706)

### Container

[Moving k8s communication to gRPC](https://blog.cloudflare.com/moving-k8s-communication-to-grpc/)
[Load-balancing a gRPC service using Docker](https://www.useanvil.com/blog/engineering/grpc-load-balancing/)

### Web

[grpc/grpc-web: gRPC for Web Clients](https://github.com/grpc/grpc-web)
[gRPC-Web: Moving past REST+JSON towards type-safe Web APIs - Improbable](https://improbable.io/games/blog/grpc-web-moving-past-restjson-towards-type-safe-web-apis)
[gRPC-Web is going GA - Cloud Native Computing Foundation](https://www.cncf.io/blog/2018/10/24/grpc-web-is-going-ga/)
[gRPC-Web for .NET now available | ASP.NET Blog](https://devblogs.microsoft.com/aspnet/grpc-web-for-net-now-available/)
[Microsoft Releases gRPC-Web for .NET](https://www.infoq.com/news/2020/06/microsoft-releases-grpc-web-net/)

[grpc-ecosystem/grpc-gateway: gRPC to JSON proxy generator following the gRPC HTTP spec](https://github.com/grpc-ecosystem/grpc-gateway)

[How to use gRPC-web with React – freeCodeCamp.org](https://medium.freecodecamp.org/how-to-use-grpc-web-with-react-1c93feb691b5)
[Ditching REST with gRPC-web and Envoy - The Startup - Medium](https://medium.com/swlh/ditching-rest-with-grpc-web-and-envoy-bfaa89a39b32)

### Go

[Go | gRPC](https://www.grpc.io/docs/languages/go/)
[grpc/grpc-go: The Go language implementation of gRPC. HTTP/2 based RPC](https://github.com/grpc/grpc-go)
[grpc package - google.golang.org/grpc - pkg.go.dev](https://pkg.go.dev/google.golang.org/grpc)

[Implementing gRPC service in Golang – Kurio Toolbox](https://toolbox.kurio.co.id/implementing-grpc-service-in-golang-afb9e05c0064)
[[Tutorial, Part 1] How to develop Go gRPC microservice with HTTP/REST endpoint, middleware…](https://medium.com/@amsokol.com/tutorial-how-to-develop-go-grpc-microservice-with-http-rest-endpoint-middleware-kubernetes-daebb36a97e9)
[[Tutorial, Part 2] How to develop Go gRPC microservice with HTTP/REST endpoint, middleware…](https://medium.com/@amsokol.com/tutorial-how-to-develop-go-grpc-microservice-with-http-rest-endpoint-middleware-kubernetes-af1fff81aeb2)
[[Tutorial, Part 3] How to develop Go gRPC microservice with HTTP/REST endpoint, middleware…](https://medium.com/@amsokol.com/tutorial-part-3-how-to-develop-go-grpc-microservice-with-http-rest-endpoint-middleware-739aac8f1d7e)

[Python and Go : Part I - gRPC](https://www.ardanlabs.com/blog/2020/06/python-go-grpc.html)
[Python and Go : Part II - Extending Python With Go](https://www.ardanlabs.com/blog/2020/07/extending-python-with-go.html)
[Python and Go : Part III - Packaging Python Code](https://www.ardanlabs.com/blog/2020/08/packaging-python-code.html)
[Python and Go : Part IV - Using Python in Memory](https://www.ardanlabs.com/blog/2020/09/using-python-memory.html)

### Python

[Python | gRPC](https://www.grpc.io/docs/languages/python/quickstart/)
[Welcome to gRPC Python’s documentation! — gRPC Python documentation](https://grpc.github.io/grpc/python/)

[Implementing gRPC server using Python - Towards Data Science](https://towardsdatascience.com/implementing-grpc-server-using-python-9dc42e8daea0)
[Python Microservices With gRPC – Real Python](https://realpython.com/python-microservices-grpc/)

### Node

[Node | gRPC](https://www.grpc.io/docs/languages/node/)
[grpc/grpc-node: gRPC for Node.js](https://github.com/grpc/grpc-node)
[Documentation Namespace: grpc](https://grpc.github.io/grpc/node/grpc.html)

[grpc/examples/node · grpc/grpc](https://github.com/grpc/grpc/tree/master/examples/node)
[badsyntax/grpc-js-typescript: Generate gRPC TypeScript definitions for use with gRPC (@grpc/grpc-js).](https://github.com/badsyntax/grpc-js-typescript)

[carlessistare/grpc-promise: GRPC promisify module for all Request/Response types: standard and stream](https://github.com/carlessistare/grpc-promise)
[nicolaspearson/grpc.boom: A gRPC implementation of the awesome Boom library to help create gRPC-friendly error objects](https://github.com/nicolaspearson/grpc.boom)

[Building gRPC Service Server Note CRUD API with node.js](https://medium.com/@alfianlosari/building-grpc-service-server-note-crud-api-with-node-js-bcc5478d5bdb)

### C#

[C# | gRPC](https://www.grpc.io/docs/languages/csharp/)
[grpc/grpc-dotnet: gRPC for .NET](https://github.com/grpc/grpc-dotnet)
[Namespace Grpc.Core | gRPC for .NET](https://grpc.github.io/grpc/csharp-dotnet/api/Grpc.Core)

[The future of gRPC in C# belongs to grpc-dotnet | gRPC](https://www.grpc.io/blog/grpc-csharp-future/)
[Introduction to gRPC on .NET | Microsoft Docs](https://docs.microsoft.com/en-us/aspnet/core/grpc/)
[Create a .NET Core gRPC client and server in ASP.NET Core | Microsoft Docs](https://docs.microsoft.com/en-us/aspnet/core/tutorials/grpc/grpc-start?view=aspnetcore-5.0&tabs=visual-studio)

### Rust

[hyperium/tonic: A native gRPC client & server implementation with async/await support.](https://github.com/hyperium/tonic)

## RSocket

[RSocket](http://rsocket.io/)
[RPC Thunder Dome – Netifi – Medium](https://medium.com/netifi/rpc-thunder-dome-3103e2449957)
[Give REST a Rest with RSocket](https://www.infoq.com/articles/give-rest-a-rest-rsocket)

[Differences between gRPC and RSocket - Netifi - Medium](https://medium.com/netifi/differences-between-grpc-and-rsocket-e736c954e60)

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

## SOAP

[SOAP - Wikiwand](https://www.wikiwand.com/en/SOAP)
[How to Perform SOAP Requests With Node.js - Better Programming - Medium](https://medium.com/better-programming/how-to-perform-soap-requests-with-node-js-4a9627070eb6)
