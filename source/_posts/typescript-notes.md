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

[Documentation · TypeScript](https://www.typescriptlang.org/docs/home.html)
[tsconfig.json · TypeScript](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html)
[Compiler Options · TypeScript](https://www.typescriptlang.org/docs/handbook/compiler-options.html)
[TypeScript/spec.md at master · Microsoft/TypeScript](https://github.com/Microsoft/TypeScript/blob/master/doc/spec.md)
[Home | DefinitelyTyped](http://definitelytyped.org/) The repository for high quality TypeScript type definitions

[How to learn TypeScript: A resources guide for developers - TechRepublic](https://www.techrepublic.com/article/how-to-learn-typescript-a-resources-guide-for-developers/#ftag=CAD-00-10aag7f)
[Learn TypeScript from the ground up with James Henry](https://typescriptcourses.com/typescript-fundamentals)
[Learn TypeScript - Best TypeScript Tutorials (2018) | gitconnected](https://gitconnected.com/learn/typescript)
[Introduction · TypeScript Deep Dive](https://basarat.gitbooks.io/typescript/)

[What's new in TypeScript? | Build 2017 | Channel 9](https://channel9.msdn.com/Events/Build/2017/B8088/)
[Why I Was Wrong About TypeScript (DevReach 2017) - YouTube](https://www.youtube.com/watch?v=w6rdLx2LYz8)
[TYPESCRIPT: How I Learned To Stop Worrying And Trust The Compiler - YouTube](https://www.youtube.com/watch?v=mgTenYbX2Kw)

[What’s new in TypeScript | InfoWorld](https://www.infoworld.com/article/3249607/javascript/whats-new-in-typescript.html)
[From JavaScript to TypeScript Pt. I: Types & Variables ― Scotch](https://scotch.io/tutorials/from-javascript-to-typescript-pt-i-types-variables)
[Type Systems: Structural vs. Nominal typing explained](https://medium.com/@thejameskyle/type-systems-structural-vs-nominal-typing-explained-56511dd969f4)
[Statically typed JavaScript via Microsoft TypeScript, Facebook Flow and Google AtScript](http://www.2ality.com/2014/10/typed-javascript.html)
[niieani/typescript-vs-flowtype: Differences between Flowtype and TypeScript -- syntax and usability](https://github.com/niieani/typescript-vs-flowtype)
[Introducing TypeScript - SitePoint Premium](https://www.sitepoint.com/premium/courses/introducing-typescript-2933/)
[What is TypeScript programming? Industrial-strength JavaScript](https://www.infoworld.com/article/2871804/javascript/typescript-industrial-strength-javascript.html)
[Learn TypeScript from the ground up with James Henry](https://typescriptcourses.com/typescript-fundamentals)

[How KEEP-87 & Typeclasses will change the way we write Kotlin - QuickBird Studios Blog](https://quickbirdstudios.com/blog/keep-87-typeclasses-kotlin/)

## Libraries

[Comprehensive list of built-in utility types in TypeScript - codewithstyle.info](https://codewithstyle.info/Comprehensive-list-of-useful-built-in-types-in-TypeScript/)

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

[A type-safe approach to Redux stores in TypeScript - DEV Community 👩‍💻👨‍💻](https://dev.to/resir014/a-type-safe-approach-to-redux-stores-in-typescript--5ajm)
[Redux 4 + TypeScript 2.9: A type-safe approach - DEV Community 👩‍💻👨‍💻](https://dev.to/resir014/redux-4--typescript-29-a-type-safe-approach-2lf4)

[How To Structure Your TypeScript + React + Redux App](https://medium.com/swlh/how-to-structure-your-typescript-react-redux-app-877d1eba1c1e)

## Tips and Tricks

[Best Practices For Using TypeScript with Node.js – Bits and Pieces](https://blog.bitsrc.io/best-practices-for-using-typescript-with-node-js-50907f8cc803)
[Microsoft/TypeScript-Node-Starter: A starter template for TypeScript and Node with a detailed README describing how to use the two together.](https://github.com/Microsoft/TypeScript-Node-Starter)
[Node.js TypeScript Archives - Marcin Wanago Blog - JavaScript, both frontend and backend](https://wanago.io/courses/node-js-typescript/)
[Enterprise Node + TypeScript | Khalil Stemmler - JavaScript Developer / Designer](https://khalilstemmler.com/articles/categories/enterprise-node-type-script/)

[Some Lesser Known TypeScript Features – Articode – Medium](https://medium.com/articode/some-lesser-known-typescript-features-d067e29797d0)

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
