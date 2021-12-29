---
title: Redux
toc: true
date: 2015-12-04 12:12:25
categories:
  - web
tags:
  - react-js
  - redux-js
  - flux
  - javascript
  - web-dev
---

Redux by Dan Abramov (gaearon) implements Flux Store in a FP way. This enables a lot of interesting tools, including _time travel_ with app state. He committed the topic to a conference and Redux came out of the demo code. It is now part of the official React project.

> remove pre-Redux Toolkit tutorials

[Redux Doc](http://redux.js.org/)
[reactjs/redux: Predictable state container for JavaScript apps](https://github.com/reactjs/redux)
[Ecosystem · Redux](https://redux.js.org/introduction/ecosystem)
[The only introduction to Redux (and React-Redux) you’ll ever need](https://medium.com/javascript-in-plain-english/the-only-introduction-to-redux-and-react-redux-youll-ever-need-8ce5da9e53c6)
[xgrommx/awesome-redux](https://github.com/xgrommx/awesome-redux)
[markerikson/react-redux-links: Curated tutorial and resource links I've collected on React, Redux, ES6, and more](https://github.com/markerikson/react-redux-links)

Redux = **_Red_**ucer + Fl**_ux_**

[React.js Conf 2016 - Lin Clark - A Cartoon Guide to the Wilds of Data Handling - YouTube](https://www.youtube.com/watch?v=WIqbzHdEPVM)
[I created the exact same app with Redux and React. Here are the differences.](https://medium.com/javascript-in-plain-english/i-created-the-exact-same-app-with-react-and-redux-here-are-the-differences-6d8d5fb98222)

[React Redux Tutorial for Beginners [2019] - RWieruch](https://www.robinwieruch.de/react-redux-tutorial) !important
[How Redux Works: A Counter-Example](https://daveceddia.com/how-does-redux-work/)
[Understanding Redux: The World’s Easiest Guide to Beginning Redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6) Understanding Redux 1 in [The ReduxJS Books](https://thereduxjsbooks.com/)

[Understanding Redux: Beginner's guide to modern state management](https://www.educative.io/blog/understanding-redux)
[Redux for React: A Simple Introduction – Ross Bulat – Medium](https://medium.com/@rossbulat/redux-for-react-a-simple-introduction-b1f9dcbda8f4)
[Redux Basics Explained From A Beginner's Perspective - DEV Community 👩‍💻👨‍💻](https://dev.to/dylanmesty/redux-basics-explained-from-a-beginner-s-perspective-abm)
[Leveling Up with React: Redux | CSS-Tricks](https://css-tricks.com/learning-react-redux/)
[Blogged Answers: Resources for Learning Redux · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/12/blogged-answers-learn-redux/)
[Practical Redux · Mark's Dev Blog](https://blog.isquaredsoftware.com/series/practical-redux/)
[Idiomatic Redux: The Tao of Redux, Part 1 - Implementation and Intent · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-1/)
[Idiomatic Redux: The Tao of Redux, Part 2 - Practice and Philosophy · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-2/)

[Redux: The Under The Hood Tour - DEV Community 👩‍💻👨‍💻](https://dev.to/fawwaz2009/redux-the-under-the-hood-tour-2k87) !important, internals

## Action and ActionCreator

```js
// Action
{ type: 'ADD_TODO', payload: 'Use Redux' }

// ActionCreator
addTodo = (text) => {
  return { type: 'ADD_TODO', payload: text };
}

// thunk, return function/promise for `dispatch()`
// avoid accessing state other than conditional dispatch
// (using cached data, checking authentication)
// passing data in store is considered an anti-pattern
// OR perform any side effect (fat action)
export function addTodoWithCheck(text) {
  return (dispatch, getState) => {
    if (getState().todos.length === 3) {
      // early exit
      return;
    }

    dispatch(addTodo(text));
  }
}
```

## Reducer

```js
reducer = (state, action) => {
  return newState;
};

// reducing boilerplate with `createReducer()` and state slicing
function createReducer(initialState, handlers) {
  return function reducer(state = initialState, action) {
    if (handlers.hasOwnProperty(action.type)) {
      return handlers[action.type](state, action);
    } else {
      return state;
    }
  };
}

const visibilityReducer = createReducer("SHOW_ALL", {
  SET_VISIBILITY_FILTER: (visibilityState, action) => action.visibility,
});

const todosReducer = createReducer([], {
  // case handlers
  ADD_TODO: addTodo,
  TOGGLE_TODO: toggleTodo,
  EDIT_TODO: editTodo,
});

const appReducer = combineReducers({
  visibilityFilter: visibilityReducer,
  todos: todosReducer,
});
```

[Reusing Reducer Logic · Redux](https://redux.js.org/recipes/structuring-reducers/reusing-reducer-logic) by bounding different `name` to it for different components and state slice
[Understanding How Reducers are Used in Redux | CSS-Tricks](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/)

### Middleware

Redux middleware is designed by creating functions that can be composed together before the main dispatch method is invoked.

[You Aren’t Using Redux Middleware Enough – Jacob Parker – Medium](https://medium.com/@jacobp100/you-arent-using-redux-middleware-enough-94ffe991e6)
[Understanding Redux Middleware - Mark - Medium](https://medium.com/@meagle/understanding-87566abcfb7a)
[Methods for tracking action status in Redux - LogRocket Blog](https://blog.logrocket.com/tracking-action-status-in-redux/) `type.endsWith("_REQUEST|SUCCESS|FAILURE")` to set state

```js
(storeInstance) =>
  (functionToCallWithAnActionThatWillSendItToTheNextMiddleware) =>
  (actionThatDispatchWasCalledWith) =>
    valueToUseAsTheReturnValueOfTheDispatchCall;
// or in short
(store) => (next) => (action) => result;

// redux-thunk
const middledWare =
  ({ dispatch, getState }) =>
  (next) =>
  (action) => {
    if (typeof action === "function") {
      return action(dispatch, getState, extraArgument);
    }
    return next(action);
  };
```

```js
const middlewares = applyMiddleware(middleware1, middleware2);
const store = createStore(reducers, initialState, middlewares);
```

```js
export function loadPosts(userId) {
  return {
    // Types of actions to emit before and after
    types: ["LOAD_POSTS_REQUEST", "LOAD_POSTS_SUCCESS", "LOAD_POSTS_FAILURE"],
    // Check the cache (optional):
    shouldCallAPI: (state) => !state.posts[userId],
    // Perform the fetching:
    callAPI: () => fetch(`http://myapi.com/users/${userId}/posts`),
    // Arguments to inject in begin/end actions
    payload: { userId },
  };
}

function callAPIMiddleware({ dispatch, getState }) {
  return (next) => (action) => {
    const {
      types,
      callAPI,
      shouldCallAPI = (state) => true,
      payload = {},
    } = action;

    if (!types) {
      // Normal action: pass it on
      return next(action);
    }

    if (!shouldCallAPI(getState())) {
      return;
    }

    const [requestType, successType, failureType] = types;

    dispatch(
      Object.assign({}, payload, {
        type: requestType,
      })
    );

    return callAPI().then(
      (response) =>
        dispatch(
          Object.assign({}, payload, {
            response,
            type: successType,
          })
        ),
      (error) =>
        dispatch(
          Object.assign({}, payload, {
            error,
            type: failureType,
          })
        )
    );
  };
}
```

## Store

```js
import { combineReducers, createStore, applyMiddleware } from "redux";

rootReducer = combineReducers({ key1: reducer1, key2: reducer2 });
store = createStore(rootReducer, initState, applyMiddleware(middlewares));
```

[The Ultimate Cheat Sheet on Splitting Dynamic Redux Reducers](https://medium.com/velotio-perspectives/the-ultimate-cheat-sheet-on-splitting-dynamic-redux-reducers-322ca17d5350)

### Enhancers

Enhancers return a new **enhanced** version of `createStore()`. `applyMiddleware()` is (actually it returns) an enhancer.

```js
const ourAwesomeEnhancer =
  (createStore) => (reducer, initialState, enhancer) => {
    const store = createStore(monitoredReducer, initialState, enhancer);
    //  add enhancer logic

    return {
      ...store,
      //   you can override the some store properties or add new ones
    };
  };
```

---

[#187: Redux, React, and Functional JavaScript with Dan Abramov - The Changelog](https://changelog.com/187/)
[JSJ The Evolution of Flux Libraries with Andrew Clark and Dan Abramov](https://devchat.tv/js-jabber/181-jsj-the-evolution-of-flux-libraries-with-andrew-clark-and-dan-abramov)
[Dan Abramov - Live React: Hot Reloading with Time Travel at react-europe 2015 - YouTube](https://www.youtube.com/watch?v=xsSnOQynTHs) The presentation where Redux is born
[Dan Abramov - The Redux Journey at react-europe 2016 - YouTube](https://www.youtube.com/watch?v=uvAXVMwHJXU)

[Redux without the sanity checks in a single file.](https://gist.github.com/gaearon/ffd88b0e4f00b22c3159)
[Super minimal React + Redux app](https://gist.github.com/gaearon/074b0905337a6a835d82)

[Redux Framework](https://reduxframework.com/) for WordPress

[Idiomatic Redux · Mark's Dev Blog](http://blog.isquaredsoftware.com/series/idiomatic-redux/)
[Idiomatic Redux: The Tao of Redux, Part 1 - Implementation and Intent · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-1/)
[Idiomatic Redux: The Tao of Redux, Part 2 - Practice and Philosophy · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-2/)
[Idiomatic Redux: The History and Implementation of React-Redux · Mark's Dev Blog](https://blog.isquaredsoftware.com/2018/11/react-redux-history-implementation/)

[SurviveJS - Webpack and React - Redux - Reinventing Flux - Interview with Dan Abramov](http://survivejs.com/blog/redux-interview/)
[A cartoon intro to Redux — Code Cartoons — Medium](https://code-cartoons.com/a-cartoon-intro-to-redux-3afb775501a6#.lxpvf5krl) Redux vs Flux
[Understanding the Redux paradigm | Tryolabs | Blog](http://blog.tryolabs.com/2016/04/19/understanding-the-redux-paradigm/)
[A better way to organize redux state - ITNEXT](https://itnext.io/a-better-way-to-organize-redux-state-6a62dd79b2df)

[Step by Step Guide To Building React Redux Apps — Medium](https://medium.com/@rajaraodv/step-by-step-guide-to-building-react-redux-apps-using-mocks-48ca0f47f9a)
[Full-Stack Redux Tutorial](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)
[Full-Stack Redux Tutorial](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)
[Game of Life (React + Redux)](https://codepen.io/thepeted/pen/bpovxz)
[Complete Intro to React](https://btholt.github.io/complete-intro-to-react/) [repo](https://github.com/btholt/complete-intro-to-react)

## Screencast

[Getting Started with Redux - Course by @dan_abramov @eggheadio](https://egghead.io/series/getting-started-with-redux) free video course, !important
[Building React Applications with Idiomatic Redux from @dan_abramov on @eggheadio](https://egghead.io/courses/building-react-applications-with-idiomatic-redux) free video course, !important
[tayiorbeii/egghead.io_redux_course_notes: Notes (and partial transcription) of Dan Abramov's Redux course videos on http://egghead.io](https://github.com/tayiorbeii/egghead.io_redux_course_notes)
[Building React Applications with Idiomatic Redux - Course by @dan_abramov @eggheadio](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)
[Learn Redux — 20 video tutorials to help you learn how to build JavaScript apps with React.js and Redux.](https://learnredux.com/) !important, by Wes Bos

[17. React Redux with Dan Abramov - YouTube](https://www.youtube.com/watch?v=VJ38wSFbM3A)
[Live-editing React app without refresh on Vimeo](https://vimeo.com/100010922)
[Learn Redux - YouTube](https://www.youtube.com/playlist?list=PLu8EoSxDXHP5uyzEWxdlr9WQTJJIzr6jy) by Wes Bos

## Ecosystem

[markerikson/redux-ecosystem-links: A categorized list of Redux-related addons, libraries, and utilities](https://github.com/markerikson/redux-ecosystem-links)
[Understanding Redux Middleware – Medium](https://medium.com/@meagle/understanding-87566abcfb7a#.kpd9ykw40)

[Redux Toolkit](https://redux-toolkit.js.org/)
[reduxjs/redux-toolkit: The official, opinionated, batteries-included toolset for efficient Redux development](https://github.com/reduxjs/redux-toolkit)
[Redux Toolkit - The Standard Way to Write Redux - DEV Community](https://dev.to/nilanth/redux-toolkit-the-standard-way-to-write-redux-2g32)

[pauldijou/redux-act: An opinionated lib to create actions and reducers for Redux](https://github.com/pauldijou/redux-act)
[acdlite/redux-actions: Flux Standard Action utilities for Redux.](https://github.com/acdlite/redux-actions)
[acdlite/flux-standard-action: A human-friendly standard for Flux action objects.](https://github.com/acdlite/flux-standard-action)

[rackt/redux-router](https://github.com/rackt/redux-router)

[gaearon (Dan Abramov)](https://github.com/gaearon?tab=repositories)
[gaearon/react-hot-loader: Tweak React components in real time.](https://github.com/gaearon/react-hot-loader)
[paularmstrong/normalizr: Normalizes nested JSON according to a schema](https://github.com/paularmstrong/normalizr) normalize domain data

[reduxjs/redux-devtools: DevTools for Redux with hot reloading, action replay, and customizable UI](https://github.com/reduxjs/redux-devtools) uses normalizr and make observations on Flux
[Redux Devtools for Dummies – codeburst](https://codeburst.io/redux-devtools-for-dummies-74566c597d7)

[gajus/redux-immutable: redux-immutable is used to create an equivalent function of Redux combineReducers that works with Immutable.js state.](https://github.com/gajus/redux-immutable)

[omnidan/redux-undo](https://github.com/omnidan/redux-undo)

[Redux Utilities](https://github.com/redux-utilities)
[redux-utilities/flux-standard-action: A human-friendly standard for Flux action objects.](https://github.com/redux-utilities/flux-standard-action)
[redux-utilities/redux-promise: FSA-compliant promise middleware for Redux.](https://github.com/redux-utilities/redux-promise)
[redux-utilities/redux-actions: Flux Standard Action utilities for Redux.](https://github.com/redux-utilities/redux-actions)
[redux-utilities/reduce-reducers: Reduce multiple reducers into a single reducer from left to right](https://github.com/redux-utilities/reduce-reducers)

[acdlite/recompose: A React utility belt for function components and higher-order components.](https://github.com/acdlite/recompose) ideas incorporated into React Hooks

[leoasis/redux-immutable-state-invariant: Redux middleware that detects mutations between and outside redux dispatches. For development use only.](https://github.com/leoasis/redux-immutable-state-invariant)
[socialtables/redux-unhandled-action: Redux middleware that logs an error to the console when an action is fired and the state is not mutated](https://github.com/socialtables/redux-unhandled-action)

## On the contrary

> see `flux-alternatives.md`

[Blogged Answers: Redux - Not Dead Yet! · Mark's Dev Blog](https://blog.isquaredsoftware.com/2018/03/redux-not-dead-yet/)
[You Might Not Need Redux – Medium](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)
[Redux feels bloated, complicated and not easy. What are the alternative? : reactjs](https://www.reddit.com/r/reactjs/comments/3towfy/redux_feels_bloated_complicated_and_not_easy_what/)
[reactjs - What could be the downsides of using Redux instead of Flux - Stack Overflow](http://stackoverflow.com/questions/32021763/what-could-be-the-downsides-of-using-redux-instead-of-flux/32916602#32916602)

[Introduction - Reatom — state manager with a focus of all needs](https://artalar.github.io/reatom/#/)
[artalar/reatom: State manager with a focus of all needs](https://github.com/artalar/reatom)

### ReactN

[CharlesStover/reactn: React, but with built-in global state management.](https://github.com/CharlesStover/reactn)

[Tough Actin' ReactN ← Alligator.io](https://alligator.io/react/tough-actin-reactn/)
[The Future of React Reducers and Global State Management](https://medium.com/@rossbulat/the-future-of-react-reducers-and-global-state-management-30cda8a3b082)

### React PowerPlug

[React PowerPlug](http://rena.to/react-powerplug/)
[Rapid Prototyping Made Easy with React PowerPlug ← Alligator.io](https://alligator.io/react/react-powerplug/)
[renatorib/react-powerplug: Renderless Containers](https://github.com/renatorib/react-powerplug)

## Tips and Tricks

[Two Weird Tricks with Redux](http://jlongster.com/Two-Weird-Tricks-with-Redux)
[Scaling Redux for real-life applications – Hacker Noon](https://hackernoon.com/scaling-redux-for-real-life-applications-be18c731a54d)
[Scaling your Redux App with ducks](https://medium.freecodecamp.com/scaling-your-redux-app-with-ducks-6115955638be#.txowddfkt)
[Redux Patterns and Anti-Patterns - Affirm Tech Blog](https://tech.affirm.com/redux-patterns-and-anti-patterns-7d80ef3d53bc#.451p9ycfy)
[Optimize Redux before it kills your Application - JavaScript in Plain English - Medium](https://medium.com/javascript-in-plain-english/optimize-redux-before-it-kills-your-application-6b73cf5f520b)

## Hooks API

[Hooks · React Redux](https://react-redux.js.org/next/api/hooks)
[How To Use Redux with React Hooks - ITNEXT](https://itnext.io/how-to-use-redux-with-react-hooks-5422a7ceae6e)
[The Latest and Greatest Redux Hooks API - The Startup - Medium](https://medium.com/swlh/the-latest-and-greatest-redux-hooks-api-a0112d926fc4)
[Clean Up Redux Code with React-Redux Hooks - The Startup - Medium](https://medium.com/swlh/clean-up-redux-code-with-react-redux-hooks-71587cfcf87a)
[Redux Hooks in React: An Introduction - Ross Bulat - Medium](https://medium.com/@rossbulat/redux-hooks-in-react-an-introduction-ffa8e1057fc2)
[How I reduced the code in my Redux app by using Redux Hooks.](https://medium.com/javascript-in-plain-english/how-i-reduced-the-amount-of-code-in-my-redux-app-by-using-redux-hooks-b19c926419ea)

[Clean Up Redux Code with React-Redux Hooks | by Max González | The Startup | Medium](https://medium.com/swlh/clean-up-redux-code-with-react-redux-hooks-71587cfcf87a)
[React Hooks-Oriented Redux Coding Pattern Without Thunks and Action Creators](https://medium.com/better-programming/react-hooks-oriented-redux-coding-pattern-without-thunks-and-action-creators-b338b42c5327)
[dai-shi/reactive-react-redux: React Redux binding with React Hooks and Proxy](https://github.com/dai-shi/reactive-react-redux)

## Data flow

Handles async and side effects:
[reduxjs/redux-thunk: Thunk middleware for Redux](https://github.com/reduxjs/redux-thunk)
[redux-saga/redux-saga: An alternative side effect model for Redux apps](https://github.com/redux-saga/redux-saga) uses `while`-loop and generators
[How to perfectly handle user-interactions with redux-saga](https://itnext.io/how-to-perfectly-handle-user-interactions-with-redux-saga-5e5944e3ed8b)
[redux-loop/redux-loop: A library that ports Elm's effect system to Redux](https://github.com/redux-loop/redux-loop)
[lelandrichardson/redux-pack: Sensible promise handling and middleware for redux](https://github.com/lelandrichardson/redux-pack)

[Redux pattern: byId reducer - NEXT Engineering - Medium](https://medium.com/collaborne-engineering/redux-pattern-byid-reducers-323a863fa64e)
[Async actions handling with redux-thunk - NaNLABS](https://www.nan-labs.com/blog/handle-async-actions-redux-thunk/)
[What the heck is a 'thunk'?](https://daveceddia.com/what-is-a-thunk/)
[Thunks in Redux: The Basics - Fullstack Academy - Medium](https://medium.com/fullstack-academy/thunks-in-redux-the-basics-85e538a3fe60)
[javascript - How to dispatch a Redux action with a timeout? - Stack Overflow](https://stackoverflow.com/questions/35411423/how-to-dispatch-a-redux-action-with-a-timeout/)
[Where do I put my business logic in a React Redux application? | CodeWinds](http://codewinds.com/blog/2016-08-16-business-logic-redux.html)
[Handling Asynchronous Actions in Redux - Better Programming - Medium](https://medium.com/better-programming/handling-asynchronous-actions-in-redux-86724ed87c6c)
[Don’t use async Redux middleware - Christian Chown - Medium](https://medium.com/@christianchown/dont-use-async-redux-middleware-c8a1015299ec)
[Handling Asynchronous Actions with Redux Thunk - The Startup - Medium](https://medium.com/swlh/handling-asynchronous-actions-with-redux-thunk-86b8d8e0b83e)

[A chained modals example w/ React Bootstrap - SaltyCrane Blog](https://www.saltycrane.com/blog/2016/02/chained-modals-example-react-bootstrap/)
[A chained modals example w/ React Router (part 2) - SaltyCrane Blog](https://www.saltycrane.com/blog/2016/03/chained-modals-example-react-router-part-2/)
[Comparing vanilla React, Redux, and Redux Thunk - Chained modals exercise part 3 - SaltyCrane Blog](https://www.saltycrane.com/blog/2016/05/comparing-vanilla-react-redux-and-redux-thunk-chained-modals/)

[Actors: How to dispatch actions after Redux state changes](http://jamesknelson.com/join-the-dark-side-of-the-flux-responding-to-actions-with-actors/)
[Can I dispatch multiple actions from Redux action creators?](http://jamesknelson.com/can-i-dispatch-multiple-actions-from-redux-action-creators/)
[Updating Normalized Data · Redux](https://redux.js.org/recipes/structuring-reducers/updating-normalized-data)

[christianalfoni - The case for function tree](http://www.christianalfoni.com/articles/2016_09_11_The-case-for-function-tree)
[Redux 4 Ways – React Native Training – Medium](https://medium.com/react-native-training/redux-4-ways-95a130da0cdc#.yhkcy935e)
[State Management with Redux](http://konkle.us/state-management-with-redux/)
[Querying a Redux Store – Medium](https://medium.com/@adamrackis/querying-a-redux-store-37db8c7f3b0f#.xax4uwvif)
[Idiomatic Redux: Thoughts on Thunks, Sagas, Abstraction, and Reusability · Mark's Dev Blog](http://blog.isquaredsoftware.com/2017/01/idiomatic-redux-thoughts-on-thunks-sagas-abstraction-and-reusability/)
[You may not need to thunk – Medium](https://medium.com/@thisismissem/you-may-not-need-to-thunk-f5dc7a6fcbca#.d28w6abao)
[Using redux-saga To Simplify Your Growing React Native Codebase](https://shift.infinite.red/using-redux-saga-to-simplify-your-growing-react-native-codebase-2b8036f650de#.yhy5r2mv2)
[react-redux-links/redux-side-effects.md at master · markerikson/react-redux-links](https://github.com/markerikson/react-redux-links/blob/master/redux-side-effects.md)

[Cheng Lou - On the Spectrum of Abstraction at react-europe 2016 - YouTube](https://www.youtube.com/watch?v=mVVNJKv9esE) !important

## Authentication

[Secure Your React and Redux App with JWT Authentication](https://auth0.com/blog/secure-your-react-and-redux-app-with-jwt-authentication/)
[Role Based Authorization in React - Better Programming - Medium](https://medium.com/better-programming/role-based-authorization-in-react-c70bb7641db4)

## react-redux

[React Redux · Official React bindings for Redux](https://react-redux.js.org/)
[Api · React Redux](https://react-redux.js.org/api)
[reduxjs/react-redux: Official React bindings for Redux](https://github.com/reduxjs/react-redux)

[17. React Redux with Dan Abramov - YouTube](https://www.youtube.com/watch?v=VJ38wSFbM3A)

Notice how [`AddTodo`](https://redux.js.org/basics/usage-with-react#implementing-other-components) is implemented as a functional stateless components.

[Connecting Redux to React Using React Redux ← Alligator.io](https://alligator.io/react/react-redux/) define types, action, reducer, connect to component
[React-Redux connect(): when and how to use it – LogRocket](https://blog.logrocket.com/react-redux-connect-when-and-how-to-use-it-f2a1edab2013)

```js
// Container Components is generated with `connect()`
import { connect } from 'react-redux'

// selector and compute derived values
const mapStateToProps = (state, ownProps) => {
  return {
    value1: state.key1,
    computed: compute(state.key2)
  }
}
// add `onXXX()` callback props and dispatch the action
const mapDispatchToProps = (dispatch, ownProps) => {
  return {
    onClick: () => dispatch(...)
  }
}

// mapDispatchToProps() can be replaced by an object of ActionCreators
// they will be wrapped by `dispatch()` upon invocation
// https://react-redux.js.org/api

// `dispatch()` and the objects returned by the functions will
// be passed to the wrapped Presentation Container as `props`
const VisibleTodoList = connect(
  mapStateToProps,
  mapDispatchToProps,
  mergeProps,
  options
)(TodoList)

// if `mapStateToProps()` is expensive
// override `options.areStatesEqual` to compare subtree

export default VisibleTodoList
```

## Derived Data

[Selector pattern in React/Redux apps - NaNLABS](https://www.nan-labs.com/blog/selector-pattern-in-react-redux-apps/)
[Computing Derived Data · Redux](https://redux.js.org/recipes/computing-derived-data)
[Understanding Javascript Selectors With and Without Reselect](https://medium.com/@pearlmcphee/selectors-react-redux-reselect-9ab984688dd4)
[React, Reselect and Redux - Dan Parker - Medium](https://medium.com/@parkerdan/react-reselect-and-redux-b34017f8194c)

[reactjs/reselect: Selector library for Redux](https://github.com/reactjs/reselect) memoized transform
[heyimalex/reselect-map: Selectors for mapping over collections](https://github.com/HeyImAlex/reselect-map) the transform is expensive for each item
[Mastercard Developers](https://developer.mastercard.com/blog/common-reselect-gotchas)

```js
import { createSelector } from 'reselect'

// signature matches the invocation from `mapStateToProps()`
const inputSelector1 = (state, props) => state[props.key1]
const inputSelector2 = (state, props) => state.key2

const mySelector = createSelector(
  inputSelector1, inputSelector2...,
  (input1, input2...) => {
    return ...
  }
)

// check this if the component using `mySelector()` have multiple instances
// https://redux.js.org/recipes/computing-derived-data#sharing-selectors-across-multiple-components
```

## boilerplates

[chin-phang/react-redux-quickstart: Create React + Redux apps](https://github.com/chin-phang/react-redux-quickstart) SCSS
[FullstackTypeScript/redux-bootstrap: A bootstrap() function for initializing Redux applications.](https://github.com/FullstackTypeScript/redux-bootstrap)
[reduxjs/redux-starter-kit: A simple set of tools to make using Redux easier](https://github.com/reduxjs/redux-starter-kit)
[erikras/ducks-modular-redux: A proposal for bundling reducers, action types and actions when using Redux](https://github.com/erikras/ducks-modular-redux)

[Scaling your Redux App with ducks](https://medium.freecodecamp.com/scaling-your-redux-app-with-ducks-6115955638be#.txowddfkt) folder structure

---

## Rematch

[Rematch | Rematch](https://rematchjs.org/)
[Getting Started · Rematch](https://rematch.gitbooks.io/rematch/content/#getting-started)
[Rematch - a better Redux?](https://blog.openreplay.com/rematch-a-better-redux)
