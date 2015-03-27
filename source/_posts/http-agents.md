title: HTTP agents
date: 2014-12-11 14:42:17
categories:
- web
tags:
- shell-tool
- curl
- wget
- httpie
- postman
- web-dev
- http-agent
toc: true
---

## cURL

http://curl.haxx.se/docs/manpage.html
http://www.thegeekstuff.com/2012/04/curl-examples/

### curlify

Converts browser/Node request to `curl` commnad line.

[Node curlify](https://github.com/azproduction/node-request-as-curl)
[Chrome DevTools](https://developer.chrome.com/devtools/docs/network#copying-requests-as-curl-commands)
[Firefox DevTools](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor#Copy_as_cURL)

[NickCarneiro/curlconverter](https://github.com/NickCarneiro/curlconverter)
[Convert curl command syntax to python requests code](http://curl.trillworks.com/#node)

## wget

http://www.thegeekstuff.com/2009/09/the-ultimate-wget-download-guide-with-15-awesome-examples/

## httpie

HTTP client for CLI, more senible than cURL
[HTTPie: a CLI, cURL-like tool for humans](https://github.com/jakubroztocil/httpie)

## PostMan

https://www.getpostman.com/
https://www.getpostman.com/docs

## Node.js

[hapijs/wreck](https://github.com/hapijs/wreck) (previously `nipple`)
[request/request](https://github.com/request/request)
[tomas/needle](https://github.com/tomas/needle)
[visionmedia/superagent](https://github.com/visionmedia/superagent)
[Hulken by hellgrenj](http://hellgrenj.github.io/hulken/)

## Python

[kennethreitz/requests](https://github.com/kennethreitz/requests)

# HTTP POST payload format

## prerequisite

```sh
# https://github.com/jakubroztocil/httpie
brew install httpie

# https://www.npmjs.com/package/httpbin.js
npm install -g httpbin.js
npm install -g bunyan
```

## Term1 (server)

```sh
httpbin.js | bunyan
```

## Term2 (http agent)

```sh
# check request header and body
http -v --json POST http://localhost:35000/prq/xyz?a=b\&c=d key=value foo=bar
http -v --form POST http://localhost:35000/prq/xyz?a=b\&c=d key=value foo=bar
```

