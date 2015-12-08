---
title: Flux
toc: true
date: 2015-12-04 12:12:11
categories:
- web
tags:
- react-js
- flux
- javascript
---

Flux is a pattern for web applications architecture, *rather than a library*. Though there are some example implementations.  

Flux promotes unidirectional  data flow:
  DISPATCHER -> STORES -> COMPONENTS
Dispatcher and stores are global.
Components take immutable `prop` as input and can maintain internal mutable `state`. Changes to state via `setState()` will trigger a re-rendering.
Components can also fire "intent" (also called "action") or listen to the dispatcher/stores.

<!-- more -->

[Flux | Application Architecture for Building User Interfaces](http://facebook.github.io/flux/)
[The React.js Way: Flux Architecture with Immutable.js](http://blog.risingstack.com/the-react-js-way-flux-architecture-with-immutable-js/)
[What is the Flux Application Architecture? — Brigade Engineering — Medium](https://medium.com/brigade-engineering/what-is-the-flux-application-architecture-b57ebca85b9e)
[Understanding Flux — Medium](https://medium.com/@garychambers108/understanding-flux-f93e9f650af7)
[Flux For Stupid People](http://blog.andrewray.me/flux-for-stupid-people/)
[Fluxxor - What is Flux?](http://fluxxor.com/what-is-flux.html)
[Deconstructing ReactJS's Flux](http://spoike.ghost.io/deconstructing-reactjss-flux/)
[What the flux?](http://jonathancreamer.com/what-the-flux/)
[Application Architecture with React: rethinking Flux](http://dialelo.github.io/application-architecture-with-react-rethinking-flux.html)
[A cartoon guide to Flux — Code Cartoons — Medium](https://code-cartoons.com/a-cartoon-guide-to-flux-6157355ab207)

[Getting To Know Flux, the React.js Architecture ♥ Scotch](http://scotch.io/tutorials/javascript/getting-to-know-flux-the-react-js-architecture)
[Creating A Simple Shopping Cart with React.js and Flux ♥ Scotch](http://scotch.io/tutorials/javascript/creating-a-simple-shopping-cart-with-react-js-and-flux)

[Integrating React and Flux with Angular | MobileAppTracking Developers](https://developers.mobileapptracking.com/addressing-angular-weaknesses-with-react-and-flux/)

### christianalfoni

[christianalfoni - React js and flux](http://www.christianalfoni.com/articles/2014_08_20_React-js-and-flux)
[jQuery as a framework, could that work? - christianalfoni WebApp Enthusiast](http://christianalfoni.github.io/javascript/2014/09/08/jquery-as-a-framework-could-that-work.html)
[christianalfoni - Nailing that validation with React JS](http://www.christianalfoni.com/articles/2014_10_22_Nailing-that-validation-with-React-JS)
[My experiences building a FLUX application - christianalfoni WebApp Enthusiast](http://christianalfoni.github.io/javascript/2014/10/27/my-experiences-building-a-flux-application.html)
[christianalfoni - A browserify workflow part 2](http://www.christianalfoni.com/articles/2014_10_30_A-browserify-workflow-part-2)
[An alternative render strategy with flux and React JS - christianalfoni WebApp Enthusiast](http://christianalfoni.github.io/javascript/2014/12/04/flux-and-eventemitter2.html)
[christianalfoni - Why we are doing MVC and FLUX wrong](http://www.christianalfoni.com/articles/2015_08_02_Why-we-are-doing-MVC-and-FLUX-wrong)
[christianalfoni - Flux vs Single State Tree](http://www.christianalfoni.com/articles/2015_11_16_Flux-vs-Single-State-Tree)
[Home · christianalfoni/react-webpack-cookbook Wiki](https://github.com/christianalfoni/react-webpack-cookbook/wiki)
[jFlux - Going from MVC to FLUX - YouTube](https://www.youtube.com/watch?v=plUN2L4Ak14)
[JSFridge](http://www.jsfridge.com/courses/jFlux_-_A_framework_to_keep_you_sane/scenes/0)

### Libraries

[goatslacker-alt · GitHub](https://github.com/goatslacker/alt)
[jFlux](http://www.jflux.io/)
[kenwheeler-mcfly · GitHub](https://github.com/kenwheeler/mcfly)
[LeanKit-Labs-lux.js · GitHub](https://github.com/LeanKit-Labs/lux.js)
[spoike-refluxjs · GitHub](https://github.com/spoike/refluxjs)
  [The Reflux data flow model](http://blog.krawaller.se/posts/the-reflux-data-flow-model/)
[deloreanjs-delorean · GitHub](https://github.com/deloreanjs/delorean)
[Flummox | Minimal, isomorphic Flux](http://acdlite.github.io/flummox) now recommends Redux
[Flux | Application Architecture for Building User Interfaces](http://facebook.github.io/flux/docs/overview.html)
[Flux: No More Stores, Meet Reducer](https://blog.javascripting.com/2015/06/19/flux-no-more-stores-meet-reducer/)
[Tuxx](http://www.tuxedojs.org/)
[FluxThis](https://fluxthis.io/)
[Fluxxor - Home](http://fluxxor.com/)
[NuclearJS](https://optimizely.github.io/nuclear-js/)

### Comparison

[The State of Flux](https://reactjsnews.com/the-state-of-flux/)
[The Evolution of Flux Frameworks — Medium](https://medium.com/@dan_abramov/the-evolution-of-flux-frameworks-6c16ad26bb31)
[voronianski-flux-comparison · GitHub](https://github.com/voronianski/flux-comparison)
[staltz/flux-challenge](https://github.com/staltz/flux-challenge)
[Qualities Of Good Flux Implementations](http://www.smashingmagazine.com/2015/06/qualities-of-good-flux-implementations/)
[5 React.js + Flux tools - Progville](http://www.progville.com/javascript/5-react-js-flux-tools/)
[Qualities Of Good Flux Implementations](http://www.smashingmagazine.com/2015/06/qualities-of-good-flux-implementations/)
