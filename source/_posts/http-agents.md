title: "HTTP agents"
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
- har
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

```sh
# download all links in file, to specific folder
wget -P./download -i list.txt
```


## httpie

HTTP client for CLI, more senible than cURL
[HTTPie: a CLI, cURL-like tool for humans](https://github.com/jakubroztocil/httpie)

## PostMan

https://www.getpostman.com/
https://www.getpostman.com/docs

## Node.js

[hapijs/wreck](https://github.com/hapijs/wreck) (previously `nipple`)
[request/request](https://github.com/request/request)
[alyssaq/prequest](https://github.com/alyssaq/prequest) (promisified `request`)
[tomas/needle](https://github.com/tomas/needle)
[visionmedia/superagent](https://github.com/visionmedia/superagent)
[mzabriskie/axios](https://github.com/mzabriskie/axios)
[Hulken by hellgrenj](http://hellgrenj.github.io/hulken/)

## Python

[kennethreitz/requests](https://github.com/kennethreitz/requests)

# HAR and request/response bin

[HAR 1.2 Spec | Software is hard](http://www.softwareishard.com/blog/har-12-spec/)
[HTTP Archive Viewer](http://www.softwareishard.com/har/viewer/)
[HAR Resources | A community curated list of resources, tools, projects and applications that support HTTP Archive (HAR)](https://ahmadnassri.github.io/har-resources/)

[Mockbin by Mashape](https://mockbin.com/)
[httpbin(1): HTTP Client Testing Service](http://httpbin.org/)

[Mockable: Quickly create REST and SOAP mocks](https://www.mockable.io/)

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

