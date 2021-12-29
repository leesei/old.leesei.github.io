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

[The Lost Art of Vanilla JavaScript | by Danny Moerkerke | Better Programming](https://betterprogramming.pub/the-lost-art-of-vanilla-javascript-c11519720244)

[Vanilla JavaScript Code Snippets — Smashing Magazine](https://www.smashingmagazine.com/2021/04/vanilla-javascript-code-snippets/)
[30 seconds of code](https://www.30secondsofcode.org/)
[The Vanilla JS Toolkit](https://vanillajstoolkit.com/)
[HTML DOM - Common tasks of managing HTML DOM with vanilla JavaScript](https://htmldom.dev/)
[Cheat sheet for moving from jQuery to vanilla JavaScript | Tobias Ahlin](https://tobiasahlin.com/blog/move-from-jquery-to-vanilla-javascript/)
[Microjs: Fantastic Micro-Frameworks and Micro-Libraries for Fun and Profit!](http://microjs.com/#)
[Vanilla List: The Vanilla Javascript Repository](http://www.vanillalist.com/)
[plainJS - The Vanilla JavaScript Repository](http://plainjs.com/)
[Javascript Territory - JSter Javascript Catalog](http://jster.net/)
[JavaScripting.com - The Database of JavaScript Libraries](https://www.javascripting.com/)
[angus-c/just: A library of dependency-free utilities that do just do one thing](https://github.com/angus-c/just)

[Useful JavaScript Array Methods for Developers](https://www.decipherzone.com/blog-detail/javascript-array)

## looping

```js
// looping POJO
for (let key in obj) {
  console.log(key + " -> " + obj[key]);
}
for (let [key, value] of Object.entries(obj)) {
  console.log(`${key}: ${value}`);
}
Object.keys(obj).map((value) => {});
Object.values(obj).map((value) => {});

// looping array
for (let item of arr) {
  console.log(item);
}
// arr.map(function callback(currentValue[, index[, array]])
arr.map((item) => {});
// arr.forEach(function callback(currentValue[, index[, array]])
arr.forEach((item) => {});
```

## padding

```js
//pads left
function stringLPad(string, padChar, length) {
  var padString =
    length > string.length
      ? // limit padding char to 1 character
        new Array(length - string.length + 1).join(padChar[0])
      : "";
  // ES6: padChar[0].repeat(length-string.length+1)
  return padString + string;
}

//pads right
function stringRPad(string, padChar, length) {
  var padString =
    length > string.length
      ? // limit padding char to 1 character
        new Array(length - string.length + 1).join(padChar[0])
      : "";
  // ES6: padChar[0].repeat(length-string.length+1)
  return string + padString;
}

// usage
var str1 = "5";
console.log(stringLPad(str1, " ", 3)); //result "  5"
console.log(stringRPad(str1, "0", 3)); //result "500"

var str2 = "56789";
console.log(stringLPad(str2, " ", 3)); //result "56789"
console.log(stringRPad(str2, "0", 3)); //result "56789"
```

## querystring

[Query string | Node.js v15.12.0 Documentation](https://nodejs.org/api/querystring.html)
[lukeed/qss: A tiny (294b) browser utility for encoding & decoding a querystring.](https://github.com/lukeed/qss) for browser

```js

```

```js
const ConstructQueryString = (params: Record<string, any>): string => {
  return Object.keys(params)
    .map((k) => encodeURIComponent(k) + "=" + encodeURIComponent(params[k]))
    .join("&");
};
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
  return function () {
    var context = this,
      args = arguments;
    var later = function () {
      timeout = null;
      if (!immediate) func.apply(context, args);
    };
    var callNow = immediate && !timeout;
    clearTimeout(timeout);
    timeout = setTimeout(later, wait);
    if (callNow) func.apply(context, args);
  };
}

// Usage
var myEfficientFn = debounce(function () {
  // All the taxing stuff you do
}, 250);
window.addEventListener("resize", myEfficientFn);
input.onchange = myEfficientFn;
```

## groupBy

```js
/*!
 * Group items from an array together by some criteria or value.
 * (c) 2019 Tom Bremmer (https://tbremer.com/) and Chris Ferdinandi (https://gomakethings.com), MIT License,
 * @param  {Array}           items    The array to group items from
 * @param  {String|Function} criteria The criteria to group by
 * @return {Object}                   The grouped object
 */
export const groupBy = <K extends string | number | symbol, T>(
  items: [T],
  criteria: keyof T | ((item: T) => K)
): Record<K, [T]> => {
  return items.reduce(function (obj, item) {
    // Check if the criteria is a function to run on the item or a property of it
    const key: K =
      typeof criteria === "function"
        ? criteria(item)
        : (item[criteria] as unknown as K);

    // If the key doesn't exist yet, create it
    if (!obj.hasOwnProperty(key)) {
      obj[key] = [] as unknown as [T];
    }

    // Push the value to the object
    obj[key].push(item);

    // Return the object to the next item in the loop
    return obj;
  }, {} as Record<K, [T]>);
};
```

## ISO date

[wojtekmaj/date-utils: A collection of date-related utilities.](https://github.com/wojtekmaj/date-utils)

```js
function pad(number) {
  if (number < 10) {
    return "0" + number;
  }
  return number;
}

function ISODateString(date) {
  return (
    date.getUTCFullYear() + pad(date.getUTCMonth() + 1) + pad(date.getUTCDate())
  );
}
```

## dynamically register source

This sample code is for adding routes to Hapi, but the technique is applicable elsewhere.

```js
// Look through the routes in
// all the subdirectories of API
// and create a new route for each
glob
  .sync("api/**/routes/*.js", {
    root: __dirname,
  })
  .forEach((file) => {
    const route = require(path.join(__dirname, file));
    server.route(route);
  });
```

## pick from object

[javascript - One-liner to take some properties from object in ES 6 - Stack Overflow](https://stackoverflow.com/questions/25553910/one-liner-to-take-some-properties-from-object-in-es-6)

```js
// ES6 destructing requires a reconstruction for object output
const { color, height } = source;
const subset = { color, height };

// one liner
var subset = ["color", "height"].reduce((o, k) => {
  o[k] = source[k];
  return o;
}, {});

// function
function pick(source, ...fields) {
  return fields.reduce((o, x) => {
    if (source.hasOwnProperty(x)) o[x] = source[x];
    return o;
  }, {});
}
subset = pick(source, "color", "height");
```

## Run promises sequentially

```js
const mapSeries = async (iterable, action) => {
  for (const x of iterable) {
    await action(x);
  }
};
await mapSeries(promises);
```

[Why Using reduce() to Sequentially Resolve Promises Works | CSS-Tricks](https://css-tricks.com/why-using-reduce-to-sequentially-resolve-promises-works/)

```js
[1, 2, 5].reduce((accumulator, item) => {
  return accumulator + item;
}, 0 /* initial value */);

promises.reduce(async (previousPromise, nextPromise) => {
  await previousPromise;
  return nextPromise;
}, Promise.resolve() /* initial promise */);
```

## Convert string to ByteArray

```js
// Returns a new array of bytes representing the given string encoded in UTF-8.
function toUtf8ByteArray(str) {
  str = encodeURI(str);
  var result = [];
  for (var i = 0; i < str.length; i++) {
    if (str.charAt(i) != "%") result.push(str.charCodeAt(i));
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
var express = require("express");
var restify = require("restify");

// see http://stackoverflow.com/a/13690887/665507

// Restify server config here
var server = restify.createServer({
  name: "restify-test",
  version: "1.0.0",
});

// Express config here
var expressApp = express()
  .use(express.logger())
  .use(express.bodyParser())
  .use(express.query())
  .use(express.cookieParser())
  // And this is where the magic happens
  .use("/api", function (req, res) {
    server.server.emit("request", req, res);
  });

expressApp.listen(8080);
```

## HTTPS server

Generate key with `openssl` first.

```javascript
var express = require("express");
var app = express();

app.get("/", function (req, res) {
  res.send("Hello World");
});

var port = 3000;
var ports = 3443;

var options = {
  key: fs.readFileSync("./privatekey.pem"),
  cert: fs.readFileSync("./certificate.pem"),
};

if (port) {
  http.createServer(app).listen(port);
  console.log("Listening http on port " + port + "...");
}
if (ports) {
  https.createServer(options, app).listen(ports);
  console.log("Listening https on port " + ports + "...");
}
```
