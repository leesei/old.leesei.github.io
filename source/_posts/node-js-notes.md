---
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

[maxogden/art-of-node: a short introduction to node.js](https://github.com/maxogden/art-of-node)
[sindresorhus/awesome-nodejs](https://github.com/sindresorhus/awesome-nodejs)
[bcomnes/node-learnbook](https://github.com/bcomnes/node-learnbook)
[felixge/node-style-guide](https://github.com/felixge/node-style-guide)

[Modern Modules – Mikeal – Medium](https://medium.com/@mikeal/modern-modules-d99b6867b8f1)
[Node.js Best Practices - How to become a better Node.js developer in 2018](https://nemethgergely.com/nodejs-best-practices-how-to-become-a-better-developer-in-2018/)
[The Node Way](http://thenodeway.io/)
[Node Labs](http://www.nodelabs.org/)
[Node v4.0.0](https://talks.continuation.io/nova-node-meetup-9-15/#/) History
[The definitive Node.js handbook – freeCodeCamp.org](https://medium.freecodecamp.org/the-definitive-node-js-handbook-6912378afc6e)
[nodejs/Release: Node.js Foundation Release Working Group](https://github.com/nodejs/Release) release cadence

[Node Hero - Getting Started With Node.js | @RisingStack](https://blog.risingstack.com/node-hero-tutorial-getting-started-with-node-js/) !important
[A Node.JS Holiday Season Articles ★ Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/category/a-node-js-holiday-season/) (2012)
[Heroku | 10 Habits of a Happy Node Hacker (2016)](http://blog.heroku.com/archives/2015/11/10/node-habits-2016)

[How to get A+ on the SSL Labs test in node.js](https://certsimple.com/blog/a-plus-node-js-ssl)

## ES6

[ECMAScript 2015 (ES6) and beyond | Node.js](https://nodejs.org/en/docs/es6/)
[Node.js ES2015/ES6 support](http://node.green/)

## Video

[Node Tuts](http://nodetuts.com/index.html)
[Learn All The Nodes](http://www.learnallthenodes.com/)
[NodeJS Fan - YouTube](https://www.youtube.com/channel/UChTJTbr5kf3hYazJZO-euHg)

## Debugging

[Debugger | Node.js Documentation](https://nodejs.org/docs/latest/api/debugger.html)
[Debugging - Getting Started | Node.js](https://nodejs.org/en/docs/guides/debugging-getting-started/)
[Debugging Node.js with Chrome DevTools – Paul Irish – Medium](https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27)

```sh
node --inspect-brk app.js
# enable inspector, break on app start
# https://github.com/nodejs/node/pull/6792
```

[GoogleChromeLabs/ndb: ndb is an improved debugging experience for Node.js, enabled by Chrome DevTools](https://github.com/GoogleChromeLabs/ndb) a standalone Chromium instance as debugger

[Chrome DevTools - Debugging Node.js Application Using ndb](https://nitayneeman.com/posts/debugging-nodejs-application-in-chrome-devtools-using-ndb/)

[Easily identify problems in Node.js applications with Diagnostic Report](https://medium.com/the-node-js-collection/easily-identify-problems-in-node-js-applications-with-diagnostic-report-dc82370d8029)

[Supercharge your debugging experience for Node.js – Indrek Lasn – Medium](https://medium.com/@wesharehoodies/supercharge-your-debugging-experience-for-node-js-3f0ddfaffbb2)
[Debugging Node.js applications using core dumps - Reaktor](https://reaktor.com/blog/debugging-node-js-applications-using-core-dumps/)
[How to Debug a Node.js app in a Docker Container | @RisingStack](https://blog.risingstack.com/how-to-debug-a-node-js-app-in-a-docker-container/)

[joyent/node-stackvis: Stacktrace visualization tools](https://github.com/joyent/node-stackvis)
[defunctzombie/node-superstack: long stack traces for node.js](https://github.com/defunctzombie/node-superstack)
[mattinsler/longjohn: Long stack traces for node.js inspired](https://github.com/mattinsler/longjohn)
[davidmarkclements/cute-stack: Cute up your stack traces in Node](https://github.com/davidmarkclements/cute-stack)
[stacktracejs/stacktrace.js: Framework-agnostic, micro-library for getting stack traces in all web browsers](https://github.com/stacktracejs/stacktrace.js)

[An Introduction to the AsyncListener API](https://datahero.com/blog/2014/08/28/introduction-node-js-asynclistener-api/)
[Lessons learned from async listener · Issue #28 · node-forward/discussions](https://github.com/node-forward/discussions/issues/28)
[othiym23/node-continuation-local-storage: implementation of https://github.com/joyent/node/issues/5243](https://github.com/othiym23/node-continuation-local-storage)
[othiym23/async-listener: polyfill version of the 0.11 version of the asyncListener API](https://github.com/othiym23/async-listener)
[Node.js: Continuation-Local-Storage and the Magic of AsyncListener](http://www.slideshare.net/isharabash/cls-and-asynclistener)
[Conquering Asynchronous Context with CLS](http://fredkschott.com/post/2014/02/conquering-asynchronous-context-with-cls/)

Obsoleted:
[node-inspector/node-inspector](https:// github.com/node-inspector/node-inspector) debugger on Blink Developer Tools, deprecates since Node.js included the built-in `--inspect` in 6.3
[Debugging node.js in Docker using Node Inspector](https://keylocation.sg/our-tech/debugging-nodejs-in-docker-using-node-inspector)
[s-a/iron-node: Debug Node.js code with Chrome Developer Tools.](https://github.com/s-a/iron-node) debugger on Electron

## Threading

[A complete guide to threads in Node.js – LogRocket](https://blog.logrocket.com/a-complete-guide-to-threads-in-node-js-4fa3898fe74f)
[Using worker_threads in Node.js – Rich Trott – Medium](https://medium.com/@Trott/using-worker-threads-in-node-js-80494136dbb6)
[node.js - Nodejs worker threads shared object/store - Stack Overflow](https://stackoverflow.com/questions/51053222/nodejs-worker-threads-shared-object-store)
[Limiting concurrent operations in JavaScript – freeCodeCamp.org](https://medium.freecodecamp.org/how-to-limit-concurrent-operations-in-javascript-b57d7b80d573)

[laverdet/node-fibers: Fiber/coroutine support for v8 and node.](https://github.com/laverdet/node-fibers)

## async_hook

[Async Hooks | Node.js Documentation](https://nodejs.org/docs/latest/api/async_hooks.html)
[A Pragmatic Overview of Async Hooks API in Node.js – ITNEXT](https://itnext.io/a-pragmatic-overview-of-async-hooks-api-in-node-js-e514b31460e9)

## OS

### Runtime.js

[runtime.js – JavaScript library operating system for the cloud](http://runtimejs.org/)
[runtime.js — JavaScript library OS — Medium](https://medium.com/@iefserge/runtime-js-javascript-library-os-823ada1cc3c)
[Unikernels: Rise of the Virtual Library Operating System - ACM Queue](http://queue.acm.org/detail.cfm?id=2566628)

[An Introduction to Runtime.JS - PubNub](https://www.pubnub.com/blog/2015-01-27-introduction-runtime-js/)
[Sergii Iefremov: Runtime.JS: V8 JavaScript Kernel | JSConf EU 2014 - YouTube](https://www.youtube.com/watch?v=nPl0zlAI3MY)

### [Node OS](http://node-os.com/)

[NodeOS](https://github.com/NodeOS)

## Writing CLI apps

[Write your shell scripts in JavaScript, via Node.js](http://www.2ality.com/2011/12/nodejs-shell-scripting.html)
[Unix and Node: Command-line Arguments](http://dailyjs.com/2012/03/01/unix-node-arguments/)
[Unix and Node: Pipes and Streams](http://dailyjs.com/2012/03/08/unix-node-pipes/)
[Unix and Node: Signals](http://dailyjs.com/2012/03/15/unix-node-signals/)

[Command Line Utilities with Node.js | Shape Shed](http://shapeshed.com/command-line-utilities-with-nodejs/)
[Writing Command Line Tools with Node](http://javascriptplayground.com/blog/2015/03/node-command-line-tool/)

[Popular cli modules - Node.JS Modules](https://nodejsmodules.org/tags/cli)

[amwmedia-plop](https://github.com/amwmedia/plop) file template generator, lighter then yeoman

[zeit/pkg: Package your Node.js project into an executable](https://github.com/zeit/pkg)

### Accept pipe

You can use `process.stdin` as input stream to accept pipe input:

```js
/* choose input stream */
const inputStream =
  process.args.length > 2
    ? Fs.createReadStream(process.args[2])
    : process.stdin;
```

See [leesei/openslide-prop2json](https://github.com/leesei/openslide-prop2json).

### CLI argument parser

I need an option parser that auto generates the help page.

[yargs/yargs: yargs the modern, pirate-themed successor to optimist.](https://github.com/yargs/yargs) [Docs](http://yargs.js.org/docs/index.html) [Yargs cheatsheet](http://ricostacruz.com/cheatsheets/yargs.html)
[Yargs 4.0 Is Here - Commands 2.0](http://yargs.js.org/2016/02/13/yargs-4.html#commands-20)

[hapijs/bossy: Command line options parser](https://github.com/hapijs/bossy)
[scottcorgan/nash](https://github.com/scottcorgan/nash) (under evaluation)
[sindresorhus/meow](https://github.com/sindresorhus/meow) (under evaluation)
[leo/args: Minimal toolkit for building CLIs](https://github.com/leo/args) built on minimist
[tj/commander.js](https://github.com/tj/commander.js) is [quirky](https://github.com/tj/commander.js/issues/400) when using coercion and default value together

[substack-minimist](https://github.com/substack/minimist) (naive, no help page)
[harthur-nomnom](https://github.com/harthur/nomnom) (DEPRECATED)
[substack-node-optimist](https://github.com/substack/node-optimist) (DEPRECATED, succeeded by yargs)

#### CLI wrapper

[sindresorhus/dargs: Reverse minimist. Convert an object of options into an array of command-line arguments](https://github.com/sindresorhus/dargs)
[ShellJS](http://documentup.com/shelljs/shelljs)
[sindresorhus/execa: A better `child_process`](https://github.com/sindresorhus/execa#readme)

#### config files/env

[davidtheclark/cosmiconfig: Find and load configuration from a package.json property, rc file, or CommonJS module](https://github.com/davidtheclark/cosmiconfig)
[AdrieanKhisbe/configue: Configue All the Things.js](https://github.com/AdrieanKhisbe/configue)
[indexzero-nconf](https://github.com/indexzero/nconf) load and merge config files
[bevry/envfile](https://github.com/bevry/envfile)
[defunctzombie/localenv](https://github.com/defunctzombie/localenv)
[motdotla/dotenv](https://github.com/motdotla/dotenv)
[zeke/local-env: Load your .env file into process.env](https://github.com/zeke/local-env)

[af/envalid: Environment variable validation for Node.js](https://github.com/af/envalid)
[dominictarr/rc: The non-configurable configuration loader for lazy people.](https://github.com/dominictarr/rc)
[MoOx/rc-loader: Runtime configuration loader that supports YAML, JSON or JS.](https://github.com/MoOx/rc-loader)

#### frameworks

[12 Factor CLI Apps – Jeff Dickey – Medium](https://medium.com/@jdxcode/12-factor-cli-apps-dd3c227a0e46) !important
[Build CLIs with an open framework using Node.js | oclif](https://oclif.io/)
[Open Sourcing oclif, the CLI Framework that Powers Our CLIs | Heroku](https://blog.heroku.com/open-cli-framework)
[CLI Flags in Practice + How to Make Your Own CLI Command with oclif | Heroku](https://blog.heroku.com/cli-flags-get-started-with-oclif)
[Open CLI Framework: Create Command Line Tools Your Users Love - YouTube](https://www.youtube.com/watch?v=ZBRmOS7dmD0)

[weidagang-line-parser-js](https://github.com/weidagang/line-parser-js) configuration over implementation  
[Omelette by f](http://f.github.io/omelette/) generates event from given command and you only have to implement the handlers  
[dscape-frameless](https://github.com/dscape/frameless) event framework for CLI app  
[vdemedes-sushi](https://github.com/vdemedes/sushi) Express for CLI

### sub-shell

These allows you to build a sub-shell or yeoman-like app.

[prompt](https://www.npmjs.org/package/prompt)
[readline-sync](https://www.npmjs.com/package/readline-sync)
[scottcorgan/nash: Craft command-line masterpieces in Node.js](https://github.com/scottcorgan/nash)
[scottcorgan/nash-usage: Help/usage display plugin for Nash command line masterpieces](https://github.com/scottcorgan/nash-usage)
[tj/nshell: scriptable command-line shell written with node.js](https://github.com/tj/nshell)
[enquirer/enquirer: Intuitive, plugin-based prompt system for node.js. Much faster alternative to Inquirer, with all the same prompt types and more.](https://github.com/enquirer/enquirer)
[SBoudrias/Inquirer.js: A collection of common interactive command line user interfaces.](https://github.com/SBoudrias/Inquirer.js/)
[anseki/readline-sync: Synchronous Readline for interactively running to have a conversation with the user via a console(TTY).](https://github.com/anseki/readline-sync)

[dthree-vorpal](https://github.com/dthree/vorpal) create REPL
[dthree-vantage](https://github.com/dthree/vantage)

### CLI interface

The equivalent of [ncurses](https://www.wikiwand.com/en/Ncurses) in Linux.

[chjj/blessed: A high-level terminal interface library for node.js.](https://github.com/chjj/blessed)
[substack/node-charm: ansi control sequences for terminal cursor hopping and colors](https://github.com/substack/node-charm)
[substack/terminal-menu: retro ansi terminal menus for serious 80s technicolor business](https://github.com/substack/terminal-menu)

blessed derivative with markup support:
[yaronn/wopr: A simple markup language for creating rich terminal reports, presentations and infographics](https://github.com/yaronn/wopr)
[yaronn/blessed-contrib: Build terminal dashboards using ascii/ansi art and javascript](https://github.com/yaronn/blessed-contrib)
[Yomguithereal/react-blessed: A react renderer for blessed.](https://github.com/Yomguithereal/react-blessed)

[madbence-node-drawille](https://github.com/madbence/node-drawille) draw unicode braille characters
[sindresorhus/sparkly](https://github.com/sindresorhus/sparkly)

[node-js-libs/cli: Rapidly build command line apps](https://github.com/node-js-libs/cli)

[vadimdemedes/pastel: 🎨 Framework for effortlessly building Ink apps](https://github.com/vadimdemedes/pastel)
[vadimdemedes/ink: 🌈 React for interactive command-line apps](https://github.com/vadimdemedes/ink)
[Building rich command-line interfaces with Ink and React](https://vadimdemedes.com/posts/building-rich-command-line-interfaces-with-ink-and-react)
[Creating CLIs with Ink, React and a bit of magic](https://vadimdemedes.com/posts/creating-clis-with-ink-react-and-a-bit-of-magic)

[Text to ASCII Art Generator (TAAG)](http://patorjk.com/software/taag/)
[patorjk/figlet.js: A FIG Driver written in JavaScript which aims to fully implement the FIGfont spec.](https://github.com/patorjk/figlet.js)

Workshop:
[workshopper/workshopper](https://github.com/workshopper/workshopper)
[substack/adventure](https://github.com/substack/adventure)

### Progress

[visionmedia/node-progress: Flexible ascii progress bar for nodejs](https://github.com/visionmedia/node-progress)
[inikulin/elegant-status: Create elegant task status for CLI.](https://github.com/inikulin/elegant-status)
[SamVerschueren/listr: Terminal task list](https://github.com/SamVerschueren/listr)

### Colorizer

[chalk/chalk: 🖍 Terminal string styling done right](https://github.com/chalk/chalk)
[jorgebucaran/clorox: Node.js library for colorizing text using ANSI escape sequences.](https://github.com/jorgebucaran/clorox)
[lukeed/kleur: The fastest Node.js library for formatting terminal text with ANSI colors~!](https://github.com/lukeed/kleur)
[Marak/colors.js](https://github.com/Marak/colors.js) use chalk instead

[danielb2-purdy.js](https://github.com/danielb2/purdy.js) colored object inspect

### Logger

Requirements:

- log to console and file simultaneously
- log rotation
- debug level
- search (optional)

[NodeJS logging made right – ITNEXT](https://itnext.io/nodejs-logging-made-right-117a19e8b4ce)

[visionmedia-debug](https://github.com/visionmedia/debug) support DEBUG in env to toggle log

[trentm/node-bunyan](https://github.com/trentm/node-bunyan)
[Bunyan JSON Logs with Fluentd and Graylog – The JS Blog](https://jsblog.insiderattack.net/bunyan-json-logs-with-fluentd-and-graylog-187a23b49540)

[klauscfhq/signale: 👋 Hackable console logger](https://github.com/klauscfhq/signale)
[nuxt/consola: 🐨 Elegant Console Logger](https://github.com/nuxt/consola)
[bevry/caterpillar](https://github.com/bevry/caterpillar)
[winstonjs/winston](https://github.com/winstonjs/winston)
[nlf/bucker](https://github.com/nlf/bucker)
[tj/log.js](https://github.com/tj/log.js)
[observing/devnull: dev/null, a powerful logging module for Node.js.. Because logging to dev/null is fast! <3](https://github.com/observing/devnull)

[rvagg/bole](https://github.com/rvagg/bole) based on idea of bunyan generally, simple yet flexible API

[mcollina/pino: fast and simple node.js logger](https://github.com/mcollina/pino)
[Guest post: Pino - The Fastest Node.js Logger for production](http://www.nearform.com/nodecrunch/sematext-guest-post-pino-fastest-node-js-logger-production/)

## globbing

[jonschlinkert/micromatch](https://github.com/jonschlinkert/micromatch)
[sindresorhus/multimatch](https://github.com/sindresorhus/multimatch)
[isaacs/minimatch](https://github.com/isaacs/minimatch)

[sindresorhus/globby](https://github.com/sindresorhus/globby)
[cowboy/node-globule](https://github.com/cowboy/node-globule)

## file system watcher

[remy/nodemon](https://github.com/remy/nodemon/)
[kimmobrunfeldt/chokidar-cli](https://github.com/kimmobrunfeldt/chokidar-cli)
[Qard/onchange](https://github.com/Qard/onchange)

```sh
nodemon diagram.plantuml -x \"plantuml\"
nodemon diagram.png -x \"xdg-open\"
```

## Event Emitter

[Events Node.js v5.10.0 Manual & Documentation](https://nodejs.org/api/events.html)

[nlf/spit](https://github.com/nlf/spit) async
[xat/hoook](https://github.com/xat/hoook) async and priority

### Eavesdrop Events

```js
(function patchEmitter(emitter) {
  var oldEmit = emitter.emit;

  emitter.emit = function() {
    var args = arguments;
    console.log(args[0], [].slice.call(args, 1));
    oldEmit.apply(emitter, args);
  };
})(emitter);
```

## Stream

[Node.js Streams: Everything you need to know – freeCodeCamp.org](https://medium.freecodecamp.org/node-js-streams-everything-you-need-to-know-c9141306be93)
[Stream Node.js v5.10.0 Manual & Documentation](https://nodejs.org/api/stream.html)
[StrongLoop | What’s New in io.js 1.0 Beta? – Streams3](https://strongloop.com/strongblog/whats-new-io-js-beta-streams3/)
[stream - What is Streams3 in Node.js and how does it differ from Streams2? - Stack Overflow](http://stackoverflow.com/a/21549237/665507)

"Classic" streams are available since v0.4.  
Classic readable streams are just `EventEmitter` with `'data'` and `'end'` events and a boolean `writable` member. They can _optionally_ provides `.pause()` and `.resume()` to control buffering.  
Classic writable streams are defined by the interface `.write(buf)`, `.end(buf)` and `.destroy()`.  
Classic streams are considered legacy so avoid registering `'data'` and `'end'` listeners (with stream libraries such as [through](https://github.com/dominictarr/through), [concat-stream](https://github.com/maxogden/concat-stream)).

Streams2 (paused streams/pull streams) was added to Node v0.10.  
To [consume a Readable stream](https://github.com/substack/stream-handbook#consuming-a-readable-stream), call `.read()` on `'readable'`. To [create a Readable stream](https://github.com/substack/stream-handbook#creating-a-readable-stream), inherits `stream.Readable` and implement `._read()` to `.push()` to the Readable stream. `.push(null)` to signal end of stream. You can also peek `buf` and `unshift()`  
To [write to a Writable stream](https://github.com/substack/stream-handbook#writing-to-a-writable-stream), call `.write()` and `.end()`. To [create a Writable stream](https://github.com/substack/stream-handbook#creating-a-writable-stream), inherits `stream.Writable` and implement `_write()` to consume the chunks, call `next()` to trigger the Readable stream to provide more data.

Streams3 (combined streams) was added to iojs and Node v0.11+.

[substack/stream-handbook](https://github.com/substack/stream-handbook)
[Node.js Stream Playground](http://nodestreams.com/)
[workshopper/stream-adventure: go on an educational stream adventure!](https://github.com/workshopper/stream-adventure)

[The Basics of Node.js Streams](https://www.sitepoint.com/basics-node-js-streams/)
[Readable, Writable, and Transform Streams in Node.js | Sanders DeNardi](http://www.sandersdenardi.com/readable-writable-transform-streams-node/)
[thlorenz.com The Power of NodeJS Streams and the event-stream Module](http://thlorenz.com/blog/the-power-of-nodejs-streams-and-the-event-stream-module/)
[Thorsten Lorenz - LXJS 2013 - Node.js streams for the utterly confused - YouTube](https://www.youtube.com/watch?v=9llfAByho98)
[Streams2](http://brycebaril.github.io/streams2-presentation/) actually on Streams3

[[r.va.gg] Why I don't use Node's core 'stream' module](https://r.va.gg/2014/06/why-i-dont-use-nodes-core-stream-module.html)
[dominictarr/stream-spec: executable specification for Stream (make testing streams easy)](https://github.com/dominictarr/stream-spec)
[nodejs/readable-stream](https://github.com/nodejs/readable-stream) Streams3 for non-Node environment
[mcollina/split2: Split Streams3 style](https://github.com/mcollina/split2)
[mcollina/reduplexer: reduplexer(writable, readable, options)](https://github.com/mcollina/reduplexer)
[mafintosh/pump](https://github.com/mafintosh/pump)
[maxogden/concat-stream: writable stream that concatenates strings or data and calls a callback with the result](https://github.com/maxogden/concat-stream)
[mcollina/callback-stream: A pipeable stream that calls your callback](https://github.com/mcollina/callback-stream)
[mcollina/never-ending-stream: Automatically restarts your stream for you when it ends](https://github.com/mcollina/never-ending-stream)
[mcollina/end-of-stream: Call a callback when a readable/writable/duplex stream has completed or failed.](https://github.com/mcollina/end-of-stream)
[rvagg/through2: Tiny wrapper around Node streams2 Transform to avoid explicit subclassing noise](https://github.com/rvagg/through2)
[brycebaril/node-terminus: An abstraction for making stream.Writable streams without all the boilerplate.](https://github.com/brycebaril/node-terminus)
[dominictarr/event-stream: EventStream is like functional programming meets IO](https://github.com/dominictarr/event-stream)
[maxogden/mississippi](https://github.com/maxogden/mississippi)

> see `javascript-notes.md` Bacon.js and Highland.js

[2016 - the year of web streams - JakeArchibald.com](https://jakearchibald.com/2016/streams-ftw/) on browser

[Bind Your Error Handler Before Your Readable Handler When Using Node.js Streams](http://www.bennadel.com/blog/2676-bind-your-error-handler-before-your-readable-handler-when-using-node-js-streams.htm)
[Node.js Streams Inherit Error-Handling Behavior From EventEmitter](http://www.bennadel.com/blog/2677-node-js-streams-inherit-error-handling-behavior-from-eventemitter.htm)
[Error Events Don't Inherently Stop Streams In Node.js](http://www.bennadel.com/blog/2678-error-events-don-t-inherently-stop-streams-in-node-js.htm)
[How Error Events Affect Piped Streams In Node.js](http://www.bennadel.com/blog/2679-how-error-events-affect-piped-streams-in-node-js.htm)
[You Have To Explicitly End Streams After Pipes Break In Node.js](http://www.bennadel.com/blog/2692-you-have-to-explicitly-end-streams-after-pipes-break-in-node-js.htm)
[Does The HTTP Response Stream Need Error Event Handlers In Node.js?](http://www.bennadel.com/blog/2823-does-the-http-response-stream-need-error-event-handlers-in-node-js.htm)

[An Overview of Buffers in Node.js | www.thecodebarbarian.com](http://thecodebarbarian.com/an-overview-of-buffers-in-node-js.html)

### Appending Buffers

Combining stream to a single output [ref](http://stackoverflow.com/a/14269536/665507):

```js
var bufs = [];
stream.on("data", function(d) {
  bufs.push(d);
});
stream.on("end", function() {
  var buf = Buffer.concat(bufs);
});
```

> However this put the stream in "classic" mode, use stream libraries instead.

[rvagg/bl: Buffer List: collect buffers and access with a standard readable Buffer interface, streamable too!](https://github.com/rvagg/bl)

[concat-stream](https://www.npmjs.com/package/concat-stream)

## ES Modules

[Announcing a new — experimental-modules – Node.js Foundation – Medium](https://medium.com/@nodejs/announcing-a-new-experimental-modules-1be8d2d6c2ff)

## Native Module

[C++ Addons | Node.js Documentation](https://nodejs.org/docs/latest/api/addons.html)
[N-API | Node.js Documentation](https://nodejs.org/api/n-api.html)
[nodejs/abi-stable-node: NAPI — Node with PoC ABI stable API for native modules.](https://github.com/nodejs/abi-stable-node)
[nodejs/nan: Native Abstractions for Node.js](https://github.com/nodejs/nan)
[nodejs/node-addon-api: Module for using N-API from C++](https://github.com/nodejs/node-addon-api)
[nodejs/node-addon-examples: Node.js C++ addon examples from http://nodejs.org/docs/latest/api/addons.html](https://github.com/nodejs/node-addon-examples)

[fcanas/node-native-boilerplate: A very small, understandable node native extension with reasonable project structure](https://github.com/fcanas/node-native-boilerplate)
[vshymanskyy/node-inline-cpp: Inline C++ with Node.js](https://github.com/vshymanskyy/node-inline-cpp)
[charto/nbind: Magical headers that make your C++ library accessible from JavaScript](https://github.com/charto/nbind)

[Chrome V8 — Google Developers](https://developers.google.com/v8/)
[Create Wiki — V8 Cookbook](http://create.tpsitulsa.com/wiki/V8_Cookbook)
[v8- V8 API Reference Guide](http://izs.me/v8-docs/main.html)

[How NodeJS requires native shared objects](https://blog.ghaiklor.com/how-nodejs-requires-native-shared-objects-63648092f178#.69kh9dg4q)
[Native Extensions for Node.js – Node.js Collection – Medium](https://medium.com/the-node-js-collection/native-extensions-for-node-js-767e221b3d26)
[N-API: Next generation Node.js APIs for native modules](https://medium.com/the-node-js-collection/n-api-next-generation-node-js-apis-for-native-modules-169af5235b06)
[N-API: Next generation APIs for Node.js native addons available across all LTS release lines](https://medium.com/the-node-js-collection/n-api-next-generation-apis-for-node-js-native-addons-available-across-all-lts-release-lines-4f35b781f00e)

[C++ and Node.js Integration](http://scottfrees.com/ebooks/nodecpp/)
[Scott Frees - Getting your C++ to the Web with Node.js](http://blog.scottfrees.com/getting-your-c-to-the-web-with-node-js)
[Scott Frees - C++ processing from Node.js](http://blog.scottfrees.com/c-processing-from-node-js)
[Scott Frees - C++ processing from Node.js - Part 2](http://blog.scottfrees.com/c-processing-from-node-js-part-2)
[Scott Frees - C++ processing from Node.js - Part 3 - Arrays](http://blog.scottfrees.com/c-processing-from-node-js-part-3-arrays)
[Scott Frees - C++ processing from Node.js - Part 4 - Asynchronous addons](http://blog.scottfrees.com/c-processing-from-node-js-part-4-asynchronous-addons)
[Scott Frees - Building an Asynchronous C++ Addon for Node.js using Nan](https://blog.scottfrees.com/building-an-asynchronous-c-addon-for-node-js-using-nan)

[Creating Multiplatform Precompiled Binaries for Node.js Modules](http://cylonjs.com/blog/2014/11/19/creating-multiplatform-precompiled-binaries-for-node-modules/)
[mapbox/node-pre-gyp: Node.js tool for easy binary deployment of C++ addons](https://github.com/mapbox/node-pre-gyp)
[mafintosh/node-gyp-build: Build tool and bindings loader for node-gyp that supports prebuilds](https://github.com/mafintosh/node-gyp-build)

[Neon · Fast and Safe Native Node.js Modules](https://neon-bindings.com/)
[Neon: Node + Rust = 💖](http://calculist.org/blog/2015/12/23/neon-node-rust/)
[Rust Bridge](https://github.com/rustbridge)
[RisingStack/node-with-rust](https://github.com/RisingStack/node-with-rust)

[Native JavaScript modules - YouTube](https://www.youtube.com/watch?v=RIct51T6ZoA)

## Isomorphism

[Isomorphic JavaScript - The future of web app development](http://isomorphic.net/)

[Universal JavaScript — Medium](https://medium.com/@mjackson/universal-javascript-4761051b7ae9)
[Is “Isomorphic JavaScript” a good term?](http://www.2ality.com/2015/08/isomorphic-javascript.html)
[Universal vs Isomorphic — Medium](https://medium.com/@svenarobbestad/universal-vs-isomorphic-10fc30aac39d#.aucslo83a)
[Capital One Engineering - Why Everyone is Talking About Isomorphic / Universal JavaScript and Why it Matters](http://www.capitalone.io/blog/why-is-everyone-talking-about-isomorphic-javascript/)

[Lazymorphic Apps: Bringing back the static web](https://blog.andyet.com/2015/05/18/lazymorphic-apps-bringing-back-static-web/) serving an `index.html` for landing/login and `200.html` for anything else

[Isomorphic JavaScript: The Future of Web Apps - Airbnb Engineering](http://nerds.airbnb.com/isomorphic-javascript-future-web-apps/)
[Why and How Coursera Does Isomorphic Javascript: A Fast and Snappy Quiz - Coursera Technology](https://tech.coursera.org/blog/2015/08/18/why-and-how-coursera-does-isomorphic-javascript-a-fast-and-snappy-quiz/)
[How to Migrate React to Isomorphic Rendering - Coursera Technology](https://tech.coursera.org/blog/2015/10/01/how-to-migrate-react-to-isomorphic-rendering/)

[spikebrehm/isomorphic-examples](https://github.com/spikebrehm/isomorphic-examples)
[spikebrehm/isomorphic-tutorial](https://github.com/spikebrehm/isomorphic-tutorial)

[RickWong/react-isomorphic-starterkit](https://github.com/RickWong/react-isomorphic-starterkit)
[tildeio/ember-cli-fastboot](https://github.com/tildeio/ember-cli-fastboot)
[trueadm/inferno: An extremely fast, React-like JavaScript library for building modern user interfaces](https://github.com/trueadm/inferno)

## Internals (Runtime and VM)

[Philip Roberts: What the heck is the event loop anyway? | JSConf EU 2014 - YouTube](https://www.youtube.com/watch?v=8aGhZQkoFbQ) !important
[latentflip.com/loupe/](http://latentflip.com/loupe/)

[Understanding the Node.js Event Loop](https://nodesource.com/blog/understanding-the-nodejs-event-loop/)
[The JavaScript Event Loop: Explained](http://blog.carbonfive.com/2013/10/27/the-javascript-event-loop-explained/)
[Event loop from 10,000ft - core concept behind Node.js](http://bytearcher.com/articles/event-loop-10-000ft/)
[Why the New V8 is so Damn Fast - NodeSource](https://nodesource.com/blog/why-the-new-v8-is-so-damn-fast)
[JavaScript V8 Engine Explained – Hacker Noon](https://hackernoon.com/javascript-v8-engine-explained-3f940148d4ef)
[Making the Switch from Node.js to Golang | via @codeship](https://blog.codeship.com/making-the-switch-from-node-js-to-golang/)
[HTML Standard Event loops](https://html.spec.whatwg.org/multipage/webappapis.html#event-loops)
[The Main Event… Loop – Codezillas – Medium](https://medium.com/codezillas/the-main-event-loop-3928adcd2413)

[Event Loop and the Big Picture — NodeJS Event Loop Part 1](https://jsblog.insiderattack.net/event-loop-and-the-big-picture-nodejs-event-loop-part-1-1cb67a182810)
[Timers, Immediates and Process.nextTick— NodeJS Event Loop Part 2](https://jsblog.insiderattack.net/timers-immediates-and-process-nexttick-nodejs-event-loop-part-2-2c53fd511bb3)
[Promises, Next-Ticks and Immediates— NodeJS Event Loop Part 3](https://jsblog.insiderattack.net/promises-next-ticks-and-immediates-nodejs-event-loop-part-3-9226cbe7a6aa)
[Handling IO — NodeJS Event Loop Part 4 – The JS Blog](https://jsblog.insiderattack.net/handling-io-nodejs-event-loop-part-4-418062f917d1)
[Event Loop Best Practices — NodeJS Event Loop Part 5](https://jsblog.insiderattack.net/event-loop-best-practices-nodejs-event-loop-part-5-e29b2b50bfe2)
[New Changes to the Timers and Microtasks in Node v11.0.0 ( and above)](https://jsblog.insiderattack.net/new-changes-to-timers-and-microtasks-from-node-v11-0-0-and-above-68d112743eb3)

[How JavaScript works – SessionStack Blog](https://blog.sessionstack.com/tagged/tutorial)
[How JavaScript works: an overview of the engine, the runtime, and the call stack](https://blog.sessionstack.com/how-does-javascript-actually-work-part-1-b0bacc073cf)
[How JavaScript works: inside the V8 engine + 5 tips on how to write optimized code](https://blog.sessionstack.com/how-javascript-works-inside-the-v8-engine-5-tips-on-how-to-write-optimized-code-ac089e62b12e)

[mö.js - explaining js vm in js - YouTube](https://www.youtube.com/watch?v=y8hVeKMD_oM)
[StrongLoop | What’s New in Node.js v0.12 – Running Multiple Instances in a Single Process](https://strongloop.com/strongblog/whats-new-node-js-v0-12-multiple-context-execution/)
[A Guide to JavaScript Engines for Idiots -Telerik Developer Network](http://developer.telerik.com/featured/a-guide-to-javascript-engines-for-idiots/)
[Writing Fast, Memory-Efficient JavaScript – Smashing Magazine](http://www.smashingmagazine.com/2012/11/writing-fast-memory-efficient-javascript/)
[How to Compile Node.js Code Using Bytenode? – Hacker Noon](https://hackernoon.com/how-to-compile-node-js-code-using-bytenode-11dcba856fa9)

[JavaScript engine fundamentals: Shapes and Inline Caches · Mathias Bynens](https://mathiasbynens.be/notes/shapes-ics)
[JavaScript Engines: The Good Parts™ - Mathias Bynens & Benedikt Meurer - JSConf EU 2018 - YouTube](https://www.youtube.com/watch?v=5nmpokoRaZI)

[JavaScript essentials: why you should know how the engine works](https://medium.freecodecamp.org/javascript-essentials-why-you-should-know-how-the-engine-works-c2cc0d321553) hidden class/object shapes, inline caching
[JavaScript Engines Hidden Classes (and Why You Should Keep Them in Mind) | concise notes](https://draft.li/blog/2016/12/22/javascript-engines-hidden-classes/)
[JavaScript engine fundamentals: Shapes and Inline Caches · Mathias Bynens](https://mathiasbynens.be/notes/shapes-ics)

[Crossing the JS/C++ Boundary — Advanced NodeJS Internals — Part 1](https://jsblog.insiderattack.net/crossing-the-js-c-boundary-advanced-nodejs-internals-part-1-cb52957758d8)

[A Quick Guide To Reading Node.js Core Source — Medium](https://medium.com/@Trott/a-quick-guide-to-reading-node-js-core-source-c968d83e4194#.p8prejow7)
[Architecture of Node.js’ Internal Codebase — Yet Another Node.js Blog — Medium](https://medium.com/yet-another-node-js-blog/architecture-of-node-js-internal-codebase-57cd8376b71f#.75t44fdz7)
[How does NodeJS work? — Eugene Obrezkov](https://blog.ghaiklor.com/how-nodejs-works-bfe09efc80ca#.cv91pzo3n)

## Tips and Tricks

[i0natan/nodebestpractices: The largest Node.js best practices list (April 2019)](https://github.com/i0natan/nodebestpractices)

[Working with Node: What you need to know](http://www.nearform.com/nodecrunch/working-node-need-know/) also some best practices
[Node.js tips #1: develop debugging techniques](http://www.nearform.com/nodecrunch/node-js-develop-debugging-techniques/)
[Node.js: How to Avail & Beware of the Ecosystem](http://www.nearform.com/nodecrunch/coding-with-nodejs/)
[10 tips for coding with Node.js #3: Throwing](http://www.nearform.com/nodecrunch/10-tips-coding-node-js-3-know-throw-2/)
[10 tips for coding with Node.js #4: reproduce core callback signatures - nearForm](http://www.nearform.com/nodecrunch/10-tips-coding-node-js-4-reproduce-core-callback-signatures/)

[Production Practices - Developer Center - Joyent](https://www.joyent.com/developers/node)

[continuationlabs/toolbag: preloaded Node.js tooling enhancements](https://github.com/continuationlabs/toolbag) exposes reporting and command interface for analytics
[continuationlabs/borland: hapi plugin for working with toolbag](https://github.com/continuationlabs/borland)

### Error Handling

[Errors | Node.js Manual & Documentation](https://nodejs.org/api/errors.html)
[Checklist: Best Practices of Node.JS Error Handling – Yoni Goldberg](http://goldbergyoni.com/checklist-best-practices-of-node-js-error-handling/)
[Joyent | Error Handling](https://www.joyent.com/node-js/production/design/errors)
[Joyent | Debug](https://www.joyent.com/node-js/production/debug#postmortem)

## #perfmatters

[Benchmark.js](http://benchmarkjs.com/)
[jonschlinkert/benchmarked: Easily generate benchmarks from a glob of files. Wrapper for Benchmark.js.](https://github.com/jonschlinkert/benchmarked)

[isaacs/node-bench](https://github.com/isaacs/node-bench)
[pierrec/node-visualbench](https://github.com/pierrec/node-visualbench)
[mcollina/fastbench: the simplest benchmark you can run on node](https://github.com/mcollina/fastbench)
[mcollina/loopbench: Benchmark your event loop](https://github.com/mcollina/loopbench)
[bench vs benchmark | Wyatt](http://jsgeek.com/posts/bench-benchmark.html)
[davidmarkclements/0x: 🔥 single-command flamegraph profiling 🔥](https://github.com/davidmarkclements/0x)

[Understanding Garbage Collection and hunting Memory Leaks in Node.js | Dynatrace blog](https://www.dynatrace.com/blog/understanding-garbage-collection-and-hunting-memory-leaks-in-node-js/)
[How to Self Detect a Memory Leak in Node - nearForm](http://www.nearform.com/nodecrunch/self-detect-memory-leak-node/)
[Understanding Garbage Collection and Memory in Node.js | via @codeship](https://blog.codeship.com/understanding-garbage-collection-in-node-js/)
[V8 JavaScript Engine: Concurrent marking in V8](https://v8project.blogspot.com/2018/06/concurrent-marking.html)
[How to track down CPU issues in Node.js - about:performance](http://apmblog.dynatrace.com/2016/01/14/how-to-track-down-cpu-issues-in-node-js/)

[jsPerf: JavaScript performance playground](http://jsperf.com/)

[Optimization killers · petkaantonov/bluebird Wiki](https://github.com/petkaantonov/bluebird/wiki/Optimization-killers#3-managing-arguments)

[Performance: reaching ludicrous speed - nearForm](http://www.nearform.com/nodecrunch/performance-reaching-ludicrous-speed/) [Reaching Ludicrous Speed - YouTube](https://www.youtube.com/watch?v=_0W_822Dijg)
[CPU Profiling in Production Node.js Applications - StackImpact](https://stackimpact.com/blog/cpu-profiling-in-production-node-js-applications/)

## npm

[npm Documentation](https://docs.npmjs.com/)
[A Beginner's Guide to npm — the Node Package Manager](http://www.sitepoint.com/beginners-guide-node-package-manager/)
[9 Quick Tips About npm](https://ponyfoo.com/articles/9-quick-tips-about-npm)
[The npm Blog — npm and front-end packaging](http://blog.npmjs.org/post/101775448305/npm-and-front-end-packaging)
[Tour of npm](http://tobyho.com/2012/02/09/tour-of-npm/)
[npm forum](https://npm.community/)

[unpkg](https://unpkg.com/#/) get file from package
[Pika | Pika | Search modern module esm packages on npm](https://www.pikapkg.com/)

```sh
# return the current `node_modules` folder
npm root
# prune modules
npm dedupe && npm prune
```

### Module discovery

[Search and Discover Great Node Modules - CenturyLink Cloud Developer Center](https://www.ctl.io/developers/blog/post/scoutjs-search-npm)
[finding modules](http://substack.net/finding_modules) by substack

[npm](https://www.npmjs.com/)
[npms](https://npms.io/)
[npmsearch - node.js Package Search Utility](https://npmsearch.com/)
[Scout JS](http://scoutjs.com/)
[JS.coach](https://js.coach/)
[NodeZoo - A search engine for reliable node.js modules.](http://nodezoo.com/) with NodeRank
[Better search for Node.js modules](http://node-modules.com/)
[Nipster! npm search tool for Node.js](http://nipstr.com/)
[Browsenpm.org | Nodejitsu Inc.](http://browsenpm.org/)
[npm - Libraries](https://libraries.io/npm)

### Private registry

[rlidwka/sinopia](https://github.com/rlidwka/sinopia)
[Using private npm on Heroku | Nodejitsu Inc.](http://blog.nodejitsu.com/using-private-npm-on-heroku/)
[An Alternative to npm Private Modules](http://fiznool.com/blog/2015/05/20/an-alternative-to-npm-private-modules/) host on GitHub/Bitbucket

### `require()` algorithm

[Modules Node.js Manual & Documentation](https://nodejs.org/docs/latest/api/modules.html#modules_all_together)
[substack/node-resolve](https://github.com/substack/node-resolve)

[Where Does Node.js And Require() Look For Modules?](http://www.bennadel.com/blog/2169-where-does-node-js-and-require-look-for-modules.htm)
[The Node Way - How `require()` Actually Works](http://thenodeway.io/posts/how-require-actually-works/)

### Git URL as dependencies

[Git URLs as Dependencies | npm Documentation](https://docs.npmjs.com/files/package.json#git-urls-as-dependencies)

```
git://github.com/user/project.git#commit-ish
git+ssh://user@hostname:project.git#commit-ish
git+ssh://user@hostname/project.git#commit-ish
git+http://user@hostname/project/blah.git#commit-ish
git+https://user@hostname/project/blah.git#commit-ish
```

GitHub repo can be simplified as `user/repo`:

```json
{
  "name": "foo",
  "version": "0.0.0",
  "dependencies": {
    "express": "visionmedia/express",
    "mocha": "visionmedia/mocha#4727d357ea"
  }
}
```

### Yarn

[Yarn](https://yarnpkg.com/)
[Compare Yarn Performance | Yarn](https://yarnpkg.com/en/compare)

## System service

[NicolaOrritos/probiotic: The simplified multi-workers daemon](https://github.com/NicolaOrritos/probiotic)
[NicolaOrritos/progenic: Multi-workers daemon module](https://github.com/NicolaOrritos/progenic)

## Node Project

[npm module maintainer must-haves](https://hannah.wf/npm-maintenance/)
[mattdesl/module-best-practices: some best practices for JS modules](https://github.com/mattdesl/module-best-practices)
[Choosing and making quality npm modules | Yannick Croissant](https://yannick.cr/posts/choosing-and-making-quality-npm-modules/post)

[maxogden/maintenance-modules: a list of modules that are useful for maintaining or developing modules](https://github.com/maxogden/maintenance-modules)
[HenrikJoreteg/fixpack: A package.json file scrubber for the truly insane.](https://github.com/henrikjoreteg/fixpack) `standard` for `package.json`
[feross/standard: JavaScript Standard Style](https://github.com/feross/standard)

[Design and Build Your Own JavaScript Library: Tips & Tricks](https://www.sitepoint.com/design-and-build-your-own-javascript-library/)
[Advanced Node.js Project Structure Tutorial - via @codeship | via @codeship](https://blog.codeship.com/advanced-node-js-project-structure-tutorial/)
[Fractal — Nodejs app structure – codeburst](https://codeburst.io/fractal-a-nodejs-app-structure-for-infinite-scale-d74dda57ee11)

[Modern Modules – Mikeal – Medium](https://medium.com/@mikeal/modern-modules-d99b6867b8f1?imm_mid=0f6b9c&cmp=em-web-na-na-newsltr_20170927)
[semantic-release/semantic-release: fully automated package publishing](https://github.com/semantic-release/semantic-release)

### Package Management

[developers | npm Documentation](https://docs.npmjs.com/misc/developers)
[These 6 essential tools will release, version, and maintain your NPM modules for you](https://hackernoon.com/these-6-essential-tools-will-maintain-your-npm-modules-for-you-4cbbee88e0cb)

dep bots:  
[Greenkeeper | Automate your npm dependency management](https://greenkeeper.io/) bot to check if dependency update breaks your module
[Dependabot](https://dependabot.com/)
[Depfu: Continuous automated dependency updates for Ruby and JavaScript](https://depfu.com/) bot that creates PR for updated dependency
[dylang/npm-check: Check for outdated, incorrect, and unused dependencies.](https://github.com/dylang/npm-check)
[Rever: Releaser of Versions!](https://regro.github.io/rever-docs/)

[FOSSA - Open Source Management for Modern Development](https://fossa.com/) multi-lingual, free-tier
[Renovate | Automated Dependency Updates](https://renovatebot.com/) multi-lingual, no free-tier

[nlf/git-validate](https://github.com/nlf/git-validate)
[nlf/precommit-hook](https://github.com/nlf/precommit-hook)
[observing/pre-commit: Automatically installs a git pre-commit script in your git repository which runs your `npm test` on pre-commit](https://github.com/observing/pre-commit)

[mattdesl/module-best-practices: some best practices for JS modules](https://github.com/mattdesl/module-best-practices)
[Command-line tips for effective release announcements | codeinthehole.com by David Winterbottom](http://codeinthehole.com/writing/command-line-tips-for-effective-release-announcements/)

[nexe by jaredallard](https://jaredallard.me/nexe/)

### Publishing

[sindresorhus/np: A better `npm publish`](https://github.com/sindresorhus/np)

[How to Build and Publish ES6 Modules Today, with Babel and Rollup — Medium](https://medium.com/@tarkus/how-to-build-and-publish-es6-modules-today-with-babel-and-rollup-4426d9c7ca71)
[inikulin/publish-please: Safe and highly functional replacement for `npm publish`.](https://github.com/inikulin/publish-please)
[What is npm’s prepublish, and why is it so confusing? — Greenkeeper Blog](https://blog.greenkeeper.io/what-is-npm-s-prepublish-and-why-is-it-so-confusing-a948373e6be1#.ec58iaknh)

### `package.json`

[package.json | npm Documentation](https://docs.npmjs.com/files/package.json)
[package.json: an interactive guide - browsenpm.org](http://browsenpm.org/package.json)

Use `^` to lock to major version, `~` to lock to minor version. (`npm help update`)

### Files in package

[`files` in `package.json`](https://docs.npmjs.com/files/package.json#files)
[Keeping files out of your package](https://docs.npmjs.com/misc/developers#keeping-files-out-of-your-package)

By default all files under the package tree will be published, with predefined blacklist and whitelist, and respects `.npmignore` (or `.gitignore` if `.npmignore` is absent).
You can specify `files` in `package.json` to define your own file list, this will also respects `.npmignore` (or `.gitignore` if `.npmignore` is absent).

### shrinkwrap

> obsolete by lock file

[lockdown](https://www.npmjs.com/package/lockdown)
[shrinkwrap | npm Documentation](https://docs.npmjs.com/cli/shrinkwrap)

[NPM - An intervention » Debuggable - Node.js Consulting](http://debuggable.com/posts/npm-an-intervention:4f44dd25-a114-4361-ada1-6cefcbdd56cb)
[Managing Node.js Dependencies with Shrinkwrap | Node.js](https://nodejs.org/en/blog/npm/managing-node-js-dependencies-with-shrinkwrap/)

### Local Dev Dependency

[Mono-repo or multi-repo? Why choose one, when you can have both?](https://medium.com/@patrickleet/mono-repo-or-multi-repo-why-choose-one-when-you-can-have-both-e9c77bd0c668) `meta`
[Repo style wars: mono vs multi](http://www.gigamonkeys.com/mono-vs-multi/)

[Advantages of monorepos](https://danluu.com/monorepo/)
[babel/monorepo.md at master · babel/babel](https://github.com/babel/babel/blob/master/doc/design/monorepo.md)
[Monorepos: Please don’t! – Matt Klein – Medium](https://medium.com/@mattklein123/monorepos-please-dont-e9a279be011b)

[Lerna · A tool for managing JavaScript projects with multiple packages.](https://lernajs.io/)
[Dombo/node-lerna-monorepo](https://github.com/Dombo/node-lerna-monorepo)
[Quramy/lerna-yarn-workspaces-example: How to build TypeScript mono-repo project with yarn and lerna](https://github.com/Quramy/lerna-yarn-workspaces-example)
[Solve code sharing and setup project with Lerna and monorepo - Michal Zalecki](https://michalzalecki.com/solve-code-sharing-and-setup-project-with-lerna-and-monorepo/)
[Sharing UI Components with Lerna and Yarn Workspaces](https://medium.com/naresh-bhatia/sharing-ui-components-with-lerna-and-yarn-workspaces-be1ebca06efe)

[Bit - Share and build with code components](https://bitsrc.io/)
[Monorepos Made Easier with Bit and NPM – Bits and Pieces](https://blog.bitsrc.io/monorepo-architecture-simplified-with-bit-and-npm-b1354be62870)

[Workspaces | Yarn](https://yarnpkg.com/lang/en/docs/workspaces/)
[guigrpa/oao: A Yarn-based, opinionated monorepo management tool](https://github.com/guigrpa/oao)

[jfhbrook/npmlinxxx: a kinder, gentler alternative to npm link](https://github.com/jfhbrook/npmlinxxx)

[feross/zelda: Automatically `npm link` all your packages together!](https://github.com/feross/zelda) cannot get it work

### Linter

[![js-semistandard-style](https://cdn.rawgit.com/flet/semistandard/master/badge.svg)](https://github.com/Flet/semistandard)

```
[![js-semistandard-style](https://cdn.rawgit.com/flet/semistandard/master/badge.svg)](https://github.com/Flet/semistandard)
```

[![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg?style=flat-square)](https://github.com/Flet/semistandard)

```
[![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg?style=flat-square)](https://github.com/Flet/semistandard)
```

[Enforcing Code Quality for Node.js – Hacker Noon](https://hackernoon.com/enforcing-code-quality-for-node-js-c3b837d7ae17)

### CI and Testing

Most Continuous Integration service provide badges.

> see `dev-testing.md#continuous-integration`

### Check-in dependencies?

[Why we stopped vendoring our npm dependencies](http://blog.bithound.io/why-we-stopped-vendoring-our-npm-dependencies/)
[shrinkwrap | npm Documentation](https://docs.npmjs.com/cli/shrinkwrap)

### Visualize dependencies

[pahen/madge - JavaScript](https://github.com/pahen/madge)
[auchenberg/dependo](https://github.com/auchenberg/dependo)

## Node REPL

```
$ node
> console.log('Node is running');
Node is running
> .help
.break Sometimes you get stuck, this gets you out
.clear Alias for .break
.exit  Exit the repl
.help  Show repl options
.load  Load JS from a file into the REPL session
.save  Save all evaluated commands in this REPL session to a file
> .exit
```

`node -i -e "$(< script.js)"` to save the `.load` in REPL.

Try [Nesh by danielgtaylor](http://danielgtaylor.github.io/nesh/).

```
nesh> .help
.cls    Clear the screen
.history    Show command history
.versions   Show Node version information
break   Sometimes you get stuck, this gets you out
clear   Alias for .break
doc Shows documentation for an expression; you can also type Ctrl-Q in-line
exit    Exit the repl
help    Show repl options
load    Load JS from a file into the REPL session
require Require a module and assign it to a variable with the same name
save    Save all evaluated commands in this REPL session to a file
nesh> .exit
```

## In the Wild

[What are the biggest websites built with Node.js on the server side? - Quora](https://www.quora.com/What-are-the-biggest-websites-built-with-Node-js-on-the-server-side)
[Why Walmart is using Node.js | VentureBeat | Dev | by J. O'Dell](http://venturebeat.com/2012/01/24/why-walmart-is-using-node-js/)
[Node at scale: What Google, Mozilla, & Yahoo are doing with Node.js | VentureBeat | Dev | by J. O'Dell](http://venturebeat.com/2012/01/24/node-at-google-mozilla-yahoo/)
[Projects, Applications, and Companies Using Node · nodejs/node-v0.x-archive Wiki](https://github.com/nodejs/node-v0.x-archive/wiki/Projects,-Applications,-and-Companies-Using-Node)
