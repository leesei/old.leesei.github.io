title: Flux Alternatives
toc: true
date: 2015-12-04 12:12:24
categories:
- web
tags:
- react-js
- flux
- javascript
---

Sometimes React.js alone may serve your need, you don't have to prematurely flux it.
[The Case for Flux — Startups, Wanderlust, and Life Hacking — Medium](https://medium.com/swlh/the-case-for-flux-379b7d1982c6)

And there are other strategies besides Flux for architecting your application.
[6 no-Flux strategies for React component communication](http://andrewhfarmer.com/component-communication/)

Gist of a modern data-driven app:
- don’t use fat models
- data from server is just another input, not your model, [CQRS](http://martinfowler.com/bliki/CQRS.html)
- modify state via a *SINGLE* component

## React + Backbone/Marionette/Ampersand

[Using React components as Backbone Views](http://www.thomasboyt.com/2013/12/17/using-reactjs-as-a-backbone-view.html)
[clayallsopp/react.backbone](https://github.com/clayallsopp/react.backbone)
[Tutorial: Building React Apps With Flux and Backbone | Toptal](http://www.toptal.com/front-end/simple-data-flow-in-react-applications-using-flux-and-backbone)

[Gentle Migration from Marionette to React - Jamie Gaskins](http://jgaskins.org/blog/2015/02/06/gentle-migration-from-marionette-to-react)
[Integrating React with Marionette](https://gist.github.com/BinaryMuse/334120e0ef156e410f98)

[human javascript by Henrik Joreteg](http://humanjavascript.com/)
[Human JavaScript Videos](http://learn.humanjavascript.com/react-ampersand)

## Immutability

[facebook/immutable-js](https://github.com/facebook/immutable-js)
[scottcorgan/immu](https://github.com/scottcorgan/immu)
[Pros and Cons of using immutability with React.js - React Kung Fu](http://reactkungfu.com/2015/08/pros-and-cons-of-using-immutability-with-react-js/)

Also see Baobab, Redux, Freeze

## Redux

Redux = ***Red***ucer + Fl***ux***
Implements Flux Store in a FP way. This enables a lot of interesting tools, including *time travel* with app state.

[rackt/redux](https://github.com/rackt/redux)
[Read Me | Redux](http://rackt.org/redux/)

[Dan Abramov - Live React: Hot Reloading with Time Travel at react-europe 2015 - YouTube](https://www.youtube.com/watch?v=xsSnOQynTHs)
[Live-editing React app without refresh on Vimeo](https://vimeo.com/100010922)
[Getting started with Redux - Example application | jchapron](http://www.jchapron.com/2015/08/14/getting-started-with-redux/)
[SurviveJS - Webpack and React - Redux - Reinventing Flux - Interview with Dan Abramov](http://survivejs.com/blog/redux-interview/)
[Flux: Reduce Your Side Effects](https://blog.javascripting.com/2015/08/12/reduce-your-side-effects/)
[What the Flux?! Let’s Redux. | &yet Blog](https://blog.andyet.com/2015/08/06/what-the-flux-lets-redux)

[JSJ The Evolution of Flux Libraries with Andrew Clark and Dan Abramov](https://devchat.tv/js-jabber/181-jsj-the-evolution-of-flux-libraries-with-andrew-clark-and-dan-abramov)
[Feeback wanted: Rewrite with ideas from @acdlite by gaearon · Pull Request #46 · rackt/redux](https://github.com/rackt/redux/pull/46)
[JavaScript Tutorials and Video Workshops - @eggheadio #levelup](https://egghead.io/instructors/dan-abramov)

[State Management with Redux](http://konkle.us/state-management-with-redux/)
[Full-Stack Redux Tutorial](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)
[roderickwang/redux-2way-binding](https://github.com/roderickwang/redux-2way-binding)

[rackt/react-redux](https://github.com/rackt/react-redux)
[gaearon/react-hot-loader](https://github.com/gaearon/react-hot-loader)
[gaearon/redux-devtools](https://github.com/gaearon/redux-devtools)
[omnidan/redux-undo](https://github.com/omnidan/redux-undo)
[gaearon/redux-thunk](https://github.com/gaearon/redux-thunk)
[erikras/redux-form](https://github.com/erikras/redux-form)
[rackt/react-tabs](https://github.com/rackt/react-tabs)
[rackt/react-modal](https://github.com/rackt/react-modal)
[faassen/reselect](https://github.com/faassen/reselect)
[acdlite/redux-actions](https://github.com/acdlite/redux-actions)
[rackt/redux-router](https://github.com/rackt/redux-router)
[acdlite/redux-promise](https://github.com/acdlite/redux-promise)
[acdlite/redux-transducers](https://github.com/acdlite/redux-transducers)
[rackt/react-tabs](https://github.com/rackt/react-tabs)
[xgrommx/awesome-redux](https://github.com/xgrommx/awesome-redux)

gaearon uses normalizr and make observations on Flux
[gaearon/flux-react-router-example](https://github.com/gaearon/flux-react-router-example)
[gaearon/normalizr](https://github.com/gaearon/normalizr)

[How to implement shouldComponentUpdate with this.context? · Issue #2517 · facebook/react](https://github.com/facebook/react/issues/2517)

### boilerplates

[gaearon/library-boilerplate](https://github.com/gaearon/library-boilerplate) webpack
[mattdennewitz/universal-redux-boilerplate](https://github.com/mattdennewitz/universal-redux-boilerplate) webpack
[jackielii/simplest-redux-example](https://github.com/jackielii/simplest-redux-example) browserify
[jonathanp/map-item-filter](https://github.com/jonathanp/map-item-filter) browserify

## Freezer

[React.js the simple way — Medium](https://medium.com/@arqex/react-the-simple-way-cabdf1f42f12)

[arqex/freezer](https://github.com/arqex/freezer)
[arqex/freezer-redux-devtools](https://github.com/arqex/freezer-redux-devtools)

## Baobab

[Yomguithereal/baobab](https://github.com/Yomguithereal/baobab) a tree data structure

[How to improve the data flow in your React app? Introduction to Baobab - React Kung Fu](http://reactkungfu.com/2015/08/how-to-improve-the-data-flow-in-your-react-app-introduction-to-baobab/)
[christianalfoni - Plant a Baobab tree in your flux application](http://www.christianalfoni.com/articles/2015_02_06_Plant-a-Baobab-tree-in-your-flux-application)
[christianalfoni - Handling complex state with Baobab](http://www.christianalfoni.com/articles/2015_04_26_Handling-complex-state-with-Baobab)
