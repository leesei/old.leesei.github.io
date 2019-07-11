---
title: "JavaScript Pipeline"
categories:
  - web
toc: true
date: 2015-12-21 11:43:29
tags:
  - browserify
  - webpack
  - web-dev
---

[Understanding JavaScript Modules: Bundling & Transpiling](http://www.sitepoint.com/javascript-modules-bundling-transpiling/)
[Polyfills: everything you ever wanted to know, or maybe a bit less](https://hackernoon.com/polyfills-everything-you-ever-wanted-to-know-or-maybe-a-bit-less-7c8de164e423)
[Modern JavaScript Explained For Dinosaurs – Node.js Collection – Medium](https://medium.com/the-node-js-collection/modern-javascript-explained-for-dinosaurs-f695e9747b70)
[How to combine Webpack 4 and Babel 7 to create a fantastic React app](https://medium.freecodecamp.org/how-to-combine-webpack-4-and-babel-7-to-create-a-fantastic-react-app-845797e036ff)

[These tools will help you write clean code – freeCodeCamp.org](https://medium.freecodecamp.org/these-tools-will-help-you-write-clean-code-da4b5401f68e)
[Prepack · Partial evaluator for JavaScript](https://prepack.io/) optimizes code in build time

<!-- more -->

# Transpilers

[JavaScript Transpilers: What They Are & Why We Need Them | Scotch](https://scotch.io/tutorials/javascript-transpilers-what-they-are-why-we-need-them)

## Babel

[Babel · The compiler for writing next generation JavaScript](http://babeljs.io/)
[6.0.0 Released · Babel](https://babeljs.io/blog/2015/10/29/6.0.0/)
[Setting up Babel 6 · Babel](https://babeljs.io/blog/2015/10/31/setting-up-babel-6/)
[The Complete Guide to ES6 with Babel 6](http://jamesknelson.com/the-complete-guide-to-es6-with-babel-6/)
[Setting up ES6 | Leanpub](https://leanpub.com/setting-up-es6/read)
[Hail, Babel! The Transpiling Overlord -Telerik Developer Network](http://developer.telerik.com/featured/hail-babel-the-transpiling-overlord/)
[A Smart(er) Transpilation Strategy | getiblog](http://blog.getify.com/smarter-transpilation-strategy/)

[thejameskyle/babel-handbook: A guided handbook on how to use Babel and how to create plugins for Babel.](https://github.com/thejameskyle/babel-handbook)
[babel-handbook/README.md at master · thejameskyle/babel-handbook](https://github.com/thejameskyle/babel-handbook/blob/master/translations/en/README.md)
[Understanding ASTs by Building Your Own Babel Plugin](https://www.sitepoint.com/understanding-asts-building-babel-plugin/)

[results for babel-plugin](https://www.npmjs.com/search?q=babel-plugin)
[codemix/babel-plugin-closure-elimination](https://github.com/codemix/babel-plugin-closure-elimination)
[ooflorent/babel-plugin-graphql](https://github.com/ooflorent/babel-plugin-graphql)
[chocolateboy/babel-plugin-source-map-support](https://github.com/chocolateboy/babel-plugin-source-map-support)
[zloirock/core-js](https://github.com/zloirock/core-js) es6 shim used in Babel

```json
{
  "name": "wsi-viewer",
  "version": "1.0.0",
  "description": "",
  "main": "bundle.js",
  "scripts": {
    "build": "browserify src/index.js --debug | exorcist public/bundle.js.map | uglifyjs -cm > public/bundle.js",
    "watch": "watchify src/index.js -d -o public/bundle.js -v",
    "test": "tape test/*.js",
    "coverage": "covert test/*.js"
  },
  "author": "KY LEE <kylee@astri.org>",
  "browserify": {
    "transform": ["browserify-shim", "babelify"]
  },
  "browserify-shim": {
    "openseadragon": "global:OpenSeadragon"
  },
  "babel": {
    "presets": ["es2015", "react"]
  },
  "devDependencies": {
    "babel-preset-es2015": "^6.1.18",
    "babel-preset-react": "^6.1.18",
    "babelify": "^7.2.0",
    "browserify": "^12.0.1",
    "browserify-shim": "^3.8.11",
    "covert": "^1.1.0",
    "exorcist": "^0.4.0",
    "tape": "^4.2.2",
    "uglify-js": "^2.6.1",
    "watchify": "^3.6.1"
  },
  "dependencies": {}
}
```

## Closure Compiler

[Closure Compiler  |  Google Developers](https://developers.google.com/closure/compiler/)

## Installing the Right Version

[JavaScript needs the compile step (on install) | Better world by better software](https://glebbahmutov.com/blog/javascript-needs-compile-step/)
[Precompiled JavaScript | Better world by better software](https://glebbahmutov.com/blog/precompiled-javascript/)
[bahmutov/compiled: Compiles the ES\* bundle to your NodeJS version on install](https://github.com/bahmutov/compiled)

## Others

[esnext - Tomorrow’s JavaScript syntax today](http://esnext.github.io/esnext/#)

[Bublé – the blazing fast, batteries-included ES2015 compiler](https://buble.surge.sh/)
[Bublé Guide](https://buble.surge.sh/guide/)

[google/traceur-compiler](https://github.com/google/traceur-compiler)
[facebook/jstransform](https://github.com/facebook/jstransform)

---

# Minifiers

[babel/babili: An ES6+ aware minifier based on the Babel toolchain (beta)](https://github.com/babel/babili)
[estools/esmangle: esmangle is mangler / minifier for Mozilla Parser API AST](https://github.com/estools/esmangle)
[bholloway/esmangleify: A minifier browserify transform using esmangle](https://github.com/bholloway/esmangleify)
[UglifyJS — JavaScript parser, compressor, minifier written in JS](http://lisperator.net/uglifyjs/)

---

# CodeMod

[facebook/jscodeshift: A JavaScript codemod toolkit.](https://github.com/facebook/jscodeshift)
[cpojer/js-codemod: Codemod scripts to transform code to next generation JS](https://github.com/cpojer/js-codemod)

[Refactoring With Codemods and jscodeshift | Toptal](https://www.toptal.com/javascript/write-code-to-rewrite-your-code)
[Effective JavaScript Codemods – Christoph Pojer – Medium](https://medium.com/@cpojer/effective-javascript-codemods-5a6686bb46fb)

[Christoph Pojer: Evolving Complex Systems Incrementally | JSConf EU 2015 - YouTube](https://www.youtube.com/watch?v=d0pOgY8__JM)
[Master the Art of the AST & Take Control of Your JS (English) - YouTube](https://www.youtube.com/watch?v=Xt7PFzOBTPk)

---

# Bundlers

[Modular JavaScript: A Beginners Guide to SystemJS & jspm](http://www.sitepoint.com/modular-javascript-systemjs-jspm/)

[olegakbarov/webpack-vs-browserify](https://github.com/olegakbarov/webpack-vs-browserify)
[Journey from browserify to webpack — Medium](https://medium.com/@tomchentw/why-webpack-is-awesome-9691044b6b8e#.1gloc2xyv)
[Browserify VS Webpack - JS Drama](http://blog.namangoel.com/browserify-vs-webpack-js-drama)
[Webpack and Rollup: the same but different – webpack – Medium](https://medium.com/webpack/webpack-and-rollup-the-same-but-different-a41ad427058c)
[Comparing bundlers: Webpack, Rollup & Parcel – js@imaginea – Medium](https://medium.com/js-imaginea/comparing-bundlers-webpack-rollup-parcel-f8f5dc609cfd)

[pkg.module · rollup/rollup Wiki](https://github.com/rollup/rollup/wiki/pkg.module) instruct bundlers to use ES2015 modules

## Bundle size

[Reduce Your bundle.js File Size By Doing This One Thing](https://lacke.mn/reduce-your-bundle-js-file-size/)
[samccone/coverage-ext: Generate code coverage for any webpage](https://github.com/samccone/coverage-ext)

[webpack-contrib/webpack-bundle-analyzer: Webpack plugin and CLI utility that represents bundle content as convenient interactive zoomable treemap](https://github.com/webpack-contrib/webpack-bundle-analyzer)
[Webpack Visualizer](https://chrisbateman.github.io/webpack-visualizer/)
[131/discify: A browserify plugin to analyse bundle statistics](https://github.com/131/discify)
[danvk/source-map-explorer: Analyze and debug space usage through source maps](https://github.com/danvk/source-map-explorer)

---

# Browserify

[Browserify](http://browserify.org/)
[substack/browserify-handbook](https://github.com/substack/browserify-handbook)
[substack/browserify-handbook (builtins)](https://github.com/substack/browserify-handbook#builtins)

```sh
# export `require()` in browser and the module 'slugger'
browserify -r ./lib/slugger:slugger > static/bundle.js
```

UMD builds
[Forbes Lindesay — Standalone Browserify Builds](http://www.forbeslindesay.co.uk/post/46324645400/standalone-browserify-builds)

```sh
# can now use require.js/<script> to load `bundle.js`
browserify -s ./index.js > dist/bundle.js
```

Build for Node

```sh
browserify --node ./index.js > dist/bundle.js
```

[Getting Started with Browserify | Scotch](https://scotch.io/tutorials/getting-started-with-browserify)
[Cross platform JavaScript with Browserify - Sharing Code Between Node.js and the Browser - codecentric Blog : codecentric Blog](https://blog.codecentric.de/en/2014/02/cross-platform-javascript/)
[How to work with Browserify?](http://www.merixstudio.com/blog/how-work-browserify/)

[browserify for webpack users](https://gist.github.com/substack/68f8d502be42d5cd4942)
[browserify+stylus+babel+hotreload](https://gist.github.com/anonymous/b05e6549d2ee3a1e33e4)

[atomify/atomify](https://github.com/atomify/atomify)
[atomify/atomify-js](https://github.com/atomify/atomify-js)
[atomify/atomify-css](https://github.com/atomify/atomify-css)

## internals

[How Browserify Works](http://benclinkinbeard.com/posts/how-browserify-works/)
[Introduction to Browserify • Blake Embrey](http://blakeembrey.com/articles/2013/09/introduction-to-browserify/)
[substack/browserify-handbook (how browserify works)](https://github.com/substack/browserify-handbook#how-browserify-works)
[substack/browserify-handbook (bundling)](https://github.com/substack/browserify-handbook#bundling)
[Browserify V2 and You (nix) on Vimeo](https://vimeo.com/62988591)

## option passing

[substack/node-browserify](https://github.com/substack/node-browserify#browser-field) browser-field in `pacakge.json`
[substack/browserify-handbook (package.json)](https://github.com/substack/browserify-handbook#packagejson)
[substack/subarg: parse arguments with recursive contexts](https://github.com/substack/subarg)

### CLI

```
browserify -t [ foo -v --bar=555 ] main.js
```

### API

```js
var bundler = browserify("main.js");

bundler.transform("foo", {
  v: true,
  bar: 555
});

bundler.bundle().pipe(process.stdout);
```

```js
var bundler = browserify({ debug: true });

bundler
  .add("index.js")
  .transform("uglifyify")
  .bundle()
  .pipe(process.stdout);
```

### package.json

```json
"browserify": {
  "transform": [
    [
      "foo",
      {
        "v": true,
        "bar": 555
      }
    ]
  ]
},
```

## transforms

[substack/node-browserify (transforms)](https://github.com/substack/node-browserify#browserifytransform)
[substack/browserify-handbook (transforms)](https://github.com/substack/browserify-handbook#transforms)
[list of transforms · substack/node-browserify Wiki](https://github.com/substack/node-browserify/wiki/list-of-transforms)
[npm browserify-transform](https://www.npmjs.com/browse/keyword/browserify-transform)

[babel/babelify](https://github.com/babel/babelify)

The ordering of transforms matters, run `babelify` first since transforms doesn't understand ES6:

```json
  "browserify": {
    "transform": [
      "babelify",
      "browserify-shim",
      "require-globify"
    ]
  },
```

## plugins

[substack/node-browserify (plugins)](https://github.com/substack/node-browserify#plugins)
[substack/browserify-handbook (plugins)](https://github.com/substack/browserify-handbook#plugins)
[npm browserify-plugin](https://www.npmjs.com/browse/keyword/browserify-plugin)

[browserify for webpack users](https://gist.github.com/substack/68f8d502be42d5cd4942#gistcomment-1615377) using cssify

### dom

[Matt-Esch/virtual-dom: A Virtual DOM and diffing algorithm](https://github.com/Matt-Esch/virtual-dom)
[substack/hyperx: tagged template string virtual dom builder](https://github.com/substack/hyperx)
[substack/hyperglue: update html elements by mapping query selectors to attributes, text, and hypertext](https://github.com/substack/hyperglue)

### styles

[substack/insert-css: insert a string of css into the <head>](https://github.com/substack/insert-css)

[davidguttman/cssify: Simple middleware for Browserify to add css styles to the browser.](https://github.com/davidguttman/cssify) using css-module
[css-modules/css-modulesify: A browserify plugin to load CSS Modules](https://github.com/css-modules/css-modulesify)

[stackcss/sheetify: Modular CSS bundler for browserify](https://github.com/stackcss/sheetify)
[stackcss/css-extract: Extract CSS from a browserify bundle](https://github.com/stackcss/css-extract) create a `.css` file

## server

[mattdesl/budo: a dev server for rapid prototyping](https://github.com/mattdesl/budo)
[andyinabox/budo-demo: A tool for quickly building budo projects](https://github.com/andyinabox/budo-demo)
[joseluisq/node-random-strings-demo: Random strings demo using Budo + Browserify](https://github.com/joseluisq/node-random-strings-demo)
[jumpsuit/jumpsuit: Jump in. Zip up. Build great apps.](https://github.com/jumpsuit/jumpsuit)
[css-modules/browserify-demo: A working demo of CSS Modules, using css-modulesify](https://github.com/css-modules/browserify-demo) using budo
[mattdesl/prot: highly opinionated dev environment [Proof of concept]](https://github.com/mattdesl/prot)
[remixz/run-js: A prototyping server that just works.](https://github.com/remixz/run-js)

[HenrikJoreteg/moonboots: A set of conventions and tools for bundle and serving clientside apps with node.js](https://github.com/HenrikJoreteg/moonboots)
[wraithgar/moonboots_hapi: Hapi plugin for moonboots](https://github.com/wraithgar/moonboots_hapi)
[lukekarrys/moonboots-static: A static build plugin for moonboots.](https://github.com/lukekarrys/moonboots-static)

[mattdesl/watchify-server: a bare-bones development server for watchify](https://github.com/mattdesl/watchify-server)

[yoshuawuyts/bankai: DIY asset server](https://github.com/yoshuawuyts/bankai)

[mattdesl/garnish: prettifies ndjson from wzrd and similar tools](https://github.com/mattdesl/garnish) Prettifies ndjson or bole logs from budo, wzrd and other tools.

## tools

[browserify tools · substack/node-browserify Wiki](https://github.com/substack/node-browserify/wiki/browserify-tools)
[npm browserify-tool](https://www.npmjs.com/browse/keyword/browserify-tool)

## lazy loading

[Journey from RequireJS to Browserify - Esa-Matti Suuronen](http://esa-matti.suuronen.org/blog/2013/03/22/journey-from-requirejs-to-browserify/)
[A Journey From Require.js to Browserify – Oren Farhi – Thoughts On Javascript and Development](http://orizens.com/wp/topics/a-journey-from-require-js-to-browserify/)
[Asynchronous module loading with Browserify - Esa-Matti Suuronen](http://esa-matti.suuronen.org/blog/2013/04/15/asynchronous-module-loading-with-browserify/)
[scriptjs](https://www.npmjs.com/package/scriptjs)

[Browserify, why and how?](http://www.jeromesteunou.net/browserify-why-and-how.html) External & require

[niksy/browserify-require-async: Browserify transform to handle require.async calls.](https://github.com/niksy/browserify-require-async)
[substack/factor-bundle: factor browser-pack bundles into common shared bundles](https://github.com/substack/factor-bundle)
[arian/partition-bundle: A browserify plugin to partition your modules in different bundles](https://github.com/arian/partition-bundle)

## ecosystem

[substack/schoolbus](https://github.com/substack/schoolbus)
[substack/yarnify](https://github.com/substack/yarnify)
[substack/webworkify](https://github.com/substack/webworkify)

### Livereload

> Use Browsersync instead of livereload
> see `web-development.md#browsersync`

[chrisdickinson/beefy](https://github.com/chrisdickinson/beefy)
[B E E F Y | a tiny browserify server](http://didact.us/beefy/)

[milankinen/livereactload](https://github.com/milankinen/livereactload)

[Kureev/browserify-react-live](https://github.com/Kureev/browserify-react-live)
[Kureev/browserify-patch-server](https://github.com/Kureev/browserify-patch-server)

[React Live Demo](https://react-live.kitten.sh/)
[FormidableLabs/react-live: A production-focused playground for live editing React components](https://github.com/FormidableLabs/react-live)
[FormidableLabs/component-playground: A component for rendering React components with editable source and live preview](https://github.com/formidablelabs/component-playground)

[A Minimal Example of HMR in a Redux Application | Toptal](https://www.toptal.com/javascript/hot-module-replacement-in-redux)
[AgentME/browserify-hmr](https://github.com/AgentME/browserify-hmr)
[AgentME/ud](https://github.com/AgentME/ud)
[substack/react-starter-hmr](https://github.com/substack/react-starter-hmr)
[AgentME/react-hot-transform](https://github.com/AgentME/react-hot-transform)

### browserify-shim

Use [thlorenz/browserify-shim](https://github.com/thlorenz/browserify-shim) to wrap non-CommonJS library to make them `require()`-able

[mattdesl/shimbro](https://github.com/mattdesl/shimbro)
[substack/browserify-handbook (browserify-shim)](https://github.com/substack/browserify-handbook#browserify-shim)
[browserify shim recipes · thlorenz/browserify-shim Wiki](https://github.com/thlorenz/browserify-shim/wiki/browserify-shim-recipes)

```js
{
  // using different files for browser
  "browser": {
    "jquery": "./js/vendor/jquery.js"
  },
  // configure require-mapping
  "browserify-shim": {
    "jquery": "global:$"
    "three": "global:THREE"
  }
}
```

jQuery will be bundled in `bundle.js`; and you are supposed to include `three.js` in HTML.

```sh
BROWSERIFYSHIM_DIAGNOSTICS=1 browserify -d . -o js/bundle.js
```

### watchify

watchify wrapped browserify is as good as browserify

```js
var b = browserify(opts);
if (opts.watch) {
  b = watchify(b);
}
```

[gulp/fast-browserify-builds-with-watchify.md at master · gulpjs/gulp](https://github.com/gulpjs/gulp/blob/master/docs/recipes/fast-browserify-builds-with-watchify.md)

### dynamic requires

[javascript - Compiling dynamically required modules with Browserify - Stack Overflow](http://stackoverflow.com/questions/21642398/compiling-dynamically-required-modules-with-browserify)
[capaj/require-globify](https://github.com/capaj/require-globify)
[substack/bulkify](https://github.com/substack/bulkify)

### bower

[taptapship/wiredep](https://github.com/taptapship/wiredep)
[eugeneware/debowerify](https://github.com/eugeneware/debowerify)

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

### Online Conversion

[Browserify-CDN](https://wzrd.in/) official
[Browserify CDN](https://www.brcdn.org/)

---

# Webpack

Webpack does too much magic behind the scene.
The config file syntax has been simplified and docs improved in 2.0 release.

[webpack](https://webpack.js.org/)
[Configuration](https://webpack.js.org/configuration/)
[webpack – Medium](https://medium.com/webpack)
[webpack for browserify users](http://webpack.github.io/docs/webpack-for-browserify-users.html)

[webpack-contrib/awesome-webpack: A curated list of awesome Webpack resources, libraries and tools](https://github.com/webpack-contrib/awesome-webpack)

[Learn Using Webpack for the First Time – Webpack 4 Fundamentals](https://frontendmasters.com/courses/webpack-fundamentals/using-webpack-for-the-first-time/)
[The Core Concepts | webpack learning academy](https://webpack.academy/p/the-core-concepts)

[Lessons Learned From a Year of Fighting With Webpack and Babel](https://levelup.gitconnected.com/lessons-learned-from-a-year-of-fighting-with-webpack-and-babel-ce3b4b634c46)

[Learn Webpack - Best Webpack Tutorials (2019) | gitconnected](https://gitconnected.com/learn/webpack)
[Webpack 4: Universal Code Splitting in React… The inventors are back baby!](https://medium.com/@ScriptedAlchemy/webpack-4-universal-code-splitting-in-react-the-inventors-are-back-baby-453745f9665d)
[Setting up webpack 4 for a project - DEV Community 👩‍💻👨‍💻](https://dev.to/teroauralinna/setting-up-webpack-4-for-a-project-5f5e)

[GoogleChromeLabs/webpack-libs-optimizations: Using a library in your webpack project? Here’s how to optimize it](https://github.com/GoogleChromeLabs/webpack-libs-optimizations)

[SurviveJS - Webpack](https://survivejs.com/webpack/)
[Webpack - From Apprentice to Journeyman](http://presentations.survivejs.com/webpack-from-apprentice-to-journeyman/#/)
[Webpack - From Journeyman to Master](https://presentations.survivejs.com/webpack-from-journeyman-to-master/#/)
[Re-imagining Webpack](https://presentations.survivejs.com/re-imagining-webpack/#/)

[Backend Apps with Webpack (Part I)](http://jlongster.com/Backend-Apps-with-Webpack--Part-I)
[Backend Apps with Webpack: Driving with Gulp (Part II)](http://jlongster.com/Backend-Apps-with-Webpack--Part-II)
[Live Editing JavaScript with Webpack (Part III)](http://jlongster.com/Backend-Apps-with-Webpack--Part-III)

[petehunt/webpack-howto](https://github.com/petehunt/webpack-howto)
[OSCON 2014: How Instagram.com Works; Pete Hunt - YouTube](https://www.youtube.com/watch?v=VkTCL6Nqm6Y)

[Using ES6 and ES7 in the Browser, with Babel 6 and Webpack](http://jamesknelson.com/using-es6-in-the-browser-with-babel-6-and-webpack/)
[Webpack Made Simple - Building ES6 & LESS w/ autorefresh](http://jamesknelson.com/webpack-made-simple-build-es6-less-with-autorefresh-in-26-lines/)
[liady/webpack-node-externals: Easily exclude node modules in Webpack](https://github.com/liady/webpack-node-externals)

[Webpack — The Confusing Parts — Medium](https://medium.com/@rajaraodv/webpack-the-confusing-parts-58712f8fcad9#.ufwhgyu5f)

Minimal `webpack.config.js`:

```js
var webpack = require("webpack");
var path = require("path");

var BUILD_DIR = path.resolve(__dirname, "src/client/public");
var APP_DIR = path.resolve(__dirname, "src/client/app");

var config = {
  entry: APP_DIR + "/index.jsx",
  output: {
    path: BUILD_DIR,
    filename: "bundle.js"
  }
};

module.exports = config;
```

Adding loader:

```js
var config = {
  // Existing Code ....
  module: {
    loaders: [
      {
        test: /\.jsx?/,
        include: APP_DIR,
        loader: "babel"
      }
    ]
  }
};
```

## server

[facebookincubator/create-react-app: Create React apps with no build configuration.](https://github.com/facebookincubator/create-react-app) !important
[Fullstack React: How to get "create-react-app" to work with your API](https://www.fullstackreact.com/articles/using-create-react-app-with-a-server/)

[Minimal Webpack and React Starter boilerplate.. Seriously?!](https://medium.com/@hashem.khalifa/minimal-webpack-and-react-starter-boilerplate-seriously-d90a673e134f)

[coryhouse/react-slingshot: React + Redux starter kit / boilerplate with Babel, hot reloading, testing, linting and a working example app built in](https://github.com/coryhouse/react-slingshot)

[Introduction · Neutrino](https://neutrino.js.org/)
[mozilla-neutrino/neutrino-dev: Create and build modern JavaScript applications with zero initial configuration.](https://github.com/mozilla-neutrino/neutrino-dev)
[Modern JavaScript Apps with Neutrino](https://davidwalsh.name/neutrino)

[insin/nwb: A toolkit for React, Preact & Inferno apps, React libraries and other npm modules for the web, with no configuration (until you need it)](https://github.com/insin/nwb)
[petehunt/rwb](https://github.com/petehunt/rwb)
[mzabriskie/rackt-cli: Command line interface for automating common tasks when building React.js components](https://github.com/mzabriskie/rackt-cli)

[zeit/next.js: Framework for server-rendered React apps](https://github.com/zeit/next.js)

---

# Rollup.js

[rollup.js](http://rollupjs.org/)
[rollup.js guide](http://rollupjs.org/guide/)
[frostney/rollup-babel-lib-bundler: Utility to bundle JavaScript libraries with Rollup](https://github.com/frostney/rollup-babel-lib-bundler)

[Webpack and Rollup: the same but different – webpack – Medium](https://medium.com/webpack/webpack-and-rollup-the-same-but-different-a41ad427058c)

https://github.com/rollup/rollup/wiki/Plugins

https://github.com/rollup/rollup-plugin-babel
https://github.com/rollup/rollup-plugin-commonjs
https://github.com/rollup/rollup-plugin-node-resolve

# FuseBox

[FuseBox - Blazing fast js bundler/loader with super powers](https://fuse-box.org/)
[fuse-box/fuse-box: A blazing fast js bundler/loader with a comprehensive API](https://github.com/fuse-box/fuse-box)

# Parcel

[📦 Parcel](https://parceljs.org/)
[parcel-bundler/awesome-parcel: 🔗 A curated list of awesome Parcel resources, libraries, tools and boilerplates](https://github.com/parcel-bundler/awesome-parcel)

[parcel-bundler/awesome-parcel: 🔗 A curated list of awesome Parcel resources, libraries, tools and boilerplates](https://github.com/parcel-bundler/awesome-parcel)

[Everything You Need To Know About Parcel: The Blazing Fast Web App Bundler 🚀](https://medium.freecodecamp.org/all-you-need-to-know-about-parcel-dbe151b70082)
[Parcel vs webpack - Jakob Lind](http://blog.jakoblind.no/parcel-webpack/)

[Using Parcel as a Bundler for React Applications | CSS-Tricks](https://css-tricks.com/using-parcel-as-a-bundler-for-react-applications/)

[Parcel bundler: Like Webpack but effortless | InfoWorld](https://www.infoworld.com/article/3337242/javascript/parcel-bundler-like-webpack-but-effortless.html)
[Parcel bundler: Testing Parcel’s asset support | InfoWorld](https://www.infoworld.com/article/3338085/javascript/parcel-bundler-testing-parcels-asset-support.html)
[Parcel bundler: Production builds and best practices | InfoWorld](https://www.infoworld.com/article/3340378/javascript/parcel-bundler-production-builds-and-best-practices.html)

# Pika

[Pika - Search npm for fast, modern packages.](https://www.pikapkg.com/)
[A Future Without Webpack - Pika](https://www.pikapkg.com/blog/pika-web-a-future-without-webpack/)

# Packem

[Packem – A precompiled JavaScript module bundler](https://packem.github.io/)
[packem/packem: 📦⚡ A precompiled JavaScript module bundler](https://github.com/packem/packem)

[Introducing Packem: a super fast experimental bundler written in Rust](https://medium.freecodecamp.org/introducing-packem-a-super-fast-experimental-bundler-written-in-rust-e981af875517)
