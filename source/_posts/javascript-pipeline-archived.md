---
title: "JavaScript Pipeline (archived)"
categories:
  - web
toc: true
date: 2021-02-26 11:43:29
tags:
  - browserify
  - webpack
  - web-dev
  - bundler
---

# Transpilers

> these are usually embedded in pipelines and we don't use it directly

[JavaScript Transpilers: What They Are & Why We Need Them | Scotch](https://scotch.io/tutorials/javascript-transpilers-what-they-are-why-we-need-them)

[Overview - Editions](https://editions.bevry.me/) Editions are the best way to produce and consume the JavaScript packages you care about. With Editions you can produce packages beautifully, and consume packages perfectly.

## Babel

[Babel · The compiler for next generation JavaScript](https://babeljs.io/)
[6.0.0 Released · Babel](https://babeljs.io/blog/2015/10/29/6.0.0/)
[Setting up Babel 6 · Babel](https://babeljs.io/blog/2015/10/31/setting-up-babel-6/)
[The Complete Guide to ES6 with Babel 6](http://jamesknelson.com/the-complete-guide-to-es6-with-babel-6/)
[Setting up ES6 | Leanpub](https://leanpub.com/setting-up-es6/read)
[Hail, Babel! The Transpiling Overlord -Telerik Developer Network](http://developer.telerik.com/featured/hail-babel-the-transpiling-overlord/)
[A Smart(er) Transpilation Strategy | getiblog](http://blog.getify.com/smarter-transpilation-strategy/)

[jamiebuilds/babel-handbook: A guided handbook on how to use Babel and how to create plugins for Babel.](https://github.com/jamiebuilds/babel-handbook)
[babel-handbook/README.md at master · jamiebuilds/babel-handbook](https://github.com/jamiebuilds/babel-handbook/blob/master/translations/en/README.md)
[Understanding ASTs by Building Your Own Babel Plugin](https://www.sitepoint.com/understanding-asts-building-babel-plugin/)
[Writing custom Babel and ESLint plugins with ASTs - Kent C. Dodds](https://kentcdodds.com/talks/#writing-custom-babel-and-es-lint-plugins-with-as-ts)

[Zero-config code transformation with babel-plugin-macros · Babel](https://babeljs.io/blog/2017/09/11/zero-config-with-babel-macros)
[All about macros with babel-plugin-macros 🎣 - Kent C. Dodds](https://kentcdodds.com/talks/#all-about-macros-with-babel-plugin-macros)

[results for babel-plugin](https://www.npmjs.com/search?q=babel-plugin)
[codemix/babel-plugin-closure-elimination](https://github.com/codemix/babel-plugin-closure-elimination)
[ooflorent/babel-plugin-graphql](https://github.com/ooflorent/babel-plugin-graphql)
[chocolateboy/babel-plugin-source-map-support](https://github.com/chocolateboy/babel-plugin-source-map-support)
[tleunen/babel-plugin-module-resolver: Custom module resolver plugin for Babel](https://github.com/tleunen/babel-plugin-module-resolver)
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

[Closure Compiler | Google Developers](https://developers.google.com/closure/compiler/)

## Installing the Right Version

[JavaScript needs the compile step (on install) | Better world by better software](https://glebbahmutov.com/blog/javascript-needs-compile-step/)
[Precompiled JavaScript | Better world by better software](https://glebbahmutov.com/blog/precompiled-javascript/)
[bahmutov/compiled: Compiles the ES\* bundle to your NodeJS version on install](https://github.com/bahmutov/compiled)

---

# Minifiers

[babel/minify: An ES6+ aware minifier based on the Babel toolchain (beta)](https://github.com/babel/minify)
[estools/esmangle: esmangle is mangler / minifier for Mozilla Parser API AST](https://github.com/estools/esmangle)
[bholloway/esmangleify: A minifier browserify transform using esmangle](https://github.com/bholloway/esmangleify)
[UglifyJS — JavaScript parser, compressor, minifier written in JS](http://lisperator.net/uglifyjs/)

[terser · JavaScript parser, mangler and compressor toolkit for ES6+](https://terser.org/)
[terser/terser: 🗜 JavaScript parser, mangler and compressor toolkit for ES6+](https://github.com/terser/terser)

---

# Webpack

Webpack does too much magic behind the scene.
The config file syntax has been simplified and docs improved in v2 release. v4 updated API and hence new recommended sets of plugins.
Beware of articles for old version.

[webpack](https://webpack.js.org/)
[Configuration](https://webpack.js.org/configuration/)

[Webpack your bags - madewithlove](https://madewithlove.com/blog/software-engineering/webpack-your-bags/) from the first principle
[Get to Know Webpack | recallact.com](https://www.recallact.com/presentation/get-know-webpack)
[Learn Webpack - Best Webpack Tutorials (2020) | gitconnected](https://gitconnected.com/learn/webpack)
[webpack for browserify users](http://webpack.github.io/docs/webpack-for-browserify-users.html)

[webpack-contrib/awesome-webpack: A curated list of awesome Webpack resources, libraries and tools](https://github.com/webpack-contrib/awesome-webpack)
[Lessons Learned From a Year of Fighting With Webpack and Babel](https://levelup.gitconnected.com/lessons-learned-from-a-year-of-fighting-with-webpack-and-babel-ce3b4b634c46)
[A Complete Webpack Setup for React - The Startup - Medium](https://medium.com/swlh/a-complete-webpack-setup-for-react-e56a2edf78ae)

[3 ways webpack surprises web developers - rossta.net](https://rossta.net/blog/three-ways-webpack-surprises-rails-developers.html)
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
[Webpack your bags - madewithlove](https://madewithlove.be/webpack-your-bags/) 2015

[How to boost the speed of your webpack build? - DEV Community](https://dev.to/slashgear_/how-to-boost-the-speed-of-your-webpack-build-16h0)

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
    filename: "bundle.js",
  },
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
        loader: "babel",
      },
    ],
  },
};
```

---

# Browserify

> this is kept for archival purposes as there are now better tools

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
  bar: 555,
});

bundler.bundle().pipe(process.stdout);
```

```js
var bundler = browserify({ debug: true });

bundler.add("index.js").transform("uglifyify").bundle().pipe(process.stdout);
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

## budo

[mattdesl/budo: a dev server for rapid prototyping](https://github.com/mattdesl/budo)
[andyinabox/budo-demo: A tool for quickly building budo projects](https://github.com/andyinabox/budo-demo)
[joseluisq/node-random-strings-demo: Random strings demo using Budo + Browserify](https://github.com/joseluisq/node-random-strings-demo)
[css-modules/browserify-demo: A working demo of CSS Modules, using css-modulesify](https://github.com/css-modules/browserify-demo) using budo
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
