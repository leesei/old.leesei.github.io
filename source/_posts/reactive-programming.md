---
title: Reactive programming
categories:
  - web
tags:
  - javascript
  - rxjs
  - mobx
toc: true
date: 2016-03-13 15:03:01
---

> Most of the study gears towards JavaScript/web development
> see `functional-programming.md`

[Reactive programming - Wikiwand](https://www.wikiwand.com/en/Reactive_programming)
[The Reactive Manifesto](https://www.reactivemanifesto.org/)

[Reactive programming and Vert.x tutorial: Reactica Coderland](https://developers.redhat.com/coderland/reactive/)
[Functional Programming as the Pillar of Reactive Programming - DZone Web Dev](https://dzone.com/articles/functional-programming-as-the-pillar-of-reactive-p)
[The Best Explanation of JavaScript Reactivity 🎆 – Vue Mastery – Medium](https://medium.com/vue-mastery/the-best-explanation-of-javascript-reactivity-fea6112dd80d)

[The introduction to Reactive Programming you've been missing](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754)
[How React isn't reactive, and why you shouldn't care - DEV Community](https://dev.to/ryansolid/how-react-isn-t-reactive-and-why-you-shouldn-t-care-152m)

[The actor model in 10 minutes](https://www.brianstorti.com/the-actor-model/)
[Hewitt, Meijer and Szyperski: The Actor Model (everything you wanted to know...) - YouTube](https://www.youtube.com/watch?v=7erJ1DV_Tlo)

<!-- more -->

---

[xstream](http://staltz.com/xstream/)
[staltz/xstream: An extremely intuitive, small, and fast functional reactive stream library for JavaScript](https://github.com/staltz/xstream)

[garbles/yolk: A library for building asynchronous user interfaces.](https://github.com/garbles/yolk)

## Xstate

[XState Docs](https://xstate.js.org/docs/)
[davidkpiano/xstate: State machines and statecharts for the modern web.](https://github.com/davidkpiano/xstate)
[@xstate/immer | XState Docs](https://xstate.js.org/docs/packages/xstate-immer/)
[Welcome to the world of Statecharts - Statecharts](https://statecharts.github.io/)

[XState Version 4 Released 🚀. It’s been over a year since I first… | by David Khourshid | Medium](https://medium.com/@DavidKPiano/xstate-version-4-released-665b59409f99)
[The case for statechart and xstate -- why it matters and how we can benefit from it - DEV Community](https://dev.to/coodoo/the-case-for-statechart-and-xstate-why-it-matters-and-how-we-can-benefit-from-it-51fj)
[How to use statecharts - Statecharts](https://statecharts.github.io/how-to-use-statecharts.html)
[XState Tutorial](https://flaviocopes.com/xstate/)
[An Introduction to XState in TypeScript - DEV Community](https://dev.to/giantmachines/an-introduction-to-xstate-in-typescript-1pdn)

[Communicating with spawned and invoked xstate actors in React | by Ismayil Khayredinov | ITNEXT](https://itnext.io/communicating-with-spawned-and-invoked-xstate-actors-in-react-999cca56506b)

[State Chart XML (SCXML): State Machine Notation for Control Abstraction](https://www.w3.org/TR/scxml/)

```js
Statechart =
{
  id: 'state_id',
  context: {
    /* ... */
  }
  initial: 'initial_state',
  states: {
    /* ... */
  }
}

MachineOptions =
{
  {
    actions: {
      /* ... */
    },
    activities: {
      /* ... */
    },
    delays: {
      /* ... */
    },
    guards: {
      /* ... */
    },
    services: {
      /* ... */
    }
  }
}

Machine = (Statechart, MachineOptions)
// Machine has `state`, `context`, `transition()`
// this is merely a declaration of state, not an instance
// `interpret()` it as as Service that stores the current value
// [Machine() | xstate](https://xstate.js.org/api/globals.html#machine)
// [StateMachine | xstate](https://xstate.js.org/api/interfaces/statemachine.html)

Service = interpret(Machine)
// Service has `start()`, `stop()`, `send()`, `onTransition()`
// [interpret() | xstate](https://xstate.js.org/api/globals.html#interpret)
// [Interpreter | xstate](https://xstate.js.org/api/classes/interpreter.html)
```

[Resources | XState Docs](https://xstate.js.org/docs/about/resources.html)
[Showcase | XState Docs](https://xstate.js.org/docs/about/showcase.html)
[darrylhebbes/awesome_xstate: Everything awesome about XState](https://github.com/darrylhebbes/awesome_xstate)

### Playgrounds/Visualizer

[XState Visualizer](https://xstate.js.org/viz/) live preview your state
[StatesKit | Visual Statechart and Finite State Machine editor](https://stateskit.com/) live preview your state, more powerful
[XState TS Viz Template - CodeSandbox](https://codesandbox.io/s/xstate-ts-viz-template-qzdvv?file=/src/index.ts) with TypeScript support

[amitnovick/xstate-devtools](https://github.com/amitnovick/xstate-devtools)

[@xstate/inspect | XState Docs](https://xstate.js.org/docs/packages/xstate-inspect/) open statechart at https://statecharts.io/, only works on web?
[xstate/packages/xstate-inspect at master · davidkpiano/xstate · GitHub](https://github.com/davidkpiano/xstate/tree/master/packages/xstate-inspect)

### Tutorial

[The React Podcast #5: Finite State Machines with David Khourshid | News and podcasts for developers | Changelog](https://changelog.com/reactpodcast/5)
[Modeling UI States in A React Form Component Using A Finite State Machine](https://tech.okcupid.com/modeling-ui-states-in-react-form-component-using-finite-state-machine/)
[Implementing a simple state machine library in JavaScript](https://kentcdodds.com/blog/implementing-a-simple-state-machine-library-in-javascript)
[Finite State Machines with React | CSS-Tricks](https://css-tricks.com/finite-state-machines-with-react/)
[Robust React User Interfaces with Finite State Machines | CSS-Tricks](https://css-tricks.com/robust-react-user-interfaces-with-finite-state-machines/)
[State Machines in React](https://mastery.games/post/state-machines-in-react/)
[Stop using isLoading booleans](https://kentcdodds.com/blog/stop-using-isloading-booleans) use `status` (state machine)
[Coding a Finite-State Machine in a React Hook - The Non-Traditional Developer - Medium](https://medium.com/the-non-traditional-developer/coding-a-finite-state-machine-in-a-react-hook-9c58e2296df0)
[Thoughts on state management with XState and ReactJS - DEV Community](https://dev.to/rjdestigter/thoughts-on-state-management-with-xstate-and-reactjs-3d19)
[rjdestigter/xstate-sample-kit: Sample or starter kit for developing web applications with reactjs, xstate, typescript, xstate/test, storybook, typedoc, fp-ts, and other libraries.](https://github.com/rjdestigter/xstate-sample-kit)
[Introducing state machine advent: 24 bite-sized blog posts about state machines and statecharts - DEV Community](https://dev.to/codingdive/introducing-state-machine-advent-24-bite-sized-blog-posts-about-state-machines-and-statecharts-2ce0)
[XState TodoMVC - CodeSandbox](https://codesandbox.io/s/xstate-todomvc-33wr94qv1?from-embed=&file=/Todos.jsx)
[Model-Based Testing in React with State Machines | CSS-Tricks](https://css-tricks.com/model-based-testing-in-react-with-state-machines/)
[Intro to Xstate — a true state management library for react | Weekly Webtips](https://medium.com/weekly-webtips/intro-to-xstate-a-true-state-management-system-library-for-react-d8c0051c71e4)
[Computational Design Tsools](https://bradwoods.io/tools) games and UI sample
[coodoo/xstate-examples: A series of examples showing how to model application state with statechart using xstate](https://github.com/coodoo/xstate-examples)

### Video

[XState: Let's pair program state machines and state charts with David Khourshid - YouTube](https://www.youtube.com/watch?v=uRfQJJArZEg)
[Introduction to State Machines Using XState | egghead.io](https://egghead.io/courses/introduction-to-state-machines-using-xstate)
[Introducing Construct Sturdy UIs with XState | egghead.io](https://egghead.io/lessons/react-introducing-construct-sturdy-uis-with-xstate)
[Let’s learn state machines with David K. Piano! — Learn With Jason - YouTube](https://www.youtube.com/watch?v=czi24DqUfSA)
[David Khourshid - Formal Forms with State Machines | React Next 2019 - YouTube](https://www.youtube.com/watch?v=hiT4Q1ntvzg)
[David Khourshid - Infinitely Better UIs with Finite Automata - YouTube](https://www.youtube.com/watch?v=VU1NKX6Qkxc)
[Crafting Stateful Styles with State Machines by David Khourshid | CSSConf BP 2019 - YouTube](https://www.youtube.com/watch?v=0cqeGeC98MA)
[#React Wednesdays: XState and JavaScript State Machines - YouTube](https://www.youtube.com/watch?v=1TT2ymkYGyM)
[XState - Video Player & Nested States - Finite State Machines in React - YouTube](https://www.youtube.com/watch?v=d8V5vcZOQe4) [repo](https://github.com/leighhalliday/video-state-machine) example use XState + React, substate

## Overmind

[Overmind - OVERMIND](https://overmindjs.org/)
[Using state machines - OVERMIND](https://overmindjs.org/guides-1/using-state-machines)
[Statechart - OVERMIND](https://overmindjs.org/addons/statecharts)
[React - OVERMIND](https://overmindjs.org/views/react)

## MobX

[Introduction | MobX](https://mobxjs.github.io/mobx/)
[mobxjs/mobx: Simple, scalable state management.](https://github.com/mobxjs/mobx)
[Becoming fully reactive: an in-depth explanation of MobX — Medium](https://medium.com/@mweststrate/becoming-fully-reactive-an-in-depth-explanation-of-mobservable-55995262a254#.p9gj6ys9n)

[MobX: Ten minute introduction to MobX and React](https://mobxjs.github.io/mobx/getting-started.html)
[3 Reasons why I stopped using React.setState – Medium](https://medium.com/@mweststrate/3-reasons-why-i-stopped-using-react-setstate-ab73fc67a42e#.f1vp66jlf)

## Reactive Extensions (Rx)

[ReactiveX](http://reactivex.io/)
[ReactiveX - Intro](http://reactivex.io/intro.html)
[Functional Programming in Javascript](http://reactivex.io/learnrx/)
[Introduction to Rx](http://www.introtorx.com/)

[Reactive-Extensions/RxJS: The Reactive Extensions for JavaScript](https://github.com/Reactive-Extensions/RxJS) RxJS 4.0
[ReactiveX/RxJS: A reactive programming library for JavaScript](https://github.com/ReactiveX/RxJS) RxJS 5.0

[An introduction to reactive programming](https://codewords.recurse.com/issues/two/an-introduction-to-reactive-programming)
[Introduction | RxJS - Javascript library for functional reactive programming.](https://xgrommx.github.io/rx-book/)
[Functional Reactive Game Programming – RxJS Breakout | manu.ninja](https://manu.ninja/functional-reactive-game-programming-rxjs-breakout)
[第 12 屆 iT 邦幫忙鐵人賽::用 30 天向世界宣告，這一年來鋼鐵般的歷練](https://ithelp.ithome.com.tw/2020-12th-ironman/articles/2959?sc=iThomeR)

[RxJS with React Hooks for state management - LogRocket Blog](https://blog.logrocket.com/rxjs-with-react-hooks-for-state-management/)

[christianalfoni - RxJs the smartest dumbest tool ever](http://www.christianalfoni.com/articles/2016_03_31_RxJs-the-smartest-dumbest-tool-ever)
[christianalfoni - Creating apps with observables](http://www.christianalfoni.com/articles/2016_03_27_Creating-apps-with-observables)

[Introduction to Functional Reactive Programming with RxJS](https://www.sitepoint.com/functional-reactive-programming-rxjs/)
[10 Need-to-Know RxJS Functions with Examples](https://www.sitepoint.com/rxjs-functions-with-examples/)
[Learn RxJS in 60 Minutes for Beginners - Free Crash Course - YouTube](https://www.youtube.com/watch?v=PhggNGsSQyg)

[MVC to FRP by Gleb Bahmutov - Cycle Conf. Copenhagen 2016 - YouTube](https://www.youtube.com/watch?v=-PCq4pXaDZw)
[slide](http://slides.com/bahmutov/mvc-frp/) [notes](https://glebbahmutov.com/blog/cycle-conf/)
[Building realtime applications with CycleJS and RxJS - Pusher Blog](https://blog.pusher.com/building-realtime-applications-with-cyclejs-and-rxjs/)

## Pubsub

[PubSub for communicating between React Components - Coding Stuff - Medium](https://medium.com/coding-stuff/pubsub-for-communicating-between-react-components-999159d59a77)

[lukeed/vegemite: A Pub/Sub state manager you'll love... or hate](https://github.com/lukeed/vegemite)

## Cycle.js

[Cycle.js](http://cycle.js.org/)
[Cycle.js](https://github.com/cyclejs) GitHub org
[Basic examples › Cycle.js](http://cycle.js.org/basic-examples.html)

[Cycle.js Fundamentals from @andrestaltz on @eggheadio](https://egghead.io/courses/cycle-js-fundamentals)

## egghead

[RxJS Lessons - Screencast Video Tutorials @eggheadio](https://egghead.io/technologies/rx)
[What Is RxJS? - RxJS Video Tutorial #free @eggheadio](https://egghead.io/lessons/rxjs-what-is-rxjs)
[Cycle.js Fundamentals - Course by @andrestaltz @eggheadio](https://egghead.io/series/cycle-js-fundamentals)

---

## RxPy

[Valery Calderon - Reactive Programming with RxPy - PyCon 2018 - YouTube](https://www.youtube.com/watch?v=I5AZ3rTR4Wc) [slide](https://speakerdeck.com/pycon2018/valery-calderon-reactive-programming-with-rxpy)

## C#

[StateMachine Class (System.Activities.Statements) | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/api/system.activities.statements.statemachine?redirectedfrom=MSDN&view=netframework-4.8)
[How to: Create a State Machine Workflow | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/framework/windows-workflow-foundation/how-to-create-a-state-machine-workflow?redirectedfrom=MSDN)

[Simple state machine example in C#? - Stack Overflow](https://stackoverflow.com/questions/5923767/simple-state-machine-example-in-c)
