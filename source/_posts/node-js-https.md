title: "Node.js HTTPS server"
date: 2014-12-17 13:41:00
categories:
- comp.lang
tags:
- node-js
- openssl
- snippets
toc: true
---

## cert generation

```sh
openssl genrsa -out privatekey.pem 1024
openssl req -new -key privatekey.pem -x509 -days 7300 -out certificate.pem
```

## server

```javascript http-server.js
var express = require('express');
var app = express();

app.get('/', function(req, res){
    res.send('Hello World');
});

var port = 3000;
var ports = 3443;

var options = {
    key: fs.readFileSync('./privatekey.pem'),
    cert: fs.readFileSync('./certificate.pem')
};

if (port) {
    http.createServer(app).listen(port);
    console.log('Listening http on port ' + port + '...');
}
if (ports) {
    https.createServer(options, app).listen(ports);
    console.log('Listening https on port ' + ports + '...');
}
```
