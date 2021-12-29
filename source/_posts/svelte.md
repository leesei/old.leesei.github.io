---
title: Svelte
categories:
  - web
tags:
  - svelte
  - javascript
  - frontend
  - web-dev
toc: true
date: 2019-12-16 14:29:04
---

[Svelte • Cybernetically enhanced web apps](https://svelte.dev/)
[Introduction / Basics • Svelte Tutorial](https://svelte.dev/tutorial/basics)
[sveltejs/svelte: Cybernetically enhanced web apps](https://github.com/sveltejs/svelte)

[Svelte 3: Rethinking reactivity](https://svelte.dev/blog/svelte-3-rethinking-reactivity) 2019-04, Svelte 3 announcement
[Rich Harris - Rethinking reactivity - YouTube](https://www.youtube.com/watch?v=AdNJ3fydeao)
Svelte 3 uses JavaScript label (`$:`) to declare computed (reactive) variables which makes the code very intuitive and spreadsheet-like. It also resembles React more.
[Svelte 3 Reaction & QuickStart Tutorial - YouTube](https://www.youtube.com/watch?v=043h4ugAj4c)

Svelte is a _compiler_ for frontend applications.
[Frameworks without the framework: why didn't we think of this sooner?](https://svelte.dev/blog/frameworks-without-the-framework)
[A Guide to the Svelte Framework | Toptal](https://www.toptal.com/front-end/svelte-framework-guide)
[The Philosophy of Svelte](https://blog.scottlogic.com/2021/01/18/philosophy-of-svelte.html)

It does not use virtual-DOM diffing. The generated code requires a thin run-time (think jquery).
Svelte invalidates variables at build time to trigger a re-render. Have built-in:

- scoped styles
- linting (with a11y rules)
- unused CSS removal
- directives (transitions, binding and more)

[Introduction / Basics • Svelte Tutorial](https://svelte.dev/tutorial/basics)
[The Svelte Handbook](https://flaviocopes.com/page/svelte-handbook/)
[Hello world • REPL • Svelte](https://svelte.dev/repl/hello-world?version=3)
[Frameworks without the framework: why didn't we think of this sooner?](https://svelte.dev/blog/frameworks-without-the-framework)

[Truly reactive programming with Svelte 3.0 - LogRocket Blog](https://blog.logrocket.com/truly-reactive-programming-with-svelte-3-0-321b49b75969/)
[The Philosophy of Svelte](https://blog.scottlogic.com/2021/01/18/philosophy-of-svelte.html)
[Why I Moved From React to Svelte and Why Others Will Follow - DZone Web Dev](https://dzone.com/articles/why-i-moved-from-react-to-svelte-and-others-will-f)
[I created the exact same app in Vue and Svelte. Here are the differences.](https://medium.com/javascript-in-plain-english/i-created-the-exact-same-app-in-vue-and-svelte-here-are-the-differences-c649f8d4ce0a)
[Svelte is the most beautiful web framework I've ever seen - DEV Community 👩‍💻👨‍💻](https://dev.to/jesseskinner/svelte-is-the-most-beautiful-web-framework-i-ve-ever-seen-325f)
[Why Svelte won’t kill React. Is status quo to blame for that? Or is… | by Kit Isaev | JavaScript In Plain English | Medium](https://medium.com/javascript-in-plain-english/why-svelte-wont-kill-react-3cfdd940586a)

[First time using Svelte, let's play Tic Tac Toe! - YouTube](https://www.youtube.com/watch?v=S_6ApOagzzM)

[Vercel and Svelte: A Perfect Match for Web Developers – The New Stack](https://thenewstack.io/vercel-and-svelte-a-perfect-match-for-web-developers/) Svelte creator hired by Vercel @2021-12

## Conference

[Svelte Summit Fall 2021 - YouTube](https://www.youtube.com/watch?v=1Df-9EKvZr0&t=12s)

[Rich Harris: Futuristic Web Development - YouTube](https://www.youtube.com/watch?v=qSfdtmcZ4d0&t=937s)

## Actions/Interactivity

[Introduction to Svelte Actions - LogRocket Blog](https://blog.logrocket.com/svelte-actions-introduction/)

## Store

[Stores / Writable stores • Svelte Tutorial](https://svelte.dev/tutorial/writable-stores)
[How to work with props in Svelte](https://flaviocopes.com/svelte-props/)
[Cross-component State Management in Svelte](https://flaviocopes.com/svelte-state-management/)

## SvelteKit

> Server Side Rendering, app framework like Next.js for React

[SvelteKit • The fastest way to build Svelte apps](https://kit.svelte.dev/)
[SvelteKit is in public beta](https://svelte.dev/blog/sveltekit-beta)
[sveltejs/kit: The fastest way to build Svelte apps](https://github.com/sveltejs/kit)

[What's the deal with SvelteKit?](https://svelte.dev/blog/whats-the-deal-with-sveltekit)

## Sapper

> superseded by SvelteKit

[Sapper • The next small thing in web development](https://sapper.svelte.dev/)
[Sapper: Towards the ideal web app framework](https://svelte.dev/blog/sapper-towards-the-ideal-web-app-framework)
App framework for Svelte, with routing, SSR, code-splitting
[sveltejs/sapper: The next small thing in web development, powered by Svelte](https://github.com/sveltejs/sapper)

```sh
# for Rollup
npx degit "sveltejs/sapper-template#rollup" my-app
# for webpack
npx degit "sveltejs/sapper-template#webpack" my-app
cd my-app

npm install
npm run dev & open http://localhost:3000
```
