---
title: JavaScript Snippets
date: 2014-12-11 17:04:13
categories:
- comp.lang
tags:
- javascript
- snippets
toc: true
---

> TODO: add code from `~/commonroom/node-belt/`

## looping

```js
// looping POJO
for (let key in obj) {
    console.log(key + " -> " + obj[key]);
}
for (let [key, value] of Object.entries(obj)) {
  console.log(`${key}: ${value}`);
}
Object.keys(obj).map(value => {});
Object.values(obj).map(value => {});

// looping array
for (let item of arr) {
    console.log(item);
}
// arr.map(function callback(currentValue[, index[, array]])
arr.map(item => {});
// arr.forEach(function callback(currentValue[, index[, array]])
arr.forEach(item => {});
```

## padding

```js
//pads left
String.prototype.lpad = function(padChar, length) {
  var str = this;
  var padString = (length > str.length)?
    // limit padding char to 1 character
    Array(length-str.length+1).join(padChar[0]) : '';
  return (padString + str);
};

//pads right
String.prototype.rpad = function(padChar, length) {
  var str = this;
  var padString = (length > str.length)?
    // limit padding char to 1 character
    Array(length-str.length+1).join(padChar[0]) : '';
  return (str + padString);
};

// usage
var str = "5";
console.log(str.lpad(" ", 3)); //result "  5"
console.log(str.rpad("0", 3)); //result "500"

var str = "56789";
console.log(str.lpad(" ", 3)); //result "56789"
console.log(str.rpad("0", 3)); //result "56789"
```

## debounce

```js
// Code from _.debounce()

// Returns a function, that, as long as it continues to be invoked, will not
// be triggered. The function will be called after it stops being called for
// N milliseconds. If `immediate` is passed, trigger the function on the
// leading edge, instead of the trailing.
function debounce(func, wait, immediate) {
    var timeout;
    return function() {
        var context = this, args = arguments;
        var later = function() {
            timeout = null;
            if (!immediate) func.apply(context, args);
        };
        var callNow = immediate && !timeout;
        clearTimeout(timeout);
        timeout = setTimeout(later, wait);
        if (callNow) func.apply(context, args);
    };
};

// Usage
var myEfficientFn = debounce(function() {
    // All the taxing stuff you do
}, 250);
window.addEventListener('resize', myEfficientFn);
input.onchange = myEfficientFn;
```

## ISO date

```js
function pad(number) {
  if (number < 10) {
    return '0' + number;
  }
  return number;
}

function ISODateString(date) {
  return date.getUTCFullYear() +
    pad(date.getUTCMonth() + 1) +
    pad(date.getUTCDate());
};
```

## dynamically register source

This sample code is for adding routes to Hapi, but the technique is applicable elsewhere.

```js
// Look through the routes in
// all the subdirectories of API
// and create a new route for each
glob.sync('api/**/routes/*.js', {
  root: __dirname
}).forEach(file => {
  const route = require(path.join(__dirname, file));
  server.route(route);
});
```

## pick from object

[javascript - One-liner to take some properties from object in ES 6 - Stack Overflow](https://stackoverflow.com/questions/25553910/one-liner-to-take-some-properties-from-object-in-es-6)

```js
// ES6 destructing requires a reconstruction for object output
const {color, height} = source;
const subset = {color, height};

// one liner
var subset = ['color', 'height'].reduce(
  (o, k) => { o[k] = source[k]; return o; }, {}
);

// function
function pick(source, ...fields) {
    return fields.reduce((o, x) => {
        if(source.hasOwnProperty(x)) o[x] = source[x];
        return o;
    }, {});
}
subset = pick(source, 'color', 'height');
```

## Convert string to ByteArray

```js
// Returns a new array of bytes representing the given string encoded in UTF-8.
function toUtf8ByteArray(str) {
  str = encodeURI(str);
  var result = [];
  for (var i = 0; i < str.length; i++) {
    if (str.charAt(i) != "%")
      result.push(str.charCodeAt(i));
    else {
      result.push(parseInt(str.substr(i + 1, 2), 16));
      i += 2;
    }
  }
  return result;
}
```

[QR-Code-generator/qrcodegen.js at 98d1f0cc91d060cbb2cd19a4663e4cfac237cd51 · nayuki/QR-Code-generator](https://github.com/nayuki/QR-Code-generator/blob/98d1f0cc91d060cbb2cd19a4663e4cfac237cd51/javascript/qrcodegen.js#L881)

## Stack Restify over Express

```js
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

## HTTPS server

Generate key with `openssl` first.

```javascript
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
