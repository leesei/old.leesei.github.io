---
title: "Hapi"
date: 2015-02-16 17:58:29
categories:
  - web
tags:
  - hapi
  - javascript
toc: true
---

[hapi.js](https://hapi.dev/) is a opinionated framework developed and used by Walmart which simplifies the task of writing an API backend.

GitHub Orgs:

- [hapi.js](https://github.com/hapijs)
- [hapi pal](https://github.com/hapipal)

It has several design principles in mind:

- able to handle Black Friday traffic
- security  
  authentication and authorization is first class rather than after-thought  
  Eran Hammer is the co-author of OAuth

[Why You Should Consider hapi – hueniverse](https://hueniverse.com/why-you-should-consider-hapi-6163689bd7c2) 2018 sales pitch

Hapi v8 undergone a refactoring to better modularize the internals.
Hapi v17 supports async/await.

[hapi — Get Your Server Up and Running](https://futurestud.io/tutorials/hapi-get-your-server-up-and-running)
[hapi — v17 Upgrade Guide (Your Move to async/await)](https://futurestud.io/tutorials/hapi-v17-upgrade-guide-your-move-to-async-await)
[learn hapi Learning Path — on Future Studio](https://futurestud.io/learningpaths/learn-hapi)

[Single Page | Hapi With Typescript | Softcover.io](https://hapibook.jjude.com/book/_single-page)
[Using Typescript with hapi](https://www.solarwinter.net/using-typescript-with-hapi/)
[Hapi and TypeScript— splitting routes into multiple files | by Paul Walker | JavaScript in Plain English](https://javascript.plainenglish.io/more-hapi-and-typescript-routes-da37dfc324ca)

[hapijs/makemehapi: Self guided workshops to teach you about hapi.](https://github.com/hapijs/makemehapi) 2020 v17
[hapijs/university: Community learning experiment](https://github.com/hapijs/university/) 2017 v17, no update
[dwyl/learn-hapi](https://github.com/dwyl/learn-hapi) 2018 v18, no update

[hapi.js - API Reference](https://hapi.dev/api/)
[hapi/API.md at master · hapijs/hapi](https://github.com/hapijs/hapi/blob/master/API.md)

[Hapi vs Express: Comparing Node.js Web Frameworks](http://stackabuse.com/hapi-vs-express-comparing-node-js-web-frameworks/) 2017-12
Many Express plugins are out-of-maintenance and it's difficult to pick a high quality one from the vast choice.

[Using hapi.js with Socket.io · Matt Harrison](https://matt-harrison.com/posts/hapi-socket-io/) 2015
[Developing RESTful APIs with Hapi](https://auth0.com/blog/developing-restful-apis-with-hapijs/) 2017, v17
[Build a Secure Node.js Application with JavaScript Async Await Using Hapi ― Scotch](https://scotch.io/tutorials/build-a-secure-nodejs-application-with-javascript-async-await-using-hapi/amp) 2018, and Okta auth

[Hapi Tutorial Series - YouTube](https://www.youtube.com/playlist?list=PLkqiWyX-_LotaQ9AuppIAXl0xyV-P5Ms-) 2021, WittCode
[bradtraversy/hapiapp: Hapi.js crash course app](https://github.com/bradtraversy/hapiapp) 2020 v18, vision + handlebar for template,
[Hapi.js Framework Crash Course - YouTube](https://www.youtube.com/watch?v=2lprC0yYeFw) 2017 v16

<!-- more -->

## Sample Projects

[hapipal/hpal: hapi pal CLI](https://github.com/hapipal/hpal)
[hapipal/boilerplate: A friendly, proven starting place for your next hapi plugin or deployment](https://github.com/hapipal/boilerplate)

[JKHeadley/rest-hapi: 🚀 A RESTful API generator for Node.js](https://github.com/JKHeadley/rest-hapi) 2020 v19
[lynnaloo/mullet](https://github.com/lynnaloo/mullet) 2020 v19

[Aqua - A website and user system starter](http://jedireza.github.io/aqua/)
[Frame - A user system API for Node.js](http://jedireza.github.io/frame/)

## Authentication

[Authentication - hapi.dev](https://hapi.dev/tutorials/auth/?lang=en_US)

1. register a scheme (usually via plugin)  
   `server.auth.scheme(name, scheme)` or `server.register()`  
   when using plugin the scheme name is hardcoded
2. create strategy based on the scheme (specify options and implements validation)  
   `server.auth.strategy(name, scheme, [options])`
3. apply strategy to routes  
   `server.auth.default(strategy)` or `options: { auth: 'simple' }` on route

[Passport](http://passportjs.org/docs)'s design is similar.

[hapi.js - Plugins authentication](https://hapi.dev/plugins/#authentication)
[hapi.js - Plugins authorization](https://hapi.dev/plugins/#authorization)

[mozilla/hawk: HTTP Holder-Of-Key Authentication Scheme](https://github.com/mozilla/hawk)

[Frame - A user system API for Node.js](http://jedireza.github.io/frame/)
[franciscogouveia/hapi-rbac](https://github.com/franciscogouveia/hapi-rbac)

[hapijs/crumb: CSRF crumb generation and validation for hapi](https://github.com/hapijs/crumb)

### Token

[johnbrett/hapi-auth-bearer-token: Simple Bearer authentication scheme plugin for hapi, accepts token by Header, Cookie or Query parameter.](https://github.com/johnbrett/hapi-auth-bearer-token)

[dwyl/hapi-auth-jwt2: Secure Hapi.js authentication plugin using JSON Web Tokens (JWT) in Headers, URL or Cookies](https://github.com/dwyl/hapi-auth-jwt2)
[jwt - hapi.dev](https://hapi.dev/module/jwt/)

[now-ims/hapi-now-auth: Hapi token auth for bearer and jwt](https://github.com/now-ims/hapi-now-auth) outdated
[dwyl/hapi-auth-jwt2](https://github.com/dwyl/hapi-auth-jwt2)
[Token based auth system using JWT in hapi.js - CronJ Blog](http://www.cronj.com/blog/token-based-auth-system-using-jwt-in-hapi-js/)
[Auth in Hapi with JWT – Marcos Bérgamo – Medium](https://medium.com/@thedon/auth-in-hapi-with-jwt-780ce4d072c7)
[HapiJS Authentication - Secure Your API With JWT](https://auth0.com/blog/hapijs-authentication-secure-your-api-with-json-web-tokens/) little bit outdated, includes user creation

[hapijs/bell: Third-party login plugin for hapi](https://github.com/hapijs/bell)

### auth-cookie

[hapijs/hapi-auth-cookie](https://github.com/hapijs/hapi-auth-cookie)
[Authentication and Authorization with hapi. — Medium](https://medium.com/@poeticninja/authentication-and-authorization-with-hapi-5529b5ecc8ec)
[hapi — Authentication and Remember Me Using Cookies](https://futurestud.io/tutorials/hapi-cookie-authentication-and-remember-me)

### OAuth

[hapi — Authenticate with GitHub And Remember the Login](https://futurestud.io/tutorials/hapi-authenticate-with-github-and-remember-the-login)

### scope

use scope to handle access control
[javascript - Role based authentication in HapiJS - Stack Overflow](http://stackoverflow.com/questions/29052940/role-based-authentication-in-hapijs)
[Harnessing the magic of Hapi scopes](https://blog.andyet.com/2015/06/16/harnessing-hapi-scopes/)

[hapi.js - 18.3.2 API Reference](https://hapi.dev/api/?v=18.3.2#route-options)

## plugins

[hapi.js - Plugins](https://hapi.dev/plugins/)
[hapi pal - Home](https://hapipal.com/)

```js
// get plugin in request handler
const plugin = request.server.plugins["name"];
```

[knownasilya/hapi-decorators: Decorators for HapiJS routes](https://github.com/knownasilya/hapi-decorators)
[hapijs/scooter: User-agent information plugin for hapi](https://github.com/hapijs/scooter)
[hapijs/vision: Templates rendering support for hapi.js](https://github.com/hapijs/vision)
[wraithgar/electricfence](https://github.com/wraithgar/electricfence) better static file serving

[antonsamper/hapi-cron: 🕰️ Cron jobs for internal hapi.js routes](https://github.com/antonsamper/hapi-cron)
[hapipal/toys: The hapi utility toy chest](https://github.com/hapipal/toys)

### log

[mcollina/hapi-pino: Hapi plugin for the Pino logger](https://github.com/mcollina/hapi-pino)
https://github.com/pinojs/hapi-pino/issues/91#issuecomment-553318439 need to set `getChildBindings: () => ({})`

### routes

[glue - hapi.dev](https://hapi.dev/module/glue/)
[node.js - How to store routes in separate files when using Hapi? - Stack Overflow](https://stackoverflow.com/questions/27766623/how-to-store-routes-in-separate-files-when-using-hapi/33408326#33408326)
[sitraka-hq/hapi-auto-route: Autoloads hapi routes](https://github.com/sitraka-hq/hapi-auto-route)

[bleupen/halacious](https://github.com/bleupen/halacious) HAL/HATEOAS support
[mdibaiee/hapi-sequelize-crud: Hapi plugin that automatically generates RESTful API for CRUD](https://github.com/mdibaiee/hapi-sequelize-crud)

[futurestudio/hapi-rate-limitor: A hapi plugin for rate limiting. Simple and easy.](https://github.com/futurestudio/hapi-rate-limitor)
[patova: simple throttling for hapi.js – A sea of code](https://dschenkelman.github.io/2015/03/12/patova-simple-throttling-for-hapi-js/)
[yonjah/ralphi: Pure Node.js simple rate limiting server to prevent bruteforce attacks](https://github.com/yonjah/ralphi)

### pagination

[fknop/hapi-pagination: Hapi plugin to handle "custom" pagination](https://github.com/fknop/hapi-pagination)
[Paginating your hapi api](https://blog.andyet.com/2017/02/10/hapi-pagination/)

### router

[felixheck/bissle: Minimalist HALicious pagination response toolkit interface for HapiJS](https://github.com/felixheck/bissle)

[nlf/mudskipper](https://github.com/nlf/mudskipper) define your resource and create RESTful routes

[devinivy/loveboat: the hapi route config preprocessor](https://github.com/devinivy/loveboat)
[devinivy/loveboat-paths: support listing multiple paths in hapi route config](https://github.com/devinivy/loveboat-paths)

### docs

[krakenjs/hapi-openapi: Build design-driven apis with OpenAPI (formerly swagger) 2.0 and hapi.](https://github.com/krakenjs/hapi-openapi)

[glennjones/hapi-swagger: A Swagger interface for HAPI](https://github.com/glennjones/hapi-swagger)
[z0mt3c/hapi-swaggered: Yet another hapi plugin providing swagger compliant API specifications based on routes and joi schemas to be used with swagger-ui.](https://github.com/z0mt3c/hapi-swaggered)
[z0mt3c/hapi-swaggered-ui: An easy swagger-ui drop-in plugin for hapi (to be used with hapi-swaggered).](https://github.com/z0mt3c/hapi-swaggered-ui)
[desirable-objects/hapi-ending: An endpoint documentation plugin for HapiJS](https://github.com/desirable-objects/hapi-ending)

### Server Push/WebSocket

[mtharrison/susie: Server-sent events with hapi](https://github.com/mtharrison/susie)

[hapipal/underdog: HTTP/2 server-push for hapi](https://github.com/hapipal/underdog)

[hapijs/nes: WebSocket adapter plugin for hapi routes](https://github.com/hapijs/nes) more complication, requires corresponding client
[rse/hapi-plugin-websocket: HAPI plugin for seamless WebSocket integration](https://github.com/rse/hapi-plugin-websocket)

less active:
[Caligone/hapio: A simple bridge plugin between HapiJS and SocketIO](https://github.com/caligone/hapio)
[sibartlett/hapi-io: Awesome socket.io plugin for hapi](https://github.com/sibartlett/hapi-io)

### Data Store Drivers

[asilluron/hapi-mongoose: Hapi Plugin to handle Mongoose handshake and initial setup](https://github.com/asilluron/hapi-mongoose)
[maxnachlinger/hapi-level-db: HapiJS / LevelDB integration](https://github.com/maxnachlinger/hapi-level-db)
[fritzy/gatepost: Node.js module for binding postgres queries to models.](https://github.com/fritzy/gatepost)
[aduis/hapi-rabbit: rabbitMQ hapijs plugin](https://github.com/aduis/hapi-rabbit)
[midnightcodr/hapi-redis2: another simple redis plugin for hapijs that supports multiple connections](https://github.com/midnightcodr/hapi-redis2)

## Microservices

[Introducing chairo, a hapi.js Microservices Plugin | hueniverse](http://hueniverse.com/2015/06/02/introducing-chairo-a-hapi-js-microservices-plugin/)
[hapijs/chairo](https://github.com/hapijs/chairo)

[Seneca, a microservices toolkit for Node.js](http://senecajs.org/)

## Books

[Developing a hapi Edge: A Rich Node.JS Framework for Apps and Services eBook](https://www.amazon.co.uk/Developing-hapi-Edge-Framework-Services-ebook/dp/B013CWI3MY/254-1441755-8916502)
[Getting Started with hapi.js -O'Reilly Media](http://shop.oreilly.com/product/0636920040224.do)
[Manning | hapi.js in Action](https://www.manning.com/books/hapi-js-in-action)

## Tips and Tricks

Storing data in [`server.options.app`](hhttps://hapi.dev/api/?v=18.3.2#server.options.app)/[`server.app`](https://hapi.dev/api/?v=18.3.2#server.app)

[hapi.js - Server-side caching](https://hapi.dev/tutorials/caching/?lang=en_US#server-side)

`request.log()` in `handler()` to emit `request` event.
Register `server.events.on('request')` handler to log.

### Error

[hapijs/boom: HTTP-friendly error objects](https://github.com/hapijs/boom) is your friend
see [hapi/API.md at master · hapijs/hapi](https://github.com/hapijs/hapi/blob/master/API.md#errors)
[hapi.dev - boom](https://hapi.dev/family/boom/?v=7.4.9)

To append custom data to error:

```js
let error = Boom.badRequest("invalid query");
error.output.payload.custom = "additional error data";
```
