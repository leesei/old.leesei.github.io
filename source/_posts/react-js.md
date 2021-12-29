---
title: "React.js"
date: 2015-12-04 12:12:02
categories:
  - web
tags:
  - react-js
  - javascript
  - frontend
  - web-dev
toc: true
---

> React is moving fast, post older then 2 years should be discarded

[Getting Started | React](http://facebook.github.io/react/docs/getting-started.html)
[Tutorial | React](http://facebook.github.io/react/docs/tutorial.html)
[Thinking in React | React](http://facebook.github.io/react/docs/thinking-in-react.html)
[reactjs/react-basic: A description of the conceptual model of React without implementation burden.](https://github.com/reactjs/react-basic)
[React Tutorial: A Comprehensive Guide to learning React.js in 2018](https://tylermcginnis.com/reactjs-tutorial-a-comprehensive-guide-to-building-apps-with-react/)
[React Starters ― Scotch.io](https://scotch.io/starters/react) 2019
[Learn React - Best React Tutorials (2019) | gitconnected](https://gitconnected.com/learn/react)
[The Beginner's Guide to React | egghead.io](https://egghead.io/courses/the-beginner-s-guide-to-react) 2021
[Watch The 2020 Reactathon San Francisco Developer Conference for Free](https://www.freecodecamp.org/news/reactathon-2020-conference-live-youtube/)

[ReactJs Roadmap🗺 for beginners - 2021 - DEV Community](https://dev.to/suhailzone/reactjs-roadmap-for-beginners-2021-14en) mind map
[Why React Hooks? - YouTube](https://www.youtube.com/watch?v=eX_L39UvZes) an overview of React API history
render props and HOC creates false hierarchies and wrapper hells

[React’s true strengths](https://medium.com/@dan_abramov/youre-missing-the-point-of-react-a20e34a51e1a):

- composition
- unidirectional data flow
- freedom from DSLs
- explicit mutation
- static mental model
- minimal rendering with [vDOM diff](http://calendar.perfplanet.com/2013/diff/)

React blends view and controller more the higher up in the component hierarchy. It allows developer to "do what makes sense for your current project". This more important thing is the philosophy of uni-directional data flow.

[Your Timeline for Learning React](https://daveceddia.com/timeline-for-learning-react/)
[React Resources](https://reactresources.com/)
[React book landing page](https://softchris.github.io/books/react/)
[Learn](https://reactarmory.com/guides)
[React Fundamentals](https://frontarm.com/courses/react-fundamentals) some free lessons

[What’s new in the React.js 16 JavaScript UI library | InfoWorld](https://www.infoworld.com/article/3228113/react/whats-new-in-the-react-16-javascript-ui-library.html)
[What's New in React v16.6](https://alligator.io/react/whats-new-react-16.6/)
[Why React16 is a blessing to React developers – freeCodeCamp.org](https://medium.freecodecamp.org/why-react16-is-a-blessing-to-react-developers-31433bfc210a)
`React.lazy()`, `React.memo()`, Context API
[Sneak Peek: Beyond React 16 – React Blog](https://reactjs.org/blog/2018/03/01/sneak-peek-beyond-react-16.html)
[React 16.x Roadmap – React Blog](https://reactjs.org/blog/2018/11/27/react-16-roadmap.html)
[Dan Abramov: Beyond React 16 | JSConf Iceland 2018 - YouTube](https://www.youtube.com/watch?v=nLF0n9SACd4)

<!-- more -->

## create-react-app

[Create React App · Set up a modern web app by running one command.](https://create-react-app.dev/)
[facebook/create-react-app: Set up a modern web app by running one command.](https://github.com/facebook/create-react-app) must have
[create-react-app/packages/react-scripts at master · facebook/create-react-app](https://github.com/facebook/create-react-app/tree/master/packages/react-scripts)

[10 Fun Facts About Create React App - Better Programming - Medium](https://medium.com/better-programming/10-fun-facts-about-create-react-app-eb7124aa3785)
[create-react-app/CHANGELOG.md at master · facebook/create-react-app](https://github.com/facebook/create-react-app/blob/master/CHANGELOG.md) latest
[Create React App 2.0: Babel 7, Sass, and More – React Blog](https://reactjs.org/blog/2018/10/01/create-react-app-v2.html)

[My Awesome Custom React Environment Variables Setup](https://medium.com/@robertsavian/my-awesome-custom-react-environment-variables-setup-8ebb0797d8ac)
[Feature/different env config files #1343 by tuchk4 · Pull Request #1344 · facebook/create-react-app](https://github.com/facebook/create-react-app/pull/1344)
[bkeepers/dotenv: A Ruby gem to load environment variables from `.env`.](https://github.com/bkeepers/dotenv#what-other-env-files-can-i-use)

[gsoft-inc/craco: Create React App Configuration Override, an easy and comprehensible configuration layer for create-react-app](https://github.com/gsoft-inc/craco) !important, override
[javascript - How to make an import shortcut/alias in create-react-app? - Stack Overflow](https://stackoverflow.com/questions/63067555/how-to-make-an-import-shortcut-alias-in-create-react-app)
[create-react-app v3, What's new? ― Scotch](https://scotch.io/bar-talk/create-react-app-v3-whats-new/amp)

[Customizing create-react-app: How to Make Your Own Template](https://auth0.com/blog/how-to-configure-create-react-app/)

[jaredpalmer/tsdx: Zero-config CLI for TypeScript package development](https://github.com/jaredpalmer/tsdx)

Fix `react-scripts` issue when running on Dropbox's synced folder:
`ln -sf ../react-scripts/bin/react-scripts.js node_modules/.bin/react-scripts`

`npx create-react-app my-app --template typescript` since 3.3
[create-react-app/packages/cra-template-typescript at master · facebook/create-react-app](https://github.com/facebook/create-react-app/tree/master/packages/cra-template-typescript)
[cra-template-\* - npm search](https://www.npmjs.com/search?q=cra-template-*)
[rafrex/spa-github-pages: Host single page apps with GitHub Pages](https://github.com/rafrex/spa-github-pages) React Router `<BrowserRouter />` and custom `404.html`

[From create-react-app to PWA - LogRocket Blog](https://blog.logrocket.com/from-create-react-app-to-pwa/)

[JetBrains/create-react-kotlin-app: Create React apps using Kotlin with no build configuration](https://github.com/JetBrains/create-react-kotlin-app)

[Create Apps with No Configuration - React Blog](https://facebook.github.io/react/blog/2016/07/22/create-apps-with-no-configuration.html)
[Getting started with create-react-app, Redux, React Router & Redux Thunk](https://medium.com/@notrab/getting-started-with-create-react-app-redux-react-router-redux-thunk-d6a19259f71f)
[notrab/create-react-app-redux: Basic starter kit for using React Router & Redux with create-react-app](https://github.com/notrab/create-react-app-redux)
[Beyond Create React App: React Router, Redux, Redux Saga, and More](https://auth0.com/blog/beyond-create-react-app-react-router-redux-saga-and-more/)
[btg5679/react-redux-prod-starter: A ReactJS/Redux Production ready project foundation](https://github.com/btg5679/react-redux-prod-starter)
[How to build a React project from scratch using Webpack 4 and Babel](https://hackernoon.com/how-to-build-a-react-project-from-scratch-using-webpack-4-and-babel-56d4a26afd32)
[v4 Create React + Redux app structure with build configurations. What’s new?](https://medium.com/@shystruk/v4-create-react-redux-app-structure-with-build-configurations-whats-new-523bdec328c6)

### Extending CRA

[How to Use the Optional Chaining Operator in Your React App Right Now - DEV Community 👩‍💻👨‍💻](https://dev.to/aumayeung/how-to-use-the-optional-chaining-operator-in-your-react-app-right-now-1ocj)
[10 Fun Facts About Create React App - Better Programming - Medium](https://medium.com/better-programming/10-fun-facts-about-create-react-app-eb7124aa3785)

[arackaf/customize-cra: Override webpack configurations for create-react-app 2.0](https://github.com/arackaf/customize-cra)

[timarney/react-app-rewired: Override create-react-app webpack configs without ejecting](https://github.com/timarney/react-app-rewired)
[Customize Create React App (CRA) without ejecting using react-app-rewired from @dceddia on @eggheadio](https://egghead.io/lessons/react-customize-create-react-app-cra-without-ejecting-using-react-app-rewired)
[Override Create React App conf w/react-app-rewired - Today I Learned](https://til.hashrocket.com/posts/ihkbvw5zfv-override-create-react-app-conf-wreact-app-rewired)

### Proxy

[Proxying API Requests in Development | Create React App](https://create-react-app.dev/docs/proxying-api-requests-in-development/#configuring-the-proxy-manually) `src/setupProxy.js` since 2.0

Easiest way: add "proxy" key to `package.json` (for simple proxying)

```json
{
  "proxy": "http://myhost.com:4000"
}
```

Or install `http-proxy-middleware` and add `src/setProxy.js` to the project.

```js
const proxy = require("http-proxy-middleware");
module.exports = function (app) {
  app.use(
    "/api1",
    proxy({
      target: "http://myhost1:4000",
      changeOrigin: true,
    })
  );
  app.use(
    "/api2",
    proxy({
      target: "http://myhost2:5000",
      changeOrigin: true,
    })
  );
};
```

### Project structure

[How to Structure Your React Project](https://daveceddia.com/react-project-structure/)
[How to structure your react app. - By](https://hackernoon.com/how-to-structure-your-react-app-98c48e102aad)
[How to structure your React app 2. - ITNEXT](https://itnext.io/how-to-structure-your-react-app-2-2cf3b8040634)
[How I structure a React project - DEV Community 👩‍💻👨‍💻](https://dev.to/maciekchmura/how-i-structure-a-react-project-3c2i)
[folder-structure.md](https://gist.github.com/ryanflorence/daafb1e3cb8ad740b346#how-it-works)
[Fractal — A react app structure for infinite scale | Hacker Noon](https://hackernoon.com/fractal-a-react-app-structure-for-infinite-scale-4dab943092af)
[Folder Structure in React Apps - Noteworthy - The Journal Blog](https://blog.usejournal.com/folder-structure-in-react-apps-c2ae8974d21f)

[Structuring projects and naming components in React | Hacker Noon](https://hackernoon.com/structuring-projects-and-naming-components-in-react-1261b6e18d76) `src/screen` (= page, matches routes), `src/components`

[CRUV: Structure React apps in 4 directories and 3 files - James K Nelson](http://jamesknelson.com/cruv-react-project-structure/)

- `/containers/`
- `/routes/`
- `/utils/`
- `/views/`
- `/config.js`
- `/contexts.js`
- `/store/` (optional)

[A Simple Approach to File Structures in React Apps | by Juan Bernal | JavaScript In Plain English | Medium](https://medium.com/javascript-in-plain-english/solving-the-file-structure-problem-in-react-apps-4b5b5dca775b)

[Scalable file structure for React and other projects](https://react-file-structure.surge.sh/)
move files around until it feels right

### Environments

[My Awesome Custom React Environment Variables Setup](https://medium.com/@robertsavian/my-awesome-custom-react-environment-variables-setup-8ebb0797d8ac)
[Feature/different env config files #1343 by tuchk4 · Pull Request #1344 · facebook/create-react-app](https://github.com/facebook/create-react-app/pull/1344)
[bkeepers/dotenv: A Ruby gem to load environment variables from `.env`.](https://github.com/bkeepers/dotenv#what-other-env-files-can-i-use)

[Adding Custom Environment Variables · Create React App](https://create-react-app.dev/docs/adding-custom-environment-variables)
[Deployment · Create React App](https://create-react-app.dev/docs/deployment#customizing-environment-variables-for-arbitrary-build-environments)

### Live server

[React Live Demo](https://react-live.kitten.sh/)
[FormidableLabs/react-live: A production-focused playground for live editing React components](https://github.com/FormidableLabs/react-live)

## Introduction

[React Tutorials and Courses - Thinkster](https://thinkster.io/topics/react)
[Getting Started with React - Thinkster](https://thinkster.io/getting-started-with-react)
[React Screencasts](https://www.reactscreencasts.com/crash_courses/react_with_hooks)
[The Road to React](https://roadtoreact.com/) several free courses

[petehunt/react-howto: Your guide to the (sometimes overwhelming!) React ecosystem.](https://github.com/petecinnhunt/react-howto) !important
[A React Beginners Roadmap through the React Eco System](https://codeburst.io/a-react-beginners-roadmap-through-the-react-eco-system-e27c57e2678a)

[Fullstack React 🐬: React Tutorial: Cloning Yelp](https://www.fullstackreact.com/articles/react-tutorial-cloning-yelp/)
[Fullstack React: 30 Days of React](https://www.fullstackreact.com/30-days-of-react/)
[Start Learning React from @joemaddalone on @eggheadio](https://egghead.io/courses/start-learning-react)
[React Testing Cookbook from @trevordmiller on @eggheadio](https://egghead.io/courses/react-testing-cookbook)

[React.Component – React](https://reactjs.org/docs/react-component.html)
[React lifecycle methods diagram](http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/) [src](https://github.com/wojtekmaj/react-lifecycle-methods-diagram)
[React Component Lifecycle - DEV Community 👩‍💻👨‍💻](https://dev.to/jaylcaetano/react-component-lifecycle-2npl)

[JavaScript's History and How it Led To ReactJS - The New Stack](http://thenewstack.io/javascripts-history-and-how-it-led-to-reactjs/)
[Baby’s First Reaction — JavaScript Scene — Medium](https://medium.com/javascript-scene/baby-s-first-reaction-2103348eccdd)
[The React Handbook](https://flaviocopes.com/page/react-handbook/)
[ReactJS For Stupid People](http://blog.andrewray.me/reactjs-for-stupid-people/)
[Josh Haberman: React Demystified](http://blog.reverberate.org/2014/02/react-demystified.html)
[The React.js Way: Getting Started Tutorial](http://blog.risingstack.com/the-react-way-getting-started-tutorial/)
[ifandelse/ReactJS-Rethinking-Web-UI](https://github.com/ifandelse/ReactJS-Rethinking-Web-UI)
[ES2015 (ES6) Features Commonly Used with Functional Style React - BEKK Open](http://open.bekk.no/es2015-es6-features-commonly-used-with-functional-style-react)
[Introduction | React 入门教程](http://hulufei.gitbooks.io/react-tutorial/content/)
[Setting State in React - Frontend Masters](https://frontendmasters.com/courses/react/setting-state/)
[These are the concepts you should know in React.js (after you learn the basics)](https://medium.freecodecamp.org/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030)
[Reintroducing React: every React update since v16 demystified.](https://medium.freecodecamp.org/reintroducing-react-every-react-update-since-v16-demystified-60686ee292cc)

[React JS Todo 2 - JSFiddle](http://jsfiddle.net/johnthethird/NXCyC/9/)

[Want to learn React.js? Here’s my free course which teaches it by building a chat app.](https://medium.freecodecamp.org/want-to-learn-react-js-heres-my-free-course-which-teaches-it-through-building-a-chat-app-c86333e5b88c)
[Building a chat app with React.js and Chatkit | Scrimba.com](https://scrimba.com/g/greactchatkit)
[Building a React-based Chat Client with Redux – ITNEXT](https://itnext.io/building-a-react-based-chat-client-with-redux-816b47cb8c74)

## Why React

[Why We Moved From Angular to React](http://blog.belong.co/why-we-moved-from-angular-to-react)
[Why I Ditched Angular for React](http://sixrevisions.com/javascript/why-i-ditched-angular-for-react/)
[Why are we using React.js in our projects? - React Kung Fu](http://reactkungfu.com/2015/07/why-are-we-using-react-js-in-our-projects/)
[From Ember to React — Medium](https://medium.com/@eluciano11/from-ember-to-react-5c2faa0e8d10#.lwydw1kir)

[Pete Hunt: React: Rethinking best practices -- JSConf EU 2013 - YouTube](https://www.youtube.com/watch?v=x7cQ3mrcKaY)
[Built With React](http://builtwithreact.io/)

[React vs. Ember - Alex Matchneer - EmberNYC meetup - Google Slides](https://docs.google.com/presentation/d/1afMLTCpRxhJpurQ97VBHCZkLbR1TEsRnd3yyxuSQ5YY/edit#slide=id.p)
[Removing User Interface Complexity, or Why React is Awesome](http://jlongster.com/Removing-User-Interface-Complexity,-or-Why-React-is-Awesome)
[javascript - Pros and Cons of Facebook's React vs. Web Components (Polymer) - Programmers Stack Exchange](http://programmers.stackexchange.com/questions/225400/pros-and-cons-of-facebooks-react-vs-web-components-polymer)
[React.js and How Does It Fit In With Everything Else? - Funny Ant](http://www.funnyant.com/reactjs-what-is-it/)
[Is React killing Angular? - Quora](https://www.quora.com/Is-React-killing-Angular)
[Should I learn ReactJS or AngularJS? - Quora](https://www.quora.com/Should-I-learn-ReactJS-or-AngularJS)

## On the contrary

[React vs. Vue: Clash of the JavaScript titans | InfoWorld](https://www.infoworld.com/article/3291619/javascript/react-vs-vue-clash-of-the-javascript-titans.html)

[Don't React - webbisauna](http://staltz.com/dont-react/)
[You probably shouldn’t be using React – Noteworthy - The Journal Blog](https://blog.usejournal.com/you-probably-shouldt-be-using-react-2f45ca487c8e)
[Boiling React Down to a Few Lines in jQuery - Hackflow](http://hackflow.com/blog/2015/03/08/boiling-react-down-to-few-lines-in-jquery/)
[Is React Overrated?. Or does it actually have some merits… | by Aphinya Dechalert | Mad Hash*Map* | Medium](https://medium.com/madhash/is-react-overrated-c7f8efb75e3e)
[Really, why React? - DEV Community](https://dev.to/jfbrennan/really-why-react-5958)

## React/TypeScript

[TypeScript and React](https://fettblog.eu/typescript-react/)
[React TypeScript Cheatsheets | React TypeScript Cheatsheets](https://react-typescript-cheatsheet.netlify.app/)

[Using TypeScript with React ← Alligator.io](https://alligator.io/react/typescript-with-react/)
[How to Use TypeScript in React | The Ionic Blog](https://blog.ionicframework.com/how-to-use-typescript-in-react/)
[Getting started with Typescript in Create React App](https://medium.com/byteconf/getting-started-with-typescript-in-create-react-app-2306b713088f)
[Using Create React App v2 and TypeScript ― Scotch](https://scotch.io/tutorials/using-create-react-app-v2-and-typescript)
[Using TypeScript with React ← Alligator.io](https://alligator.io/react/typescript-with-react/)
[React TypeScript: Basics and Best Practices | by Fernando Doglio | Bits and Pieces](https://blog.bitsrc.io/react-typescript-cheetsheet-2b6fa2cecfe2)
[How to Migrate a React App to TypeScript - SitePoint](https://www.sitepoint.com/how-to-migrate-a-react-app-to-typescript/)
[The React TypeScript Cheatsheet – How To Set Up Types on Hooks](https://www.freecodecamp.org/news/react-typescript-how-to-set-up-types-on-hooks/)
[How to Use TypeScript with React Components](https://dmitripavlutin.com/typescript-react-components/)

[TypeScript and React using create-react-app: A step-by-step guide to setting up your first app](https://levelup.gitconnected.com/typescript-and-react-using-create-react-app-a-step-by-step-guide-to-setting-up-your-first-app-6deda70843a4)
[React-Redux with Typescript – Better Programming – Medium](https://medium.com/better-programming/react-redux-with-typescript-7ff678bc17ab)

[Making the most boring website ever with TypeScript, NodeJs, React. - YouTube](https://www.youtube.com/playlist?list=PL7b0cPjh8z6K_4qLNu_QdE3RpiU6omViC)

- write all your code in `.ts`/`.tsx`
- context
  [reactjs - React createContext issue in Typescript? - Stack Overflow](https://stackoverflow.com/questions/54577865/react-createcontext-issue-in-typescript)

```js
import { createContext } from 'react';

interface IUserObject {}

interface IUserContext {
  user: IUserObject;
  setUser: React.Dispatch<IUserObject>;
}
const UserContext = createContext<IUserContext>({} as IUserContext);
export const UserProvider = UserContext.Provider;
export const UserConsumer = UserContext.Consumer;
export default UserContext;
```

```js
interface Props {
  seriesList: SeriesProps["seriesList"];
  setSeriesList: Dispatch<SetStateAction<SeriesProps["seriesList"]>>;
}

const handleChange: ChangeEventHandler<HTMLInputElement> = (event) => {
  //
};

const handleClick: MouseEventHandler<HTMLButtonElement> = (event) => {
  // ...
};
```

- missing `.d.ts`
  create `modules.d.ts` and define module

## Minimal React

> without build step

[Minimal React.js Without A Build Step (Updated) | Shing's Blog](https://shinglyu.github.io/web/2018/02/08/minimal-react-js-without-a-build-step-updated.html) 2018-02
[How to add React to a simple html file – Toni Petrina – Medium](https://medium.com/@to_pe/how-to-add-react-to-a-simple-html-file-a11511c0235f) 2017-01

[Pure React](https://daveceddia.com/pure-react/) coupon code: INDIA9?

## Internals

[React In Depth – Medium](https://medium.com/react-in-depth)
[Overreacted — A blog by Dan Abramov](https://overreacted.io/)

[React as a UI Runtime — Overreacted](https://overreacted.io/react-as-a-ui-runtime/)
[How Virtual-DOM and diffing works in React – Gethyl George Kurian – Medium](https://medium.com/@gethylgeorge/how-virtual-dom-and-diffing-works-in-react-6fc805f9f84e)
[Performance Calendar » React’s diff algorithm](http://calendar.perfplanet.com/2013/diff/)

[Blogged Answers: A (Mostly) Complete Guide to React Rendering Behavior · Mark's Dev Blog](https://blog.isquaredsoftware.com/2020/05/blogged-answers-a-mostly-complete-guide-to-react-rendering-behavior/)
[Understanding Rendering Behavior in React](https://geekflare.com/react-rendering/)
[A Visual Guide to React Rendering - Cheat Sheet | Alex Sidorenko](https://alexsidorenko.com/blog/react-render-cheat-sheet/)
[A Visual Guide to React Rendering - DOM | Alex Sidorenko](https://alexsidorenko.com/blog/react-render-dom/)

[React - Under the hood](https://www.freecodecamp.org/news/react-under-the-hood/)
[A Closer Look at ReactDOM.render - The Need to Know and More -- newline](https://www.newline.co/@KumailP/a-closer-look-at-reactdomrender-the-need-to-know-and-more--891fed64)
[Managing DOM components with ReactDOM - LogRocket Blog](https://blog.logrocket.com/managing-dom-components-reactdom/)

[SyntheticEvent – React](https://reactjs.org/docs/events.html)
[Getting started with React SyntheticEvent - LogRocket Blog](https://blog.logrocket.com/getting-started-react-synthetic-event/)

[React Components, Elements, and Instances – React Blog](https://reactjs.org/blog/2015/12/18/react-components-elements-and-instances.html)
[React Components, Elements, and Instances — Medium](https://medium.com/@dan_abramov/react-components-elements-and-instances-90800811f8ca)
[How Does React Tell a Class from a Function? — Overreacted](https://overreacted.io/how-does-react-tell-a-class-from-a-function/)
[Why Do React Elements Have a \$\$typeof Property? — Overreacted](https://overreacted.io/why-do-react-elements-have-typeof-property/)

[Why Do We Write super(props)? — Overreacted](https://overreacted.io/why-do-we-write-super-props/)
[Understanding Constructors with React Components ← Alligator.io](https://alligator.io/react/constructors-with-react-components/)
for `this.state` and `this.props`

[Lucy | How does React decide to re-render a component?](https://lucybain.com/blog/2017/react-js-when-to-rerender/)

### Error Boundaries

[Error Boundaries – React](https://reactjs.org/docs/error-boundaries.html)
[Understanding Error Boundaries in React | by Chidume Nnamdi 🔥💻🎵🎮 | Bits and Pieces](https://blog.bitsrc.io/understanding-error-boundaries-in-react-2ac8be8771c6)

[How to handle errors in ReactJS | InfoWorld](https://www.infoworld.com/article/3604336/how-to-handle-errors-in-reactjs.html)

### Renderer

[Virtual DOM and Internals – React](https://reactjs.org/docs/faq-internals.html)
[react/packages/react-reconciler at main · facebook/react](https://github.com/facebook/react/tree/main/packages/react-reconciler)

[3 common mistakes that impede React reconciliation and updating processes](https://medium.com/strands-tech-corner/3-common-mistakes-that-impede-react-reconciliation-and-updating-processes-8b917ebde61e)
[Understanding Rendering Behavior in React](https://geekflare.com/react-rendering/)

[Test Renderer – React](https://reactjs.org/docs/test-renderer.html)

[⚛️👆 Part 1/3 - Beginners guide to Custom React Renderers. How to build your own renderer from scratch? | Blog](https://blog.atulr.com/react-custom-renderer-1/)
[⚛️✌️ Part 2/3 - Beginners guide to Custom React Renderers. How to build your own renderer from scratch? | Blog](https://blog.atulr.com/react-custom-renderer-2/)
[⚛️🤟 Part 3/3 - Beginners guide to Custom React Renderers. How to build your own renderer from scratch? | Blog](https://blog.atulr.com/react-custom-renderer-3/)

### Fiber

Async Rendering is renamed to Concurrent Rendering

[React 16: A look inside a rewrite of our frontend UI library - Facebook Code](https://code.fb.com/web/react-16-a-look-inside-an-api-compatible-rewrite-of-our-frontend-ui-library/)
[Facebook scraps React as we know it, welcomes successor React Fiber - JAXenter](https://jaxenter.com/facebook-rewrites-react-133403.html)
[Sneak Peek: Beyond React 16 - React Blog](https://reactjs.org/blog/2018/03/01/sneak-peek-beyond-react-16.html)
[Update on Async Rendering - React Blog](https://reactjs.org/blog/2018/03/27/update-on-async-rendering.html)
[Concurrent UI Patterns (Experimental) – React](https://reactjs.org/docs/concurrent-mode-patterns.html)
[acdlite/react-fiber-architecture: A description of React's new core algorithm, React Fiber](https://github.com/acdlite/react-fiber-architecture)

[Get Ready For Concurrent Rendering In React - Well Red - Medium](https://medium.com/well-red/get-ready-for-concurrent-rendering-in-react-120c2fdcd7a9) use `<StrictMode>` to get ready, `<ConcurrentMode>` to opt-in

[Concurrent Rendering in React - Andrew Clark and Brian Vaughn - React Conf 2018 - YouTube](https://www.youtube.com/watch?v=ByBPyMBTzM0)
[How To Properly Use the React useRef Hook in Concurrent Mode](https://medium.com/better-programming/how-to-properly-use-the-react-useref-hook-in-concurrent-mode-38c54543857b) put side effects in `useEffect()`
[React: Rendering using Concurrent Mode and Suspense | by Shanika Wickramasinghe | Bits and Pieces](https://blog.bitsrc.io/react-rendering-using-concurrent-mode-and-suspense-1600c574f996)

[acdlite/react-fiber-architecture: A description of React's new core algorithm, React Fiber](https://github.com/acdlite/react-fiber-architecture)
[A deep dive into React Fiber internals - LogRocket Blog](https://blog.logrocket.com/deep-dive-into-react-fiber-internals/)
[Inside Fiber: in-depth overview of the new reconciliation algorithm in React](https://medium.com/react-in-depth/inside-fiber-in-depth-overview-of-the-new-reconciliation-algorithm-in-react-e1c04700ef6e)
[The how and why on React’s usage of linked list in Fiber](https://medium.com/react-in-depth/the-how-and-why-on-reacts-usage-of-linked-list-in-fiber-67f1014d0eb7)

[Lin Clark - A Cartoon Intro to Fiber - React Conf 2017 - YouTube](https://www.youtube.com/watch?v=ZCuYPiUIONs)
[Andrew Clark: What's Next for React — ReactNext 2016 - YouTube](https://www.youtube.com/watch?v=aV1271hd9ew)

### Fire

[React Fire: Modernizing React DOM · Issue #13525 · facebook/react](https://github.com/facebook/react/issues/13525) an effort to modernize `react-dom`

## Components

[React.Component - React](https://reactjs.org/docs/react-component.html)

- Stateful and Stateless
- Classes and Functions
- Pure and Impure

Use `memo()` HOC to wrap functional components for `PureComponent`.
Set `displayName` property of the function to help debugging.

[React Component Lifecycle Methods Cheatsheet 📄 - DEV Community 👩‍💻👨‍💻](https://dev.to/bunlong/react-component-lifecycle-methods-cheatsheet-1eaf)
[React Component Lifecycle Hooks Cheatsheet 📄 - DEV Community 👩‍💻👨‍💻](https://dev.to/bunlong/react-component-lifecycle-hooks-cheatsheet-1p6)

[React component patterns - Team Subchannel - Medium](https://medium.com/teamsubchannel/react-component-patterns-e7fb75be7bb0)
[React Component Patterns by Michael Chan - YouTube](https://www.youtube.com/watch?v=YaZg8wg39QQ)

[Advanced React Component Patterns workshop @ PayPal (Part 1) - YouTube](https://www.youtube.com/watch?v=SuzutbwjUp8)
[Advanced React Component Patterns workshop @ PayPal (Part 2) - YouTube](https://www.youtube.com/watch?v=ubXtOROjILU)

[React Component Lifecycle - DZone Web Dev](https://dzone.com/articles/react-component-lifecycle)
[React Stateless Functional Components: Nine Wins You Might Have Overlooked](https://hackernoon.com/react-stateless-functional-components-nine-wins-you-might-have-overlooked-997b0d933dbc#.1x45gqq9l) !important
[Understanding React’s Components: Stateless and Stateful](https://blog.hipolabs.com/understanding-reacts-components-stateless-and-stateful-66fa9f31de34)
[React component patterns – Team Subchannel – Medium](https://medium.com/teamsubchannel/react-component-patterns-e7fb75be7bb0)
[Writing Resilient Components — Overreacted](https://overreacted.io/writing-resilient-components/) mostly a pitch to hooks
[How the “Golden Rule” of React components can help you write better code](https://medium.freecodecamp.org/how-the-golden-rule-of-react-components-can-help-you-write-better-code-127046b478eb)
[Better Reusable React Components with the Overrides Pattern](https://medium.com/@dschnr/better-reusable-react-components-with-the-overrides-pattern-9eca2339f646)
[Anti-patterns to avoid when building a component library in React Native](https://levelup.gitconnected.com/anti-patterns-to-avoid-when-building-a-component-library-in-react-native-61f11d8c9797)
[How to write great React - The Startup - Medium](https://medium.com/swlh/how-to-write-great-react-c4f23f2f3f4f)

### Props passing

[Composition vs Inheritance – React](https://reactjs.org/docs/composition-vs-inheritance.html)

[Prop Drilling](https://kentcdodds.com/blog/prop-drilling)
[React Anti-Pattern: Prop-Drilling - codeburst](https://codeburst.io/react-anti-pattern-prop-drilling-54474d5236bd) with HOC
[When to break up a component into multiple components](https://kentcdodds.com/blog/when-to-break-up-a-component-into-multiple-components)
[How to Solve Render Props Callback Hell](https://dmitripavlutin.com/solve-react-render-props-callback-hell/)
[Application State Management with React](https://kentcdodds.com/blog/application-state-management-with-react)
[How to use React Context effectively](https://kentcdodds.com/blog/how-to-use-react-context-effectively)
[How to Avoid Prop Drilling with Composition - The Non-Traditional Developer - Medium](https://medium.com/the-non-traditional-developer/how-to-avoid-prop-drilling-with-composition-6862cd4e253a)

[How to pass props to components in React - RWieruch](https://www.robinwieruch.de/react-pass-props-to-component)
[the-road-to-learn-react/react-slot-pattern-example: An example implementation of React's slot pattern for passing components as props](https://github.com/the-road-to-learn-react/react-slot-pattern-example)

[In-depth explanation of state and props update in React](https://medium.com/react-in-depth/in-depth-explanation-of-state-and-props-update-in-react-51ab94563311)

### Smart and Dump Components

Smart and Dump
Container and Presentational
View/Page/Screen and Component
Fat and Skinny

[Presentational and Container Components — Medium](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0)
[Presentational and Container Components in Redux docs](http://redux.js.org/docs/basics/UsageWithReact.html#presentational-and-container-components)
[Smart and Dumb Components in React | Jake Trent](https://jaketrent.com/post/smart-dumb-components-react/)
[Leveling Up With React: Container Components | CSS-Tricks](https://css-tricks.com/learning-react-container-components/)
[Categorizing Components Into Smart & Dumb Components, in React ← Alligator.io](https://alligator.io/react/smart-dumb-components/)

### Controlled and Uncontrolled Component

An component is _controlled_ if the parent explicitly set its value (probably from state/store) and provides a callback to update this value. It is _uncontrolled_ if it has internal state and response to inputs without the parent knowing, which is similar to letting the DOM handling the state.
Note that controlled components are no longer interactive by default (as it reflects the state). You must use `onChange()` to update the state when the component is changed.
Also note that `null` or `undefined` are considered uncontrolled in React. Set initial state of controlled component to `''` or `false`.

[Forms | React](https://facebook.github.io/react/docs/forms.html)
[Value of null for Controlled Input | React](https://facebook.github.io/react/tips/controlled-input-null-value.html)
[Video: Controlled vs Uncontrolled Components in React](http://www.sitepoint.com/video-controlled-vs-uncontrolled-components-in-react/)
[How “Controllable” React components maximize reusability](https://medium.com/myheritage-engineering/how-controllable-react-components-maximize-reusability-86e3d233fa8e)
[To Be or Not to Be - Better Programming - Medium](https://medium.com/better-programming/to-be-or-not-to-be-2c372198a01c)

[Building a Dynamic, Controlled Form with React – ITNEXT](https://itnext.io/building-a-dynamic-controlled-form-in-react-together-794a44ee552c) `data-*` as `dateset`
[Controlled Form Inputs in React - DEV Community 👩‍💻👨‍💻](https://dev.to/firebase007/controlled-form-inputs-in-react-586c)

[You Probably Don't Need Derived State – React Blog](https://reactjs.org/blog/2018/06/07/you-probably-dont-need-derived-state.html) derived state in child component is also uncontrolled data

[jquense/uncontrollable: Wrap a controlled react component, to allow spcific prop/handler pairs to be uncontrolled](https://github.com/jquense/uncontrollable)

### Compound Components

[React Tutorial - Compound Components in React - Styled Components - React Design Patterns - YouTube](https://www.youtube.com/watch?v=nHMAMS38x-E)

[Compound Components In React — Smashing Magazine](https://www.smashingmagazine.com/2021/08/compound-components-react/)
[Compound Components with React Context API - Noteworthy - The Journal Blog](https://blog.usejournal.com/compound-components-react-context-38da96bfb384)
[Ryan Florence - Compound Components - YouTube](https://www.youtube.com/watch?v=hEGg-3pIHlE) critics on how we compose components, uses `cloneElement()`
[Using the React.cloneElement() function to clone elements - LogRocket Blog](https://blog.logrocket.com/using-react-cloneelement-function/)

[React.js — Compound Components - Dane Sirois - Medium](https://medium.com/@Dane_s/react-js-compound-components-a6e54b5c9992)

[enkidevs/seapig: 🌊🐷 Utility for generalized composition of React components](https://github.com/enkidevs/seapig)

## State

3 camps:

- Flux (Redux, Zustand)
- Proxy (Mobx, Valtio)
- Atomic (Recoil, Jotai)

[React State Management in 2020 - Better Programming - Medium](https://medium.com/better-programming/react-state-management-in-2020-719d10c816bf)
[State of React State Management for 2019 - Bits and Pieces](https://blog.bitsrc.io/state-of-react-state-management-in-2019-779647206bbc)
[Application State Management – kentcdodds](https://blog.kentcdodds.com/application-state-management-66de608ccb24)
[Exploring React's State Propagation](https://www.sitepoint.com/exploring-reacts-state-propagation/)
[Common React.js mistakes: Unneeded state - React Kung Fu](http://reactkungfu.com/2015/09/common-react-dot-js-mistakes-unneeded-state/)
[State is an antipattern : reactjs](https://www.reddit.com/r/reactjs/comments/3bjdoe/state_is_an_antipattern/)
[How to become a pro with React setState() in 10 minutes](https://medium.freecodecamp.org/get-pro-with-react-setstate-in-10-minutes-d38251d1c781)
[How Does setState Know What to Do? — Overreacted](https://overreacted.io/how-does-setstate-know-what-to-do/)
[How State Updates Are Merged in React - Robin Kim - Medium](https://medium.com/@rykyou/how-state-updates-are-merged-in-react-e07fc669fec2)
[3 Essential Tips for Managing State in React Applications](https://www.telerik.com/blogs/3-essential-tips-for-managing-state-in-react-applications)
[Changing children's state from another component with React Hooks](https://itnext.io/changing-children-state-from-another-component-with-react-hooks-5c982c042e8) `forwardRef()` and context
[Where do I put my business logic in a React Redux application? | CodeWinds](http://codewinds.com/blog/2016-08-16-business-logic-redux.html)

[4 options to prevent extra rerenders with React context · Daishi Kato's blog](https://blog.axlight.com/posts/4-options-to-prevent-extra-rerenders-with-react-context/)
[Global state with React | Basefactor](https://www.basefactor.com/global-state-with-react)

[Four patterns for global state with React hooks: Context or Redux](https://itnext.io/four-patterns-for-global-state-with-react-hooks-context-or-redux-cbc2dc787380)
[Redux-less context-based useSelector hook that has same performance as React-Redux](https://itnext.io/redux-less-context-based-useselector-hook-that-has-same-performance-as-react-redux-450b1853f744)
[React Global State without Redux - RWieruch](https://www.robinwieruch.de/react-global-state-without-redux)
[React State with Hooks: useReducer, useState, useContext - RWieruch](https://www.robinwieruch.de/react-state-usereducer-usestate-usecontext) !important
[Passing callbacks down with React Hooks - Trabe - Medium](https://medium.com/trabe/passing-callbacks-down-with-react-hooks-4723c4652aff) `useContext()`, with `useMemo()`, `useCallback()` to make the callback stable
[Improve Performance in React.js Using Hooks - Better Programming - Medium](https://medium.com/better-programming/improve-performance-in-react-js-using-hooks-3d0ebbad6956)
[React — Why useContext() will clean your code – Michael Majdanski – Medium](https://medium.com/@mmajdanski/react-why-usecontext-will-clean-your-code-ca2b185e23f5)
[Simple Painter in ReactJS — useContext, useState – Prima – Medium](https://medium.com/@anMagpie/simple-painter-in-reactjs-usecontext-usestate-2f7c1dfc898d)
[The modern guide to React state patterns - LogRocket Blog](https://blog.logrocket.com/modern-guide-react-state-patterns/)

[React Tracked · Simple and fast global state with React Context. Eliminate unnecessary re-renders without hassle.](https://react-tracked.js.org/)
[dai-shi/react-tracked: Simple and fast global state with React Context. Eliminate unnecessary re-renders without hassle.](https://github.com/dai-shi/react-tracked)

[useRedux — state management pattern with React Hooks](https://hackernoon.com/useredux-state-management-pattern-with-react-hooks-fa8e1413b9f1)
[diegohaz/constate: React Context + State](https://github.com/diegohaz/constate)

[developit/stockroom: 🗃 Offload your store management to a worker easily.](https://github.com/developit/stockroom)

[Pullstate · Simple state stores using immer and React hooks](https://lostpebble.github.io/pullstate/)

[storeon/storeon: 🌩 A tiny (185 bytes) event-based Redux-like state manager for React, Preact, Angular, Vue, and Svelte](https://github.com/storeon/storeon)
[Storeon: "Redux" in 173 bytes — Martian Chronicles, Evil Martians’ team blog](https://evilmartians.com/chronicles/storeon-redux-in-173-bytes)
[Event-driven state management in React using Storeon - LogRocket Blog](https://blog.logrocket.com/event-driven-state-management-in-react-using-storeon/)

### Context API

> since 16.3
> TODO: clean-up trivial posts

[Context - React](https://reactjs.org/docs/context.html)
Store states local to a compound component, alleviate the need for Redux

[diegohaz/awesome-react-context: 😎 A curated list of stuff related to the new React Context API](https://github.com/diegohaz/awesome-react-context)

[Heres how React's New Context API Works - YouTube](https://www.youtube.com/watch?v=XLJN4JfniH4)
[What can the React Context API do for you? Multi-language text, Modals, and Themes](https://codeburst.io/what-can-react-context-api-do-for-you-multi-language-text-modals-and-theme-switchers-9cfbc8e5ee5e)

[Digging Into React Context | CSS-Tricks](https://css-tricks.com/digging-into-react-context/)
[Understanding the React Context API ← Alligator.io](https://alligator.io/react/context-api/)
[Nesting and overriding new React Context API - DEV Community 👩‍💻👨‍💻](https://dev.to/iamandrewluca/nesting-and-overriding-new-react-context-api-220i)
[An Introduction To React’s Context API — Smashing Magazine](https://www.smashingmagazine.com/2020/01/introduction-react-context-api/)
[Redux vs. The React Context API](https://daveceddia.com/context-api-vs-redux/)
[React's Context API explained: Provider and Consumer - RWieruch](https://www.robinwieruch.de/react-context-api)
[React’s ⚛️ new Context API – DailyJS – Medium](https://medium.com/dailyjs/reacts-%EF%B8%8F-new-context-api-70c9fe01596b)
[React Context API – Zsolt Nagy](http://www.zsoltnagy.eu/react-context-api/)
[React Context API - A Replacement for Redux? – Bits and Pieces](https://blog.bitsrc.io/react-context-api-a-replacement-for-redux-6e20790492b3)
[React Context API vs Redux — the eternal dichotomy – SoftwareMill Tech Blog](https://blog.softwaremill.com/react-context-api-vs-redux-the-eternal-dichotomy-24639907fc98)
[Implementing State Management using Context API and Hooks in React - DEV Community 👩‍💻👨‍💻](https://dev.to/gloriamaris/implementing-state-management-using-context-api-and-hooks-in-react-36jk)
[Learn the React Context API with a Practical Example You Can Bring to Your Apps](https://itnext.io/understanding-the-react-context-api-through-building-a-shared-snackbar-for-in-app-notifications-6c199446b80c)
[React Context and Re-Renders: React Take the Wheel - Ryan Florence - Medium](https://medium.com/@ryanflorence/react-context-and-re-renders-react-take-the-wheel-cd1d20663647) use state and `setState()` as value for Provider, usable with Hooks

In the old days, most React routers (and Redux) use the undocumented `this.context`
[React.js: Communication between Components with Contexts - JScrambler Blog](https://blog.jscrambler.com/react-js-communication-between-components-with-contexts/)

### Hook as Redux alternative

> TODO: clean-up trivial posts

Hooks provides some helper functions that can make it an alternative to introducing Redux to your project.
But React Hooks and Redux are not mutually exclusive!!
[Stop Asking if React Hooks Replace Redux - The Startup - Medium](https://medium.com/swlh/stop-asking-if-react-hooks-replace-redux-448c54d79551)

> see `redux-js.md#hooks-api`

```js
import React, { useReducer } from "react";
export const Store = React.createContext();

const initialState = {
  counter: 5,
};

const reducer = (state = initialState, action) => {
  switch (action.types) {
    case "ADD":
      return { ...state, counter: state.counter + 1 };
    case "SUB":
      return { ...state, counter: state.counter - 1 };
    default:
      return state;
  }
};

export const StoreProvider = (props) => {
  const [state, dispatch] = useReducer(reducer, initialState);
  return (
    <Store.Provider value={{ state, dispatch }}>
      {props.children}
    </Store.Provider>
  );
};
```

[Simplifying Global State with React Hooks - Pete Givens - Medium](https://medium.com/@pgivens/simplifying-global-state-with-react-hooks-4d7df52d363)
[React Hooks is the functional paradise you’ve been waiting for](https://medium.com/capbase-engineering/react-hooks-is-the-functional-paradise-youve-been-waiting-for-994e53f65f94)
[Using React Hooks to manage local state with Functional Components](https://medium.com/capbase-engineering/part-2-using-react-hooks-to-manage-local-state-with-functional-components-3676fcd5646e)
[A simpler entry to Redux (without Redux) using React Hooks | by Elliott Greaves | The Startup | Medium](https://medium.com/swlh/a-simpler-entry-to-redux-without-redux-using-react-hooks-3de90ec2f060)
[The React Hooks based alternative to Redux and the Flux pattern](https://medium.com/capbase-engineering/part-3-the-react-hooks-based-alternative-to-redux-and-the-flux-pattern-a726220a8a9a)
[Mimic Redux with React Context API and hooks - The Startup - Medium](https://medium.com/swlh/mimic-redux-with-react-context-api-and-hooks-21fbec280205)
[An alternative to React Redux by React Hooks API (For both JavaScript and TypeScript)](https://itnext.io/an-alternative-to-react-redux-by-react-hooks-api-for-both-javascript-and-typescript-c5e9a351ba0b)
[Replacing Redux with React Hooks and Context: A small concrete example with reactive-react-redux](https://levelup.gitconnected.com/redux-meets-hooks-for-non-redux-users-a-small-concrete-example-with-reactive-react-redux-6babc881639b)
[State Management with React Hooks — No Redux or Context API](https://medium.com/javascript-in-plain-english/state-management-with-react-hooks-no-redux-or-context-api-8b3035ceecf8)

[Do React Hooks Replace Redux? - JavaScript Scene - Medium](https://medium.com/javascript-scene/do-react-hooks-replace-redux-210bab340672)
[Use Hooks + Context, not React + Redux - LogRocket Blog](https://blog.logrocket.com/use-hooks-and-context-not-react-and-redux/) `useContext()`, `useReducer()`
[React's useReducer vs Redux - RWieruch](https://www.robinwieruch.de/redux-vs-usereducer)

[Life after Redux - ITNEXT](https://itnext.io/life-after-redux-21f33b7f189e)
[Replace Redux state with React Hooks and Context - ITNEXT](https://itnext.io/replace-redux-state-with-react-hooks-and-context-7906e0fd5521)
[Replacing redux with react hooks and context (part 1)](https://medium.com/octopus-labs-london/replacing-redux-with-react-hooks-and-context-part-1-11b72ffdb533)
[Replacing redux with react hooks and context (part 2)](https://medium.com/octopus-labs-london/replacing-redux-with-react-hooks-and-context-part-2-838fd20e6739)
[How to Redux with React Hooks? - RWieruch](https://www.robinwieruch.de/redux-with-react-hooks/)
[A simpler entry to Redux (without Redux) using React Hooks](https://medium.com/swlh/a-simpler-entry-to-redux-without-redux-using-react-hooks-3de90ec2f060)

[The Container Pattern for Better State Management in React. | by Spencer | Sep, 2020 | Medium | Better Programming](https://medium.com/better-programming/the-container-pattern-for-better-state-management-in-react-9351fe4381d1) like Recoil very much

### Recoil

[Recoil](https://recoiljs.org/) have larger footprint

[Recoil - a New State Management Library for React](https://www.infoq.com/news/2020/05/recoil-react-state-management/)
[Recoil: State Management for Today's React - Dave McCabe aka @mcc_abe at @ReactEurope 2020 - YouTube](https://www.youtube.com/watch?v=_ISAA_Jt9kI)
[React: Intro to Recoil - YouTube](https://www.youtube.com/watch?v=So4ny9Aa7Oo)

### Jotai

[pmndrs/jotai: 👻 Primitive, flexible state management for React](https://github.com/pmndrs/jotai)
[jotai/xstate.md at master · pmndrs/jotai · GitHub](https://github.com/pmndrs/jotai/blob/master/docs/api/xstate.md)

[Jotai, a New Granular State Management Library for React](https://www.infoq.com/news/2020/09/jotai-react-state-management/)
[Redux-Free State Management with Jotai | by Nathan Sebhastian | Bits and Pieces](https://blog.bitsrc.io/redux-free-state-management-with-jotai-2c8f34a6a4a)
[Jotai vs. Recoil: What are the differences? - LogRocket Blog](https://blog.logrocket.com/jotai-vs-recoil-what-are-the-differences/)

### Nano Stores

[nanostores/nanostores: A tiny (198 bytes) state manager for React/RN/Preact/Vue/Svelte with many atomic tree-shakable stores](https://github.com/nanostores/nanostores)

### Proxy-based

[pmndrs/valtio: 💊 Valtio makes proxy-state simple for React and Vanilla](https://github.com/pmndrs/valtio) Suspense compatible

[bennyg123/entangle: Global state management tool for react hooks inspired by RecoilJS and Jotai using proxies.](https://github.com/bennyg123/entangle)

## Refs

[Refs and the DOM - React](https://reactjs.org/docs/refs-and-the-dom.html)
Use `React.createRef()` since 16.3

[How to Use React Refs – Ross Bulat – Medium](https://medium.com/@rossbulat/how-to-use-react-refs-4541a7501663)
[Working with refs in React | CSS-Tricks](https://css-tricks.com/working-with-refs-in-react/)
[When to use React's Ref on a DOM node in React - RWieruch](https://www.robinwieruch.de/react-ref-attribute-dom-node/) callback ref
[Cleaning up the DOM with ForwardRef in React - LogRocket Blog](https://blog.logrocket.com/cleaning-up-the-dom-with-forwardref-in-react/)

[React Refs, both Class and Functional Components. - JavaScript in Plain English - Medium](https://medium.com/javascript-in-plain-english/react-refs-both-class-and-functional-components-76b7bce487b8)

`useRef()` not limited to DOM node, hold previous state and store non-state value
[How to get previous props/state with React Hooks - LogRocket Blog](https://blog.logrocket.com/how-to-get-previous-props-state-with-react-hooks/)
[8 Useful Practices for React Apps You Should Know - DEV Community 👩‍💻👨‍💻](https://dev.to/jsmanifest/8-useful-practices-for-react-apps-you-should-know-5k9)
[React Hooks - Passing Child Component State Up with useRef](https://medium.com/@renatognunes/react-hooks-passing-child-component-state-up-with-useref-de88401c2654)

The old string refs are deprecated
[Refs in React : All you need to know ! – Hacker Noon](https://hackernoon.com/refs-in-react-all-you-need-to-know-fb9c9e2aeb81)

## Portal

> since 16.0

[Portals – React](https://reactjs.org/docs/portals.html)
[Using React Portals to Render Children Outside the DOM Hierarchy | CSS-Tricks](https://css-tricks.com/using-react-portals-to-render-children-outside-the-dom-hierarchy/)
[React’s Portals in 3 minutes - codeburst](https://codeburst.io/reacts-portals-in-3-minutes-9b2efb74e9a9)
[Using a React 16 Portal to do something cool - HackerNoon.com - Medium](https://hackernoon.com/using-a-react-16-portal-to-do-something-cool-2a2d627b0202)
[React Portals: What are they and why should we use them?](https://levelup.gitconnected.com/react-portals-what-are-they-and-why-should-we-use-them-7c082a62e8fa)
[React-cool-portal: What it is and how to use it - LogRocket Blog](https://blog.logrocket.com/react-cool-portal-what-it-is-and-how-to-use-it/)
[diegomura/react-portalgun: Lightweight portal system for React. Mega seeds included 🔫](https://github.com/diegomura/react-portalgun)
[tajo/react-portal: 🎯 React component for transportation of modals, lightboxes, loading bars... to document.body or else.](https://github.com/tajo/react-portal)

## Code Splitting/Lazy Loading

> since 16.6

[Code-Splitting – React](https://reactjs.org/docs/code-splitting.html)
[Magic of React Suspense with concurrent react and React.lazy API - By Vivek Nayyar](https://hackernoon.com/magic-of-react-suspense-with-concurrent-react-and-react-lazy-api-e32dc5f30ed1)
[Async React using React Router & Suspense – ITNEXT](https://itnext.io/async-react-using-react-router-suspense-a86ade1176dc)
[Analyze your React app’s bundle size and reduce it using code-splitting · Emma Goto](https://www.emgoto.com/react-bundles-and-code-splitting/)
[React.js: reduce your javascript bundle with code splitting](https://medium.com/kaliop/react-js-reduce-your-javascript-bundle-with-code-splitting-f2d24abd42b8)
[React.js Hooks Crash Course - YouTube](https://www.youtube.com/watch?v=-MlNBTSg_Ww)
[Lazy Loading React Components (with react.lazy and suspense)](https://blog.bitsrc.io/lazy-loading-react-components-with-react-lazy-and-suspense-f05c4cfde10c)
[How to Reduce React App Loading Time By 70% - DEV Community](https://dev.to/nilanth/how-to-reduce-react-app-loading-time-by-70-1kmm)

[Loadable Components - React code splitting](https://loadable-components.com/) can embed async components for SSR
[Comparison with React.lazy - Loadable Components](https://loadable-components.com/docs/loadable-vs-react-lazy/)
[An SEO approach to async components with loadable-components - LogRocket Blog](https://blog.logrocket.com/seo-approach-async-loadable-components/)
[Code splitting in React: An overview - LogRocket Blog](https://blog.logrocket.com/code-splitting-in-react-an-overview/)

## App Frameworks/Distros

[React Distros](https://www.swyx.io/react-distros/)
[Server Side Rendering - Loadable Components](https://loadable-components.com/docs/server-side-rendering/)

[Hydrogen overview](https://shopify.dev/custom-storefronts/hydrogen)
[Shopify/hydrogen: React-based framework for building dynamic, Shopify-powered custom storefronts.](https://github.com/Shopify/hydrogen)

[refine | A React-based framework for building data-intensive applications in no time! | refine](https://refine.dev/)

[Remix - Build Better Websites](https://remix.run/)
[Remix: A guide to the newly open-sourced React framework - LogRocket Blog](https://blog.logrocket.com/remix-guide-newly-open-sourced-react-framework/)

[Remix vs. Next.js vs. SvelteKit - LogRocket Blog](https://blog.logrocket.com/react-remix-vs-next-js-vs-sveltekit/)

### Next.js

> Server Side Rendering, app framework

[Next.js by Vercel - The React Framework](https://nextjs.org/)
[Learn | Next.js](https://nextjs.org/learn/)
[The Next.js Handbook](https://www.freecodecamp.org/news/the-next-js-handbook/)

[Create Next App | Next.js](https://nextjs.org/docs/api-reference/create-next-app)
[next.js/examples at master · vercel/next.js](https://github.com/vercel/next.js/tree/master/examples)

```sh
yarn create next-app --ts  # recommended
npx create-next-app --example api-routes --use-npm

npx dev
npx build && npx start  # local deployment with app server
npx build && npx export -o build/ # static HTML without need of app server
```

[Next.js in 100 Seconds // Plus Full Beginner's Tutorial - YouTube](https://www.youtube.com/watch?v=Sklc_fQBmcs)
[Next.js Architecture for Common Solutions | Chris Hannaby - YouTube](https://www.youtube.com/watch?v=ZGAR8RdBdok)
[Next.js Tutorials - YouTube](https://www.youtube.com/playlist?list=PLFsfg2xP7cbI1U7BZJwmJwTVs4D0pqX1F) Colby Fayock
[Next.js 101: What Features You Should Know About](https://www.netlify.com/blog/2020/06/18/next.js-101-what-you-should-know/)

[Next step after Node.js: Framework for 'universal' JavaScript apps | InfoWorld](http://www.infoworld.com/article/3136337/javascript/next-step-after-nodejs-framework-for-universal-javascript-apps.html)
[We migrated to Next.js to serve our home page 7.5× faster](https://blog.manifold.co/we-migrated-to-next-js-to-serve-our-home-page-7-5-faster-559443219c84)

[Next.js vs Gatsby vs create-react-app](https://flaviocopes.com/next-vs-gatsby-vs-cra/)
[How to Start ReactJS Development Fast: 3 Solid Tools and Best Practices - Codica](https://www.codica.com/blog/how-to-start-reactjs-development-fast-3-solid-tools-and-best-practices/)
[Build a Portfolio Using Next.js, Tailwind, and Vercel | by Nilanth | Aug, 2021 | Better Programming](https://betterprogramming.pub/build-a-portfolio-using-next-js-tailwind-and-vercel-48c645d007ba)

[Next.js Trash Course - Part 1/3 - DEV Community](https://dev.to/vinicius77/next-js-trash-course-part-1-3-2dlb)
[Next.js Trash Course - Part 2/3 - DEV Community](https://dev.to/vinicius77/next-js-trash-course-part-2-3-3115)
[Next.js Trash Course - Part 3/3 - DEV Community](https://dev.to/vinicius77/next-js-trash-course-part-3-3-3igc)

[How to install Next.js](https://flaviocopes.com/how-to-install-nextjs/)
[Linking two pages in Next.js using Link](https://flaviocopes.com/nextjs-link-two-pages/)
[Dynamic content in Next.js with the router](https://flaviocopes.com/nextjs-dynamic-content/)
[How to Integrate MongoDB Into Your Next.js App](https://developer.mongodb.com/how-to/nextjs-with-mongodb/)
[How I Built my Blog using MDX, Next.js, and React](https://www.joshwcomeau.com/blog/how-i-built-my-blog/)
[How to Build a Blog with Next 9.4, Netlify, and Markdown](https://www.netlify.com/blog/2020/05/04/building-a-markdown-blog-with-next-9.4-and-netlify/)

### Deployment

#### Vercel

[Deployment | Next.js](https://nextjs.org/docs/deployment)

#### Netlify

[Next.js from the Ground Up - Jamstack Explorers](https://explorers.netlify.com/learn/nextjs)
[Next.js on Netlify | Netlify Docs](https://docs.netlify.com/configure-builds/common-configurations/next-js/)
[netlify/netlify-plugin-nextjs: A build plugin to integrate Next.js seamlessly with Netlify](https://github.com/netlify/netlify-plugin-nextjs/)

[How to set up a headless e-commerce site with Next.js and the Shopify Storefront API](https://www.netlify.com/blog/2021/09/13/build-your-own-headless-commerce-site-with-next.js-and-shopify/)

#### Static HTML

[Advanced Features: Static HTML Export | Next.js](https://nextjs.org/docs/advanced-features/static-html-export)

[Speed up your Next.js (React) app with this neat trick - YouTube](https://www.youtube.com/watch?v=98gcHJSW1mY) pure HTML+CSS

```js
export const config = {
  unstable_runtimeJS: false,
};
```

## React Server Component

[Introducing Zero-Bundle-Size React Server Components – React Blog](https://reactjs.org/blog/2020/12/21/data-fetching-with-react-server-components.html)
[React Server Components. - It’s not server-side rendering. | by Nathan Sebhastian | Bits and Pieces](https://blog.bitsrc.io/react-server-components-1ca621ac2519)
[I Tested React Server Components And I'm Not A Fan (Yet).](https://marmelab.com/blog/2021/06/15/react-server-components.html)
[What are React Server Components? - International Javascript Conference](https://javascript-conference.com/blog/what-are-react-server-components/)

## Suspense

> since 16.6

`<Suspense>` captures a _thrown_ `Promise` from its children in render tree and renders the component in `fallback` prop.
[React Suspense: Bringing a Bit of Hitchcock to UI Performance](https://medium.com/@mark.okeeffe_11887/react-suspense-bringing-a-bit-of-hitchcock-to-ui-performance-d132aa986e99)
[Understanding Suspense-ful coding in React - DEV Community](https://dev.to/zackdotcomputer/understanding-suspense-ful-coding-in-react-3n53) uses [`suspension`](https://github.com/zackdotcomputer/suspension)

Fetch-then-render, as opposed to Fetch-on-render as in `useEffect()` and `componentDidMount()`. The fetched data are supposed to be stored in some global cache as the current component is removed.

Present and future
[Why React Suspense Will Be a Game Changer - React In Depth - Medium](https://medium.com/react-in-depth/why-react-suspense-will-be-a-game-changer-37b40fea71ec)
[What the heck is this in React ? 🥁🥁(Suspense) 🥁🥁](https://itnext.io/what-the-heck-is-this-in-react-suspense-c5e641e487a)

[Dan Abramov - Suspense! - ReactFest 🎡 - YouTube](https://www.youtube.com/watch?v=6g3g0Q_XVb4) !important, code splitting
[Dan Abramov: Beyond React 16 | JSConf Iceland 2018 - YouTube](https://www.youtube.com/watch?v=nLF0n9SACd4)
[Moving To React Suspense - Jared Palmer - React Conf 2018 - YouTube](https://www.youtube.com/watch?v=SCQgE4mTnjU)
[Andrew Clark: React Suspense - YouTube](https://www.youtube.com/watch?v=z-6JC0_cOns)
[Data Fetching With Suspense In Relay | Joe Savona - YouTube](https://www.youtube.com/watch?v=Tl0S7QkxFE4)

[A Quick Walkthrough of SuspenseList in React - Bits and Pieces](https://blog.bitsrc.io/quick-walkthrough-to-suspenselist-in-react-b930d1ece892)

Another use case is for data fetching (experimental), using `react-cache` (experimental).
This function also be archived by Hooks as of now.
[The Suspense is Killing Redux - Ryan Florence - Medium](https://medium.com/@ryanflorence/the-suspense-is-killing-redux-e888f9692430)
[Suspense for Data Fetching (Experimental) – React](https://reactjs.org/docs/concurrent-mode-suspense.html#approach-3-render-as-you-fetch-using-suspense)
[React Suspense in Practice | CSS-Tricks](https://css-tricks.com/react-suspense-in-practice/)
[How to use React Suspense for Data Fetching Now | Level Up Coding](https://levelup.gitconnected.com/how-you-can-use-react-suspense-for-data-fetching-in-real-world-applications-now-9fda8138f687)
[React Suspense with the Fetch API – Levelup Your Coding](https://levelup.gitconnected.com/react-suspense-with-the-fetch-api-93e40231263d)
[React's Experimental Suspense API Will Rock for Fallback UI During Data Fetches | CSS-Tricks](https://css-tricks.com/reacts-experimental-suspense-api-will-rock-for-fallback-ui-during-data-fetches/)

`<SuspenseList>` controls order of rendering
[First Look at React Suspense List - YouTube](https://www.youtube.com/watch?v=KO8rPRyCZd4)
[Concurrent UI Patterns (Experimental) – React](https://reactjs.org/docs/concurrent-mode-patterns.html)
[Concurrent Mode API Reference (Experimental) – React](https://reactjs.org/docs/concurrent-mode-reference.html#suspenselist)

## Hook

> since 16.8
> TODO: clean-up trivial posts

new API to replace life cycle API, co-locate effect/logic and state to a reusable function

[Introducing Hooks – React](https://reactjs.org/docs/hooks-intro.html) !important
[Rules of Hooks – React](https://reactjs.org/docs/hooks-rules.html)
[Hooks at a Glance – React](https://reactjs.org/docs/hooks-overview.html)
[Hooks FAQ – React](https://reactjs.org/docs/hooks-faq.html)
[Hooks API Reference – React](https://reactjs.org/docs/hooks-reference.html)

[Collection - React Hooks and Suspense on @eggheadio](https://egghead.io/playlists/react-hooks-and-suspense-650307f2)
[Rundown of the Most Important React Hooks | by Kunal Vishnoi | Better Programming | Medium](https://medium.com/better-programming/rundown-of-the-most-important-react-hooks-5c9ec4cac5a2)
[Underrated React Hooks you're missing out on - LogRocket Blog](https://blog.logrocket.com/underrated-react-hooks-youre-missing-out-on/)
[React Hooks: The good, the bad, and the ugly - LogRocket Blog](https://blog.logrocket.com/react-hooks-the-good-the-bad-and-the-ugly/)
[What are React Hooks and Why do I need them?](https://geekflare.com/understanding-react-hooks/)
[Making Sense of React Hooks - DEV Community 👩‍💻👨‍💻](https://dev.to/dan_abramov/making-sense-of-react-hooks-2eib)

[troch/reinspect: Use redux devtools to inspect useState and useReducer](https://github.com/troch/reinspect)

[React Today and Tomorrow - Sophie Alpert and Dan Abramov - React Conf 2018 - YouTube](https://www.youtube.com/watch?v=V-QO-KO90iQ)
[90% Cleaner React With Hooks - Ryan Florence - React Conf 2018 - YouTube](https://www.youtube.com/watch?v=wXLf18DsV-I)
[ryanflorence/react-conf-2018](https://github.com/ryanflorence/react-conf-2018)

[Developer Productivity Tips from 25 React Experts | KendoReact](https://www.telerik.com/kendo-react-ui/react-hooks-guide/)
[Hooked on React - ITNEXT](https://itnext.io/hooked-on-react-10affe4cca3c)

[Build Tic Tac Toe with React Hooks](https://scrimba.com/g/greactgame)

[React Hooks cheat sheet: Unlock solutions to common problems - LogRocket Blog](https://blog.logrocket.com/react-hooks-cheat-sheet-unlock-solutions-to-common-problems-af4caf699e70/)
[State management using only React Hooks - LogRocket Blog](https://blog.logrocket.com/state-management-using-only-react-hooks/)
[Frustrations with React Hooks - LogRocket Blog](https://blog.logrocket.com/frustrations-with-react-hooks/)
[Solutions to frustrations with React Hooks - LogRocket Blog](https://blog.logrocket.com/solutions-to-frustrations-with-react-hooks/)
[React Hooks — Gotchas - Fuzz - Medium](https://medium.com/fuzz/react-hooks-gotchas-b8fcd25cc1b6)
[Best Practices With React Hooks — Smashing Magazine](https://www.smashingmagazine.com/2020/04/react-hooks-best-practices/)

[DejaVu: Caching versus Memoization - DEV Community 👩‍💻👨‍💻](https://dev.to/thekashey/dejavu-caching-versus-memoization-298n) PUSH mode of hook cause double rendering
[Easier Asynchronous State Modelling in React Redux or Hooks](https://medium.com/@jesterxl/easier-asynchronous-state-modelling-in-react-redux-or-hooks-a05924b7bfa1)

[Introducing: Redux Hooks – ITNEXT](https://itnext.io/introducing-redux-hooks-1bf9c568ecc2)
[An Intro to Advanced React Hooks - In the Weeds - Medium](https://medium.com/in-the-weeds/an-intro-to-advanced-react-hooks-a8af6397fe28)
[Why React Hooks, and how did we even get here? – freeCodeCamp.org](https://medium.freecodecamp.org/why-react-hooks-and-how-did-we-even-get-here-aa5ed5dc96af)
[Why React Hooks? A developer’s perspective. – Hacker Noon](https://hackernoon.com/why-react-hooks-a-developers-perspective-2aedb8511f38)
[Hooked on Hooks - The Startup - Medium](https://medium.com/swlh/hooked-on-hooks-637f53ba9323)
[Introduction to React Hooks](https://alligator.io/react/react-hooks)
[An Overview of React Hooks with Examples – Level Up Your Code](https://levelup.gitconnected.com/react-hooks-cliff-notes-for-the-junior-dev-c2027aaf58cc)
[⚛️ React: Hooks vs. Render Props vs. Higher-Order Components 👨‍🔬 - DEV Community 👩‍💻👨‍💻](https://dev.to/bettercodingacademy/react-hooks-vs-render-props-vs-higher-order-components-1al0)
[Understanding Hooks in React. An introduction to React 16.7 hooks… | by Mahesh Haldar | Bits and Pieces](https://blog.bitsrc.io/understanding-hooks-in-react-a-deep-dive-d5d5dc88ecd9)
[How to Reuse Logic with React Hooks | Rafael Quintanilha](https://rafaelquintanilha.com/how-to-reuse-logic-with-react-hooks/)
[How to Create Your First React Hook from Start to Finish](https://www.freecodecamp.org/news/code-react-hooks/) `useCopyToClipboard()`

[How to Use Basic React Hooks for State and Effects](https://www.telerik.com/blogs/how-to-use-basic-react-hooks-for-state-and-effects)
[How to Use Basic React Hooks for Context](https://www.telerik.com/blogs/how-to-use-basic-react-hooks-for-context)
[How to Use Basic React Hooks for Reducers](https://www.telerik.com/blogs/how-to-use-basic-react-hooks-for-reducers)
[A Dark Mode Toggle with React and ThemeProvider | CSS-Tricks](https://css-tricks.com/a-dark-mode-toggle-with-react-and-themeprovider/)

[Programming Patterns with React Hooks - JavaScript in Plain English - Medium](https://medium.com/javascript-in-plain-english/programming-patterns-with-react-hooks-329c22b96461)
[Advanced React (anti)patterns - Frontend Weekly - Medium](https://medium.com/front-end-weekly/advanced-react-anti-patterns-a644c55437fe) async `useCallback()`

[Frustrations with React Hooks - LogRocket Blog](https://blog.logrocket.com/frustrations-with-react-hooks/)
[Gotchas of working with React Hooks and Concurrent mode](https://medium.com/capbase-engineering/gotchas-of-working-with-react-hooks-and-concurrent-mode-72157f5367eb)

[Asynchronous Functional Programming Using React Hooks](https://medium.com/capbase-engineering/asynchronous-functional-programming-using-react-hooks-e51a748e6869)

[Notes on TypeScript: React Hooks - DEV Community 👩‍💻👨‍💻](https://dev.to/busypeoples/notes-on-typescript-react-hooks-28j2)
[10 React Hooks you Should Have in Your Toolbox – Bits and Pieces](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)

Alternatives API design:
[Why Do React Hooks Rely on Call Order? — Overreacted](https://overreacted.io/why-do-hooks-rely-on-call-order/)
[RFC: React Hooks by sebmarkbage · Pull Request #68 · reactjs/rfcs](https://github.com/reactjs/rfcs/pull/68#issuecomment-439314884)

[How to Build a Todo List with React Hooks – freeCodeCamp.org](https://medium.freecodecamp.org/how-to-build-a-todo-list-with-react-hooks-ebaa4e3db3b)

### Internals

[Under the hood of React’s hooks system – The Guild – Medium](https://medium.com/the-guild/under-the-hood-of-reacts-hooks-system-eb59638c9dba) !important
[React hooks: not magic, just arrays – Rudi Yardley – Medium](https://medium.com/@ryardley/react-hooks-not-magic-just-arrays-cd4f1857236e)
[React Hooks in depth - JavaScript in Plain English - Medium](https://medium.com/javascript-in-plain-english/react-hooks-3461b10907fa)

[Demystifying React Hooks: useCallback and useMemo - DEV](https://dev.to/milu_franz/demystifying-react-hooks-usecallback-and-usememo-1a8j)
[Demystifying React Hooks: useRef - DEV](https://dev.to/milu_franz/demystifying-react-hooks-useref-2ddp)
[Demystifying React Hooks: useContext - DEV](https://dev.to/milu_franz/demystifying-react-hooks-usecontext-5g4a)
[Demystifying React Hooks: useReducer - DEV](https://dev.to/milu_franz/demystifying-react-hooks-usereducer-3o3n)

[Fun with React Hooks - Michael Jackson and Ryan Florence - YouTube](https://www.youtube.com/watch?v=1jWS7cCuUXw)

- CrappyHooks from scratch
- how hooks solves life-cycle issues with async data
- since all hooks are functions, it is easy to create custom reusable hooks

[swyx Speaking | Getting Closure on Hooks (JSConf Edition)](https://www.swyx.io/speaking/react-hooks/)
[Deep dive: How do React hooks really work? | Netlify](https://www.netlify.com/blog/2019/03/11/deep-dive-how-do-react-hooks-really-work/)
[A guide to useState in React – LogRocket](https://blog.logrocket.com/a-guide-to-usestate-in-react-ecb9952e406c)
[Get Hooked: Hooks in React and Beyond - Circle Engineering](https://engineering.circle.com/get-hooked-hooks-in-react-and-beyond-aaacb228959a)
[How does React Hooks re-renders a function Component?](https://medium.com/swlh/how-does-react-hooks-re-renders-a-function-component-cc9b531ae7f0)

### `useEffect()`

[React "hooking" into lifecyle methods](https://sebhastian.com/react-hooks-useeffect) hook as lifecycle methods

1. state initialization
2. cleanup
3. when dependencies change
   a) cleanup the last subscription
   b) re-initialize subscription

[A Complete Guide to useEffect — Overreacted](https://overreacted.io/a-complete-guide-to-useeffect/) deep dive
[Simplifying useEffect | TkDodo's blog](https://tkdodo.eu/blog/simplifying-use-effect)
[The last guide to the useEffect Hook you'll ever need - LogRocket Blog](https://blog.logrocket.com/guide-to-react-useeffect-hook/)
[4 Ways to useEffect() - DEV Community 👩‍💻👨‍💻](https://dev.to/spukas/4-ways-to-useeffect-pf6)
[Mastering the useEffect API - DEV Community 👩‍💻👨‍💻](https://dev.to/macmacky/mastering-the-useeffect-api-57ed)
[React useEffect Hook. What is the useEffect hook, how does it… | by Ceci García García | Trabe | Medium](https://medium.com/trabe/react-useeffect-hook-44d8aa7cccd0)
[React useEffect Hooks in Action - Better Programming - Medium](https://medium.com/better-programming/https-medium-com-mayank-gupta-6-88-react-useeffect-hooks-in-action-2da971cfe83f)

```js
// mimicking life cycle functions
const Component = props => {
  useEffect(
    // effect function
    () => {
      // componentDidMount() code

      return () => {
        // componentWillUnmount() code
      };
    },
    // only run effect after these values are changed
    // omitting mean run every render, empty array means run once
    []
  );

  render (</>);
}
```

```js
// conditional update upon props change
useEffect(() => {
  const subscription = props.source.subscribe();
  return () => {
    subscription.unsubscribe();
  };
}, [props.source]);
```

For DOM related effects use [`useLayoutEffect()`](https://reactjs.org/docs/hooks-reference.html#uselayouteffect)

### `useReducer()`

[Hooks, State, Closures, and useReducer | Adam Reacts](https://adamrackis.dev/state-and-use-reducer/)
simplify `useEffect()` with reducer
[React hooks useState and useReducer are equivalent in theoretical expressiveness](https://itnext.io/react-hooks-usestate-and-usereducer-are-equivalent-in-theoretical-expressiveness-a7d1c109770)
[React useReducer hook. What is the useReducer hook, how does… | by Ceci García García | Trabe | Medium](https://medium.com/trabe/react-usereducer-hook-2b1331bb768)

```js
// note 2nd param is array
function scanReducer(state, [type, payload]) {
  switch (type) {
    case "initial":
      return { ...state, pending: payload.pending };
    case "pendingBookAdded":
      return { ...state, pending: state.pending + 1 };
    case "bookAdded":
      return {
        ...state,
        pending: state.pending - 1,
        booksSaved: [payload, ...state.booksSaved],
      };
    case "bookLookupFailed":
      return {
        ...state,
        pending: state.pending - 1,
        booksSaved: [
          {
            _id: "" + new Date(),
            title: `Failed lookup for ${payload.isbn}`,
            success: false,
          },
          ...state.booksSaved,
        ],
      };
  }
  return state;
}
const initialState = { pending: 0, booksSaved: [] };

const BookEntryList = (props) => {
  const [state, dispatch] = useReducer(scanReducer, initialState);

  useEffect(() => {
    const ws = new WebSocket(webSocketAddress("/bookEntryWS"));

    ws.onmessage = ({ data }) => {
      let packet = JSON.parse(data);
      dispatch([packet._messageType, packet]);
    };
    return () => {
      try {
        ws.close();
      } catch (e) {}
    };
  }, []);

  //...
};
```

### Applications

[beizhedenglong/react-hooks-lib: A set of reusable React Hooks.](https://github.com/beizhedenglong/react-hooks-lib)
[wojtekmaj/react-hooks: A collection of React Hooks.](https://github.com/wojtekmaj/react-hooks)
[craig1123/react-recipes: 👩‍🍳 A list of React Hooks utility library containing popular customized hooks](https://github.com/craig1123/react-recipes)
[Beautiful React Hooks docs](https://beautifulinteractions.github.io/beautiful-react-hooks/)
[useHooks - Easy to understand React Hook recipes](https://usehooks.com/)
[useHooks(🔥).ts | useHooks(🔥).ts](https://usehooks-typescript.com/)
[Hooks.guide](https://hooks-guide.netlify.com/)
[React Hooks: Recipes - codeburst](https://codeburst.io/react-hooks-recipes-1c18e5984abe) !important
[11 Useful Custom React Hooks for Your Next Web App - Bits and Pieces](https://blog.bitsrc.io/11-useful-custom-react-hooks-for-your-next-app-c66307cf0f0c)
[5 top React Hooks libraries compared - LogRocket Blog](https://blog.logrocket.com/5-top-react-hooks-libraries-compared/)
[How to execute a function only after the user stops typing? - DEV](https://dev.to/przemwo/how-to-execute-a-function-only-after-the-user-stops-typing-beh) `useEffect()` for debouncing

[streamich/react-use: React Hooks — 👍](https://github.com/streamich/react-use)
[15 Custom Hooks to Make your React Component Lightweight - DEV Community](https://dev.to/nilanth/15-custom-hooks-to-make-your-react-component-lightweight-17cd)

[Building Your Own Hooks – React](https://reactjs.org/docs/hooks-custom.html)
[React: Writing a custom API hook - DEV Community 👩‍💻👨‍💻](https://dev.to/patrixr/react-writing-a-custom-api-hook-l16)
[Writing Your Own React Hooks, the Return Value - DEV Community 👩‍💻👨‍💻](https://dev.to/namick/writing-your-own-react-hooks-the-return-value-3lp6)
[Build your own React hook - DEV Community 👩‍💻👨‍💻](https://dev.to/notrab/build-a-react-hook-from-scratch-15ia)

[Essential React Hooks Design Patterns - ITNEXT](https://itnext.io/essential-react-hooks-design-patterns-a04309cc0404)
`useLink`, `useThrottle`, `DelayedInput`
[youtube/videos/react-demos/src/demo at master · hswolff/youtube](https://github.com/hswolff/youtube/tree/master/videos/react-demos/src/demo)

[How to Build a Simple Pokémon Web App with React Hooks and the Context API](https://www.freecodecamp.org/news/building-a-simple-pokemon-web-app-with-react-hooks-and-context-api/amp/)

[Using React Hooks to create sticky headers - LogRocket Blog](https://blog.logrocket.com/using-react-hooks-to-create-sticky-headers/)
[A Practical Guide to Creating Reusable React Components - SitePoint](https://www.sitepoint.com/creating-reusable-react-components/)
[The power of custom hooks in React (responsive design example) - DEV Community](https://dev.to/mlevi1806/the-power-of-custom-hooks-in-react-responsive-design-example-4flb)

[React Hooks: Inverting Container/Presenter - ITNEXT](https://itnext.io/react-hooks-inverting-container-presenter-5758a1dfdaa)
[helloitsjoe/react-hooks-compose: Decouple Hooks from the presentational components that use them](https://github.com/helloitsjoe/react-hooks-compose) inject hook to presentational components

[React Custom Hooks — useAutoScroll - Level Up Coding](https://levelup.gitconnected.com/react-custom-hooks-useautoscroll-d63f17037a2d)
[MarkGeeRomano/useAutoScroll](https://github.com/MarkGeeRomano/useAutoScroll)

[Implementing private routes with React Router and Hooks](https://medium.com/trabe/implementing-private-routes-with-react-router-and-hooks-ed38d0cf93d5) `useAuthDataContext()` with provider

[Delayed rendering of React Components - Trabe - Medium](https://medium.com/trabe/delayed-render-of-react-components-3482f8ad48ad)

[How I Developed React Hooks for Web Workers - ITNEXT](https://itnext.io/how-i-developed-react-hooks-for-web-workers-9e97efc86266)

[useBreakpoint Hook — Get Media Query Breakpoints in React](https://medium.com/better-programming/usebreakpoint-hook-get-media-query-breakpoints-in-react-3f1779b73568)
[How To Use Media Queries Programmatically in React - Better Programming - Medium](https://medium.com/better-programming/how-to-use-media-queries-programmatically-in-react-4d6562c3bc97)

[Using React Hooks to sync your component state and the URL Query string](https://medium.com/swlh/using-react-hooks-to-sync-your-component-state-with-the-url-query-string-81ccdfcb174f)

[Build an Infinite Scroll Component in React using React Hooks - Upmostly](https://upmostly.com/tutorials/build-an-infinite-scroll-component-in-react-using-react-hooks/)
[How To Create a Custom useInfiniteScroll() With React Hooks](https://medium.com/better-programming/how-to-create-a-custom-useinfinitescroll-with-react-hooks-248f4531384c)

[Using requestAnimationFrame with React Hooks | CSS-Tricks](https://css-tricks.com/using-requestanimationframe-with-react-hooks/)

[react-use-date | bmalehorn](https://bmalehorn.com/react-use-date/)
[Making setInterval Declarative with React Hooks — Overreacted](https://overreacted.io/making-setinterval-declarative-with-react-hooks/)

#### Forms

[Using Custom React Hooks to Simplify Forms - Upmostly](https://upmostly.com/tutorials/using-custom-react-hooks-simplify-forms/)
[React Custom Hook: useSubmit - JavaScript in Plain English - Medium](https://medium.com/javascript-in-plain-english/react-custom-hook-useonesubmit-b10be17245d8)
[How to Build a Dynamic, Controlled Form with React Hooks (2019)](https://itnext.io/how-to-build-a-dynamic-controlled-form-with-react-hooks-2019-b39840f75c4f)
[Using React Hooks To Create Awesome Forms - Rajat S - Medium](https://medium.com/@geeky_writer_/using-react-hooks-to-create-awesome-forms-6f846a4ce57)
[How React Hooks Change The Way We Build Forms - YouTube](https://www.youtube.com/watch?v=8yo44xN7-nQ)
[How to Build a Dynamic, Controlled Form with React Hooks (2019) | by Mike Cronin | ITNEXT](https://itnext.io/how-to-build-a-dynamic-controlled-form-with-react-hooks-2019-b39840f75c4f)

#### Data Fetching

> basically a `useEffect()` wrapping and async task with loading state, Suspense will support this use case in future release

[How to fetch data with React Hooks? - RWieruch](https://www.robinwieruch.de/react-hooks-fetch-data) `useDataApi()`, `useEffect()` and states managed by `useReducer()`

[dai-shi/react-hooks-fetch: A React custom hook for data fetching with Suspense](https://github.com/dai-shi/react-hooks-fetch) experimental lib
[How to create React custom hooks for data fetching with useEffect](https://itnext.io/how-to-create-react-custom-hooks-for-data-fetching-with-useeffect-74c5dc47000a)
[dai-shi/react-hooks-async: An abortable async function library with React Hooks](https://github.com/dai-shi/react-hooks-async) production lib, like RWieruch's example, cancelable with axios, build async pipeline like async

[SWR – SWR](https://swr.vercel.app/) !important, stale-while-revalidate
[RFC 5861 - HTTP Cache-Control Extensions for Stale Content](https://tools.ietf.org/html/rfc5861)
[vercel/swr: React Hooks library for remote data fetching](https://github.com/vercel/swr)

[slorber/react-async-hook: React hook to handle any async operation in React components](https://github.com/slorber/react-async-hook)
[Handling API request race conditions in React](https://sebastienlorber.com/handling-api-request-race-conditions-in-react) how to handle stale API calls
[How to handle async side effects in 2019 - LogRocket Blog](https://blog.logrocket.com/how-to-handle-async-side-effects-in-2019/)

[React Query - Hooks for fetching, caching and updating asynchronous data in React](https://react-query.tanstack.com/)
[tannerlinsley/react-query: ⚛️ Hooks for fetching, caching and updating asynchronous data in React](https://github.com/tannerlinsley/react-query)
[How and Why You Should Use React Query | by Nathan Sebhastian | Jul, 2020 | Bits and Pieces](https://blog.bitsrc.io/how-to-start-using-react-query-4869e3d5680d)
[Using Suspense with react-query - LogRocket Blog](https://blog.logrocket.com/using-suspense-with-react-query/)
[Practical React Query | TkDodo's blog](https://tkdodo.eu/blog/practical-react-query)

[How To Fetch Data From An API With React Hooks – codeburst](https://codeburst.io/how-to-fetch-data-from-an-api-with-react-hooks-9e7202b8afcd)
[Fetch API data using useEffect React hook - Code Fountain - Medium](https://medium.com/musibs/fetch-api-data-using-useeffect-react-hook-465809ca12c6)
[React Hooks Tutorial on Developing a Custom Hook for Data Fetching](https://itnext.io/react-hooks-tutorial-on-developing-a-custom-hook-for-data-fetching-8ad5840db7ae)
[useFetch: React custom hook for Fetch API with Suspense and Concurrent Mode in Mind](https://itnext.io/usefetch-react-custom-hook-for-fetch-api-with-suspense-and-concurrent-mode-in-mind-1d3ba9250e0)

## Render Props/HoC

[Michael Jackson - Never Write Another HoC - YouTube](https://www.youtube.com/watch?v=BcVAq3YFiuc) inversion of control, higher component invokes render props function
[Render Props in React – Byteconf – Medium](https://medium.com/byteconf/render-props-in-react-6081b6fa3593)
[An Overview of Render Props in React | CSS-Tricks](https://css-tricks.com/an-overview-of-render-props-in-react/)

[How to Use React Higher-Order Components - Ross Bulat - Medium](https://medium.com/@rossbulat/how-to-use-react-higher-order-components-c0be6821eb6c)

[React Higher-Order Components](https://tylermcginnis.com/react-higher-order-components/)
[Andrew Clark - Recomposing your React application at react-europe 2016 - YouTube](https://www.youtube.com/watch?v=zD_judE-bXk)

[React Render Props](https://tylermcginnis.com/react-render-props/)
[Use a Render Prop! – componentDidBlog](https://cdb.reacttraining.com/use-a-render-prop-50de598f11ce)
[When to NOT use Render Props](https://kentcdodds.com/blog/when-to-not-use-render-props/)

[Introduction to higher order components (HOC) in React](https://medium.com/@soorajchandran/introduction-to-higher-order-components-hoc-in-react-383c9343a3aa)
[How Are Function Components Different from Classes? — Overreacted](https://overreacted.io/how-are-function-components-different-from-classes/)
[Container Components and Stateless Functional Components in React – Zsolt Nagy](http://www.zsoltnagy.eu/container-components-and-stateless-functional-components-in-react/)

[Why I stopped spreading props on React Components - DEV Community 👩‍💻👨‍💻](https://dev.to/aurelio/why-i-stopped-spreading-props-on-react-components-o3f)

## James K Nelson

[Interacting with the DOM in React.js, By Example](http://jamesknelson.com/react-js-by-example-interacting-with-the-dom/)
[Interacting with the DOM in React.js, By Example](http://jamesknelson.com/react-js-by-example-interacting-with-the-dom/)
[Learn React By Itself -- no JSX, no Flux, no ES6, no Webpack.](http://jamesknelson.com/learn-raw-react-no-jsx-flux-es6-webpack/)
[Structuring React Applications: Higher-Order Components - James K Nelson](http://jamesknelson.com/structuring-react-applications-higher-order-components/#more-338)

## Reparenting

[Home | React-reparenting](https://paol-imi.github.io/react-reparenting/)
[Reparenting is now possible with React | The Startup](https://medium.com/swlh/reparenting-with-react-426d12fb6d0d)

Reparenting nodes, good for moving components without re-initializing

## chantastic

[Learn React with chantastic — Medium](https://medium.com/@learnreact)
[Container Components — Medium](https://medium.com/@learnreact/container-components-c0e67432e005#.qhhgzfwnm)

## Scotch.io

[Tag Archive for "react" | Scotch](https://scotch.io/tag/react)
[React Starters ― Scotch.io](https://scotch.io/starters/react) 2019 edition

## christianalfoni

[React JS and a browserify workflow - christianalfoni WebApp Enthusiast](http://christianalfoni.github.io/javascript/2014/08/15/react-js-workflow.html)
[christianalfoni - Choosing the correct packaging tool for React js](http://www.christianalfoni.com/articles/2014_08_29_Choosing-the-correct-packaging-tool-for-React-js)
[christianalfoni - Webpack and react is awesome](http://www.christianalfoni.com/articles/2014_12_13_Webpack-and-react-is-awesome)

## Alligator.io

[Posts About React ← Alligator.io](https://alligator.io/react)

## dan_abramov

[Mixins Are Dead. Long Live Composition — Medium](https://medium.com/@dan_abramov/mixins-are-dead-long-live-higher-order-components-94a0d2f9e750) higher-order component vs mixin
[Two React Tips — Medium](https://medium.com/@dan_abramov/two-weird-tricks-that-fix-react-7cf9bbdef375#.oggyawin6)

- Beware of multiple React instances
- Always put a root `<div>` into `<body>` and mount React to it.

The new terms are "Container" (connected) and "Presentational Components" (not connected, can be stateful or pure).

## Resources

[ReactJS - Building Web Apps w/JavaScript](https://www.reddit.com/r/reactjs/)
[Home - React Kung Fu](http://reactkungfu.com/)
[Blogged Answers: Resources for Learning React · Mark's Dev Blog](https://blog.isquaredsoftware.com/2017/12/blogged-answers-learn-react/)

[enaqx/awesome-react](https://github.com/enaqx/awesome-react)
[Some of the best resources to learn ReactJS DebugMe Blog](http://blog.debugme.eu/best-resources-to-learn-reactjs/)
[luismartinezs/react-katas: Each folder contains a "kata" to practice a specific technique of intermediate to advanced React](https://github.com/luismartinezs/react-katas)
[arkency/reactjs_koans: Learn basics of React.js making the tests pass](https://github.com/arkency/reactjs_koans)

[ReactRally - YouTube](https://www.youtube.com/channel/UCXBhQ05nu3L1abBUGeQ0ahw)

[The React Handbook – freeCodeCamp.org](https://medium.freecodecamp.org/the-react-handbook-b71c27b0a795) [download](https://reacthandbook.com/)
[SurviveJS - React](https://survivejs.com/react/)
[How to Learn React – Best Free Online Resources for Beginners | Blog Brainhub.eu](https://brainhub.eu/blog/how-to-learn-react-best-free-online-resources/)
[The React Way by Andrew Clark - YouTube](https://www.youtube.com/watch?v=HOpyRiXB5WQ)
[The Beginner's Guide to React from @kentcdodds on @eggheadio](https://egghead.io/courses/the-beginner-s-guide-to-react)

[Building a React-based Chat Client with Redux – ITNEXT](https://itnext.io/building-a-react-based-chat-client-with-redux-816b47cb8c74)
[Concepts to become an advanced React developer – wineofbits – Medium](https://medium.com/wineofbits/concepts-to-become-an-advanced-react-developer-684d90c086c2)

[React.js Conf 2015 - Making your app fast with high-performance components - YouTube](https://www.youtube.com/watch?v=KYzlpRvWZ6c)
[React.js Conf 2016 - YouTube](https://www.youtube.com/playlist?list=PLb0IAmt7-GS0M8Q95RIc2lOM6nc77q1IY)
[React Conf 2017 - YouTube](https://www.youtube.com/playlist?list=PLb0IAmt7-GS3fZ46IGFirdqKTIxlws7e0)

[Lin Clark: A cartoon guide to performance in React - JSConf Iceland 2016 - YouTube](https://www.youtube.com/watch?v=NGxVLnJKhP8)
[ReactRally - YouTube](https://www.youtube.com/channel/UCXBhQ05nu3L1abBUGeQ0ahw/videos)
[James Long - Debugging Your Debugger - YouTube](https://www.youtube.com/watch?v=gvVpSezT5_M)

## Tools

[5 Tools For Faster Development In React – Bits and Pieces](https://blog.bitsrc.io/5-tools-for-faster-development-in-react-676f134050f2)
[11 Top React Developer Tools for 2020 - Bits and Pieces](https://blog.bitsrc.io/11-top-react-developer-tools-for-2020-3860f734030b)

[Complementary Tools · facebook/react Wiki](https://github.com/facebook/react/wiki/Complementary-Tools)
[A Guide to React.js Tools and Libraries | Toptal](http://www.toptal.com/react/navigating-the-react-ecosystem)
[style-guides/react.md at master · Khan/style-guides](https://github.com/Khan/style-guides/blob/master/style/react.md)
[Development workflow with rackt-cli - revolunet blog](http://blog.revolunet.com/blog/2015/11/01/dev-workflow-with-rackt-cli/)
[garbles/why-did-you-update: Puts your console on blast when React is making unnecessary updates.](https://github.com/garbles/why-did-you-update)

[alidcastano/rogue.js: A nearly invisible SSR experience for React - only an `App.js` and some `getInitialProps` magic](https://github.com/alidcastano/rogue.js)

[reactjs/react-docgen: A CLI and toolbox to extract information from React component files for documentation generation purposes.](https://github.com/reactjs/react-docgen)

[Redux DevTools Extension](http://extension.remotedev.io/)
[React Devtools: A Brief Introduction ← Alligator.io](https://alligator.io/react/react-devtools-intro/)
[Introducing the New React DevTools – React Blog](https://reactjs.org/blog/2019/08/15/new-react-devtools.html) 2019-08 v4
[React DevTools tutorial](https://react-devtools-tutorial.now.sh/)
[React Dev Tools — Debug Like a Ninja - Thinkmill - Medium](https://medium.com/the-thinkmill/react-dev-tools-debug-like-a-ninja-c3a5d09895c6)

[Realize for React](https://www.realizeforreact.com/)

[React Sight](https://www.reactsight.com/)

### Structor

[ipselon/structor: An advanced GUI editor for React](https://github.com/ipselon/structor) WYSIWYG editor for React components
[Structor as a playground for React Applications — Medium](https://medium.com/@alex_pustovalov/structor-as-a-playground-for-react-applications-49accf4544b8#.8o4r48uc9)
[Structor Market](https://helmetrex.com/)

### Documentation

[reactjs/react-docgen](https://github.com/reactjs/react-docgen)
[sapegin/react-styleguidist](https://github.com/sapegin/react-styleguidist)
[Babel Classes · Issue #1 · ctumolosus/jsdoc-babel](https://github.com/ctumolosus/jsdoc-babel/issues/1#issuecomment-119172591)

[Docz](https://www.docz.site/)

[documentationjs](http://documentation.js.org/) not active

[ESDoc - A Documentation Generator For JavaScript(ES6)](https://esdoc.org/)
[Write a documentation React and ES6 project by ESDoc](http://en.blog.koba04.com/2015/06/28/esdoc-documentation-for-react-and-es6/)
ESDoc requires `class` syntax.

## Tips and Tricks

[React.js cheatsheet](http://ricostacruz.com/cheatsheets/react.html)

[14 Beneficial Tips to Write Cleaner Code in React Apps - DEV Community 👩‍💻👨‍💻](https://dev.to/jsmanifest/14-beneficial-tips-to-write-cleaner-code-in-react-apps-1gcf)
[5 common practices that you can stop doing in React](https://blog.logrocket.com/5-common-practices-that-you-can-stop-doing-in-react-9e866df5d269)
[5 Awesome React.js Libraries You Should Know About - Better Programming - Medium](https://medium.com/better-programming/5-awesome-react-js-libraries-you-should-know-about-ef0274fe4a56)
[6 Tips and Best Practices for a Scalable React Project | by Nathan Sebhastian | Bits and Pieces](https://blog.bitsrc.io/best-practices-and-tips-for-a-scalable-react-application-db708ae49227)

[React.js and Dynamic Children - Why the Keys are Important - Arkency Blog](http://blog.arkency.com/2014/10/react-dot-js-and-dynamic-children-why-the-keys-are-important/) properly define keys for React to diff the virtual DOM
[React.js loses input focus on typing - React Kung Fu](http://reactkungfu.com/2015/09/react-js-loses-input-focus-on-typing/)

[reactpatterns.com](http://reactpatterns.com/)
[krasimir/react-in-patterns: List of design patterns/techniques used while developing with React](https://github.com/krasimir/react-in-patterns)
[cjcenizal/react-design-workshop: A workshop on the process of designing React components and applications.](https://github.com/cjcenizal/react-design-workshop)

[React JSX: How to Do It the Right Way, Part I - DZone Web Dev](https://dzone.com/articles/react-jsx-how-to-do-it-the-right-way-part-i)
[React JSX: How to Do It the Right Way, Part II - DZone Web Dev](https://dzone.com/articles/react-jsx-how-to-do-it-the-right-way-part-ii-1)
[React Guide to Props - Part I - DZone Web Dev](https://dzone.com/articles/react-guide-to-props-part-i)
[React Guide to Props - Part II - DZone Web Dev](https://dzone.com/articles/react-guide-to-props-part-ii)
[React Guide to Props - Part III - DZone Web Dev](https://dzone.com/articles/react-guide-to-props-part-iii)
[State Management in React Apps - Part I - DZone Web Dev](https://dzone.com/articles/state-management-in-react-apps-part-i)

[How To Write Better Code in React – Bits and Pieces](https://blog.bitsrc.io/how-to-write-better-code-in-react-best-practices-b8ca87d462b0)

[React.js Best Practices for 2016 | @RisingStack](https://blog.risingstack.com/react-js-best-practices-for-2016/)
[3 Performance Tips to Speed Up Your React Applications](https://www.telerik.com/blogs/3-performance-tips-to-speed-up-your-react-applications)

[Using Derived State in React ← Alligator.io](https://alligator.io/react/get-derived-state/)
[You Probably Don't Need Derived State – React Blog](https://reactjs.org/blog/2018/06/07/you-probably-dont-need-derived-state.html)

[Implementing Infinite Scroll Into a React Component ← Alligator.io](https://alligator.io/react/react-infinite-scroll/)
[How to implement shouldComponentUpdate with this.context? · Issue #2517 · facebook/react](https://github.com/facebook/react/issues/2517)

### #perfmatters

[PureComponent – React](https://reactjs.org/docs/react-api.html#reactpurecomponent)
[Optimizing Performance – React](https://reactjs.org/docs/optimizing-performance.html)
[Performance Engineering with React](http://benchling.engineering/performance-engineering-with-react/)
[A Deep Dive into React Perf Debugging](http://benchling.engineering/deep-dive-react-perf-debugging/)
[React optimization tips – ITNEXT](https://itnext.io/react-optimization-tips-224c66b4b30d)
[React Rally: Animated -- React Performance Toolbox // Speaker Deck](https://speakerdeck.com/vjeux/react-rally-animated-react-performance-toolbox)
[React is Slow, React is Fast: Optimizing React Apps in Practice](https://medium.com/dailyjs/react-is-slow-react-is-fast-optimizing-react-apps-in-practice-394176a11fba)
[React Training: React, Inline Functions, and Performance](https://reacttraining.com/blog/react-inline-functions-and-performance/)
[React Performance Fixes on Airbnb Listing Pages – Airbnb Engineering & Data Science – Medium](https://medium.com/airbnb-engineering/recent-web-performance-fixes-on-airbnb-listing-pages-6cd8d93df6f4)
[10 Ways to Optimize Your React App’s Performance | by Chidume Nnamdi 🔥💻🎵🎮 | Bits and Pieces](https://blog.bitsrc.io/10-ways-to-optimize-your-react-apps-performance-e5e437c9abce)
[6 tips for better React performance – ITNEXT](https://itnext.io/6-tips-for-better-react-performance-4329d12c126b)
[What to do when your React app feels slow – ITNEXT](https://itnext.io/what-to-do-when-your-react-app-feels-slow-3744c966ddf)
[Render Performance Optimization With React - Adaptive Financial Consulting](https://weareadaptive.com/2020/04/09/render-performance-optimization-react/)
[5 Packages to Optimize and Speed Up Your React App During Development - DEV Community](https://dev.to/nilanth/5-packages-to-optimize-and-speed-up-your-react-app-during-development-4h5f)

[Fix the slow render before you fix the re-render](https://kentcdodds.com/blog/fix-the-slow-render-before-you-fix-the-re-render)
[Before You memo() — Overreacted](https://overreacted.io/before-you-memo/)

[@welldone-software/why-did-you-render - npm](https://www.npmjs.com/package/@welldone-software/why-did-you-render)

[Introducing the React Profiler – React Blog](https://reactjs.org/blog/2018/09/10/introducing-the-react-profiler.html)
[Deep dive with the React DevTools profiler - YouTube](https://www.youtube.com/watch?v=nySib7ipZdk)

[Improve React Performance - Vena Engineering - Medium](https://medium.com/vena-engineering/optimizing-react-rendering-61a10e741edb)
[Performance Optimization Techniques In React - Level Up Coding](https://levelup.gitconnected.com/performance-optimization-techniques-in-react-31dee64c3b5)

[Cache your React event listeners to improve performance.](https://itnext.io/cache-your-react-event-listeners-to-improve-performance-9466e92506b6)
[setState(), shouldComponentUpdate(), And render() Timing In ReactJS](https://www.bennadel.com/blog/2905-setstate-shouldcomponentupdate-and-render-timing-in-reactjs.htm)
[shouldComponentUpdate() Will Short-Circuit An Entire Subtree Of Components In ReactJS](https://www.bennadel.com/blog/2904-shouldcomponentupdate-will-short-circuit-an-entire-subtree-of-components-in-reactjs.htm)

#### Hook perf

[Improve React App Performance Through Memoization – Bits and Pieces](https://blog.bitsrc.io/improve-react-app-performance-through-memoization-cd651f561f66)
[React Hooks: Optimizing for performance - ITNEXT](https://itnext.io/optimizing-react-code-with-hooks-3eaaf5978351)
`useMemo()` and `useCallback()` create stable variable that can be used in improving re-render speed
` useCallback(fn, deps)`` is equivalent to `useMemo(() => fn, deps)`.
[React hooks: useCallback and useEffect dependencies - YouTube](https://www.youtube.com/watch?v=L59rOas2AYE)
[use-updating-callbacks - npm](https://www.npmjs.com/package/use-updating-callbacks) use the latest closure

[React.Memo vs Memoize - Better Programming - Medium](https://medium.com/better-programming/react-memo-vs-memoize-71f85eb4e1a)
[React Hooks: Memoization - Sandro Dolidze - Medium](https://medium.com/@sdolidze/react-hooks-memoization-99a9a91c8853)
[When to useMemo and useCallback](https://kentcdodds.com/blog/usememo-and-usecallback)
[`useMemo()` Hooks API Reference – React](https://reactjs.org/docs/hooks-reference.html#usememo)
[`useCallback()` Hooks API Reference – React](https://reactjs.org/docs/hooks-reference.html#usecallback)
[`React.memo()` React Top-Level API – React](https://reactjs.org/docs/react-api.html#reactmemo)

```js
import React, { useState, useCallback } from "react";

function formatCounter(counterVal) {
  return `The counter value is ${counterVal}`;
}
function App() {
  const [counter, setCounter] = useState(0);
  const onClick = useCallback(() => {
    setCounter((prevState) => ++prevState);
  }, []);
  return (
    <div className="App">
      <div>{formatCounter(counter)}</div>
      <button onClick={onClick}>Increment</button>
    </div>
  );
}
```

```js
import React, { useMemo } from "react";
function App({ text }) {
  const [state, setState] = useState(true);
  const someRandomObject = useMemo(
    () => ({
      a: state ? 3 : 4,
      b: !!state,
    }),
    [state]
  );
  return (
    <div className="App">
      <div>{text}</div>
      <button onClick={() => setState(!state)}>Change</button>
    </div>
  );
}
```

### PropTypes

> use TypeScript if you really need PropTypes

Specifying `PropTypes` allows for a clearer contract of your component and React will validate them in dev mode. You should put _all_ props you accessed in `PropTypes` (enforced by [feross/eslint-config-standard-react](https://github.com/feross/eslint-config-standard-react))

`PropTypes` is now a optional dependency.
For type checking use `interface` and TypeScript.

### Using `class`

Syntax for defining React Component:
[React on ES6+ · Babel](http://babeljs.io/blog/2015/06/07/react-on-es6-plus/)
[What React component class syntax should I use? - React Kung Fu](http://reactkungfu.com/2015/07/what-react-component-class-syntax-should-i-use/)

- ES5 `React.createClass()`
- ES6 `extends React.Component` with `constructor()`, `Class.defaultProps` and `.bind(this)`
- ES6 `extends React.Component` with class properties
  It is explained [here](http://reactkungfu.com/2015/07/why-and-how-to-bind-methods-in-your-react-component-classes/) (with reference to JS's function calling and ES6 syntax)
  [How to Use Classes and Sleep at Night — Medium](https://medium.com/@dan_abramov/how-to-use-classes-and-sleep-at-night-9af8de78ccb4#.cln2rrt6t) Your component should only extends from `Component`; use composition.

### Conditional Rendering

[Conditional Rendering – React](https://reactjs.org/docs/conditional-rendering.html)
[8 React conditional rendering methods – LogRocket](https://blog.logrocket.com/conditional-rendering-in-react-c6b0e5af381e)
[Conditional Rendering in React and JSX, the solution](https://medium.com/@BrodaNoel/conditional-rendering-in-react-and-jsx-the-solution-7c80beba1e36)

```js
const Conditional = (props) => {
  return !!props.if && props.children;
};
```

## Non-UI Components

[Draggin' and Droppin' in React | CSS-Tricks](https://css-tricks.com/draggin-and-droppin-in-react/)
[Mastering Drag & Drop with ReactJS - Datorama Engineering](https://engineering.datorama.com/mastering-drag-drop-with-reactjs-part-01-39bed3d40a03)
[Build a Drag and Drop layout builder with React and ImmutableJS](https://medium.com/javascript-in-plain-english/build-a-drag-and-drop-dnd-layout-builder-with-react-and-immutablejs-78a0797259a6) TypeScript, raw HTML events
[How To Use The HTML Drag-And-Drop API In React — Smashing Magazine](https://www.smashingmagazine.com/2020/02/html-drag-drop-api-react/)

[gaearon/react-dnd: Drag and Drop for React](https://github.com/gaearon/react-dnd)
[React DnD Intro for the Redux developer – Medium](https://medium.com/@adamrackis/react-dnd-intro-for-the-redux-developer-d447c2c1577b#.2h4h2niwb)
[Scrabblr — A React game with react-dnd and react-flip-move](https://hackernoon.com/scrabblr-a-react-game-with-react-dnd-and-react-flip-move-40cfaac786e2)

[atlassian/react-beautiful-dnd: Beautiful and accessible drag and drop for lists with React](https://github.com/atlassian/react-beautiful-dnd)
[Beautiful and Accessible Drag and Drop with react-beautiful-dnd from @alexandereardon on @eggheadio](https://egghead.io/courses/beautiful-and-accessible-drag-and-drop-with-react-beautiful-dnd)

[nfl/react-helmet: A document head manager for React](https://github.com/nfl/react-helmet) allows for SSR
[It's All In the Head: Managing the Document Head of a React Powered Site With React Helmet | CSS-Tricks](https://css-tricks.com/its-all-in-the-head-managing-the-document-head-of-a-react-powered-site-with-react-helmet/)

[Converting tables to grids with React compound components - LogRocket Blog](https://blog.logrocket.com/converting-tables-to-grids-with-react-compound-components/) `<LayoutSwitch>`
[KRRISH96/react-layout-switch-blog-example: A Compound Component Example](https://github.com/KRRISH96/react-layout-switch-blog-example/)

[Using "window" the React Way with react-fns ← Alligator.io](https://alligator.io/react/declarative-html5-apis-react-fns/)
[gaearon/react-document-title: Declarative, nested, stateful, isomorphic document.title for React](https://github.com/gaearon/react-document-title)
[gaearon/react-side-effect: Create components whose nested prop changes map to a global side effect](https://github.com/gaearon/react-side-effect)
[ericclemmons/react-resolver: Async rendering & data-fetching for universal React applications.](https://github.com/ericclemmons/react-resolver)
[dleitee/react-fetches: React Fetches a new way to make requests into your REST API's.](https://github.com/dleitee/react-fetches)

### Animation

[React Animation Libraries for 2020 - Bits and Pieces](https://blog.bitsrc.io/react-animation-libraries-for-2020-437a21c73fed)
[5 Ways to animate a React app in 2019. - Dmitry Nozhenko - Medium](https://medium.com/@dmitrynozhenko/5-ways-to-animate-a-reactjs-app-in-2019-56eb9af6e3bf)
[15 个有用的 React 动画库，马上让你的项目变得高大上-技术圈](https://jishuin.proginn.com/p/763bfbd544da)

[Production-Ready Animation Library for React | Framer Motion](https://www.framer.com/motion/)

[Pose | A truly simple animation library for React, React Native, and Vue](https://popmotion.io/pose/)
[Amazing React animation with react-pose - João Miguel Cunha - Medium](https://medium.com/@joomiguelcunha/amazing-react-animation-with-react-pose-3b67d9eb6e07)

[chenglou/react-motion: A spring that solves your animation problems.](https://github.com/chenglou/react-motion)
[animatedjs/animated: Declarative Animations Library for React and React Native](https://github.com/animatedjs/animated)
[FormidableLabs/react-animations: 🎊 A collection of animations for inline style libraries](https://github.com/formidablelabs/react-animations)
[FormidableLabs/react-shuffle: Animated shuffling of child components on change](https://github.com/formidablelabs/react-shuffle)
[aholachek/react-flip-toolkit: A lightweight magic-move library for configurable layout transitions](https://github.com/aholachek/react-flip-toolkit)
[Animating Between Views in React | CSS-Tricks](https://css-tricks.com/animating-between-views-in-react/)

[React Transition Group](https://reactcommunity.org/react-transition-group/)
[reactjs/react-transition-group: An easy way to perform animations when a React component enters or leaves the DOM](https://github.com/reactjs/react-transition-group)

[brunnolou/react-morph: Morphing Ui transitions made simple](https://github.com/brunnolou/react-morph)
[Morphing UI Transitions with React Morph | DigitalOcean](https://www.digitalocean.com/community/tutorials/react-react-morph)

[react-spring](https://react-spring.io/) hook for animation
[pmndrs/react-spring: ✌️ A spring physics based React animation library](https://github.com/pmndrs/react-spring)
[Hooks in react-spring, a tutorial – Paul Henschel – Medium](https://medium.com/@drcmda/hooks-in-react-spring-a-tutorial-c6c436ad7ee4)

[React-Stonecutter](https://dantrain.github.io/react-stonecutter/)

#### Typing

[jstejada/react-typist: Typing animations with React](https://github.com/jstejada/react-typist)
[BraisC/react-text-typist: React component that simulates human typing on a keyboard.](https://github.com/BraisC/react-text-typist)
[haowen737/react-typewriter-hook: ⌨️Use react hooks for typing effect easily](https://github.com/haowen737/react-typewriter-hook)
[typekev/react-mk: A tiny react component which mimics typing](https://github.com/typekev/react-mk)

[Typed.js - Type your heart out](https://mattboldt.github.io/typed.js/)

[How to stop your spinner from jumping in React - DEV Community 👩‍💻👨‍💻](https://dev.to/selbekk/how-to-stop-your-spinner-from-jumping-in-react-5cmp)

### Router

[React Router Mega Demo](http://react-router-mega-demo.herokuapp.com/)

[Building a Router with Raw React](http://jamesknelson.com/routing-with-raw-react/)
[React and pushState: You're doing it wrong](http://jamesknelson.com/push-state-vs-hash-based-routing-with-react-js/)
[Simple Routing with Redux and React](http://jamesknelson.com/simple-routing-redux-react/)

[ReactDOM.render and the Top Level React API | React](http://facebook.github.io/react/blog/2015/10/01/react-render-and-top-level-api.html) you need to call `unmountComponentAtNode()` if you ever change the root component

[You might not need React Router](https://medium.freecodecamp.com/you-might-not-need-react-router-38673620f3d#.opx7tmqtk)

[The Holy Grail of React Router transitions on the web](https://itnext.io/the-holy-grail-of-react-router-transitions-on-the-web-4b29a74861df)

[molefrog/wouter: A minimalistic (~1KB) routing for React. Nothing extra, just HOOKS.](https://github.com/molefrog/wouter)

#### Reach Router

[Reach Router - Overview](https://reach.tech/router)

[Battle of the Routers: Reach Router vs React Router ← Alligator.io](https://alligator.io/react/reach-router-vs-react-router/)

#### React Router

> 201709: all react-router pre-v4 tutorials are obsolete

[React Router: Declarative Routing for React.js](https://reacttraining.com/react-router/) [source](https://github.com/ReactTraining/react-router)
[Leveling Up With React: React Router | CSS-Tricks](https://css-tricks.com/learning-react-router/)

[A guide to using React Router v6 in React apps - LogRocket Blog](https://blog.logrocket.com/react-router-v6/)

[React Router v4: Philosophy and Introduction](https://tylermcginnis.com/react-router-philosophy-introduction/)
[React Router: Declarative Routing for React.js](https://reacttraining.com/react-router/web/guides/philosophy)
[reactjs/react-router: A complete routing solution for React.js](https://github.com/reactjs/react-router) [v4 example](http://codepen.io/pen?template=jyYjeW)
[ReactTraining/react-router: Declarative routing for React](https://github.com/ReactTraining/react-router)
[react-router/blocked-updates.md at master · ReactTraining/react-router](https://github.com/ReactTraining/react-router/blob/master/packages/react-router/docs/guides/blocked-updates.md)

[supasate/connected-react-router: A Redux binding for React Router v4](https://github.com/supasate/connected-react-router)
[react-router/redux.md at master · ReactTraining/react-router](https://github.com/ReactTraining/react-router/blob/master/packages/react-router/docs/guides/redux.md)

React Router 5 introduced Hooks support
[A Complete Beginner's Guide to React Router (Including Router Hooks)](https://www.freecodecamp.org/news/a-complete-beginners-guide-to-react-router-include-router-hooks/amp/)
[The Hooks of React Router | CSS-Tricks](https://css-tricks.com/the-hooks-of-react-router/)

[React Router v4 Unofficial Migration Guide](https://codeburst.io/react-router-v4-unofficial-migration-guide-5a370b8905a) !important
[Using the Link and NavLink Components to Navigate to a Route | Codementor](https://www.codementor.io/packt/using-the-link-and-navlink-components-to-navigate-to-a-route-rieqipp42)
[A Simple React Router v4 Tutorial – Paul Sherman – Medium](https://medium.com/@pshrmn/a-simple-react-router-v4-tutorial-7f23ff27adf)
[Ambiguous Matches with React Router v4](https://tylermcginnis.com/react-router-ambiguous-matches/)
[React Router: How to add child routes - ITNEXT](https://itnext.io/react-router-how-to-add-child-routes-62e23d1a0c5e)

[React Router Tutorial | React For Beginners - YouTube](https://www.youtube.com/watch?v=Law7wfdg_ls)
[Intro to React Router Redux - YouTube](https://www.youtube.com/watch?v=5Knp04GZAj8)
[React Router v4 with Michael Jackson and Ryan Florence - Modern Web - YouTube](https://www.youtube.com/watch?v=Vur2dAFZ4GE)
[Michael Jackson - React Router at react-europe 2015 - YouTube](https://www.youtube.com/watch?v=Q6Kczrgw6ic)

[React Router: Declarative Routing for React.js](https://reacttraining.com/react-router/web/guides/scroll-restoration)
[Automatic scroll restoration in Single Page Applications (SPA) — Childhood Cancer Data Lab](https://www.ccdatalab.org/blog/automatic-scroll-restoration-single-page-applications)

#### other

[acdlite/redux-router: Redux bindings for React Router – keep your router state inside your Redux store](https://github.com/acdlite/redux-router)
[react-router-component :: viewdocs.io](http://strml.viewdocs.io/react-router-component)
[router5/react-router5](https://github.com/router5/react-router5)
[callum/redux-routing: Universal routing built on top of redux](https://github.com/callum/redux-routing)
[FormidableLabs/redux-little-router: A tiny router for Redux that lets the URL do the talking.](https://github.com/FormidableLabs/redux-little-router)

[An Introduction to the Redux-First Routing Model – freeCodeCamp](https://medium.freecodecamp.org/an-introduction-to-the-redux-first-routing-model-98926ebf53cb)
[mksarge/redux-first-routing: A minimal, framework-agnostic API for accomplishing Redux-first routing.](https://github.com/mksarge/redux-first-routing)
[mksarge/redux-json-router: Declarative, Redux-first routing for React/Redux browser applications.](https://github.com/mksarge/redux-json-router)

[flexdinesh/react-render-in-browser: A React component to render browser specific content](https://github.com/flexdinesh/react-render-in-browser)

[MoOx/react-topbar-progress-indicator: `topbar` progress indicator as a React component](https://github.com/MoOx/react-topbar-progress-indicator)
[topbar by buunguyen](https://buunguyen.github.io/topbar/)

### Pure JavaScript

[router5 | HTML5 router for reactive applications](http://router5.github.io/)
[Routie | Javascript hash router](http://projects.jga.me/routie/)
[visionmedia/page.js](https://github.com/visionmedia/page.js)
[tildeio/router.js](https://github.com/tildeio/router.js/)
[glassresistor/i40](https://github.com/glassresistor/i40)
[bevacqua/ruta3](https://github.com/bevacqua/ruta3)
[leeluolee/stateman](https://github.com/leeluolee/stateman)

## UI frameworks

[Design Systems for React Developers | @RisingStack](https://blog.risingstack.com/design-systems-react/)
[The Most Popular React UI Component Libraries in 2022 - SitePoint](https://www.sitepoint.com/popular-react-ui-component-libraries/)
[11 React UI Component Libraries you Should Know in 2019](https://blog.bitsrc.io/11-react-component-libraries-you-should-know-178eb1dd6aa4)
[9 Web Components UI Libraries You Should Know in 2019](https://blog.bitsrc.io/9-web-component-ui-libraries-you-should-know-in-2019-9d4476c3f103)
[Top 7 UI libraries and kits for React - LogRocket Blog](https://blog.logrocket.com/top-7-ui-libraries-and-kits-for-react/)
[React UI Kits - DEV Community 👩‍💻👨‍💻](https://dev.to/kayis/react-ui-kits-3fm2)
[React UI Roundup](https://react-ui-roundup.dimitrimitropoulos.com/)

[Material UI - Material Design React Components](http://material-ui.com/)
[Elegant UX in React with Material-UI ← Alligator.io](https://alligator.io/react/material-ui/)
[The definitive guide to React Material – LogRocket](https://blog.logrocket.com/the-definitive-guide-to-react-material-d730c8a3e8ba) 1.0
[Develop for the Web - Material Design](https://material.io/develop/web/)[Materialize](http://materializecss.com/)
[react-md](https://react-md.mlaursen.com/)

[React Bootstrap](http://react-bootstrap.github.io/)
[React Bootstrap with Material Design - Powerful and free UI KIT - Material Design for Bootstrap](https://mdbootstrap.com/docs/react)
[reactstrap - React Bootstrap 4 components](https://reactstrap.github.io/)

[Chakra UI - A simple, modular and accessible component library that gives you the building blocks you need to build your React applications. - Chakra UI](https://chakra-ui.com/)

[Ant Design - The world's second most popular React UI framework](https://ant.design/)
[Ant Design of React - Ant Design](https://ant.design/docs/react/introduce)
[Ant Design of Vue - Ant Design Vue](https://vue.ant.design/docs/vue/introduce/)

[PrimeReact](https://www.primefaces.org/primereact/showcase/#/)

[Sanity UI: A composable, accessible, beautiful React component library](https://www.sanity.io/blog/streamline-your-studio-development-with-sanity-ui)

[Reach UI](https://reach.tech/)

[Rebass](https://rebassjs.org/) UI components for React

[React Suite | React components](https://rsuitejs.com/en/)

[Blueprint – A React-based UI toolkit for the web](https://blueprintjs.com/)

[PatternFly 4](https://www.patternfly.org/v4/)

[Grommet v2](https://v2.grommet.io/) Styled components for Reactjs
[Belle - Configurable React Components with great UX](http://nikgraf.github.io/belle/)

[Anypoint Components](http://ux.mulesoft.com/#/)
[Atlaskit by Atlassian](https://atlaskit.atlassian.com/) mostly APL
[Shopify Polaris](https://polaris.shopify.com/)
[Base Web - Base Web React Components](https://baseweb.design/) by Uber

[create-react-app & Tailwind CSS – Mike Francis – Medium](https://medium.com/@mikeeeeeeey/create-react-app-tailwind-css-feat-postcss-631d9e33ba8c)
[Steps to setup Tailwind with React using POSTCSS – Ajit Singh – Medium](https://medium.com/@ajitid/steps-to-setup-tailwind-with-react-using-postcss-66147b93f5f4)

[Material Design Color, Flat Colors, Icons, Color Palette | Material UI](https://www.materialui.co/)

[Home - Office UI Fabric](https://developer.microsoft.com/en-us/fabric/#/controls/web)
[OfficeDev/office-ui-fabric-react: React components for building Microsoft web experiences.](https://github.com/OfficeDev/office-ui-fabric-react)

[Evergreen](https://evergreen.segment.com/) not responsive as of v4
[React Materialize](https://react-materialize.github.io/)
[React Desktop | React UI Components for OS X El Capitan and Windows 10](http://reactdesktop.js.org/)

[Semantic UI React](https://react.semantic-ui.com/)
[Getting Started | Semantic UI](https://semantic-ui.com/introduction/getting-started.html)

[plaxdan/react-topcoat](https://github.com/plaxdan/react-topcoat) [plaxdan/react-topcoat-demo](https://github.com/plaxdan/react-topcoat-demo)
[Mesosphere UI Components](http://mesosphere.github.io/reactjs-components/)

### Headless UI

[Headless UI – Unstyled, fully accessible UI components](https://headlessui.dev/) from Tailwind Labs, a11y

[tailwindlabs/headlessui: Completely unstyled, fully accessible UI components, designed to integrate beautifully with Tailwind CSS.](https://github.com/tailwindlabs/headlessui/)
[@headlessui/react Menu Example - CodeSandbox](https://codesandbox.io/s/headlessuireact-menu-example-b6xje?file=/src/App.js)

### Reakit

[Reakit – Toolkit for building accessible UIs](https://reakit.io/) a11y

## UI widgets

[9 React Styled-Components UI Libraries for 2019 - Bits and Pieces](https://blog.bitsrc.io/9-react-styled-components-ui-libraries-for-2018-4e1a0bd3e179)
[10 Useful React Components for 2020 - Bits and Pieces](https://blog.bitsrc.io/10-useful-react-components-for-2020-35fd6af56909)
[jquense/react-widgets: An à la carte set of polished, extensible, and accessible inputs built for React](https://github.com/jquense/react-widgets)

[JedWatson-react-hammerjs · GitHub](https://github.com/JedWatson/react-hammerjs)

[Lapple-react-transitive-number · GitHub](https://github.com/Lapple/react-transitive-number)
[React Color](http://casesandberg.github.io/react-color/)
[react-component/slider](https://github.com/react-component/slider/)
[react-overlays](http://react-bootstrap.github.io/react-overlays/examples/)
[React-Waypoint](http://brigade.github.io/react-waypoint/) Scrollspy
[Flipboard/react-canvas: High performance <canvas> rendering for React components](https://github.com/Flipboard/react-canvas)
[RxMarbles: Interactive diagrams of Rx Observables](http://rxmarbles.com/)
[react-ui-tree](https://pqx.github.io/react-ui-tree/)
[wwayne/react-tooltip: react tooltip component](https://github.com/wwayne/react-tooltip)
[shoumma/organigram: A JSON based tree structure with drag and drop functionally to re-arrange the tree.](https://github.com/shoumma/organigram)
[wojtekmaj/react-calendar: Ultimate calendar for your React app.](https://github.com/wojtekmaj/react-calendar)
[amarofashion/react-credit-cards: Beautiful credit cards for your payment forms](https://github.com/amarofashion/react-credit-cards#readme)

spinners:
[React Spinners](https://www.davidhu.io/react-spinners/)
[How I Created My Own React Spinners Library - DEV Community 👩‍💻👨‍💻](https://dev.to/joshk2/how-i-created-my-own-react-spinners-library-4ckn)
[react-spinners-css by joshk · Bit](https://bit.dev/joshk/react-spinners-css)
[react-spinners-kit](https://dmitrymorozoff.github.io/react-spinners-kit/)
[react-loader-spinner - npm](https://www.npmjs.com/package/react-loader-spinner)
[wdtLoading - Application Loading Screen](https://ned.im/wdtLoading/)
[fakiolinho/react-loading: React component for loading animations](https://github.com/fakiolinho/react-loading)

[react-window](https://react-window.now.sh) reimplementation of react-virtualized, not all the features
[React Virtual Window - virtualise anything for a performance boost! - DEV Community](https://dev.to/miketalbot/react-virtual-window-virtualise-anything-for-a-performance-boost-full-tutorial-3moe)
[react-virtualized](https://bvaughn.github.io/react-virtualized/#/components/List)
[Performant Lists in React with react-window ← Alligator.io](https://alligator.io/react/lists-with-react-window/)
[AddyOsmani.com - Rendering large lists with react-window](https://addyosmani.com/blog/react-window/)
[Windowing wars: React-virtualized vs. react-window - LogRocket Blog](https://blog.logrocket.com/windowing-wars-react-virtualized-vs-react-window/)
[Creating More Efficient React Views with Windowing - ForwardJS San Francisco - YouTube](https://www.youtube.com/watch?v=t4tuhg7b50I) [slides](https://bvaughn.github.io/forward-js-2017/)
[clauderic/react-tiny-virtual-list: A tiny but mighty 3kb list virtualization library, with zero dependencies 💪 Supports variable heights/widths, sticky items, scrolling to index, and more!](https://github.com/clauderic/react-tiny-virtual-list)
[react-eternal-list](https://react-eternal-list.rinas.in/)
[How I Rendered a Massive List in React Without Memory and CPU Issues](https://medium.com/better-programming/how-i-rendered-a-massive-list-in-react-without-memory-and-cpu-issues-7ac6fe6a697b)

[balloob/react-sidebar: A sidebar component for React](https://github.com/balloob/react-sidebar)

[SortableJS/react-sortablejs: React bindings for SortableJS](https://github.com/SortableJS/react-sortablejs)

modal:
[Boron](http://madscript.com/boron/) (modal)
[reactjs/react-modal: Accessible modal dialog component for React](https://github.com/reactjs/react-modal)

image loader:
[glslio/diaporama-react](https://github.com/glslio/diaporama-react) [gre/diaporama](https://github.com/gre/diaporama) [Diaporama: Examples](http://greweb.me/diaporama/) image/video/content slideshow engine
[jide/react-imageblurloader](https://github.com/jide/react-imageblurloader)

Editor:
[Let’s build a customizable rich text editor with Slate and React](https://medium.com/@wesharehoodies/lets-build-a-customizable-rich-text-editor-with-slate-and-react-beefd5d441f2)
[Draft.js · Rich Text Editor Framework for React](https://draftjs.org/)
[Slate](https://www.slatejs.org/#/rich-text)
[React Markings - @thejameskyle](http://thejameskyle.com/react-markings) Markdown <> Component
[react-markdown - npm](https://www.npmjs.com/package/react-markdown)
[needim/minibed: It's a mini editable, customizable playground for web](https://github.com/needim/minibed)

> see wordpress.md#wordpress-gutenberg`

Context Menu:
[React ContextMenu](https://vkbansal.github.io/react-contextmenu/#/)

Date picker:
[13 React DatePickers and TimePickers for 2020 | by Jonathan Saring | Bits and Pieces](https://blog.bitsrc.io/13-react-time-and-date-pickers-for-2020-d52d88d1ca0b)
[YouCanBookMe/react-datetime](https://github.com/YouCanBookMe/react-datetime)
[quri/react-bootstrap-datetimepicker](https://github.com/quri/react-bootstrap-datetimepicker)
[Hacker0x01/react-datepicker](https://github.com/Hacker0x01/react-datepicker)
[react-widgets DateTimePicker](http://jquense.github.io/react-widgets/api/DateTimePicker/)
[jquense/react-big-calendar: gcal/outlook like calendar component](https://github.com/jquense/react-big-calendar)

Layout:
[wmira/react-panel](https://github.com/wmira/react-panel) (portal panels)
[react-burger-menu](http://negomi.github.io/react-burger-menu/)
[ReactFitText Test Page](http://softwarepsychonaut.com/react-fittext/)
[React Data Grid · Excel-like data grid component built with React](https://adazzle.github.io/react-data-grid/)
[react-animated-burgers - npm](https://www.npmjs.com/package/react-animated-burgers)

Accordion:
[daviferreira/react-sanfona](https://github.com/daviferreira/react-sanfona)
[React Tabbordion Component Demo](http://merri.github.io/react-tabbordion/)

Tabs:
[React-Tabs](https://reactcommunity.org/react-tabs/)
[reactjs/react-tabs: An accessible and easy tab component for ReactJS.](https://github.com/reactjs/react-tabs)

Table:
[Griddle - React Grid Component](http://griddlegriddle.github.io/Griddle/)
[STRML-react-grid-layout · GitHub](https://github.com/STRML/react-grid-layout)
[vaheqelyan/react-keyview: React components to display the list, table, and grid, without scrolling, use the keyboard keys to navigate through the data](https://github.com/vaheqelyan/react-keyview)
[The top React table libraries to use in 2021 - LogRocket Blog](https://blog.logrocket.com/the-top-react-table-libraries-to-use-in-2021/)
[tannerlinsley/react-table: ⚛️ Hooks for building fast and extendable tables and datagrids for React](https://github.com/tannerlinsley/react-table)
[ag-Grid: Datagrid packed with features that your users need with the performance you expect.](https://www.ag-grid.com/)

### Image Slider

[femioladeji/react-slideshow: A react component for image slideshow supporting slide, fade and zoom](https://github.com/femioladeji/react-slideshow#readme)  
[Pau1fitz/react-slidez: React Slideshow Component ➡️ ⬅️ ⬆️ ⬇️](https://github.com/pau1fitz/react-slidez)  
[Carousel | Bulma-Extensions](https://wikiki.github.io/components/carousel/)

[React Pretty Carousel](https://react-pretty-carousel.herokuapp.com/)
[Jaagrav/react-pretty-carousel: Easily add beautiful carousels to your website in no time!](https://github.com/Jaagrav/react-pretty-carousel)
[Create beautiful carousels or Image Sliders on React with this framework - DEV Community](https://dev.to/jaagrav/create-beautiful-carousels-or-image-sliders-on-react-with-this-framework-4hm1)

[React-carousel](https://brainhubeu.github.io/react-carousel/) powerful transition and customization
[brainhubeu/react-carousel: A pure extendable React carousel, powered by Brainhub (craftsmen who ❤️ JS)](https://github.com/brainhubeu/react-carousel)

[React Slider Carousel Component - react-awesome-slider](https://caferati.me/demo/react-awesome-slider) powerful transition and customization
[rcaferati/react-awesome-slider: React content transition slider. Awesome Slider is a 60fps, light weight, performant component that renders an animated set of production ready UI general purpose sliders. 🖥️ 📱](https://github.com/rcaferati/react-awesome-slider)

[react-responsive-carousel.js.org](http://react-responsive-carousel.js.org/) decent customization, easy to use
[leandrowd/react-responsive-carousel: React.js Responsive Carousel (with Swipe)](https://github.com/leandrowd/react-responsive-carousel)

[React Slick Documentation](https://react-slick.neostack.com/)  
[slick - the last carousel you'll ever need](http://kenwheeler.github.io/slick/)

[Tiny Slider 2 | tiny-slider](http://ganlanyuan.github.io/tiny-slider/)
[jechav/tiny-slider-react: wrapper of tiny-slider plugin for react.](https://github.com/jechav/tiny-slider-react)
[test tiny-slider-react - CodeSandbox](https://codesandbox.io/s/9l4vq7lxyr)

[A Simple Carousel with Scroll Indicator in React using hooks | by Harshid | auquan | Medium](https://medium.com/auquan/a-simple-carousel-with-scroll-indicator-in-react-using-hooks-f6f19968f390)

### Notification

[React Toastify](https://fkhadra.github.io/react-toastify/)
[React-toastify v8 is live - DEV Community](https://dev.to/fkhadra/react-toastify-v8-is-live-4bal)

[Super easy: Custom Toast message manager with React (and TypeScript) | by Dayan Petrow | Medium](https://dayanpetrow.medium.com/super-easy-custom-toast-message-manager-with-react-and-typescript-c9b8bfb714af)

[Beautiful, Zero Configuration, Toast Messages | CogoToast](https://cogoport.github.io/cogo-toast/) DEPRECATED?
[Cogoport/cogo-toast: Beautiful, Zero Configuration, Toast Messages for React. Only ~ 4kb gzip, with styles and icons](https://github.com/Cogoport/cogo-toast)

[Home - NOTY - a dependency-free notification library](https://ned.im/noty/#/) DEPRECATED
[Notifications in React JS using Noty](https://blog.praveen.science/notifications-in-react-js-using-noty/)

### Forms

> I would like a library that have field error and form error

[Learn React.js: Ridiculously Simple Forms](http://jamesknelson.com/learn-raw-react-ridiculously-simple-forms/)
[white-river-tl7fs - CodeSandbox](https://codesandbox.io/s/white-river-tl7fs) without any library

[jamesknelson/govern: Component-based state management for JavaScript.](https://github.com/jamesknelson/govern)
[Sensible React Forms, with Govern - James K Nelson](http://jamesknelson.com/sensible-react-forms-with-govern/)
[Component-based state management for React - James K Nelson](http://jamesknelson.com/component-based-state-management-react/)

[NewOldMax/react-material-ui-form-validator: Simple validator for forms designed with material-ui components.](https://github.com/NewOldMax/react-material-ui-form-validator)

[Formatting form inputs with Cleave.js and React - LogRocket Blog](https://blog.logrocket.com/formatting-form-inputs-with-cleave-js-and-react/)

#### Select/Multiselect

[The Best React Autocomplete Libraries](https://retool.com/blog/react-autocomplete-libraries/)

[JedWatson/react-select: The Select Component for React.js](https://github.com/JedWatson/react-select) [React-Select Example](http://jedwatson.github.io/react-select/)
[Searchable, Async Dropdowns in React Using React-Select ← Alligator.io](https://alligator.io/react/react-select/)
[CanopyTax/cpr-select](https://github.com/CanopyTax/cpr-select)
[CanopyTax/cpr-multiselect](https://github.com/CanopyTax/cpr-multiselect)
[react-widgets Multiselect](http://jquense.github.io/react-widgets/api/Multiselect/)

Downshift:
[paypal/downshift: 🏎 Primitive to build simple, flexible, WAI-ARIA compliant enhanced input React components](https://github.com/paypal/downshift)
[Downshift - Storybook](http://downshift.netlify.com/?selectedKind=Examples&selectedStory=basic&full=0&addons=1&stories=1&panelRight=0)
[kentcdodds/downshift-examples: Created with CodeSandbox](https://github.com/kentcdodds/downshift-examples)
[react-widgets DropdownList](http://jquense.github.io/react-widgets/api/DropdownList/)
[5 Most Common Dropdown Use Cases Solved with React Downshift ― Scotch](https://scotch.io/tutorials/5-most-common-dropdown-use-cases-solved-with-react-downshift)

[moroshko/react-autosuggest: WAI-ARIA compliant React autosuggest component](https://github.com/moroshko/react-autosuggest)

[Create a Rich Text Box with Autocomplete | Autocomplete | Algolia](https://www.algolia.com/doc/ui-libraries/autocomplete/guides/creating-a-rich-text-box-with-mentions-and-hashtags/)
[So, You Want to Build an @mention Autocomplete Feature? - CSS-Tricks](https://css-tricks.com/so-you-want-to-build-an-mention-autocomplete-feature/)
[What Is Autocomplete? | Autocomplete | Algolia](https://www.algolia.com/doc/ui-libraries/autocomplete/introduction/what-is-autocomplete/)

[React .focus() - The Startup - Medium](https://medium.com/swlh/react-focus-c6ffd4aa42e5)

#### React Hook Form

[Home | React Hook Form - Simple React forms validation](https://react-hook-form.com/)
[Form Builder | React Hook Form - Simple React forms validation](https://react-hook-form.com/form-builder/)
[react-hook-form/examples at master · react-hook-form/react-hook-form](https://github.com/react-hook-form/react-hook-form/tree/master/examples)

[What’s new in React Hook Form V7 - LogRocket Blog](https://blog.logrocket.com/whats-new-in-react-hook-form-v7/)
[Migrate From V6 to V7 | React Hook Form - Simple React forms validation](https://react-hook-form.com/migrate-v6-to-v7/)

[Pain-Free Forms with React Hook Form - Nordschool](https://nordschool.com/react-hook-form/#custom-input-field)
[React Hook Form — An Elegant Solution to Forms in React | by Mahesh Haldar | Bits and Pieces](https://blog.bitsrc.io/react-hook-form-an-elegant-solution-to-forms-in-react-4db64505b0cd)
[Build the Next Generation of Forms With React Hooks Forms](https://medium.com/better-programming/build-the-next-generation-of-forms-with-react-hooks-forms-b4f2039e51c1)
[Chakra UI and React-Hook-Form –How to Build Beautiful Forms](https://www.freecodecamp.org/news/how-to-use-react-hook-form-with-chakra-ui/)

[UseForm - Controller | React Hook Form - Simple React forms validation](https://react-hook-form.com/api/usecontroller/controller) Wrapper component for controlled inputs
[React Hook Form Field Array Advanced with delete, insert, append, edit - CodeSandbox](https://codesandbox.io/s/react-hook-form-field-array-advanced-with-delete-insert-append-edit-l19pz)

[React Hook Form vs. Formik: A technical and performance comparison - LogRocket Blog](https://blog.logrocket.com/react-hook-form-vs-formik-a-technical-and-performance-comparison/)
[React Hook Form VS Formik. A comprehensive comparison of the two… | by Nathan Sebhastian | Bits and Pieces](https://blog.bitsrc.io/react-hook-form-vs-formik-form-builder-library-for-react-23ed559fdae)

#### React Final Form

[React Final Form](https://final-form.org/react/)

#### Hooked-Form

[Hooked-Form · You will get hooked.](https://jovidecroock.github.io/Hooked-Form/)
[JoviDeCroock/Hooked-Form: Performant 2KB React library to manage your forms](https://github.com/JoviDeCroock/hooked-form)

#### React Form

[tannerlinsley/react-form: ⚛️ Hooks for managing form state and validation in React](https://github.com/tannerlinsley/react-form)
[react-form/validation.md at master · tannerlinsley/react-form](https://github.com/tannerlinsley/react-form/blob/master/docs/validation.md)
[react-form/api.md at master · tannerlinsley/react-form](https://github.com/tannerlinsley/react-form/blob/master/docs/api.md)
[react-form/examples.md at master · tannerlinsley/react-form](https://github.com/tannerlinsley/react-form/blob/master/docs/examples.md)

#### Formik

> does have Hook API, but design is still pre-hook

[Getting Started | Formik](https://formik.org/docs/overview)
[formium/formik: Build forms in React, without the tears 😭](https://github.com/formium/formik)
[Tear-Free Forms with React and Formik ← Alligator.io](https://alligator.io/react/forms-with-react-and-formik/) with Yup (Joi-like) schema
[An imperative guide to forms in React – LogRocket](https://blog.logrocket.com/an-imperative-guide-to-forms-in-react-927d9670170a)
[The Joy of Forms with React and Formik | Keyhole Software](https://keyholesoftware.com/2017/10/23/the-joy-of-forms-with-react-and-formik/) using `<Field>`
[No more tears, handling Forms in React using Formik, part I](https://itnext.io/no-more-tears-handling-forms-in-react-using-formik-part-i-55f1400a75ba)
[Simple React form validation with Formik, Yup and/or Spected](https://itnext.io/simple-react-form-validation-with-formik-yup-and-or-spected-206ebe9e7dcc)
[Forms with Formik + TypeScript - fotonTech - Medium](https://medium.com/fotontech/forms-with-formik-typescript-d8154cc24f8a)
[Formik Example - CodeSandbox](https://codesandbox.io/s/zkrk5yldz)

#### Formsy React

[formsy/formsy-react: A form input builder and validator for React JS](https://github.com/formsy/formsy-react)
[twisty/formsy-react-components: Bootstrap components for a formsy-react form.](https://github.com/twisty/formsy-react-components)

#### Inactive

[Final Form](https://final-form.org/)
[final-form/final-form: 🏁 Framework agnostic, high performance, subscription-based form state management](https://github.com/final-form/final-form)

[React Formal](http://jquense.github.io/react-formal/) yup validation, common message for multiple fields (form error)

[arqex/react-json](https://github.com/arqex/react-json) JSON editor

[Redux Form - Redux Form](https://redux-form.com/)
[erikras/redux-form](https://github.com/erikras/redux-form)

## Components Repo

[11 React UI Component Libraries you Should Know in 2019](https://blog.bitsrc.io/11-react-component-libraries-you-should-know-178eb1dd6aa4)
[11 React UI Component Playgrounds for 2019 - Bits and Pieces](https://blog.bitsrc.io/11-react-ui-component-playgrounds-for-2018-eef5a87a1bf8)
[19 Open Source React Component Libraries to use in your next project - David Wells](https://davidwells.io/blog/19-open-source-react-component-libraries-to-use-in-your-next-project)

[React Components](http://react-components.com/)
[react-component · GitHub](https://github.com/react-component)
[Latest ReactJS Examples](http://react.rocks/)
[React.parts – A catalog of React components](https://react.parts/web)
[JS.coach](https://js.coach/)
[www.reactjsx.com](http://www.reactjsx.com/)
[brillout/awesome-react-components: Catalog of React Components & Libraries](https://github.com/brillout/awesome-react-components)
[23 Best React UI Component Libraries And Frameworks](https://hackernoon.com/23-best-react-ui-component-libraries-and-frameworks-250a81b2ac42)
[13 Top React Component Libraries for 2020 - Bits and Pieces](https://blog.bitsrc.io/13-top-react-component-libraries-for-2020-488cc810ca49)

[Share reusable code components as a team · Bit](https://bit.dev/)
[15 Reasons to Build Your Component Library in Bit.dev](https://blog.bitsrc.io/15-reasons-to-build-your-component-library-in-bit-dev-93a514878863)
[React Component Patterns – gitconnected | Become a Better Developer](https://levelup.gitconnected.com/react-component-patterns-ab1f09be2c82)
[How to Achieve Reusability with React Components – WalmartLabs – Medium](https://medium.com/walmartlabs/how-to-achieve-reusability-with-react-components-81edeb7fb0e0)
[How to Write Cleaner React Code](https://www.freecodecamp.org/news/how-to-write-cleaner-react-code/)
[Approaches to testing React components - an overview - React Kung Fu](http://reactkungfu.com/2015/07/approaches-to-testing-react-components-an-overview/)
`bit.dev`
[3 Ways to Build Your Own React Component Library - Bits and Pieces](https://blog.bitsrc.io/3-ways-to-build-your-own-react-component-library-b4d00013a716)
[Building a React Component Library — The Right Way | by Eden Ella | Bits and Pieces](https://blog.bitsrc.io/building-a-react-component-library-d92a2da8eab9)
[How To Share React UI Components Between Projects And Apps](https://blog.bitsrc.io/how-to-easily-share-react-components-between-projects-3dd42149c09)
[How Do We Really Use Reusable Components? – Bits and Pieces](https://blog.bitsrc.io/do-we-really-use-reusable-components-959a252a0a98)

[React Cosmos](https://reactcosmos.org/) Sandbox for developing and testing
UI components in isolation

[How I share React components between projects - JavaScript in Plain English - Medium](https://medium.com/javascript-in-plain-english/how-i-share-react-components-between-projects-3896d853cbee)
[teambit/bit: Easily share code between projects with your team.](https://github.com/teambit/bit)
[Maximizing Code Reuse in React - Bits and Pieces](https://blog.bitsrc.io/maximizing-code-reuse-in-react-35ee20ad362c)

[Building Reusable React UI Components with styled-components](https://blog.bitsrc.io/building-reusable-react-ui-components-with-styled-components-290686648004)

## Components Tutorial

[FREE Advanced React.js Patterns | React Training](https://courses.reacttraining.com/p/advanced-react-free)
[Best Practices on building a UI component library for your company (David Wells) - FSF 2016 - YouTube](https://www.youtube.com/watch?v=j8eBXGPl_5E) Webpack pipeline, PostCSS
[Kent C Dodds - Simply React - YouTube](https://www.youtube.com/watch?v=AiJ8tRRH0f8)
[7 tips to publish your React components - arqex](http://arqex.com/1072/7-tips-to-publish-your-react-components)

[Commonly Used UI Components In React - DEV Community 👩‍💻👨‍💻](https://dev.to/flippedcoding/commonly-used-ui-components-in-react-5elh)
[How to Build Faster with Reusable UI Components in React](https://codeburst.io/how-to-build-faster-with-reusable-ui-components-in-react-482397dec818)
[8 Tips for Building Awesome Reusable React Components | by Eden Ella | Bits and Pieces](https://blog.bitsrc.io/9-tips-for-building-awesome-reusable-react-components-b91f4846a30a)
[Quick Front-End Integrations Through Bit Components | by Jonathan Saring | Bits and Pieces](https://blog.bitsrc.io/quick-front-end-integrations-through-components-739625e7069d)

[Building React-Select | Jed Watson - YouTube](https://www.youtube.com/watch?v=yS0jUnmBujE)
[How to Scale a React Component - Jed Watson at React Conf 2019](https://www.infoq.com/news/2020/02/reactconf2019-react-select-scale/)

[Building Timers in React: Stopwatch and Countdown - Peter Durham - Medium](https://medium.com/@peterjd42/building-timers-in-react-stopwatch-and-countdown-bc06486560a2)

[Rinse React](https://rinsejs.io/)
[cwlsn/rinse-react: 🚿 Rinse, React, repeat. A boilerplate to build a React component library.](https://github.com/cwlsn/rinse-react)
[How to Write Your Own Reusable React Component Library](https://itnext.io/how-to-write-your-own-reusable-react-component-library-a57dc7c9a210)

[How to Create a Modal in React - DEV Community](https://dev.to/franciscomendes10866/how-to-create-a-modal-in-react-3coc)

[Building a Tabs Component with React ← Alligator.io](https://alligator.io/react/tabs-component/)
[Global Snackbars in React with Redux, and Material UI](https://browntreelabs.com/snackbars-in-react-redux-and-material-ui/)
[Pure React Modal with Transition Events & Styled Components](https://medium.com/@lucksp_22012/pure-react-modal-6e562a317b85)

[Building an Accordion Component with React ← Alligator.io](https://alligator.io/react/react-accordion-component/)
[Build a React Accordion Component from Scratch Using React Hooks](https://medium.com/skillthrive/build-a-react-accordion-component-from-scratch-using-react-hooks-a71d3d91324b)
[https://react-bootstrap.github.io/components/accordion/](https://react-bootstrap.github.io/components/accordion/)
[Accordion - Semantic UI React](https://react.semantic-ui.com/modules/accordion/)

[Fullstack React 🐬: How to Write a Google Maps React Component](https://www.fullstackreact.com/articles/how-to-write-a-google-maps-react-component)

[Using ReactJS and KendoUI Together](http://ifandelse.com/using-reactjs-and-kendoui-together/)

[React - how to make left-side animated menu - DEV Community](https://dev.to/dirask/react-how-to-make-left-side-animated-menu-15l6)
[Hamburger Menu with a Side of React Hooks and Styled Components | CSS-Tricks](https://css-tricks.com/hamburger-menu-with-a-side-of-react-hooks-and-styled-components/)
[React Styled Components — Hooks, Refs, and Security](https://levelup.gitconnected.com/react-styled-components-hooks-refs-and-security-281fb8ab0341)

[Simple Image Upload with React - codeburst](https://codeburst.io/react-image-upload-with-kittens-cc96430eaece)

[How create ⚛️ React Swiper Slider - easy tutorial 👨‍🏫 - DEV Community](https://dev.to/kerthin/how-create-react-swiper-slider-easy-tutorial-51il)

[How to create email chips in pure React - freeCodeCamp.org - Medium](https://medium.com/free-code-camp/how-to-create-email-chips-in-pure-react-ad1cc3ecea16)

[Implement Tree view component with ReactJS and Styled-Components](https://medium.com/@davidtranwd/implement-tree-view-component-with-reactjs-and-styled-components-5eea3b1603cf)

[How To Build a Color Picker with React - Level Up Coding](https://levelup.gitconnected.com/how-to-build-a-color-picker-5fbacc54f16c)

[React Charts Examples](https://react-charts.js.org/)
[tannerlinsley/react-charts: ⚛️ Fast & simple charts for React](https://github.com/tannerlinsley/react-charts)

[Render Abstract Syntax Trees with React - DEV Community 👩‍💻👨‍💻](https://dev.to/codejamninja/render-abstract-syntax-trees-with-react-349j)
[codejamninja/react-ast: render abstract syntax trees with react](https://github.com/codejamninja/react-ast)

[Animating with React, Redux, and d3 - A geek with a hat](https://swizec.com/blog/animating-with-react-redux-and-d3/swizec/6775)
[How to Make a Piechart using React and d3 - A geek with a hat](https://swizec.com/blog/how-to-make-a-piechart-using-react-a`nd-d3/swizec/6785)
[Tiny React & D3 flamegraph tutorial - A geek with a hat](https://swizec.com/blog/tiny-react-d3-flamegraph-tutorial/swizec/8440)

### Building Components

[create-react-app/package.json at master · facebook/create-react-app](https://github.com/facebook/create-react-app/blob/master/package.json) top level linting
[Building a Multi-CRA using Lerna and Monorepo - The Startup - Medium](https://medium.com/swlh/building-a-multi-cra-using-lerna-and-monorepo-4628de405c6b) Storybook usage, quite complicated setup
[Zero-Config Monorepo for a React Component Library in 2019](https://medium.com/@MattBlackDev/zero-config-monorepo-for-a-react-component-library-in-2019-dd9137bdd0a6) yarn + microbundle + babel
[philipp-spiess/react-recomponent: 🥫 Reason-style reducer components for React using ES6 classes.](https://github.com/philipp-spiess/react-recomponent) microbundle + babel
[Making of a component library for React - By](https://hackernoon.com/making-of-a-component-library-for-react-e6421ea4e6c7) Rollup + Babel
[How to create a React component and publish it on NPM](https://medium.com/@BrodaNoel/how-to-create-a-react-component-and-publish-it-in-npm-668ad7d363ce) Webpack + Babel
[Bootstrapping a React library with Parcel Bundler - DEV Community 👩‍💻👨‍💻](https://dev.to/jdmg94/bootstrapping-a-react-library-with-parcel-bundler-4l50) Parcel + Babel
[CREATE LIBRARY OF REACT COMPONENT - DEV Community 👩‍💻👨‍💻](https://dev.to/arpitjain_in/create-library-of-react-component-1fa8) CRA + Babel
[Building a React component as an NPM module - recraftrelic - Medium](https://medium.com/recraftrelic/building-a-react-component-as-a-npm-module-18308d4ccde9) Babel + CRA test app
[5 Ways to Document React Components in 2020 - Bits and Pieces](https://blog.bitsrc.io/5-ways-to-document-react-components-in-2020-ecf60f24dee8)

[helloitsjoe/react-hooks-compose: Decouple Hooks from the presentational components that use them](https://github.com/helloitsjoe/react-hooks-compose) Webpack (webpack-simple)
[webpack-simple/template at master · vuejs-templates/webpack-simple](https://github.com/vuejs-templates/webpack-simple/tree/master/template)

[reactjs/react-docgen: A CLI and toolbox to extract information from React component files for documentation generation purposes.](https://github.com/reactjs/react-docgen)

### Styleguidist

[React Styleguidist: isolated React component development environment with a living style guide](https://react-styleguidist.js.org/)

[Setup a React Component Library using Create React App, React Styleguidist and TypeScript | Codementor](https://www.codementor.io/mukuljainx/setup-a-react-component-library-using-create-react-app-react-styleguidist-and-typescript-vnmi6rdky)

### Storybook

[Storybook - UI dev environment you'll love to use](https://storybook.js.org/)
[Addons | Storybook](https://storybook.js.org/addons/)
[Storybook Tutorials](https://www.learnstorybook.com/)
[The Storybook Story – Storybook – Medium](https://medium.com/storybookjs/the-storybook-story-dd3c1ab0d2ce)
[Storybook for React](https://storybook.js.org/docs/guides/guide-react/)
[Getting Started with Storybook in React](https://geekflare.com/storybook-in-react/)

[storybooks/storybook: Interactive UI component dev & test: React, React Native, Vue, Angular, Ember](https://github.com/storybooks/storybook)
Component Story Format

[Component-Driven Development Using Storybook | recallact.com](https://www.recallact.com/presentation/component-driven-development-using-storybook)

[Using Storybook to develop React components faster - LogRocket Blog](https://blog.logrocket.com/using-storybook-to-develop-react-components-faster/)
[How to use Storybook with React - DEV Community 👩‍💻👨‍💻](https://dev.to/tducasse/how-to-use-storybook-with-react-10g1)
[Documenting React Components With Storybook - DEV Community 👩‍💻👨‍💻](https://dev.to/emmawedekind/documenting-react-components-with-storybook-4h3b)
[Reactjs Unit Testing with Storybook + Jest - CloudBoost](https://blog.cloudboost.io/reactjs-unit-testing-with-storybook-jest-2c3ac5ff37ba)
[How To Build a UI Component with React and Storybook | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-build-a-ui-component-with-react-and-storybook)

#### Examples

[gumdrops.gumgum.com - Storybook](https://gumdrops.gumgum.com)
[gumgum/gumdrops: GumGum's React Reusable Component Library](https://github.com/gumgum/gumdrops)

[storybook.netlify.com - Storybook](https://storybook.netlify.com)

[storybook.storefrontui.io - Storybook](https://storybook.storefrontui.io/)

[newline-sandbox/react-d3-charts: D3 chart visualizations built with React](https://github.com/newline-sandbox/react-d3-charts)

## JSX: curse or blessing

[JSX | XML-like syntax extension to ECMAScript](http://facebook.github.io/jsx/)

[JSX in Depth | React](http://facebook.github.io/react/docs/jsx-in-depth.html)
[JSX Looks Like An Abomination — JavaScript Scene — Medium](https://medium.com/javascript-scene/jsx-looks-like-an-abomination-1c1ec351a918)
[How I learned to stop worrying and love React](http://firstdoit.com/react-1/)
[React’s JSX: The Other Side of the Coin — Medium](https://medium.com/@housecor/react-s-jsx-the-other-side-of-the-coin-2ace7ab62b98)

[Learn React By Itself -- no JSX, no Flux, no ES6, no Webpack.](http://jamesknelson.com/learn-raw-react-no-jsx-flux-es6-webpack/)
[How I learned to stop worrying and love the JSX - James K Nelson](http://jamesknelson.com/learned-stop-worrying-love-jsx/)

[developit/vhtml: Render JSX/Hyperscript to HTML strings, without VDOM 🌈](https://github.com/developit/vhtml)
[af/JSnoX](https://github.com/af/JSnoX)

JSX must return a _single_ element (use `div` to wrap list).

```
/** @jsx React.DOM */
var HelloMessage = React.createClass({
  render: function() {
    return <div>{'Hello ' + this.props.name}</div>;
  }
});

React.renderComponent(<HelloMessage name="John" />, mountNode);
```

```js
var HelloMessage = React.createClass({
  render: function () {
    return React.DOM.div({ className: "mystyle" }, "Hello " + this.props.name);
  },
});

React.renderComponent(HelloMessage({ name: "John" }), mountNode);
```

JSX don't have loop.

```js
var PostComment = require('component/post-comment');

var Posts = React.createClass({
  render: function() {
    // need to create comments array here
    let comments = this.props.post.comments.map(comment =>
      <PostComment key={comment.id}>{comment.body}</PostComment>
    );
    return (
      <div>
        <h1 class="post-title">this.props.post.title</h1>
        <p>this.props.post.body</p>
        <ul class="post-comments">
          {comments}
        </ul>
      </div>;
    );
  }
});
```

## Testing

[Testing In React, Part 1: Types & Tools | by Bryn Bennett | JavaScript in Plain English](https://javascript.plainenglish.io/testing-in-react-part-1-types-tools-244107abf0c6) React Testing Library -> Jest -> Enzyme -> Cypress

[Testing React applications in 2019 - LogRocket Blog](https://blog.logrocket.com/testing-react-applications-in-2019/)
[Revisiting React Testing in 2019 - codeburst](https://codeburst.io/revisiting-react-testing-in-2019-ee72bb5346f4)
[Test Utilities – React](https://reactjs.org/docs/test-utils.html)
[React testing crash course. Test every aspect of your React app to… | by Gábor Soós | Emarsys Craftlab](https://blog.craftlab.hu/react-testing-crash-course-479f2108e6df)
[Unit testing a React component using Jasmine and Webpack - React Video Tutorial #free @eggheadio](https://egghead.io/lessons/react-unit-testing-a-react-component-using-jasmine-and-webpack)

[react-datetime/datetime-spec.js at master · arqex/react-datetime](https://github.com/arqex/react-datetime/blob/master/tests/datetime-spec.js)

[jquense/teaspoon: A jQuery like API for testing React elements and rendered components.](https://github.com/jquense/teaspoon)

### Jest + Enzyme

Jest as the test runner, assertion library, and mocking library. CRA bundles Jest by default.
Enzyme is created by Airbnb, provide additional testing utilities to interact with React components. It must work with a test runner.

[Jest | Painless JavaScript Unit Testing](https://facebook.github.io/jest/) by Facebook on top of [Jasmine](http://jasmine.github.io/edge/introduction.html)
[Testing your apps like a boss with React.js and Jest - DEV Community 👩‍💻👨‍💻](https://dev.to/softchris/testing-your-apps-like-a-boss-with-react-js-and-jest-1hkh) !important
[Rogelio Guzman - Jest Snapshots and Beyond - React Conf 2017 - YouTube](https://www.youtube.com/watch?v=HAuXJVI_bUs) comparing snapshots of rendered UI
[Test React Components with Enzyme and Jest from @iamtylerwclark on @eggheadio](https://egghead.io/courses/test-react-components-with-enzyme-and-jest)
[Testing React with Jest and Enzyme I - CodeClan - Medium](https://medium.com/codeclan/testing-react-with-jest-and-enzyme-20505fec4675)
[Example of Moving Towards Integration Testing – codeburst](https://codeburst.io/example-of-moving-towards-integration-testing-6662421ae7b2)
[Testing in React with Jest and Enzyme: An Introduction](https://medium.com/@rossbulat/testing-in-react-with-jest-and-enzyme-an-introduction-99ce047dfcf8)
[Test Driven Development in React with Jest and Enzyme](https://medium.com/@rossbulat/test-driven-development-in-react-with-jest-and-enzyme-2a6cf2cc3071)
[babel/babel-jest](https://github.com/babel/babel-jest)

[Jest testing without the noise - DEV Community](https://dev.to/pffigueiredo/jest-testing-without-the-noise-2n8g)

- `npm test -- button.test`
- `npm test -- -t '<testName> OR <testSuiteName>'`
- `.only()`

[Introduction | Enzyme](http://airbnb.io/enzyme/)
[airbnb/enzyme: JavaScript Testing utilities for React](https://github.com/airbnb/enzyme)
[Testing React using Enzyme - Findmypast Tech](http://tech.findmypast.com/testing-react-using-enzyme/)
[Tested React: Build and Test a Form using React Context](https://medium.com/front-end-weekly/tested-react-build-and-test-a-form-using-react-context-81870af6a9ac)

### React Testing Library

[React Testing Library | Testing Library](https://testing-library.com/docs/react-testing-library/intro/)
[Semantic tests with react-testing-library - LogRocket Blog](https://blog.logrocket.com/semantic-tests-with-react-testing-library/)
[React Testing Library Common Scenarios | Rafael Quintanilha](https://rafaelquintanilha.com/react-testing-library-common-scenarios/)
[React Testing Library – Tutorial with JavaScript Code Examples](https://www.freecodecamp.org/news/react-testing-library-tutorial-javascript-example-code/)
[5 Tips to Perfect React Testing Library Queries | by Michael Chang | JavaScript in Plain English](https://javascript.plainenglish.io/5-tips-to-perfect-react-testing-library-queries-ae4e49f27858)
[9 React Testing Library Tips and Tricks | by Paige Niedringhaus | Better Programming](https://betterprogramming.pub/9-react-testing-library-tips-and-tricks-5cce3e458282)
[An in-depth beginner's guide to testing React applications with React Testing Library](https://jkettmann.com/beginners-guide-to-testing-react/)
[Testing components with Jest and React Testing Library](https://itnext.io/testing-components-with-jest-and-react-testing-library-d36f5262cde2)
[React Testing Library – Tutorial with JavaScript Code Examples](https://www.freecodecamp.org/news/react-testing-library-tutorial-javascript-example-code/)
[Testing a simple component with React Testing Library - DEV Community](https://dev.to/mbarzeev/testing-a-simple-component-with-react-testing-library-5bc6)
