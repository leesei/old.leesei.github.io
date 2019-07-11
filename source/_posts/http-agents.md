---
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

[#153: 17 Years of curl With Daniel Stenberg - The Changelog](https://changelog.com/153/)
[Everything curl - GitBook](https://www.gitbook.com/book/bagder/everything-curl/details)

```sh
curl
    -X '{HTTP_METHOD}'
    -H '${KEY}: ${VALUE}' # header
    -B 'NAME1=VALUE1; NAME2=VALUE2' # cookie or cookie file
    -d '${BODY}' # body text (or file with '@')
    -L # follow redirects
    ${URL}
```

```sh
curl --data "param1=value1&param2=value2" ${URL}
curl --form "fileupload=@my-file.txt" ${URL}
curl -F "NAME1=VALUE1" -F "NAME2=VALUE2" ${URL}
curl -X POST -H "Content-Type: application/json" -d '{"type": "json"}' ${URL}
```

[curl - How To Use](https://curl.haxx.se/docs/manpage.html)
[curl - Manual](https://curl.haxx.se/docs/manual.html)
[curl - Tutorial](https://curl.haxx.se/docs/httpscripting.html)

[15 Practical Linux cURL Command Examples (cURL Download Examples)](http://www.thegeekstuff.com/2012/04/curl-examples/)
[POST Form Data with cURL](https://davidwalsh.name/curl-post-file)

[Embed curl - Embeddable curl commands for your web site.](https://www.embedcurl.com/)
[Parsing curl Commands with shlex - YouTube](https://www.youtube.com/watch?v=QnJ22Kgmb5M)
[Hurl.it - Make HTTP requests](https://www.hurl.it/)

[curl vs libcurl](https://daniel.haxx.se/docs/curl-vs-libcurl.html)
[curl vs Wget](https://daniel.haxx.se/docs/curl-vs-wget.html)

### curlify

Converts browser/Node request to `curl` command line.

[Node curlify](https://github.com/azproduction/node-request-as-curl)
[Chrome DevTools](https://developer.chrome.com/devtools/docs/network#copying-requests-as-curl-commands)
[Firefox DevTools](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor#Copy_as_cURL)

[NickCarneiro/curlconverter](https://github.com/NickCarneiro/curlconverter)
[Convert curl command syntax to python requests code](http://curl.trillworks.com/#node)

## wget

http://www.thegeekstuff.com/2009/09/the-ultimate-wget-download-guide-with-15-awesome-examples/

[wget - man page - ManKier](https://www.mankier.com/1/wget)

```sh
wget -p -k -nd -q -E -r -R js,txt,css -nc %pg%

# no upwards
get all images, etc. needed to display HTML page
recursively
make links in downloaded HTML point to local files
don't create directories
quiet
save HTML documents with `.html` extension
comma-separated list of rejected extensions: js,txt,css
skip downloads that would download to existing files

# clone website (form Just Enough Linux)
wget -e robots=off -r -np -nc -k -c <URL>
# -e robots=off: ignore we are a robot
# -r,--recursive: recursive retrieving
# -np,--no-parent: do not ascend to the parent directory when `-r`
# -nc,--no-clobber: don't redownload
# -k,--convert-links: convert links suitable for local viewing
# -c,--continue: continue getting a partially-downloaded file.

# my wget_all.sh
wget -r -l inf -nH -np -k -c -U "${SCRIPT_NAME}" ${URL}
# -m,--mirror: mirroring, equivalent to `-r -N -l inf --no-remove-listing`
# -N: ignore timestamp, conflicts with -nc
# -l: recursion depth
# -nH,--no-host-directories: do not generate directory with host name
# -U,--user-agent: set user agent
```

```sh
# download all links in file, to specific folder
wget -P./download -i list.txt
```

## httpie

HTTP client for CLI, more sensible than cURL
[jkbrzt/httpie](https://github.com/jkbrzt/httpie)

[httpie cheatsheet](https://devhints.io/httpie)
[httpie: A CLI http client that will make you smile (by @radekpazdera)](http://radek.io/2015/10/20/httpie/)
[HTTPie - HTTP for Humans – Mitesh Shah](https://miteshshah.github.io/sysadmin/httpie-http-for-humans/)
[httpie: A CLI http client that will make you smile (by @radekpazdera)](https://radek.io/2015/10/20/httpie/)

[eliangcs/http-prompt: HTTPie + prompt_toolkit = an interactive command-line HTTP client featuring autocomplete and syntax highlighting](https://github.com/eliangcs/http-prompt)

```sh
# create session to store cookies
http --session dpms85 POST http://10.6.64.85/sso token=${DPMS_TOKEN}
```

```sh
# use with Here Doc
TOKEN=$(http -b POST https://api.server/auth username=admin password=password)
http -b POST https://api.server/tokens "Authorization: Bearer ${TOKEN}" <<EOF
{
    "foo": "bar"
    "tokens": [
        "82b8d60bb4434b0083a9",
        "20458cb886154d618095",
        "c0b8191918a64e60967a",
        "3ce30cd4f5e340d09585",
        "871142606b564ce2b1de"
    ]
}
EOF
```

## Cross Origin Requests

```sh
curl -H "Origin: http://example.com" --verbose \
  https://www.googleapis.com/discovery/v1/apis?fields=

# CORS preflight, should include "Access-Control-Allow-Methods"
curl -H "Origin: http://example.com" \
  -H "Access-Control-Request-Method: POST" \
  -H "Access-Control-Request-Headers: X-Requested-With" \
  -X OPTIONS --verbose \
  https://www.googleapis.com/discovery/v1/apis?fields=
```

```sh
# CORS preflight
http --print -Hh OPTIONS \
    https://www.googleapis.com/discovery/v1/apis\?fields\= \
    Origin:http://example.com \
    Access-Control-Request-Method:POST \
    Access-Control-Request-Headers:X-Requested-With
```

## aria

[aria2/aria2: aria2 is a lightweight multi-protocol & multi-source, cross platform download utility operated in command-line. It supports HTTP/HTTPS, FTP, SFTP, BitTorrent and Metalink.](https://github.com/aria2/aria2)

## GUI App

[Insomnia REST Client](https://insomnia.rest/) open source, also supports GraphQL

[Postman - A powerful HTTP client to test web services](http://www.getpostman.com/)
[Postman Docs](https://www.getpostman.com/docs)

[Newman v3 – Postman Blog](http://blog.getpostman.com/2016/08/12/newman-v3/)

[Review: Postman Client Makes RESTful API Exploration a Breeze](http://blog.programmableweb.com/2014/01/27/review-postman-client-makes-restful-api-exploration-a-breeze/)

[Inspector](https://inspector.swagger.io/builder?url=https%3A%2F%2Fswapi.co%2Fapi%2Fpeople) web GUI from Swagger

## Node.js

[zeke/npm-collection-http-clients: A review of HTTP clients for Node.js and browsers](https://github.com/zeke/npm-collection-http-clients)
[fetch API](https://davidwalsh.name/fetch) WHATWG standard
[HTTP Requests Compared: Why Axios Is Better Than Node-Fetch (Automatic Transformations, More…](https://medium.com/@jeffrey.allen.lewis/http-requests-compared-why-axios-is-better-than-node-fetch-more-secure-can-handle-errors-better-39fde869a4a6)

Isomorphic (through bundler):
[matthew-andrews/isomorphic-fetch](https://github.com/matthew-andrews/isomorphic-fetch)
[mikeal/r2: HTTP client. Spiritual successor to request.](https://github.com/mikeal/r2)
[mzabriskie/axios](https://github.com/mzabriskie/axios)
[visionmedia/superagent](https://github.com/visionmedia/superagent)
[matthewwithanm/httpplease.js: The polite HTTP request library for node and the browser](https://github.com/matthewwithanm/httpplease.js)
[scottcorgan/httpify: Http in the browser and Node.js with no hassle](https://github.com/scottcorgan/httpify)

Server:
[bitinn/node-fetch](https://github.com/bitinn/node-fetch)
[tomas/needle](https://github.com/tomas/needle)
[hapijs/wreck](https://github.com/hapijs/wreck) (previously `nipple`)
[sindresorhus/got](https://github.com/sindresorhus/got)
[request/request](https://github.com/request/request)
[request/request-promise](https://github.com/request/request-promise) (promisified `request`)
[Hulken by hellgrenj](http://hellgrenj.github.io/hulken/) (stress testing)

## Python

[kennethreitz/requests: Python HTTP Requests for Humans™ ✨🍰✨](https://github.com/kennethreitz/requests)
[kennethreitz/requests3: Requests 3.0, for Humans and Machines, alike. 🤖](https://github.com/kennethreitz/requests3)
[encode/httpcore](https://github.com/encode/httpcore)

## Rust

[hyper.rs | hyper](https://hyper.rs/)
[reqwest - Rust](https://docs.rs/reqwest/)
[hyperium/h2: HTTP 2.0 client & server implementation for Rust.](https://github.com/hyperium/h2)

# HAR

[HAR 1.2 Spec | Software is hard](http://www.softwareishard.com/blog/har-12-spec/)
[HTTP Archive Viewer](http://www.softwareishard.com/har/viewer/)
[HAR Resources | A community curated list of resources, tools, projects and applications that support HTTP Archive (HAR)](https://ahmadnassri.github.io/har-resources/)
[HAR Adopters | Software is hard](http://www.softwareishard.com/blog/har-adopters/)

[Mashape/harplayer: Replay HAR logs](https://github.com/Mashape/harplayer)
[kkovacs/har-replay: A small, basic tool to replay requests from a HTTP Archive (HAR) file, for load testing](https://github.com/kkovacs/har-replay)
[pilsna/replay-har: A command line tool for replaying HTTP archive files.](https://github.com/pilsna/replay-har) Python
[formalin14/WWW-HarWalk: Replay HTTP requests from HAR ( HTTP Archive ) file](https://github.com/formalin14/WWW-HarWalk) Perl

[Stuk/server-replay: Replay server responses from a HAR file](https://github.com/Stuk/server-replay)

[YSlow - Official Open Source Project Website](http://yslow.org/command-line-har/) get YSlow score with HAR
[pcapperf](http://pcapperf.appspot.com/) get PageSpeed score with PCAP/HAR, PCAP -> HAR
[shaunakv1/node-chrome-har-replay: A node.js script that takes chorme HAR network log file, replays it and generates performance benchmark](https://github.com/shaunakv1/node-chrome-har-replay)

# Others

[fstab/h2c: http2client](https://github.com/fstab/h2c)
[hazbo/httpu: The terminal-first http client](https://github.com/hazbo/httpu)

# request/response bin

# Dumping HTTP requests

[httpbin(1): HTTP Client Testing Service](http://httpbin.org/)

[Hookbin - Capture and Inspect HTTP Requests](https://hookbin.com/)
[Hookbin - Capture and Inspect HTTP Requests | CSS-Tricks](https://css-tricks.com/hookbin-capture-inspect-http-requests/)

[Mockbin by Mashape](https://mockbin.com/)
[Mockable: Quickly create REST and SOAP mocks](https://www.mockable.io/)

[leesei/httpbin.js: HTTPbin-like server implemented in Node.js](https://github.com/leesei/httpbin.js)

## httpbin.js

```sh
# https://github.com/jakubroztocil/httpie
brew install httpie

# https://www.npmjs.com/package/httpbin.js
npm install -g httpbin.js
npm install -g bunyan
```

### Term1 (server)

```sh
httpbin.js | bunyan
```

### Term2 (http agent)

```sh
# check request header and body
http -v --json POST http://localhost:35000/prq/xyz?a=b\&c=d key=value foo=bar
http -v --form POST http://localhost:35000/prq/xyz?a=b\&c=d key=value foo=bar
```
