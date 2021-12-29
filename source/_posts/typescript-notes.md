---
title: TypeScript Notes
date: 2014-12-11 17:04:13
categories:
  - comp.lang
tags:
  - typescript
  - notes
toc: true
---

[TypeScript - JavaScript that scales.](https://www.typescriptlang.org/)
[Playground · TypeScript](http://www.typescriptlang.org/play/)
[TypeScript: Handbook - The TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)

[Documentation · TypeScript](https://www.typescriptlang.org/docs/home.html)
[TypeScript/spec.md at master · Microsoft/TypeScript](https://github.com/Microsoft/TypeScript/blob/master/doc/spec.md)

[What’s new in TypeScript | InfoWorld](https://www.infoworld.com/article/3249607/javascript/whats-new-in-typescript.html)
[Getting started with... TypeScript - Stack Overflow Blog](https://stackoverflow.blog/2021/05/05/getting-started-with-typescript/)

[How TypeScript’s Strict Mode Actually Fixes TypeScript | by Eran Shabi | Better Programming](https://betterprogramming.pub/how-typescripts-strict-mode-actually-fixes-typescript-736ba8108c85)
[Getting Strict With TypeScript. Making your TypeScript code more… | by Jose Granja | Better Programming](https://betterprogramming.pub/getting-strict-with-typescript-2e906b48c0a)

[Learn TypeScript: A Pocketguide Tutorial | Prisma](https://www.prisma.io/blog/learn-typescript-a-pocketguide-tutorial-q329XmXQHUjz)
[Understand Typescript in 5 minutes - Je suis un dev](https://www.jesuisundev.com/en/understand-typescript-in-5-minutes/)
[Tackling TypeScript: Upgrading from JavaScript](https://exploringjs.com/tackling-ts/toc.html)
[TypeScript for Node.js Developers - DEV Community 👩‍💻👨‍💻](https://dev.to/jeremylikness/typescript-for-node-js-developers-16o2) video and repo

[Learn TypeScript - Best TypeScript Tutorials (2021) | gitconnected](https://gitconnected.com/learn/typescript)
[Get Started With Typescript in 2019](https://www.robertcooper.me/get-started-with-typescript-in-2019)
[Get Started With TypeScript — Part 1 - Better Programming - Medium](https://medium.com/better-programming/get-started-with-typescript-part-1-440d2ec9e59)
[Get Started with TypeScript — Part 2 - Better Programming - Medium](https://medium.com/better-programming/get-started-with-typescript-part-2-46cbdd858f69)
[How to learn TypeScript: A resources guide for developers - TechRepublic](https://www.techrepublic.com/article/how-to-learn-typescript-a-resources-guide-for-developers/#ftag=CAD-00-10aag7f)
[Your basic guide to finally understand TypeScript | by Piero Borrelli | JavaScript in Plain English](https://javascript.plainenglish.io/your-basic-guide-to-finally-understand-typescript-f81ab85d2a33)
[Learn TypeScript from the ground up with James Henry](https://typescriptcourses.com/typescript-fundamentals)
[TypeScript for Beginner Programmers](https://ts.chibicode.com/)
[Introduction · TypeScript Deep Dive](https://basarat.gitbooks.io/typescript/)
[Why I Was Wrong About TypeScript (DevReach 2017) - YouTube](https://www.youtube.com/watch?v=w6rdLx2LYz8)
[TYPESCRIPT: How I Learned To Stop Worrying And Trust The Compiler - YouTube](https://www.youtube.com/watch?v=mgTenYbX2Kw)

[Write more readable code with TypeScript 4.4 - LogRocket Blog](https://blog.logrocket.com/typescript-4-4-and-more-readable-code/)
[LogRocket TypeScript Meetup: Write more readable code with TS 4.4 - YouTube](https://www.youtube.com/watch?v=LxZx3ycrxI0)

[Introduction to TypeScript with Josh Goldberg - YouTube](https://www.youtube.com/watch?v=5_RIHHpQcoM&t=17s)
[Introducing TypeScript - SitePoint Premium](https://www.sitepoint.com/premium/courses/introducing-typescript-2933/)
[Introduction to TypeScript - Ultimate Courses™](https://ultimatecourses.com/blog/typescript-introduction)
[Using Typescript with Node JS development project - Javascript Developers - Medium](https://medium.com/tkssharma/using-typescript-with-node-js-development-project-972a1f206f0f)
[What is TypeScript programming? Industrial-strength JavaScript](https://www.infoworld.com/article/2871804/javascript/typescript-industrial-strength-javascript.html)

[How KEEP-87 & Typeclasses will change the way we write Kotlin - QuickBird Studios Blog](https://quickbirdstudios.com/blog/keep-87-typeclasses-kotlin/)

## Commentary

[Statically typed JavaScript via Microsoft TypeScript, Facebook Flow and Google AtScript](http://www.2ality.com/2014/10/typed-javascript.html)
[niieani/typescript-vs-flowtype: Differences between Flowtype and TypeScript -- syntax and usability](https://github.com/niieani/typescript-vs-flowtype)

[How ActionScript foreshadowed TypeScript | by Gary Nelson | JavaScript in Plain English](https://javascript.plainenglish.io/how-actionscript-foreshadowed-typescript-149cdb764de9)

## REPL

[Hopa - zero config CLI that runs JavaScript and TypeScript](https://krasimirtsonev.com/blog/article/hopa-javascript-typescript-runner)
[a7ul/esbuild-node-tsc: Build your Typescript Node.js projects using blazing fast esbuild](https://github.com/a7ul/esbuild-node-tsc)

[TypeStrong/ts-node: TypeScript execution and REPL for node.js](https://github.com/TypeStrong/ts-node)
[Running TypeScript Scripts With Ease with ts-node ← Alligator.io](https://alligator.io/typescript/running-typescript-ts-node/)

## config

[tsconfig.json · TypeScript](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html)
[Compiler Options · TypeScript](https://www.typescriptlang.org/docs/handbook/compiler-options.html) !important

`tsc --init` generates a default `tsconfig.json`
default `tsc` targets ES3, use this `tsconfig.json`

```json
{
  "compilerOptions": {
    "target": "esnext",
    "watch": true
  }
}
```

## Types

[type-challenges/type-challenges: Collection of TypeScript type challenges with online judge](https://github.com/type-challenges/type-challenges)
[Type Challenges Solutions](https://ghaiklor.github.io/type-challenges-solutions/en/)

[Home | DefinitelyTyped](http://definitelytyped.org/) The repository for high quality TypeScript type definitions
[Writing Declaration Files for @types | TypeScript](https://devblogs.microsoft.com/typescript/writing-dts-files-for-types/)

[TypeScript: Documentation - Everyday Types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#differences-between-type-aliases-and-interfaces)
[TypeScript: Documentation - Creating Types from Types](https://www.typescriptlang.org/docs/handbook/2/types-from-types.html)

[unknown vs any in TypeScript](https://dmitripavlutin.com/typescript-unknown-vs-any/)

[TypeScript interface vs. type | pawelgrzybek.com](https://pawelgrzybek.com/typescript-interface-vs-type/)
[type vs interface in TypeScript - DEV Community](https://dev.to/saadsharfuddin/type-vs-interface-in-typescript-35i6)
[Types vs. interfaces in TypeScript - LogRocket Blog](https://blog.logrocket.com/types-vs-interfaces-in-typescript/)

> The only time I use interfaces is to expose types publicly so that the consumer of your code can extend the types if needed, or when implementing with a class.
> when object implementing some interface can have more properties than the interface defines, but types limit the shape to exactly what type has defined.

[TypeScript Interfaces: From Type to Interface - Ultimate Courses™](https://ultimatecourses.com/blog/typescript-interfaces-from-type-to-interface)
[TypeScript Interfaces vs Types - Ultimate Courses™](https://ultimatecourses.com/blog/typescript-interfaces-vs-types)
[Classes vs Interfaces in TypeScript - Ultimate Courses™](https://ultimatecourses.com/blog/classes-vs-interfaces-in-typescript)
4.4 support type guards/type narrowing
Type Guard: boolean value that have implication to type of variables of union type
[Understanding TypeScript: typeof Type Guard - Ultimate Courses™](https://ultimatecourses.com/blog/understanding-typescript-typeof-type-guard)
[Understanding TypeScript: instanceof Type Guard - Ultimate Courses™](https://ultimatecourses.com/blog/understanding-typescript-instanceof-type-guard)
[User defined Type Guards in TypeScript - Ultimate Courses™](https://ultimatecourses.com/blog/user-defined-type-guards-in-typescript)
[TypeScript Literal Type Guards and in Operator - Ultimate Courses™](https://ultimatecourses.com/blog/typescript-literal-type-guards-and-in-operator)
[LogRocket TypeScript Meetup: Write more readable code with TS 4.4 - YouTube](https://www.youtube.com/watch?v=LxZx3ycrxI0)

[A first look at quicktype](http://blog.quicktype.io/first-look/)
[Convert JSON to Swift, C#, TypeScript, Objective-C, Go, Java, C++ and more • quicktype](https://quicktype.io/)

[Infer in TypeScript, the Great and Powerful - DEV Community](https://dev.to/artemmalko/infer-in-typescript-the-great-and-powerful-5cch)

[Type Systems: Structural vs. Nominal typing explained](https://medium.com/@thejameskyle/type-systems-structural-vs-nominal-typing-explained-56511dd969f4)
[Understanding infer in TypeScript - LogRocket Blog](https://blog.logrocket.com/understanding-infer-typescript/)

[From JavaScript to TypeScript Pt. I: Types & Variables ― Scotch](https://scotch.io/tutorials/from-javascript-to-typescript-pt-i-types-variables)
[Introduction to TypeScript Data Types — Tuple, Enum, and Any | by John Au-Yeung | JavaScript in Plain English](https://javascript.plainenglish.io/introduction-to-typescript-data-types-tuple-enum-and-any-7b2ce12b5f20)
[Introduction to TypeScript Data Types (Part 1) | by John Au-Yeung | Better Programming](https://betterprogramming.pub/introduction-to-typescript-data-types-void-null-undefined-never-and-object-types-11eb839e5381)
[Introduction to TypeScript Data Types (Part 2) | by John Au-Yeung | Better Programming](https://betterprogramming.pub/introduction-to-typescript-data-types-numbers-strings-and-objects-2b6eaebd5d66)
[Introduction to TypeScript Interfaces | by John Au-Yeung | Level Up Coding](https://levelup.gitconnected.com/introduction-to-typescript-interfaces-85303aede25d)
[More TypeScript Types You Need To Know Better | by David Choi | JavaScript in Plain English](https://javascript.plainenglish.io/more-typescript-types-you-need-to-know-better-e18a5d3a02ac)

[Functions in TypeScript. Build robust functions that scale | by Dler Ari | Better Programming](https://betterprogramming.pub/functions-in-typescript-d17701fc6124)

## Libraries

[Comprehensive list of built-in utility types in TypeScript - codewithstyle.info](https://codewithstyle.info/Comprehensive-list-of-useful-built-in-types-in-TypeScript/)
[andnp/SimplyTyped: yet another Typescript type library for advanced types](https://github.com/andnp/SimplyTyped)

[Ts.ED - A Node.js and TypeScript Framework on top of Express/Koa.js.](https://tsed.io/)

### Mongoose

[TypeScript: Declaring Mongoose Schema + Model | Brian Love](https://brianflove.com/2016/10/04/typescript-declaring-mongoose-schema-model/)
[yoitsro/joigoose: Joi validation for your Mongoose models without the hassle of maintaining two schemas](https://github.com/yoitsro/joigoose)

```sh
npm install mongoose --save
npm install @types/mongoose --save-dev
npm install @types/mongodb --save-dev
```

[javascript - Mongoose the Typescript way...? - Stack Overflow](https://stackoverflow.com/questions/34482136/mongoose-the-typescript-way)
[mongoose typescript models · Appsilon/styleguide Wiki](https://github.com/Appsilon/styleguide/wiki/mongoose-typescript-models)

[szokodiakos/typegoose: Typegoose - Define Mongoose models using TypeScript classes.](https://github.com/szokodiakos/typegoose)

### React/Redux

[Why TypeScript with React? - Carl's Blog](https://www.carlrippon.com/why-typescript-with-react/)
[Microsoft/TypeScript-React-Conversion-Guide: A guide for converting a simple JavaScript/React project to TypeScript. Contains both before an after code with the step-by-step process in the README below.](https://github.com/Microsoft/TypeScript-React-Conversion-Guide#typescript-react-conversion-guide)

[TypeScript and React](https://fettblog.eu/typescript-react/)
[Taking React and Redux to the next level with Typescript - DEV Community 👩‍💻👨‍💻](https://dev.to/leomeloxp/taking-react-and-redux-to-the-next-level-with-typescript-1m84)
[10++ TypeScript Pro tips/patterns with (or without) React](https://medium.com/@martin_hotell/10-typescript-pro-tips-patterns-with-or-without-react-5799488d6680)
[Learning TypeScript with React - Part 1 - DEV Community 👩‍💻👨‍💻](https://dev.to/analizapandac/learning-typescript-with-react-part-1-3ohn)
[Learning TypeScript with React - Part 2 (The what, why and how of interfaces) - DEV Community 👩‍💻👨‍💻](https://dev.to/analizapandac/learning-typescript-with-react-part-2-the-what-why-and-how-of-interfaces-1033)....
[A type-safe approach to Redux stores in TypeScript - DEV Community 👩‍💻👨‍💻](https://dev.to/resir014/a-type-safe-approach-to-redux-stores-in-typescript--5ajm)
[Redux 4 + TypeScript 2.9: A type-safe approach - DEV Community 👩‍💻👨‍💻](https://dev.to/resir014/redux-4--typescript-29-a-type-safe-approach-2lf4)
[Improved Redux type safety with TypeScript 2.8 - Martin Hochel - Medium](https://medium.com/@martin_hotell/improved-redux-type-safety-with-typescript-2-8-2c11a8062575)
[Notes on TypeScript: Pick, Exclude and Higher Order Components - DEV Community 👩‍💻👨‍💻](https://dev.to/busypeoples/notes-on-typescript-pick-exclude-and-higher-order-components-40cp) series
[Advanced TypeScript by Example: React Form Carousel](https://medium.com/better-programming/advanced-typescript-by-example-react-form-carousel-ab2545d5a8e3)
[Writing better Reducers with React and Typescript 3.4](https://blog.usejournal.com/writing-better-reducers-with-react-and-typescript-3-4-30697b926ada)

[React Hooks in TypeScript - James Ravenscroft - Medium](https://medium.com/@jrwebdev/react-hooks-in-typescript-88fce7001d0d)
[React Render Props in TypeScript - James Ravenscroft - Medium](https://medium.com/@jrwebdev/react-render-props-in-typescript-b561b00bc67c)

[Tinkerer - Converting a React Codebase to Typescript. Part 1: Getting it to compile](http://www.gustavwengel.dk/converting-typescript-to-javascript-part-1)
[Tinkerer - React To Typescript Part 2: Converting React Components to TypeScript](http://www.gustavwengel.dk/converting-typescript-to-javascript-part-2)

[React Refs with TypeScript - Martin Hochel - Medium](https://medium.com/@martin_hotell/react-refs-with-typescript-a32d56c4d315)
[How To Structure Your TypeScript + React + Redux App](https://medium.com/swlh/how-to-structure-your-typescript-react-redux-app-877d1eba1c1e)

## Tips and Tricks

[Best Practices For Using TypeScript with Node.js – Bits and Pieces](https://blog.bitsrc.io/best-practices-for-using-typescript-with-node-js-50907f8cc803)
[Microsoft/TypeScript-Node-Starter: A starter template for TypeScript and Node with a detailed README describing how to use the two together.](https://github.com/Microsoft/TypeScript-Node-Starter)
[Node.js TypeScript Archives - Marcin Wanago Blog - JavaScript, both frontend and backend](https://wanago.io/courses/node-js-typescript/)
[How to Use Named Parameters in TypeScript | by Krzysztof Kwieciński | Better Programming](https://betterprogramming.pub/named-parameters-in-typescript-e32c763d2b2e)

[Enterprise Node + TypeScript | Khalil Stemmler - JavaScript Developer / Designer](https://khalilstemmler.com/articles/categories/enterprise-node-type-script/)

[4 Ways to Write More Effective TypeScript | by Lewis Fairweather | JavaScript in Plain English](https://javascript.plainenglish.io/4-ways-to-write-more-effective-typescript-72033322c290)
[My TypeScript Best Practices. A year ago I decided to finally try… | by Justin Travis Waith-Mair | The Non-Traditional Developer | Medium](https://medium.com/the-non-traditional-developer/my-typescript-best-practices-845e196284aa)

[Some Lesser Known TypeScript Features – Articode – Medium](https://medium.com/articode/some-lesser-known-typescript-features-d067e29797d0)
[Advanced TypeScript Types with Examples - Level Up Coding](https://levelup.gitconnected.com/advanced-typescript-types-with-examples-1d144e4eda9e)

[Path aliases with TypeScript in Node.js - DEV Community 👩‍💻👨‍💻](https://dev.to/larswaechter/path-aliases-with-typescript-in-nodejs-4353)

### npm script

It's actually better to use `tsconfig.json`.

```js
"scripts": {
  "start": "./node_modules/nodemon/bin/nodemon.js -e ts  \
    --exec \"npm run compile\"",
  "compile": "tsc --outDir ./build --module commonjs ./src/*.ts && \
    node ./build/server.js"
}
```

[Using Typescript with hapi](https://www.solarwinter.net/using-typescript-with-hapi/)

Sample server project:

[1. Setup and first query](https://nexusjs.org/docs/getting-started/tutorial/chapter-setup-and-first-query#cli)
[prisma-examples/typescript/graphql-hapi at latest · prisma/prisma-examples](https://github.com/prisma/prisma-examples/tree/latest/typescript/graphql-hapi)

### Error on `export`

```js
// error
export default const VERSION: number = 2016030600;

// change to
const VERSION: number = 2016030600;
export default VERSION;
// or
declare const VERSION: number;
export default VERSION = 2016030600;
```

[Typescript compile error: error TS1109: Expression expected - Stack Overflow](https://stackoverflow.com/questions/35821614/typescript-compile-error-error-ts1109-expression-expected)

### Checking JS code

[Type Checking JavaScript Files · TypeScript](https://www.typescriptlang.org/docs/handbook/type-checking-javascript-files.html)

```json
{
  "compilerOptions": {
    "allowJs": true /* Allow JavaScript files to be compiled. */,
    "checkJs": true /* Report errors in .js files. */,
    "lib": ["es2017"]
  },
  "include": ["src/**/*"],
  "typeAcquisition": {
    "enable": true
  }
}
```

```json
  "baseUrl": "./src",
  "paths": {
      "@modules/*": ["rest/modules/*"],
      "@services/*": ["services/*"]
  }
```
