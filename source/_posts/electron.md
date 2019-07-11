---
title: Electron
categories:
  - comp.lang
toc: true
date: 2015-07-19 14:07:01
tags:
- atom-shell
- electron
---

[Electron](http://electron.atom.io/) ([Github](https://github.com/atom/electron)), previously [Atom Shell](http://electron.atom.io/blog/2015/04/23/electron), is a platform that bundles Chromium’s rendering library and Node.js runtime for developers to write cross-platform desktop applications with JavaScript and HTML.

[Electron 1.0](http://electron.atom.io/blog/2016/05/11/electron-1-0)
[#216: GitHub's Electron with Zeke Sikelianos - Changelog](https://changelog.com/216/)

[Building a Desktop App with Vue: Electron - DEV Community 👩‍💻👨‍💻](https://dev.to/vuevixens/building-a-desktop-app-with-vue-electron-3pl)

[Electron开发，如何入坑？](https://mp.weixin.qq.com/s?__biz=MzIwNjQwMzUwMQ==&mid=2247485626&idx=1&sn=bf60e71918222186e25257d838ce7868&chksm=97236a78a054e36e987259dc4143c4cdeb5804bc9d6b6b82a93b95421c4cc88b15e63e0c08a3&scene=27#wechat_redirect)

# Packager

[javascript - electron-builder vs electron-packager - Stack Overflow](https://stackoverflow.com/questions/37113815/electron-builder-vs-electron-packager)
electron-builder > electron-packager

# Contenders

> see `nw-js.md` 

It is very similar to the [NW.js](http://nwjs.io/) project but the differences are explained [here](http://electron.atom.io/docs/latest/development/atom-shell-vs-node-webkit/).
[NW.js & Electron Compared - TangibleJS](http://tangiblejs.com/posts/nw-js-electron-compared)
[Atom Shell vs Node-Webkit - 牛角堂](http://blog.iwege.com/posts/atom-shell-vs-node-webkit.html)
[Atom-Shell vs Node-Webkit (Context篇) - 牛角堂](http://blog.iwege.com/posts/atom-shell-vs-node-webkit-context.html)
[html5 - What are the functional differences between NW.js, Brackets-Shell and Electron? - Stack Overflow](http://stackoverflow.com/questions/23731517/what-are-the-functional-differences-between-nw-js-brackets-shell-and-electron)
[The State of Desktop Applications in Node.js](https://nodesource.com/blog/the-state-of-desktop-applications-in-nodejs/)

---

[electron/electron-api-demos: Explore the Electron APIs](https://github.com/electron/electron-api-demos)
[electron/electron-quick-start: Clone to try a simple Electron app](https://github.com/electron/electron-quick-start)

[Community | Electron](https://electronjs.org/community#boilerplates)
[sindresorhus/awesome-electron](https://github.com/sindresorhus/awesome-electron)
[bcomnes/electron-handbook](https://github.com/bcomnes/electron-handbook)
[maxogden/elementary-electron: NodeSchool workshop for learning Electron](https://github.com/maxogden/elementary-electron)
[zeke/electron-universe: The Electron app I created as a slide deck for my talk about Electron at GitHub Universe 2016.](https://github.com/zeke/electron-universe)

[sindresorhus/electron-boilerplate: Boilerplate to kickstart creating an app with Electron](https://github.com/sindresorhus/electron-boilerplate)
[chentsulin/electron-react-boilerplate: Live editing development on desktop app](https://github.com/chentsulin/electron-react-boilerplate)

[electron-userland](https://github.com/electron-userland)
[electron-userland/electron-packager: Package and distribute your Electron app with OS-specific bundles (.app, .exe etc) via JS or CLI](https://github.com/electron-userland/electron-packager)
[electron-userland/electron-builder: Complete solution to package and deploy Electron apps](https://github.com/electron-userland/electron-builder)
[electron-userland/electron-prebuilt: Install Electron (formerly atom-shell) prebuilts using npm](https://github.com/electron-userland/electron-prebuilt)

[Desktop Apps With Electron And Kendo UI -Telerik Developer Network](http://developer.telerik.com/featured/desktop-apps-with-electron-and-kendo-ui/)
[Creating Desktop Applications With AngularJS and GitHub Electron | Scotch](https://scotch.io/tutorials/creating-desktop-applications-with-angularjs-and-github-electron)
[Background Processes in Electron](http://blog.smith-kyle.com/background-processes-in-electron/)

## Modules

[Devtron](http://electron.atom.io/devtron/) devtool
[Spectron](http://electron.atom.io/spectron/) testing framework
[electron/asar: Simple extensive tar-like archive format with indexing](https://github.com/electron/asar)
[maxogden/electron-spawn: easy way to run code inside of a headless electron window from the CLI](https://github.com/maxogden/electron-spawn)
[sindresorhus/electron-debug](https://github.com/sindresorhus/electron-debug)
[sindresorhus/electron-dl](https://github.com/sindresorhus/electron-dl)
[maxogden/menubar: ➖ high level way to create menubar desktop applications with electron](https://github.com/maxogden/menubar)

## Wrapper

[jiahaog/nativefier: Wrap any web page natively without even thinking, across Windows, OSX and Linux](https://github.com/jiahaog/nativefier)

[Fluid - Turn Your Favorite Web Apps into Real Mac Apps.](http://fluidapp.com/)

[Photon](http://photonkit.com/)
[connors/photon: The fastest way to build beautiful Electron apps using simple HTML and CSS](https://github.com/connors/photon)

[railsware/bozon: Bootstrap, Build, Run and Package Electron application with ease](https://github.com/railsware/bozon)

[ŷhat | How we built Rodeo with Electron](http://blog.yhathq.com/posts/how-rodeo-works.html)

## Features

First check [version](http://electron.atom.io/#electron-versions) of Electron and it dependencies.

Then check the features supported:
[Chromium Blog](http://blog.chromium.org/)
[Chrome Platform Status](https://www.chromestatus.com/samples)
[Previous Releases | Node.js](https://nodejs.org/en/download/releases/)

## Internals

[Electron Internals: Using Node as a Library - Electron](http://electron.atom.io/blog/2016/08/08/electron-internals-using-node-as-a-library)
[Electron Internals: Message Loop Integration - Electron](http://electron.atom.io/blog/2016/07/28/electron-internals-node-integration)
[Use V8 and Chromium Features in Electron - Electron](http://electron.atom.io/blog/2016/01/07/latest-v8-chromium-features)

[Practice on embedding Node.js into Atom Editor // Speaker Deck](https://speakerdeck.com/zcbenz/practice-on-embedding-node-dot-js-into-atom-editor) 2014, still Atom Shell
