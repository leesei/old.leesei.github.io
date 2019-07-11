---
title: Web Push Technologies
categories:
  - web
tags:
  - web-socket
  - server-send-event
toc: true
date: 2019-03-04 23:25:13
---

[Push technology - Wikiwand](https://www.wikiwand.com/en/Push_technology#/Long_polling)
[php - What are Long-Polling, Websockets, Server-Sent Events (SSE) and Comet? - Stack Overflow](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

> see `rpc.md#grpc`

---

# Web Socket

A persistent connection between the client and the server and both parties can start sending data at any time.

[websocket.org - Powered by Kaazing](https://www.websocket.org/)
[HTML5 WebSocket - A Quantum Leap in Scalability for the Web](http://websocket.org/quantum.html)
[About HTML5 WebSocket - Powered by Kaazing](https://www.websocket.org/aboutwebsocket.html)

[RFC 6455 - The WebSocket Protocol](https://tools.ietf.org/html/rfc6455)
[WebSockets - A Conceptual Deep-Dive | Ably Realtime](https://www.ably.io/concepts/websockets)
[WebSockets - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
[Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/#feat=websockets)

[facundofarias/awesome-websockets: A curated list of Websocket libraries and resources.](https://github.com/facundofarias/awesome-websockets)
[Introduction to WebSockets](https://flaviocopes.com/websockets/)
[Introducing WebSockets: Bringing Sockets to the Web - HTML5 Rocks](https://www.html5rocks.com/en/tutorials/websockets/basics/)
[An Introduction to WebSockets - Treehouse Blog](https://blog.teamtreehouse.com/an-introduction-to-websockets)
[Developing Real-Time Web Applications with Server-Sent EventsButton - CloseLearn More](https://auth0.com/blog/developing-real-time-web-applications-with-server-sent-events/)

[Implementing a WebSocket Server with Node.js – Hacker Noon](https://hackernoon.com/implementing-a-websocket-server-with-node-js-d9b78ec5ffa8) from scratch
[Node.js & WebSocket — Simple chat tutorial – Martin Sikora – Medium](https://medium.com/@martin.sikora/node-js-websocket-simple-chat-tutorial-2def3a841b61)

[NodeUp: fortytwo - a scaling websockets show](http://nodeup.com/fortytwo)

## Kalm

[Kalm - The socket manager](http://kalm.js.org/)
[kalm/kalm.js: The socket manager](https://github.com/kalm/kalm.js)

## Server

[8 Node.js Web Socket Libraries For 2018 – Bits and Pieces](https://blog.bitsrc.io/8-node-js-web-socket-libraries-for-2018-818e7e5b67cf)

[websockets/ws: Simple to use, blazing fast and thoroughly tested WebSocket client and server for Node.js](https://github.com/websockets/ws)
[How to Build a Chat Application using React, Redux, Redux-Saga, and Web Sockets](https://medium.freecodecamp.org/how-to-build-a-chat-application-using-react-redux-redux-saga-and-web-sockets-47423e4bc21a)

[uNetworking/uWebSockets.js: TypeScript web server - 15x faster than Deno](https://github.com/uNetworking/uWebSockets.js)
[hugmanrique/turbo-ws: Blazing fast low-level WebSocket server](https://github.com/hugmanrique/turbo-ws)
[primus/primus: Primus, the creator god of the transformers & an abstraction layer for real-time to prevent module lock-in.](https://github.com/primus/primus)

[Building a chat application with Spring Boot and WebSocket | CalliCoder](https://www.callicoder.com/spring-boot-websocket-chat-example/)

## HTTP server integration

```js
const server = new Hapi.Server();
const app = require("http").createServer(handler);
// `server.listener` is equivalent to `app`
```

## WAMP

[Web Application Messaging Protocol - Wikiwand](https://www.wikiwand.com/en/Web_Application_Messaging_Protocol) MessagePack/JSON over WebSocket
[The Web Application Messaging Protocol — Web Application Messaging Protocol version 2 documentation](https://wamp-proto.org/)

[Introduction to WAMP, a protocol enabling PUB/SUB and RPC over Websoc…](https://www.slideshare.net/sametmax/intro-wamp)

[Crossbar.io](https://crossbar.io/) Server
[Crossbar.io - autobahn](https://crossbar.io/autobahn/) Client

## Socket.io

[Socket.IO](https://socket.io/)
[WebSocket and Socket.IO](https://davidwalsh.name/websocket)
[Beyond REST: Using WebSockets for two-way communication in your React app](https://blog.logrocket.com/beyond-rest-using-websockets-for-two-way-communication-in-your-react-app-884eff6655f5)
[Using hapi.js with Socket.io](http://matt-harrison.com/using-hapi-js-with-socket-io/)
[WebSocket + Node.js + Express — Step by step using Typescript](https://medium.com/factory-mind/websocket-node-js-express-step-by-step-using-typescript-725114ad5fe4)

[Node.js: Better Performance With Socket.IO and doT](https://code.tutsplus.com/tutorials/nodejs-better-performance-with-socketio-and-dot--net-35076)
[Understanding Socket.IO - NodeSource](https://nodesource.com/blog/understanding-socketio)
[StrongLoop - Real-time Engines in Node.js](https://strongloop.com/strongblog/real-time-engines-in-node-js/)
[Adding Socket.io to multi-threaded Node.js – freeCodeCamp.org](https://medium.freecodecamp.org/how-to-add-socket-io-to-multi-threaded-node-js-df404b424276)

### On the contrary

[Why you don’t need Socket.IO – codeburst](https://codeburst.io/why-you-don-t-need-socket-io-6848f1c871cd) 2016
[node.js - Differences between socket.io and websockets - Stack Overflow](https://stackoverflow.com/questions/10112178/differences-between-socket-io-and-websockets/38558531#38558531)

## Sock.js

[sockjs/sockjs-client: WebSocket emulation - Javascript client](https://github.com/sockjs/sockjs-client)
[sockjs/sockjs-node: WebSocket emulation - Node.js server](https://github.com/sockjs/sockjs-node)
[substack/shoe: streaming sockjs for node and the browser](https://github.com/substack/shoe)

[WebSockets in React, the component way! – Practo Engineering – Medium](https://medium.com/practo-engineering/websockets-in-react-the-component-way-368730334eef)

## Authentication

[javascript - Web Socket connection with Basic Access Authentication - Stack Overflow](https://stackoverflow.com/questions/46998781/web-socket-connection-with-basic-access-authentication)
[Securing WebSocket using wss and HTTPS/TLS (Tech Tip #50)](http://blog.arungupta.me/securing-websocket-wss-https-tls-techtip50/)
[Securing WebSockets using Username/Password and Servlet Security (Tech Tip #49)](http://blog.arungupta.me/securing-websockets-username-password-servlet-security-techtip49/)

## Scaling

[SocketCluster](https://socketcluster.io/#!/) scalable server implementation
[observing/balancerbattle: WebSocket loadbalancer battle](https://github.com/observing/balancerbattle)

[ClusterWS](https://clusterws.github.io/)
[ClusterWS/ClusterWS: Lightweight, fast and powerful framework for building scalable WebSocket applications in Node.js.](https://github.com/ClusterWS/ClusterWS)

[Scaling WebSockets – Hacker Noon](https://hackernoon.com/scaling-websockets-9a31497af051)
[Scaling Node.js Socket Server with Nginx and Redis | Jscrambler Blog](https://blog.jscrambler.com/scaling-node-js-socket-server-with-nginx-and-redis/)
[Horizontally Scaling Node.js and WebSockets with Redis - GoldFire Studios](https://goldfirestudios.com/blog/136/Horizontally-Scaling-Node.js-and-WebSockets-with-Redis)
[Load Balancing Websocket Connections](https://deepstreamhub.com/blog/load-balancing-websocket-connections/)

[Websockets and scalability - Stack Overflow](https://stackoverflow.com/questions/47268038/websockets-and-scalability)
[node.js - Load balancing sockets on a horizontally scaling WebSocket server? - Stack Overflow](https://stackoverflow.com/questions/47321335/load-balancing-sockets-on-a-horizontally-scaling-websocket-server)

### Session Persistence

[Enforcing a single web socket connection per user with Node.js, Socket.IO, and Redis](https://hackernoon.com/enforcing-a-single-web-socket-connection-per-user-with-node-js-socket-io-and-redis-65f9eb57f66a)
[Distributed locks with Redis – Redis](https://redis.io/topics/distlock)

---

# Long Polling

[What is HTTP Long Polling? | PubNub](https://www.pubnub.com/blog/2014-12-01-http-long-polling/)
[Long Polling - Concepts and Considerations | Ably Realtime](https://www.ably.io/concepts/long-polling)

[rousan/comet: A http long polling comet implementation for nodejs and browser](https://github.com/rousan/comet)

---

# Server-sent Events (SSE)

[Server-sent events - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events)
[Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/#feat=eventsource)
[Server-sent events - Wikiwand](https://www.wikiwand.com/en/Server-sent_events)

[Stream Updates with Server-Sent Events - HTML5 Rocks](https://www.html5rocks.com/en/tutorials/eventsource/basics/)
[A Look at Server-Sent Events – Conectric Networks – Medium](https://medium.com/conectric-networks/a-look-at-server-sent-events-54a77f8d6ff7)
[Using SSE Instead Of WebSockets For Unidirectional Data Flow Over HTTP/2 — Smashing Magazine](https://www.smashingmagazine.com/2018/02/sse-websockets-data-flow-http2/)

[Server-Sent Events explained with usecases](https://streamdata.io/blog/server-sent-events/)
[Push: SSE vs Websockets - Streamdata.io](https://streamdata.io/blog/push-sse-vs-websockets/)
[Polling vs SSE vs WebSocket— How to choose the right one](https://codeburst.io/polling-vs-sse-vs-websocket-how-to-choose-the-right-one-1859e4e13bd9)

---

## Webhooks

[Should You Build a Webhooks API? — Brandur Leach](https://brandur.org/webhooks)
[WebHooks vs WebSub: Which Is Better For Real-Time Event Streaming? | Nordic APIs |](https://nordicapis.com/webhooks-vs-websub-which-one-is-better-to-stream-your-events-in-real-time/)

[CloudEvents](https://cloudevents.io/)

---

# WebSub

[WebSub - Wikiwand](https://www.wikiwand.com/en/WebSub) formerly PubSubHubbub
[PubSubHubbub](https://github.com/pubsubhubbub)
