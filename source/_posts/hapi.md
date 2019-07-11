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

[hapi.js](http://hapijs.com/) is a opinionated framework developed and used by Walmart which simplifies the task of writing an API backend.

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

[hapijs/makemehapi: Self guided workshops to teach you about hapi.](https://github.com/hapijs/makemehapi)
[dwyl/learn-hapi](https://github.com/dwyl/learn-hapi)
[hapijs/university: Community learning experiment](https://github.com/hapijs/university/)

[hapi/API.md at master · hapijs/hapi](https://github.com/hapijs/hapi/blob/master/API.md#request)

[Hapi vs Express: Comparing Node.js Web Frameworks](http://stackabuse.com/hapi-vs-express-comparing-node-js-web-frameworks/) 2017-12
Many Express plugins are out-of-maintenance and it's difficult to pick a high quality one from the vast choice.

[Using hapi.js with Socket.io](http://matt-harrison.com/using-hapi-js-with-socket-io/)
[Making a RESTful API with Hapi.js | Scotch](https://scotch.io/tutorials/making-a-restful-api-with-hapi-js) v16
[hapi — How to Run Separate Frontend and Backend Servers Within a Single Project](https://futurestud.io/tutorials/hapi-how-to-run-separate-frontend-and-backend-servers-within-one-project) v16
[Build a Secure Node.js Application with JavaScript Async Await Using Hapi ― Scotch](https://scotch.io/tutorials/build-a-secure-nodejs-application-with-javascript-async-await-using-hapi/amp)

[Hapi.js Framework Crash Course - YouTube](https://www.youtube.com/watch?v=2lprC0yYeFw)

<!-- more -->

## Sample Projects

[Aqua - A website and user system starter](http://jedireza.github.io/aqua/)
[Frame - A user system API for Node.js](http://jedireza.github.io/frame/)
[Dindaleon/hapi-react-starter-kit](https://github.com/Dindaleon/hapi-react-starter-kit)
[lynnaloo/mullet](https://github.com/lynnaloo/mullet)
[thebergamo/start-hapiness](https://github.com/thebergamo/start-hapiness)
[smaxwellstewart/lummox](https://github.com/smaxwellstewart/lummox)
[smaxwellstewart/hapi-dash](https://github.com/smaxwellstewart/hapi-dash)
[rjmreis/hapi-api](https://github.com/rjmreis/hapi-api)
[colonizers/colonizers](https://github.com/colonizers/colonizers)

https://github.com/abiee/es6-hapijs
https://github.com/giacomorebonato/hapi_plate
https://github.com/johnbrett/hapi-level-sample
https://github.com/bbva-javiermoure/hapi-skeleton
https://github.com/webstronauts/isomorphic-hapi-react-example
https://github.com/mtharrison/hapicasts
https://github.com/eperedo/hapi-starter
https://github.com/tribou/whatlyric

## Authentication

[Authentication](https://hapijs.com/tutorials/auth)

1. register a scheme (usually via plugin)  
   `server.auth.scheme(name, scheme)` or `server.register()`  
   when using plugin the scheme name is hardcoded
2. create strategy based on the scheme (specify options and implements validation)  
   `server.auth.strategy(name, scheme, [options])`
3. apply strategy to routes  
   `server.auth.default(strategy)` or `options: { auth: 'simple' }` on route

[Passport](http://passportjs.org/docs)'s design is similar.

[Frame - A user system API for Node.js](http://jedireza.github.io/frame/)
[franciscogouveia/hapi-rbac](https://github.com/franciscogouveia/hapi-rbac)

[hapijs/crumb: CSRF crumb generation and validation for hapi](https://github.com/hapijs/crumb)

### Token

[GitHub - johnbrett/hapi-auth-bearer-token: Simple Bearer authentication scheme plugin for hapi, accepts token by Header, Cookie or Query parameter.](https://github.com/johnbrett/hapi-auth-bearer-token)

[GitHub - now-ims/hapi-now-auth: Hapi token auth for bearer and jwt](https://github.com/now-ims/hapi-now-auth)
[dwyl/hapi-auth-jwt2](https://github.com/dwyl/hapi-auth-jwt2)
[Token based auth system using JWT in hapi.js - CronJ Blog](http://www.cronj.com/blog/token-based-auth-system-using-jwt-in-hapi-js/)
[Auth in Hapi with JWT – Marcos Bérgamo – Medium](https://medium.com/@thedon/auth-in-hapi-with-jwt-780ce4d072c7)
[HapiJS Authentication - Secure Your API With JWT](https://auth0.com/blog/hapijs-authentication-secure-your-api-with-json-web-tokens/) little bit outdated, includes user creation

[hapijs/bell: Third-party login plugin for hapi](https://github.com/hapijs/bell)

https://github.com/johnbrett/hapi-auth-bearer-token
https://github.com/hapijs/scarecrow
https://github.com/hueniverse/oz

### auth-cookie

[hapijs/hapi-auth-cookie](https://github.com/hapijs/hapi-auth-cookie)
[Authentication and Authorization with hapi. — Medium](https://medium.com/@poeticninja/authentication-and-authorization-with-hapi-5529b5ecc8ec)

[leesei/hapi-auth-example](https://github.com/leesei/hapi-auth-example)

### scope

use scope to handle access control
[javascript - Role based authentication in HapiJS - Stack Overflow](http://stackoverflow.com/questions/29052940/role-based-authentication-in-hapijs)
[Harnessing the magic of Hapi scopes](https://blog.andyet.com/2015/06/16/harnessing-hapi-scopes/)

[12.1.0 API Reference: Route](http://hapijs.com/api#route-options)

## plugins

[Hapi.js Plugins](https://hapi-plugins.com/)
[hapi Plugins](http://hapijs.com/plugins)

[Best hapi modules for Node.js - Pincer.io](http://www.pincer.io/node/keywords/hapi/best)
[The hapi.js eco-system](http://blog.yld.io/2016/01/19/the-hapi-js-eco-system/)
[geek/hapi-plugin-example: Example plugin for hapi](https://github.com/geek/hapi-plugin-example)

[labibramadhan/mastery: MasteryJS, a scalable REST API framework build on top of Hapi and Sequelize](https://github.com/labibramadhan/mastery)

[Building APIs with Hapi.js - nearForm](http://www.nearform.com/nodecrunch/building-apis-hapi-js/) wrapping login as plug-in and test

```js
var plugin = request.server.plugins["name"];
```

[hapijs/good: hapi process monitoring](https://github.com/hapijs/good)
[mcollina/hapi-pino: Hapi plugin for the Pino logger](https://github.com/mcollina/hapi-pino)

[mtharrison/susie: Server-sent events with hapi](https://github.com/mtharrison/susie)
[mac-/ratify: A Hapi plugin for validating the schema of path, query, request body, and response body params using JSON-schema](https://github.com/mac-/ratify) also create Swagger documentation
[knownasilya/hapi-decorators: Decorators for HapiJS routes](https://github.com/knownasilya/hapi-decorators)
[hapijs/scooter: User-agent information plugin for hapi](https://github.com/hapijs/scooter)
[hapijs/vision: Templates rendering support for hapi.js](https://github.com/hapijs/vision)
[bleupen/halacious](https://github.com/bleupen/halacious) HAL/HATEOAS support
[wraithgar/electricfence](https://github.com/wraithgar/electricfence) better static file serving
[mdibaiee/hapi-sequelize-crud: Hapi plugin that automatically generates RESTful API for CRUD](https://github.com/mdibaiee/hapi-sequelize-crud)

[continuationlabs/hapi-setup: hapi plugin for viewing the server configuration](https://github.com/continuationlabs/hapi-setup)
[continuationlabs/borland: hapi plugin for working with toolbag](https://github.com/continuationlabs/borland)
[nlf/hapi-profile](https://github.com/nlf/hapi-profile)

[patova: simple throttling for hapi.js – A sea of code](https://dschenkelman.github.io/2015/03/12/patova-simple-throttling-for-hapi-js/)

[fknop/hapi-pagination: Hapi plugin to handle "custom" pagination](https://github.com/fknop/hapi-pagination)
[Paginating your hapi api](https://blog.andyet.com/2017/02/10/hapi-pagination/)

### router

[nlf/mudskipper](https://github.com/nlf/mudskipper) define your resource and create RESTful routes

[devinivy/loveboat: the hapi route config preprocessor](https://github.com/devinivy/loveboat)
[devinivy/loveboat-paths: support listing multiple paths in hapi route config](https://github.com/devinivy/loveboat-paths)

### docs

[glennjones/hapi-swagger](https://github.com/glennjones/hapi-swagger)
[mac-/ratify: A Hapi plugin for validating the schema of path, query, request body, and response body params using JSON-schema](https://github.com/mac-/ratify) also create Swagger documentation

[z0mt3c/hapi-swaggered](https://github.com/z0mt3c/hapi-swaggered)
[z0mt3c/hapi-swaggered-ui](https://github.com/z0mt3c/hapi-swaggered-ui)

[hapijs/lout](https://github.com/hapijs/lout)

### WebSocket

[hapijs/nes: WebSocket adapter plugin for hapi routes](https://github.com/hapijs/nes) more complication, requires corresponding client
[rse/hapi-plugin-websocket: HAPI plugin for seamless WebSocket integration](https://github.com/rse/hapi-plugin-websocket)

less active:
[Caligone/hapio: A simple bridge plugin between HapiJS and SocketIO](https://github.com/caligone/hapio)
[sibartlett/hapi-io: Awesome socket.io plugin for hapi](https://github.com/sibartlett/hapi-io)

### Data Store Drivers

https://github.com/aduis/hapi-rabbit
[fritzy/gatepost: Node.js module for binding postgres queries to models.](https://github.com/fritzy/gatepost)
[watchup/hapi-mongoose: An Hapi.js plugin that maps mongoose models to routes written in TypeScript 1.5](https://github.com/watchup/hapi-mongoose)
[maxnachlinger/hapi-level-db: HapiJS / LevelDB integration](https://github.com/maxnachlinger/hapi-level-db)

## Microservices

[Introducing chairo, a hapi.js Microservices Plugin | hueniverse](http://hueniverse.com/2015/06/02/introducing-chairo-a-hapi-js-microservices-plugin/)
[hapijs/chairo](https://github.com/hapijs/chairo)

[Seneca, a microservices toolkit for Node.js](http://senecajs.org/)

## Books

[Developing a hapi Edge: A Rich Node.JS Framework for Apps and Services eBook](https://www.amazon.co.uk/Developing-hapi-Edge-Framework-Services-ebook/dp/B013CWI3MY/254-1441755-8916502)
[Getting Started with hapi.js - O'Reilly Media](http://shop.oreilly.com/product/0636920040224.do)
[Manning | hapi.js in Action](https://www.manning.com/books/hapi-js-in-action)

## Tips and Tricks

Storing data in [`server.settings.app`](https://hapijs.com/api#-serveroptionsapp)/[`server.app`](https://hapijs.com/api#server.app)

[Server side caching](https://hapijs.com/tutorials/caching?lang=en_US#user-content-server-side-caching)

[Validation](https://hapijs.com/tutorials/validation)

`request.log()` in `handler()` to emit `request` event.
Register `server.events.on('request')` handler to log.

### Error

[hapijs/boom: HTTP-friendly error objects](https://github.com/hapijs/boom) is your friend

To append custom data to error:

```js
let error = Boom.badRequest("invalid query");
error.output.payload.custom = "additional error data";
```

### Joi validation

see [hapi/API.md at master · hapijs/hapi](https://github.com/hapijs/hapi/blob/master/API.md#errors)

[hapijs/joi: Object schema validation](https://github.com/hapijs/joi)
[RunKit + npm: joi](https://npm.runkit.com/joi)
[tlivings/enjoi: Converts a JSON schema to a Joi schema.](https://github.com/tlivings/enjoi)

[joi/examples at master · hapijs/joi](https://github.com/hapijs/joi/tree/master/examples)
[What I’ve Learned Validating with Joi – ITNEXT](https://itnext.io/what-ive-learned-validating-with-joi-20007e2b2b68)
[Node API Schema Validation with Joi ― Scotch](https://scotch.io/tutorials/node-api-schema-validation-with-joi)

[Handling Joi validation errors in Hapi 17 – Piotr Karpala – Medium](https://medium.com/@piotrkarpaa/handling-joi-validation-errors-in-hapi-17-26fc07448576) !important, return validation error to client

[Expressing complex logic in `when()` · Issue #1663 · hapijs/joi](https://github.com/hapijs/joi/issues/1663#issuecomment-441366556) use `when()` on schema
