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

[Redux Doc](http://redux.js.org/)
[reactjs/redux: Predictable state container for JavaScript apps](https://github.com/reactjs/redux)
[Ecosystem · Redux](http://redux.js.org/docs/introduction/Ecosystem.html)
[xgrommx/awesome-redux](https://github.com/xgrommx/awesome-redux)
[markerikson/react-redux-links: Curated tutorial and resource links I've collected on React, Redux, ES6, and more](https://github.com/markerikson/react-redux-links)

Redux = **_Red_**ucer + Fl**_ux_**

[React.js Conf 2016 - Lin Clark - A Cartoon Guide to the Wilds of Data Handling - YouTube](https://www.youtube.com/watch?v=WIqbzHdEPVM)

[How Redux Works: A Counter-Example](https://daveceddia.com/how-does-redux-work/)
[Understanding Redux: The World’s Easiest Guide to Beginning Redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6) Understanding Redux 1 in [The ReduxJS Books](https://thereduxjsbooks.com/)

[Redux for React: A Simple Introduction – Ross Bulat – Medium](https://medium.com/@rossbulat/redux-for-react-a-simple-introduction-b1f9dcbda8f4)
[How to use Redux in ReactJS with real-life examples](https://medium.freecodecamp.org/how-to-use-redux-in-reactjs-with-real-life-examples-687ab4441b85)
[Leveling Up with React: Redux | CSS-Tricks](https://css-tricks.com/learning-react-redux/)
[Blogged Answers: Resources for Learning Redux · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/12/blogged-answers-learn-redux/)
[Practical Redux · Mark's Dev Blog](https://blog.isquaredsoftware.com/series/practical-redux/)
[Idiomatic Redux: The Tao of Redux, Part 1 - Implementation and Intent · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-1/)
[Idiomatic Redux: The Tao of Redux, Part 2 - Practice and Philosophy · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-2/)

## Action and ActionCreator

```js
// Action
{ type: 'ADD_TODO', text: 'Use Redux' }

// ActionCreator
addTodo = (text) => {
  return { type: 'ADD_TODO', text };
}

// thunk, return function/promise for `dispatch()`
// avoid accessing state other than conditional dispatch
// (using cached data, checking authentication)
// passing data in store is considered an anti-pattern
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
  SET_VISIBILITY_FILTER: (visibilityState, action) => action.visibility
});

const todosReducer = createReducer([], {
  // case handlers
  ADD_TODO: addTodo,
  TOGGLE_TODO: toggleTodo,
  EDIT_TODO: editTodo
});

const appReducer = combineReducers({
  visibilityFilter: visibilityReducer,
  todos: todosReducer
});
```

[Reusing Reducer Logic · Redux](http://redux.js.org/docs/recipes/reducers/ReusingReducerLogic.html) by bounding different `name` to it for different components and state slice

### Middleware

[You Aren’t Using Redux Middleware Enough – Jacob Parker – Medium](https://medium.com/@jacobp100/you-arent-using-redux-middleware-enough-94ffe991e6)

```js
storeInstance => functionToCallWithAnActionThatWillSendItToTheNextMiddleware => actionThatDispatchWasCalledWith =>
  valueToUseAsTheReturnValueOfTheDispatchCall;
// or in short
store => next => action => result;
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
    shouldCallAPI: state => !state.posts[userId],
    // Perform the fetching:
    callAPI: () => fetch(`http://myapi.com/users/${userId}/posts`),
    // Arguments to inject in begin/end actions
    payload: { userId }
  };
}

function callAPIMiddleware({ dispatch, getState }) {
  return next => action => {
    const { types, callAPI, shouldCallAPI = () => true, payload = {} } = action;

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
        type: requestType
      })
    );

    return callAPI().then(
      response =>
        dispatch(
          Object.assign({}, payload, {
            response,
            type: successType
          })
        ),
      error =>
        dispatch(
          Object.assign({}, payload, {
            error,
            type: failureType
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

---

[#187: Redux, React, and Functional JavaScript with Dan Abramov - The Changelog](https://changelog.com/187/)
[JSJ The Evolution of Flux Libraries with Andrew Clark and Dan Abramov](https://devchat.tv/js-jabber/181-jsj-the-evolution-of-flux-libraries-with-andrew-clark-and-dan-abramov)
[Dan Abramov - Live React: Hot Reloading with Time Travel at react-europe 2015 - YouTube](https://www.youtube.com/watch?v=xsSnOQynTHs) The presentation where Redux is born
[Dan Abramov - The Redux Journey at react-europe 2016 - YouTube](https://www.youtube.com/watch?v=uvAXVMwHJXU)

[Redux without the sanity checks in a single file.](https://gist.github.com/gaearon/ffd88b0e4f00b22c3159)
[Super minimal React + Redux app](https://gist.github.com/gaearon/074b0905337a6a835d82)

[Redux Framework](https://reduxframework.com/) for WordPress

[Idiomatic Redux · Mark's Dev Blog](http://blog.isquaredsoftware.com/series/idiomatic-redux/)
[An Introduction To Redux – Smashing Magazine](https://www.smashingmagazine.com/2016/06/an-introduction-to-redux/)
[Getting Started with Redux: An Intro | Scotch](https://scotch.io/bar-talk/getting-started-with-redux-an-intro)
[Getting started with Redux - Example application | jchapron](http://www.jchapron.com/2015/08/14/getting-started-with-redux/)
[SurviveJS - Webpack and React - Redux - Reinventing Flux - Interview with Dan Abramov](http://survivejs.com/blog/redux-interview/)
[Flux: Reduce Your Side Effects](https://blog.javascripting.com/2015/08/12/reduce-your-side-effects/)
[What the Flux?! Let’s Redux. | &yet Blog](https://blog.andyet.com/2015/08/06/what-the-flux-lets-redux)
[The Just Enough Redux Reading List — Medium](https://medium.com/@Lilobase/the-just-enough-redux-reading-list-74c954e1941#.2k80kp6mz)
[A cartoon intro to Redux — Code Cartoons — Medium](https://code-cartoons.com/a-cartoon-intro-to-redux-3afb775501a6#.lxpvf5krl) Redux vs Flux
[Understanding the Redux paradigm | Tryolabs | Blog](http://blog.tryolabs.com/2016/04/19/understanding-the-redux-paradigm/)

[Step by Step Guide To Building React Redux Apps — Medium](https://medium.com/@rajaraodv/step-by-step-guide-to-building-react-redux-apps-using-mocks-48ca0f47f9a)
[Full-Stack Redux Tutorial](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)
[Secure Your React and Redux App with JWT Authentication](https://auth0.com/blog/secure-your-react-and-redux-app-with-jwt-authentication/)

[Feeback wanted: Rewrite with ideas from @acdlite by gaearon · Pull Request #46 · rackt/redux](https://github.com/rackt/redux/pull/46)

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
[Does use of context API scales if the project grows? · React](https://spectrum.chat/thread/039f91ed-9a7c-4768-ab70-6fbbcd89495f)

[Redux feels bloated, complicated and not easy. What are the alternative? : reactjs](https://www.reddit.com/r/reactjs/comments/3towfy/redux_feels_bloated_complicated_and_not_easy_what/)
[reactjs - What could be the downsides of using Redux instead of Flux - Stack Overflow](http://stackoverflow.com/questions/32021763/what-could-be-the-downsides-of-using-redux-instead-of-flux/32916602#32916602)

## Tips and Tricks

[Two Weird Tricks with Redux](http://jlongster.com/Two-Weird-Tricks-with-Redux)
[Scaling Redux for real-life applications – Hacker Noon](https://hackernoon.com/scaling-redux-for-real-life-applications-be18c731a54d)
[Scaling your Redux App with ducks](https://medium.freecodecamp.com/scaling-your-redux-app-with-ducks-6115955638be#.txowddfkt)

## Data flow

Handles async and side effects:
[gaearon/redux-thunk: Thunk middleware for Redux](https://github.com/gaearon/redux-thunk)
[redux-saga/redux-saga: An alternative side effect model for Redux apps](https://github.com/redux-saga/redux-saga) uses `while`-loop and generators
[redux-loop/redux-loop: A library that ports Elm's effect system to Redux](https://github.com/redux-loop/redux-loop)
[lelandrichardson/redux-pack: Sensible promise handling and middleware for redux](https://github.com/lelandrichardson/redux-pack)
[Async actions handling with redux-thunk - NaNLABS](https://www.nan-labs.com/blog/handle-async-actions-redux-thunk/)
[javascript - How to dispatch a Redux action with a timeout? - Stack Overflow](https://stackoverflow.com/questions/35411423/how-to-dispatch-a-redux-action-with-a-timeout/)
[Where do I put my business logic in a React Redux application? | CodeWinds](http://codewinds.com/blog/2016-08-16-business-logic-redux.html)

[A chained modals example w/ React Bootstrap - SaltyCrane Blog](https://www.saltycrane.com/blog/2016/02/chained-modals-example-react-bootstrap/)
[A chained modals example w/ React Router (part 2) - SaltyCrane Blog](https://www.saltycrane.com/blog/2016/03/chained-modals-example-react-router-part-2/)
[Comparing vanilla React, Redux, and Redux Thunk - Chained modals exercise part 3 - SaltyCrane Blog](https://www.saltycrane.com/blog/2016/05/comparing-vanilla-react-redux-and-redux-thunk-chained-modals/)

[Actors: How to dispatch actions after Redux state changes](http://jamesknelson.com/join-the-dark-side-of-the-flux-responding-to-actions-with-actors/)
[Can I dispatch multiple actions from Redux action creators?](http://jamesknelson.com/can-i-dispatch-multiple-actions-from-redux-action-creators/)
[Updating Normalized Data · Redux](http://redux.js.org/docs/recipes/reducers/UpdatingNormalizedData.html)

[christianalfoni - The case for function tree](http://www.christianalfoni.com/articles/2016_09_11_The-case-for-function-tree)
[Redux 4 Ways – React Native Training – Medium](https://medium.com/react-native-training/redux-4-ways-95a130da0cdc#.yhkcy935e)
[State Management with Redux](http://konkle.us/state-management-with-redux/)
[Querying a Redux Store – Medium](https://medium.com/@adamrackis/querying-a-redux-store-37db8c7f3b0f#.xax4uwvif)
[Idiomatic Redux: Thoughts on Thunks, Sagas, Abstraction, and Reusability · Mark's Dev Blog](http://blog.isquaredsoftware.com/2017/01/idiomatic-redux-thoughts-on-thunks-sagas-abstraction-and-reusability/)
[You may not need to thunk – Medium](https://medium.com/@thisismissem/you-may-not-need-to-thunk-f5dc7a6fcbca#.d28w6abao)
[Using redux-saga To Simplify Your Growing React Native Codebase](https://shift.infinite.red/using-redux-saga-to-simplify-your-growing-react-native-codebase-2b8036f650de#.yhy5r2mv2)
[react-redux-links/redux-side-effects.md at master · markerikson/react-redux-links](https://github.com/markerikson/react-redux-links/blob/master/redux-side-effects.md)

[Cheng Lou - On the Spectrum of Abstraction at react-europe 2016 - YouTube](https://www.youtube.com/watch?v=mVVNJKv9esE) !important

## react-redux

[rackt/react-redux](https://github.com/rackt/react-redux)
[Implementing Container Components · Redux](http://redux.js.org/docs/basics/UsageWithReact.html#implementing-container-components)

[17. React Redux with Dan Abramov - YouTube](https://www.youtube.com/watch?v=VJ38wSFbM3A)
[react-redux/api.md at master · reactjs/react-redux](https://github.com/reactjs/react-redux/blob/master/docs/api.md)

Notice how [`AddTodo`](http://redux.js.org/docs/basics/UsageWithReact.html#implementing-other-components) is implemented as a functional stateless components.

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
// https://github.com/reactjs/react-redux/blob/master/docs/api.md

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

[reactjs/reselect: Selector library for Redux](https://github.com/reactjs/reselect) memoized transform
[heyimalex/reselect-map: Selectors for mapping over collections](https://github.com/HeyImAlex/reselect-map) the transform is expensive for each item
[Computing Derived Data · Redux](http://redux.js.org/docs/recipes/ComputingDerivedData.html)
[Selector pattern in React/Redux apps - NaNLABS](https://www.nan-labs.com/blog/selector-pattern-in-react-redux-apps/)

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
// http://redux.js.org/docs/recipes/ComputingDerivedData.html#sharing-selectors-across-multiple-components
```

## boilerplates

[chin-phang/react-redux-quickstart: Create React + Redux apps](https://github.com/chin-phang/react-redux-quickstart) SCSS
[FullstackTypeScript/redux-bootstrap: A bootstrap() function for initializing Redux applications.](https://github.com/FullstackTypeScript/redux-bootstrap)
[reduxjs/redux-starter-kit: A simple set of tools to make using Redux easier](https://github.com/reduxjs/redux-starter-kit)
[erikras/ducks-modular-redux: A proposal for bundling reducers, action types and actions when using Redux](https://github.com/erikras/ducks-modular-redux)

[Scaling your Redux App with ducks](https://medium.freecodecamp.com/scaling-your-redux-app-with-ducks-6115955638be#.txowddfkt) folder structure
