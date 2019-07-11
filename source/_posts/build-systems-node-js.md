---
title: "Build Systems (Node.js)"
categories:
  - comp.lang
tags:
  - node-js
toc: true
date: 2015-06-11 15:54:08
---

[Understanding Build Processes](https://ponyfoo.com/articles/understanding-build-processes)

> see `javascript-pipeline.md`, `css-pipeline.md`

> TODO: add `~/web/nodejs/build`
[Jake: JavaScript build tool task runner for NodeJS](http://jakejs.com/)

## Source map

[​Everything You Wanted to Know About JavaScript Source Maps | Scotch](https://scotch.io/tutorials/​everything-you-wanted-to-know-about-javascript-source-maps)
[Anatomy of source maps](https://blog.bugsnag.com/source-maps/)

## npm

You can define npm scripts in `package.json`. npm will automatically resolve binaries in `node_modules`.
You can use shell pipe in the command. This works great is your toolchains support piping.
If you need cross-platform support (well, Windows support), consider using Vanilla JS.

[scripts | npm Documentation](https://docs.npmjs.com/misc/scripts)
[run-script | npm Documentation](https://docs.npmjs.com/cli/run-script)

[Why we should stop using Grunt & Gulp](http://blog.keithcirkel.co.uk/why-we-should-stop-using-grunt/)
[How to Use npm as a Build Tool](http://blog.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/)
[Why I Left Gulp and Grunt for npm Scripts — Free Code Camp — Medium](https://medium.freecodecamp.com/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8#.uvq7td3ik)
[Choose: Grunt, Gulp, or npm?](https://ponyfoo.com/articles/choose-grunt-gulp-or-npm)

[Give Grunt the Boot! A Guide to Using npm as a Build Tool](http://www.sitepoint.com/guide-to-npm-as-a-build-tool/)
[Gulp is awesome, but do we really need it?](http://gon.to/2015/02/26/gulp-is-awesome-but-do-we-really-need-it/)
[You don’t need Grunt — Medium](https://medium.com/@julesbou/you-don-t-need-grunt-a48605915319#.4dz5pd3we) with CLI replacements
[You Might Not Need Gulp.js — Startups, Wanderlust, and Life Hacking — Medium](https://medium.com/swlh/you-might-not-need-gulp-js-89a0220487dd#.1z2zfrucg)
[Using npm Scripts to Build an Asset Pipeline](http://blog.modulus.io/using-npm-scripts-to-build-asset-pipeline)
[task automation with npm run](http://substack.net/task_automation_with_npm_run)

## Vanilla JS

If your toolchain expose Node.js API, you can write an Node.js app as your pipeline. This is better the other task runners as you have nothing more to learn other then JavaScript and the API of the toolchain you are using.

[Node.js as a build script | Blog | Miller Medeiros](http://blog.millermedeiros.com/node-js-as-a-build-script/)
[Node.js, Ant, Grunt and other build tools | Blog | Miller Medeiros](http://blog.millermedeiros.com/node-js-ant-grunt-and-other-build-tools/)

[introducing ./task.js, THE new javascript task runner automation framework](https://gist.github.com/substack/8313379)
[Bevry News 2015 Weeks 34, 35, 36 — Bevry Blog](https://blog.bevry.me/bevry-news-2015-weeks-34-35-36-7f1516cb2580)

[jprichardson/node-fs-extra: Node.js: extra methods for the fs object like copy(), remove(), mkdirs()](https://github.com/jprichardson/node-fs-extra)
[keithamus/hashmark: Take contents of a file (or stdin), and output as new file with a hash in the name](https://github.com/keithamus/hashmark)
[nicholaswyoung/revv](https://github.com/nicholaswyoung/revv)

### ShellJS

[ShellJS](http://documentup.com/shelljs/shelljs) portable Unix shell commands
[nzakas/shelljs-nodecli](https://github.com/nzakas/shelljs-nodecli) easier to run binaries in `node_modules`, like npm scripts

[Building JavaScript apps](http://kjbekkelund.github.io/presentations/js-build/) [source](https://github.com/kjbekkelund/js-build)

https://github.com/firebug/firebug/blob/master/extension/build.js
https://github.com/kjbekkelund/js-build/blob/master/make.js
https://github.com/madrobby/zepto/blob/master/make
https://github.com/mozilla/pdf.js/blob/master/make.js
https://github.com/gnab/remark/blob/develop/make.js

## Metalsmith

Metalsmith was advertised as a static site generator, but the pipeline and plugins allow it to be used as a build system.

[Metalsmith](http://www.metalsmith.io/)

## Grunt

[Grunt: The JavaScript Task Runner](http://gruntjs.com/)
[Plugins - Grunt: The JavaScript Task Runner](http://gruntjs.com/plugins)
[Grunt Tips and Tricks](https://ponyfoo.com/articles/grunt-tips-and-tricks) 

[bahmutov/grunty](https://github.com/bahmutov/grunty) Run any grunt plugin as NPM script without Gruntfile.js

## Gulp

[gulp.js - the streaming build system](http://gulpjs.com/)
[The Complete-Ish Guide to Upgrading to Gulp 4 | Joe Zim's JavaScript Blog](https://www.joezimjs.com/javascript/complete-guide-upgrading-gulp-4/)
[Automate Your Tasks Easily with Gulp.js | Scotch](https://scotch.io/tutorials/automate-your-tasks-easily-with-gulp-js)
[Gulp Basics Course](http://teamtreehouse.com/library/gulp-basics)
[Gulp, Grunt, Whatever](https://ponyfoo.com/articles/gulp-grunt-whatever)

[Learning Gulp - YouTube](https://www.youtube.com/playlist?list=PLLnpHn493BHE2RsdyUNpbiVn-cfuV7Fos)

## Brunch

[Brunch - ultra-fast HTML5 build tool](http://brunch.io/)
[brunch/brunch-guide](https://github.com/brunch/brunch-guide)
