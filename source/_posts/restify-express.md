title: Restify Express
date: 2014-12-17 13:49:46
categories:
- web
tags:
  - node-js
  - restify
  - express
  - snippets
---

Stack Restify over Express 

```javascript
var express = require('express');
var restify = require('restify');

// see http://stackoverflow.com/a/13690887/665507

// Restify server config here
var server = restify.createServer({
  name: 'restify-test',
  version: '1.0.0',
});

// Express config here
var expressApp = express()
    .use(express.logger())
    .use(express.bodyParser())
    .use(express.query())
    .use(express.cookieParser())
    // And this is where the magic happens
    .use("/api", function (req, res) {
             server.server.emit('request', req, res);
         });

expressApp.listen(8080);
```
