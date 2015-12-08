title: "Node.js notes"
date: 2014-12-11 16:55:43
categories:
- comp.lang
tags:
- node-js
- notes
toc: true
---

[NodeJS Basics: An Introductory Training - YouTube](https://www.youtube.com/watch?v=G0924T2uoiY)

[sindresorhus/awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs)
[bcomnes/node-learnbook](https://github.com/bcomnes/node-learnbook)
[felixge/node-style-guide](https://github.com/felixge/node-style-guide)

[node-inspector/node-inspector](https://github.com/node-inspector/node-inspector) debugger on Blink Developer Tools

[Heroku | 10 Habits of a Happy Node Hacker (2016)](http://blog.heroku.com/archives/2015/11/10/node-habits-2016)

## Badges

[nodei.co](https://nodei.co/)
[Shields.io: Quality metadata badges for open source projects](http://shields.io/)
[bevry-badges · GitHub](https://github.com/bevry/badges)

[gendocs](https://www.npmjs.com/package/gendocs)

## Node.js on mobile

[JXcore · a Node.JS distribution with additional features](http://jxcore.com/home/)
[jxcore·io](http://jxcore.io/)

[paddybyers/anode](https://github.com/paddybyers/anode)

[Duktape](http://duktape.org/)

[JavaScript engine for Internet of Things](http://samsung.github.io/jerryscript/)
[Samsung/iotjs](https://github.com/Samsung/iotjs)
[JerryScript & IoT.js: JavaScript for IoT from Samsung](http://www.infoq.com/news/2015/08/iotjs-jerryscript-samsung)

## OS

### Runtime.js

[runtime.js – JavaScript library operating system for the cloud](http://runtimejs.org/)
[runtime.js — JavaScript library OS — Medium](https://medium.com/@iefserge/runtime-js-javascript-library-os-823ada1cc3c)
[Unikernels: Rise of the Virtual Library Operating System - ACM Queue](http://queue.acm.org/detail.cfm?id=2566628)

[An Introduction to Runtime.JS - PubNub](https://www.pubnub.com/blog/2015-01-27-introduction-runtime-js/)
[Sergii Iefremov: Runtime.JS: V8 JavaScript Kernel | JSConf EU 2014 - YouTube](https://www.youtube.com/watch?v=nPl0zlAI3MY)

### [Node OS](http://node-os.com/)

## Writing CLI apps

[Write your shell scripts in JavaScript, via Node.js](http://www.2ality.com/2011/12/nodejs-shell-scripting.html)
[Unix and Node: Command-line Arguments](http://dailyjs.com/2012/03/01/unix-node-arguments/)
[Unix and Node: Pipes and Streams](http://dailyjs.com/2012/03/08/unix-node-pipes/)
[Unix and Node: Signals](http://dailyjs.com/2012/03/15/unix-node-signals/)

[Command Line Utilities with Node.js | Shape Shed](http://shapeshed.com/command-line-utilities-with-nodejs/)
[Writing a Command Line Node Tool - Blog -- The JavaScript Playground](http://javascriptplayground.com/blog/2012/08/writing-a-command-line-node-tool)

[Popular cli modules - Node.JS Modules](https://nodejsmodules.org/tags/cli)

You can use `process.stdin` as input stream to accept pipe input:
```js
// choose input stream
const inputStream = (process.args.length > 2)?
  ? Fs.createReadStream(process.args[2])
  : process.stdin;
```

See [leesei/openslide-prop2json](https://github.com/leesei/openslide-prop2json).

[amwmedia-plop · GitHub](https://github.com/amwmedia/plop) file template generator, lighter then yeoman

### CLI argument parser

I need an option parser that auto generates the help page.

[tj/commander.js](https://github.com/tj/commander.js)
[bcoe/yargs](https://github.com/bcoe/yargs)

[indexzero-nconf · GitHub](https://github.com/indexzero/nconf) load and merge config files

[harthur-nomnom · GitHub](https://github.com/harthur/nomnom) (DEPRECATED)
[substack-node-optimist](https://github.com/substack/node-optimist) (DEPRECATED, succeeded by yargs)
[substack-minimist](https://github.com/substack/minimist) (naive, no help page)

#### frameworks

[weidagang-line-parser-js · GitHub](https://github.com/weidagang/line-parser-js) configuration over implementation
[Omelette by f](http://f.github.io/omelette/) generates event from given command and you only have to implement the handler
[dscape-frameless · GitHub](https://github.com/dscape/frameless) event framework for CLI app
[vdemedes-sushi · GitHub](https://github.com/vdemedes/sushi) Express for CLI

### sub-shell

These allows you to build a sub-shell or yeoman-like app.

[prompt](https://www.npmjs.org/package/prompt)
[readline-sync](https://www.npmjs.com/package/readline-sync)
[SBoudrias-Inquirer.js · GitHub](https://github.com/SBoudrias/Inquirer.js/)
[scottcorgan-nash · GitHub](https://github.com/scottcorgan/nash)
[scottcorgan-nash-usage · GitHub](https://github.com/scottcorgan/nash-usage)

[dthree-vorpal · GitHub](https://github.com/dthree/vorpal)
[dthree-vantage · GitHub](https://github.com/dthree/vantage)

### CLI interface

The equivalent of [ncurses](https://www.wikiwand.com/en/Ncurses) in Linux.

[chjj-blessed · GitHub](https://github.com/chjj/blessed)
[substack-node-charm · GitHub](https://github.com/substack/node-charm)
[substack/terminal-menu](https://github.com/substack/terminal-menu)

blessed derivative with markup support:
[yaronn/wopr](https://github.com/yaronn/wopr)
[yaronn-blessed-contrib · GitHub](https://github.com/yaronn/blessed-contrib)
[Yomguithereal-react-blessed · GitHub](https://github.com/Yomguithereal/react-blessed)

[madbence-node-drawille · GitHub](https://github.com/madbence/node-drawille) draw unicode braille characters

Workshop:
[workshopper/workshopper](https://github.com/workshopper/workshopper)
[substack/adventure](https://github.com/substack/adventure)

### Colorizer

[sindresorhus-chalk · GitHub](https://github.com/sindresorhus/chalk)
[Marak-colors.js · GitHub](https://github.com/Marak/colors.js) use chalk instead

[danielb2-purdy.js · GitHub](https://github.com/danielb2/purdy.js) colored object inspect

### Logger

Requirements:
- log to console and file simultaneously
- log rotation
- debug level
- search (optional)

[visionmedia-debug · GitHub](https://github.com/visionmedia/debug) support DEBUG in env to toggle log

[hapijs-good · GitHub](https://github.com/hapijs/good)
[bevry-caterpillar · GitHub](https://github.com/bevry/caterpillar)
[trentm-node-bunyan · GitHub](https://github.com/trentm/node-bunyan)
[winstonjs-winston · GitHub](https://github.com/winstonjs/winston)

[rvagg/bole](https://github.com/rvagg/bole) based on idea of bunyan generally, simple yet flexible API

## stream

[substack/stream-handbook](https://github.com/substack/stream-handbook)

[Readable, Writable, and Transform Streams in Node.js | Sanders DeNardi](http://www.sandersdenardi.com/readable-writable-transform-streams-node/)

[[r.va.gg] Why I don't use Node's core 'stream' module](https://r.va.gg/2014/06/why-i-dont-use-nodes-core-stream-module.html)
[rvagg/through2](https://github.com/rvagg/through2)

## npm

[Give Grunt the Boot! A Guide to Using npm as a Build Tool](http://www.sitepoint.com/guide-to-npm-as-a-build-tool/)
[You Might Not Need Gulp.js — Startups, Wanderlust, and Life Hacking — Medium](https://medium.com/swlh/you-might-not-need-gulp-js-89a0220487dd#.1z2zfrucg)
[How to Use npm as a Build Tool](http://blog.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/)
[task automation with npm run](http://substack.net/task_automation_with_npm_run)

Say you have a module written in ES6 (`src/main.js`), you can use this config to convert it to ES5 before publishing.

```json
{
    "scripts": {
      "prepublish": "babel -d lib src/"
    },
    "main": "lib/main.js",
    "dependencies": "babel@latest"
}
```

### `package.json`

[Package.json- an interactive guide](http://package.json.nodejitsu.com/)

### `require()` algorithm

[Modules Node.js Manual & Documentation](https://nodejs.org/docs/latest/api/modules.html#modules_all_together)
[substack/node-resolve](https://github.com/substack/node-resolve)

[Where Does Node.js And Require() Look For Modules?](http://www.bennadel.com/blog/2169-where-does-node-js-and-require-look-for-modules.htm)

## Native Modules

[Chrome V8 — Google Developers](https://developers.google.com/v8/)
[Create Wiki — V8 Cookbook](http://create.tpsitulsa.com/wiki/V8_Cookbook)
[v8- V8 API Reference Guide](http://izs.me/v8-docs/main.html)

[nodejs/nan](https://github.com/nodejs/nan)
[RisingStack/node-with-rust](https://github.com/RisingStack/node-with-rust)
