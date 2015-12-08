---
title: Browserify
categories:
  - web
toc: true
date: 2015-11-27 17:47:35
tags:
---

[Browserify](http://browserify.org/)
[substack/browserify-handbook](https://github.com/substack/browserify-handbook)
[substack/browserify-handbook (builtins)](https://github.com/substack/browserify-handbook#builtins)

[Cross platform JavaScript with Browserify - Sharing Code Between Node.js and the Browser - codecentric Blog : codecentric Blog](https://blog.codecentric.de/en/2014/02/cross-platform-javascript/)

```sh
$ browserify -r ./lib/slugger:slugger > static/bundle.js
# export `require()` in browser and the module 'slugger'
```

[browserify for webpack users](https://gist.github.com/substack/68f8d502be42d5cd4942)

## internals

[How Browserify Works](http://benclinkinbeard.com/posts/how-browserify-works/)
[Introduction to Browserify • Blake Embrey](http://blakeembrey.com/articles/2013/09/introduction-to-browserify/)
[substack/browserify-handbook (how browserify works)](https://github.com/substack/browserify-handbook#how-browserify-works)
[substack/browserify-handbook (bundling)](https://github.com/substack/browserify-handbook#bundling)

## option passing

[substack/node-browserify](https://github.com/substack/node-browserify#browser-field) browser-field in `pacakge.json`
[substack/browserify-handbook (package.json)](https://github.com/substack/browserify-handbook#packagejson)

### CLI

```
browserify -t [ foo -v --bar=555 ] main.js
```

### API

```
b.transform('foo', { v: true, bar: 555 })
```

### package.json

```
"browserify": {
  "transform": [
    [
      "foo",
      {
        v: true
        "bar": 555
      }
    ]
  ]
},
```

---

## transforms

[list of transforms · substack/node-browserify Wiki](https://github.com/substack/node-browserify/wiki/list-of-transforms)
[substack/browserify-handbook (transforms)](https://github.com/substack/browserify-handbook#transforms)
[npm browserify-transform](https://www.npmjs.com/browse/keyword/browserify-transform)

[substack/node-browserify](https://github.com/substack/node-browserify#browserifytransform)

## plugins

[npm browserify-plugin](https://www.npmjs.com/browse/keyword/browserify-plugin)

[substack/node-browserify (plugins)](https://github.com/substack/node-browserify#plugins)
[substack/browserify-handbook (plugins)](https://github.com/substack/browserify-handbook#plugins)

[css-modules/css-modulesify](https://github.com/css-modules/css-modulesify)
[css-modules/browserify-demo](https://github.com/css-modules/browserify-demo)

## tools

[browserify tools · substack/node-browserify Wiki](https://github.com/substack/node-browserify/wiki/browserify-tools)
[npm browserify-tool](https://www.npmjs.com/browse/keyword/browserify-tool)

## ecosystem

[substack/schoolbus](https://github.com/substack/schoolbus)
[substack/yarnify](https://github.com/substack/yarnify)
[substack/webworkify](https://github.com/substack/webworkify)

### Livereload

[chrisdickinson/beefy](https://github.com/chrisdickinson/beefy)
[milankinen/livereactload](https://github.com/milankinen/livereactload)

[AgentME/browserify-hmr](https://github.com/AgentME/browserify-hmr)
[substack/react-starter-hmr](https://github.com/substack/react-starter-hmr)

### browserify-shim

Use [thlorenz/browserify-shim](https://github.com/thlorenz/browserify-shim) to wrap non-CommonJS library to make them `require()`-able

[mattdesl/shimbro](https://github.com/mattdesl/shimbro)
[substack/browserify-handbook (browserify-shim)](https://github.com/substack/browserify-handbook#browserify-shim)

[browserify shim recipes · thlorenz/browserify-shim Wiki](https://github.com/thlorenz/browserify-shim/wiki/browserify-shim-recipes)

```js
// configure bundle files
"browser": {
  "jquery": "./js/vendor/jquery.js"
},
// configure require-mapping
"browserify-shim": {
  "jquery": "$"
  "three": "global:THREE"
}
```

jQuery will be bundled in `bundle.js`; and you are supposed to include `three.js` in HTML.

```sh
BROWSERIFYSHIM_DIAGNOSTICS=1 browserify -d . -o js/bundle.js
```

### bower

[taptapship/wiredep](https://github.com/taptapship/wiredep)

### testing

[how I write tests for node and the browser](http://substack.net/how_I_write_tests_for_node_and_the_browser)

[substack/testling](https://github.com/substack/testling)
Test in headless browser:
```sh
$ browserify test/beep.js | testling
```
[https://ci.testling.com](https://ci.testling.com/)

[substack/coverify](https://github.com/substack/coverify)
```sh
$ browserify -t coverify test/*.js | node | coverify
```
[substack/covert](https://github.com/substack/covert)
