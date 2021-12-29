---
title: Flux Alternatives
toc: true
date: 2015-12-04 12:12:24
categories:
  - web
tags:
  - react-js
  - flux
  - javascript
  - web-dev
---

Sometimes React.js alone may serve your need, you don't have to prematurely flux it.
[The Case for Flux — Startups, Wanderlust, and Life Hacking — Medium](https://medium.com/swlh/the-case-for-flux-379b7d1982c6)
[GantMan/ReactStateMuseum: A whirlwind tour of React state management systems by example](https://github.com/GantMan/ReactStateMuseum)

And there are other strategies besides Flux for architecting your application.
[6 no-Flux strategies for React component communication](http://andrewhfarmer.com/component-communication/)

[What the Flux? An Overview of the React State Management Ecosystem - The New Stack](http://thenewstack.io/flux-overview-react-state-management-ecosystem/)
[André Staltz - Unidirectional User Interface Architectures](http://staltz.com/unidirectional-user-interface-architectures.html)

[voronianski/flux-comparison](https://github.com/voronianski/flux-comparison)

[What is the best state container library for React?](https://medium.com/swlh/what-is-the-best-state-container-library-for-react-b6989a45f236)

Gist of a modern data-driven app:

- don’t use fat models
- unidirectional data flow
- _SINGLE_ source of truth
- mutate data via a _SINGLE_ component
- data from server is just another input, not your model
- [CQRS](http://martinfowler.com/bliki/CQRS.html)
- [Event Sourcing](https://martinfowler.com/eaaDev/EventSourcing.html)

<!-- more -->

> see `ampersand-js.md`
> see `redux-js.md`
> see `reactive-programming.md`

## React Easy State

[Design Patterns with React Easy State – DailyJS – Medium](https://medium.com/dailyjs/design-patterns-with-react-easy-state-830b927acc7c)
[solkimicreb/react-easy-state: Simple React state management. Made with ❤️ and ES6 Proxies.](https://github.com/solkimicreb/react-easy-state)

[The Ideas Behind React Easy State – ITNEXT](https://itnext.io/the-ideas-behind-react-easy-state-901d70e4d03e)

## Recollect

[A different way to manage state in React – Hacker Noon](https://hackernoon.com/a-different-way-to-manage-state-in-react-2d21dfb94482)
Change detection with `Proxy`, a simplified version of what MobX does.

## React + Backbone/Marionette/Ampersand

[Using React components as Backbone Views](http://www.thomasboyt.com/2013/12/17/using-reactjs-as-a-backbone-view.html)
[clayallsopp/react.backbone](https://github.com/clayallsopp/react.backbone)
[Tutorial: Building React Apps With Flux and Backbone | Toptal](http://www.toptal.com/front-end/simple-data-flow-in-react-applications-using-flux-and-backbone)

[Gentle Migration from Marionette to React - Jamie Gaskins](http://jgaskins.org/blog/2015/02/06/gentle-migration-from-marionette-to-react)
[Integrating React with Marionette](https://gist.github.com/BinaryMuse/334120e0ef156e410f98)

## Immutability

[Optimizing Performance – React](https://reactjs.org/docs/optimizing-performance.html)
[React Top-Level API – React.PureComponent](https://reactjs.org/docs/react-api.html#reactpurecomponent)

[Immutable.js](https://facebook.github.io/immutable-js/)
[Turbocharge Your React Application with shouldComponentUpdate and Immutable.js](http://blog.javascripting.com/2015/03/31/turbocharge-your-react-application-with-shouldcomponentupdate-and-immutable-js/)
[The React.js Way: Getting Started Tutorial | RisingStack](https://blog.risingstack.com/the-react-way-getting-started-tutorial/)
[The React.js Way: Flux Architecture with Immutable.js](https://blog.risingstack.com/the-react-js-way-flux-architecture-with-immutable-js/)
[Immutable.js, persistent data structures and structural sharing – Medium](https://medium.com/@dtinth/immutable-js-persistent-data-structures-and-structural-sharing-6d163fbd73d2#.a0af6xid4)
[Building Efficient UI with React and Redux | Toptal](https://www.toptal.com/react/react-redux-and-immutablejs)
[React.js pure render performance anti-pattern – Medium](https://medium.com/@esamatti/react-js-pure-render-performance-anti-pattern-fb88c101332f#.hgg97gg99)
[Pros and Cons of using immutability with React.js - React Kung Fu](http://reactkungfu.com/2015/08/pros-and-cons-of-using-immutability-with-react-js/)
[Using Immutable.JS with Redux · Redux](http://redux.js.org/docs/recipes/UsingImmutableJS.html#what-are-some-opinionated-best-practices-for-using-immutablejs-with-redux)

[Introducing Immer: Immutability the easy way – Hacker Noon](https://hackernoon.com/introducing-immer-immutability-the-easy-way-9d73d8f71cb3)
[mweststrate/immer: Create the next immutable state by mutating the current one](https://github.com/mweststrate/immer)

## Freezer

[React.js the simple way — Medium](https://medium.com/@arqex/react-the-simple-way-cabdf1f42f12)

Freezer by Javier Márquez (arqex) provides immutable state and event emitter that can replace Store and Action/Dispatcher. This greatly reduced the boilerplate and make the Flux flow more understandable. Since it is only a immutable state and event emitter, it is extremely flexible. You can adapt it to _your_ style.

It is true that the state will change often. However, the immutability allows for optimization with [`PureComponent`](https://facebook.github.io/react/docs/react-api.html#react.purecomponent).

[arqex/freezer](https://github.com/arqex/freezer)
[arqex/freezer-redux-devtools](https://github.com/arqex/freezer-redux-devtools)
[Using redux devtools without redux - arqex](http://arqex.com/1087/using-redux-devtools-without-redux) compares design of redux and freezer, and explains the implementation of freezer-redux-devtools

[Test on JS Bin](http://jsbin.com/fedeva/4/edit?js,console)

### Ticker for State Mutation

Use this to generate a ticker that mutate the state ever second.
And use the above `componentDidUpdate()` code for monitoring component updates.

```js
const AppContainer = React.createClass({
  componentDidMount() {
    State.on("update", (obj) => {
      this.forceUpdate();
    });

    State.trigger("test:tick", State.get().tick);
  },
});

// reaction.js or state.js
State.on("test:tick", (tick) => {
  console.log(`tick: ${tick}`);
  State.get().set("tick", tick);

  // trigger next tick
  tick++;
  setTimeout(() => State.trigger("test:tick", tick), 1000);
});
```

## Postal

[postaljs/postal.js: JavaScript pub/sub library supporting advanced subscription features, and several helpful add-ons.](https://github.com/postaljs/postal.js)
[postal.js](https://github.com/postaljs) Org

[a2labs/postal.devtools: A extension for Google Chrome that allows you to view postal messages and interact with the message bus.](https://github.com/a2labs/postal.devtools)

## Cerebral

[Cerebral](http://www.cerebraljs.com/) uses [Yomguithereal/baobab](https://github.com/Yomguithereal/baobab), a tree data structure, as its state. It is similar to Freeze.js.

[How to improve the data flow in your React app? Introduction to Baobab - React Kung Fu](http://reactkungfu.com/2015/08/how-to-improve-the-data-flow-in-your-react-app-introduction-to-baobab/)
[christianalfoni - Plant a Baobab tree in your flux application](http://www.christianalfoni.com/articles/2015_02_06_Plant-a-Baobab-tree-in-your-flux-application)
[christianalfoni - Handling complex state with Baobab](http://www.christianalfoni.com/articles/2015_04_26_Handling-complex-state-with-Baobab)
[christianalfoni - Introducing Cerebral](http://www.christianalfoni.com/articles/2015_09_22_Introducing-Cerebral)

[markuplab/catbee: High level framework based on Catberry, Baobab and Cerebral concepts](https://github.com/markuplab/catbee)

## Reflux

[reflux/refluxjs](https://github.com/reflux/refluxjs)
[Deconstructing ReactJS's Flux](http://spoike.ghost.io/deconstructing-reactjss-flux/)
[The Reflux data flow model](http://blog.krawaller.se/posts/the-reflux-data-flow-model/)

## Unstated

[jamiebuilds/unstated: State so simple, it goes without saying](https://github.com/jamiebuilds/unstated)
[Managing State in React With Unstated | CSS-Tricks](https://css-tricks.com/managing-state-in-react-with-unstated/)

- Put state in `Container`
- Subscribe to `Container` in components
