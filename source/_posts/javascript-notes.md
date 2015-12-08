title: "JavaScript notes"
date: 2014-12-11 17:04:13
categories:
- comp.lang
tags:
- javascript
- notes
toc: true
---

JavaScript was conceived by Brendan Eich, then employee of Netscape, in ten days time. The name "JavaScript" was chosen intendedly with reference Java to give the impression of "write once, run everywhere".

Sun (now Oracle) owns the trademark of the name “Java”, hence "JavaScript". So the standard for JavaScript is [ECMA-262](http://www.ecma-international.org/publications/standards/Ecma-262.htm) (or ECMAScript), after the standard body ECMA.

Harmony stands for the ES5+ feature set. Some of them will be in ES6, some of them will be in the future version of ES.

[ECMAScript - Wikiwand](http://www.wikiwand.com/en/ECMAScript)
[Brendan Eich » Blog Archive » A Brief History of JavaScript](https://brendaneich.com/2010/07/a-brief-history-of-javascript/)
[JavaScript: how it all began](http://www.2ality.com/2011/03/javascript-how-it-all-began.html)
[A JavaScript glossary: ECMAScript, TC39, etc.](http://www.2ality.com/2011/06/ecmascript.html)
[ES5, ES6, ES2016, ES.Next: What's going on with JavaScript versioning?](http://benmccormick.org/2015/09/14/es5-es6-es2016-es-next-whats-going-on-with-javascript-versioning/)

[DevChat.TV](https://devchat.tv/js-jabber/124-jsj-the-origin-of-javascript-with-brendan-eich)

<!-- more -->

## Language

[Expressions versus statements in JavaScript](http://www.2ality.com/2012/09/expressions-vs-statements.html)

### Scope

[JavaScript variable scoping and its pitfalls](http://www.2ality.com/2011/02/javascript-variable-scoping-and-its.html)
[Variable declarations: three rules you can break](http://www.2ality.com/2012/11/var-statement-rules.html)

### Types

[12 JavaScript quirks](http://www.2ality.com/2013/04/12quirks.html)
[JavaScript’s type system](http://www.2ality.com/2013/09/types.html)
[Categorizing values in JavaScript](http://www.2ality.com/2013/01/categorizing-values.html)
[JavaScript: fixing categorization](http://www.2ality.com/2013/02/isinstance.html)
[Coercing objects to primitives](http://www.2ality.com/2012/11/coercing-objects.html)

Objects are like map, but see [The pitfalls of using objects as maps in JavaScript](http://www.2ality.com/2012/01/objects-as-maps.html) and [Using objects as dictionaries is surprisingly tricky](http://www.2ality.com/2015/08/object-literals-es5.html#using_objects_as_dictionaries_is_surprisingly_tricky).
[Chapter 17. Objects and Inheritance: The dict Pattern](http://speakingjs.com/es5/ch17.html#dict_pattern)

[19. Maps and Sets](http://exploringjs.com/es6/ch_maps-sets.html)
[Converting ES6 Maps to and from JSON](http://www.2ality.com/2015/08/es6-map-json.html)

[Statically typed JavaScript via Microsoft TypeScript, Facebook Flow and Google AtScript](http://www.2ality.com/2014/10/typed-javascript.html)

[10 Interview Questions Every JavaScript Developer Should Know — JavaScript Scene — Medium](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95)

### Internals (Runtime and VM)

[Philip Roberts: What the heck is the event loop anyway? | JSConf EU 2014 - YouTube](https://www.youtube.com/watch?v=8aGhZQkoFbQ) (Recommended)
[latentflip.com/loupe/](http://latentflip.com/loupe/)
[mö.js - explaining js vm in js - YouTube](https://www.youtube.com/watch?v=y8hVeKMD_oM)
[StrongLoop | What’s New in Node.js v0.12 – Running Multiple Instances in a Single Process](https://strongloop.com/strongblog/whats-new-node-js-v0-12-multiple-context-execution/)
[A Guide to JavaScript Engines for Idiots -Telerik Developer Network](http://developer.telerik.com/featured/a-guide-to-javascript-engines-for-idiots/)
[Writing Fast, Memory-Efficient JavaScript – Smashing Magazine](http://www.smashingmagazine.com/2012/11/writing-fast-memory-efficient-javascript/)

[Event loop from 10,000ft - core concept behind Node.js](http://bytearcher.com/articles/event-loop-10-000ft/)
[Parallel vs Concurrent in Node.js](http://bytearcher.com/articles/parallel-vs-concurrent/)

### Style

[Brace styles and JavaScript](http://www.2ality.com/2013/01/brace-styles.html)
[Video: JavaScript coding tips](http://www.2ality.com/2014/08/javascript-coding-tips.html)

[Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)

## Array

[Apply and arrays: three tricks](http://www.2ality.com/2012/07/apply-tricks.html)
[Destructuring and parameter handling in ECMAScript 6](http://www.2ality.com/2015/01/es6-destructuring.html#the_spread_operator_%28...%29)

```javascript
// delete n elements at index i, insert args at that position
[].splice(i, n, [, arg1[, arg2[, ...]]])

// convert arguments to true Array
[].slice.call(arguments);

// bind() returns a new function
f2 = f1.bind(thisArg[, arg1[, arg2[, ...]]])
f1.call(thisArg[, arg1[, arg2[, ...]]])

// call Array function on array-like objec
tvar meta = document.getElementsByTagName('meta');
var filtered = [].filter.call(meta, function (val) {
    if(val.name === 'description') return val;
});
```

## Closure/IFFE

[Self Invoked Anonymous Function? Sounds iffy… « Eric Elliott – JavaScript Architect (A JavaScript Blog)](http://ericleads.com/2013/02/self-invoked-anonymous-function-sounds-iffy/)

[13. Callable entities in ECMAScript 6: Avoid IIFEs in ES6](http://exploringjs.com/es6/ch_callables.html#sec_iifes-in-es6)

[How do JavaScript closures work under the hood [Dmitry Frank]](http://dmitryfrank.com/articles/js_closures)

## Promise

[Asynchronous JavaScript Interfaces](http://medikoo.com/asynchronous-javascript-interfaces/)
[Asynchronous programming and continuation-passing style in JavaScript](http://www.2ality.com/2012/06/continuation-passing-style.html)
[JavaScript Promises: There and back again - HTML5 Rocks](http://www.html5rocks.com/en/tutorials/es6/promises/)
[Making Change.org — Promises and Error Handling](http://making.change.org/post/69613524472/promises-and-error-handling)
[Promise nuggets](http://promise-nuggets.github.io/)
[Promises and design patterns in AngularJS | Xebia Blog](http://blog.xebia.com/2014/02/23/promises-and-design-patterns-in-angularjs/)
[Promises in Node.js with Q – An Alternative to Callbacks - StrongLoop](http://blog.strongloop.com/promises-in-node-js-with-q-an-alternative-to-callbacks/)
[How-to Compose Node.js Promises with Q - StrongLoop](http://blog.strongloop.com/how-to-compose-node-js-promises-with-q/)
[Why I am switching to promises](http://spion.github.io/posts/why-i-am-switching-to-promises.html)
[Promises + FP = Beautiful Streams - Tech.pro](http://tech.pro/blog/6888/promises--fp--beautiful-streams)
[From callback to (Future -> Functor -> Monad) - Tech.pro](http://tech.pro/blog/6742/callback-to-future-functor-applicative-monad)
[async-to-q.js](https://gist.github.com/wavded/6116786)
[wbinnssmith/awesome-promises](https://github.com/wbinnssmith/awesome-promises)

[Promisees · Courtesy of ponyfoo.com](http://bevacqua.github.io/promisees/)

### Libraries

[calvinmetcalf/lie](https://github.com/calvinmetcalf/lie)
[petkaantonov-bluebird · GitHub](https://github.com/petkaantonov/bluebird)
[duereg-songbird · GitHub](https://github.com/duereg/songbird)
[nodegit/promisify-node](https://github.com/nodegit/promisify-node)

Use `Bluebird.promisifyAll(module)` ` to create an async version of every method the module provides.

### Promise (ES6)

[Introduction to ES6 Promises – The Four Functions You Need To Avoid Callback Hell | James K Nelson](http://jamesknelson.com/grokking-es6-promises-the-four-functions-you-need-to-avoid-callback-hell/)
[Promise - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

[We have a problem with promises](http://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html)
- don't use 2nd param of `then()`, trailing `catch()` is better in all cases
- passing `then()` non-function will cause the previous promise's result to fall through

```js
doSomething().then(function () {
  return doSomethingElse();
});

doSomething().then(function () {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```

```js
new Promise(function(resolve, reject){})
    .then(successHandler1)
    .catch(failureHandler1)  // captures all rejection and exception
    .then(successHandler2)
    .catch(failureHandler2); // captures all rejection and exception
```

```js
Promise.all([promise1, promise2, ...])
    .then(successHandler)    // parameter: [value1, value2, ... ]
    .catch(failureHandler);  // parameter: the first rejection

// properly loop through an array
db.allDocs().then(function (docs) {
  return Promise.all(docs.map(function (docs) {
    return db.remove(doc);
  }));
}).then(function (arrayOfResults) {
  // All docs have been removed() now!
})
.catch(console.log.bind(console)); // <-- this is badass
```

![Cheatsheet](http://jamesknelson.com/grokking-es6-promises.png)

## Generators (ES6)

[The Definitive Guide to the JavaScript Generators](http://gajus.com/blog/2/the-definetive-guide-to-the-javascript-generators)
[Analysis of generators and other async patterns in node](http://spion.github.io/posts/analysis-generators-and-other-async-patterns-node.html)
[ES6 Generators Deliver Go Style Concurrency](http://swannodette.github.io/2013/08/24/es6-generators-and-csp/)
[ES6 generators in depth](http://www.2ality.com/2015/03/es6-generators.html)
[Generators: the Gnarly Bits](http://updates.html5rocks.com/2014/10/Generators-the-Gnarly-Bits)
[Generators vs Fibers - How To Node - NodeJS](http://howtonode.org/generators-vs-fibers)
[How should I format the ECMAScript 6 generator asterisk?](http://www.2ality.com/2014/08/formatting-generator-asterisk.html)
[Introduction to Generators & Koa.js - Tuts+ Code Tutorials](http://code.tutsplus.com/series/introduction-to-generators-koajs--cms-690)
[StrongLoop | Generators in Node.js: Common Misconceptions and Three Good Use Cases](http://strongloop.com/strongblog/how-to-generators-node-js-yield-use-cases/)
[Generators Are Like Arrays](https://gist.github.com/jkrems/04a2b34fb9893e4c2b5c)
[Callbacks vs Coroutines — Medium](https://medium.com/@tjholowaychuk/callbacks-vs-coroutines-174f1fe66127)

## Strict mode

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/Strict_mode
http://howardabrams.com/presentations/?use-strict
http://stackoverflow.com/a/15251160/665507

## Decorators

[Exploring ES2016 Decorators — Google Developers — Medium](https://medium.com/google-developers/exploring-es7-decorators-76ecb65fb841)

## Strings/Regex

[Unicode-aware regular expressions in ECMAScript 6 · Mathias Bynens](https://mathiasbynens.be/notes/es6-unicode-regex)
[New regular expression features in ECMAScript 6](http://www.2ality.com/2015/07/regexp-es6.html)

### Template Strings (ES6)

[Using ES6 template strings for regular expressions](http://www.2ality.com/2012/12/template-strings-xregexp.html)
[HTML templating with ES6 template strings](http://www.2ality.com/2015/01/template-strings-html.html)
[Template strings: embedded DSLs in ECMAScript 6](http://www.2ality.com/2011/09/quasi-literals.html)
[A closer look at Underscore templates](http://www.2ality.com/2012/06/underscore-templates.html)
[Getting Literal With ES6 Template Strings](http://updates.html5rocks.com/2015/01/ES6-Template-Strings)

```js
var index = 0;
var obj = {
  [`key${index}`]: index++,
  [`key${index}`]: index++,
  [`key${index}`]: index++,
};
 
console.log(obj);
// {"key0":0,"key1":1,"key2":2}
```

## Inheritance

[Object Playground: The Definitive Guide to Object-Oriented JavaScript](http://www.objectplayground.com/)

[The Two Pillars of JavaScript — JavaScript Scene — Medium](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3)
[Common Misconceptions About Inheritance in JavaScript — JavaScript Scene — Medium](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a)
[How to Fix the ES6 `class` keyword — JavaScript Scene — Medium](https://medium.com/javascript-scene/how-to-fix-the-es6-class-keyword-2d42bb3f4caf)
[JavaScript inheritance patterns — Medium](https://medium.com/@PitaJ/javascript-inheritance-patterns-179d8f6c143c)

[Fluent JavaScript – Three Different Kinds of Prototypal OO « Eric Elliott – JavaScript Architect (A JavaScript Blog)](http://ericleads.com/2013/02/fluent-javascript-three-different-kinds-of-prototypal-oo/)
[Classical Inheritance is Obsolete – How to Think in Prototypal OO « Eric Elliott – JavaScript Architect (A JavaScript Blog)](http://ericleads.com/2013/06/classical-inheritance-is-obsolete-how-to-think-in-prototypal-oo/) [slide](http://slidedeck.io/dilvie/fluent-prototypal-oo)
[Stop Using Constructor Functions in JavaScript « Eric Elliott – JavaScript Architect (A JavaScript Blog)](http://ericleads.com/2012/09/stop-using-constructor-functions-in-javascript/)
[Composition over Inheritance — mpj on programming — Medium](https://medium.com/humans-create-software/composition-over-inheritance-cb6f88070205)

[JS Objects: Inherited a Mess](http://davidwalsh.name/javascript-objects)
[JS Objects: Distractions](http://davidwalsh.name/javascript-objects-distractions)
[JS Objects: De"construct"ion](http://davidwalsh.name/javascript-objects-deconstruction)

### Prototypal Inheritance

Prototypal Inheritance: instances inherit directly from other objects. Instances are typically instantiated via factory functions or `Object.create()`. Instances may be composed from many different objects, allowing for easy selective inheritance.


[JavaScript: __proto__](http://www.2ality.com/2012/10/proto.html)
[Prototypes as classes – an introduction to JavaScript inheritance](http://www.2ality.com/2011/06/prototypes-as-classes.html)
[Object properties in JavaScript](http://www.2ality.com/2012/10/javascript-properties.html)
[Properties in JavaScript: definition versus assignment](http://www.2ality.com/2012/08/property-definition-assignment.html)
[JavaScript terminology: the two prototypes](http://www.2ality.com/2013/01/two-prototypes.html)
[JavaScript properties: inheritance and enumerability](http://www.2ality.com/2011/07/js-properties.html)
[JavaScript inheritance by example](http://www.2ality.com/2012/01/js-inheritance-by-example.html)
[JavaScript inheritance: beyond the basics (video)](http://www.2ality.com/2012/11/js-inheritance-beyond-basics.html)
[Property assignment and the prototype chain](http://www.2ality.com/2012/11/property-assignment-prototype-chain.html)
[A closer look at _.extend and copying properties](http://www.2ality.com/2012/08/underscore-extend.html)

[Prototypal Inheritance With Stamps « Eric Elliott – JavaScript Architect (A JavaScript Blog)](http://ericleads.com/2014/02/prototypal-inheritance-with-stamps/)

[Learning Javascript with Object Graphs (Part I) - How To Node - NodeJS](http://howtonode.org/object-graphs)
[Learning Javascript with Object Graphs (Part II) - How To Node - NodeJS](http://howtonode.org/object-graphs-2)
[Learning Javascript with Object Graphs (Part III) - How To Node - NodeJS](http://howtonode.org/object-graphs-3)
[Prototypal Inheritance - How To Node - NodeJS](http://howtonode.org/prototypical-inheritance)

[Inheritance and the prototype chain - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
[Prototypal Inheritance](http://javascript.crockford.com/prototypal.html)
[Learning JavaScript Design Patterns](http://addyosmani.com/resources/essentialjsdesignpatterns/book/#prototypepatternjavascript)
[A Plain English Guide to JavaScript Prototypes - Sebastian's Blog](http://sporto.github.io/blog/2013/02/22/a-plain-english-guide-to-javascript-prototypes/)

### Class Inheritance

Class Inheritance: instances inherit from classes (like a blueprint — a description of the class), and create sub-class relationships: hierarchical class taxonomies. Instances are typically instantiated via constructor functions with the `new` keyword. Class inheritance may or may not use the `class` keyword from ES6.

Other voices:
[joshburgess/not-awesome-es6-classes](https://github.com/joshburgess/not-awesome-es6-classes/)
[christianalfoni - Think twice about ES6 classes](http://www.christianalfoni.com/articles/2015_01_01_Think-twice-about-ES6-classes)
[How to Use Classes and Sleep at Night — Medium](https://medium.com/@dan_abramov/how-to-use-classes-and-sleep-at-night-9af8de78ccb4#.cln2rrt6t)


```js
// CLASSICAL INHERITANCE

// Parent class constructor
function Parent() {
  this.a = 42;
}

// Parent class method
Parent.prototype.method = function method() {};

// Child class constructor
function Child() {
  Parent.call(this);
  this.b = 3.14159
}

// Inherit from the parent class
Child.prototype = Object.create(Parent.prototype);
Child.prototype.constructor = Child;

// Child class method
Child.prototype.method = function method() {
  Parent.prototype.method.call(this);
};

// Instantiate
this.instance = new Child();
```

[Classes in ECMAScript 6 (final semantics)](http://www.2ality.com/2015/02/es6-classes-final.html)
[Simple JavaScript Inheritance: What You Need to Know - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/simple-javascript-inheritance-what-you-need-to-know--cms-24144)
[Understanding ECMAScript 6: Class and Inheritance](http://www.sitepoint.com/understanding-ecmascript-6-class-inheritance/)
[StrongLoop | An Introduction To JavaScript ES6 Classes](https://strongloop.com/strongblog/an-introduction-to-javascript-es6-classes/)

[JavaScript Constructor Functions vs Factory Functions « Eric Elliott – JavaScript Architect (A JavaScript Blog)](http://ericleads.com/2013/01/javascript-constructor-functions-vs-factory-functions/)

http://ejohn.org/blog/simple-javascript-inheritance/
http://phrogz.net/JS/classes/OOPinJS.html  
http://phrogz.net/JS/classes/OOPinJS2.html  
http://metaduck.com/05-dump-this.html

## Modules (ES6)

[Declaring module exports (Node.js, AMD)](http://www.2ality.com/2012/04/declaring-module-exports.html)
[Understanding ES6 Modules](http://www.sitepoint.com/understanding-es6-modules/)
[ECMAScript 6 modules: the final syntax](http://www.2ality.com/2014/09/es6-modules-final.html)
[JavaScript Modules the ES6 Way ◆ 24 ways](http://24ways.org/2014/javascript-modules-the-es6-way/)
[Choose ES6 modules Today! -Telerik Developer Network](http://developer.telerik.com/featured/choose-es6-modules-today/)
[JavaScript Module Pattern: In-Depth](http://www.adequatelygood.com/JavaScript-Module-Pattern-In-Depth.html)
[mattdesl/module-best-practices](https://github.com/mattdesl/module-best-practices)
[Components Should Be Focused, Independent, Reusable, Small And Testable (FIRST)](http://addyosmani.com/first/)
[ES6 modules · rollup/rollup Wiki](https://github.com/rollup/rollup/wiki/ES6-modules)
[JavaScript Modules: Welcome to My Emo Hellscape — Medium](https://medium.com/@trek/last-week-i-had-a-small-meltdown-on-twitter-about-npms-future-plans-around-front-end-packaging-b424dd8d367a)
[JavaScript Modules](http://jsmodules.io/)

## Functional Programming

[functional js](http://fogus.github.io/lemonad/)
[baconjs/bacon.js](https://github.com/baconjs/bacon.js)
[FredyC/promised-land](https://github.com/FredyC/promised-land/)
[jussi-kalliokoski/trine](https://github.com/jussi-kalliokoski/trine)
[LUISATENCIO.NET](http://www.luisatencio.net/)

[Ramda Documentation](http://ramdajs.com/0.18.0/index.html)
[lodash](https://lodash.com/)

[Functional and Object Oriented Programming with Higher Order Functions | Zsolt Nagy](http://www.zsoltnagy.eu/functional-and-object-oriented-programming-with-higher-order-functions/)

[An Introduction to Functional JavaScript](http://www.sitepoint.com/introduction-functional-javascript/)
[Recursion in Functional JavaScript](http://www.sitepoint.com/recursion-functional-javascript/)
[Higher-Order Functions in JavaScript](http://www.sitepoint.com/higher-order-functions-javascript/)
[A Beginner's Guide to Currying in Functional JavaScript](http://www.sitepoint.com/currying-in-functional-javascript/)

[Understanding recursion in functional JavaScript programming](http://www.integralist.co.uk/posts/js-recursion.html)
[The Two Pillars of JavaScript — Pt 2: Functional Programming — JavaScript Scene — Medium](https://medium.com/javascript-scene/the-two-pillars-of-javascript-pt-2-functional-programming-a63aa53a41a4)
[Polymorphic functions and method dispatch in JavaScript « Eric Elliott – JavaScript Architect (A JavaScript Blog)](http://ericleads.com/2011/06/polymorphic-functions-and-multiple-dispatch-in-javascript/)

[Getting Functional with Javascript (Part 1)](http://www.datchley.name/getting-functional-with-javascript-part-1/)
[Getting Functional with Javascript (Part 2)](http://www.datchley.name/getting-functional-with-javascript-part-2/)
[Getting Functional with Javascript (Part 3)](http://www.datchley.name/getting-functional-with-javascript-part-3/)

[Functional programming in JavaScript - YouTube](https://www.youtube.com/playlist?list=PL0zVEGEvSaeEd9hlmCXrk5yUyqUag-n84)
[Carefully Composing Logic: Functional JavaScript on Vimeo](https://vimeo.com/138163463)

[Functional Programming in Javascript === Garbage « Thomas Reynolds](http://awardwinningfjords.com/2014/04/21/functional-programming-in-javascript-equals-garbage.html)

## Immutability

[List of immutable libraries](https://gist.github.com/jlongster/bce43d9be633da55053f)
[Immutable.js](https://facebook.github.io/immutable-js/)
[Gozala/typed-immutable](https://github.com/gozala/typed-immutable)
[scottcorgan/immu](https://github.com/scottcorgan/immu)
[arqex/freezer](https://github.com/arqex/freezer)
[rtfeldman/seamless-immutable](https://github.com/rtfeldman/seamless-immutable)

[The React.js Way: Getting Started Tutorial | RisingStack](https://blog.risingstack.com/the-react-way-getting-started-tutorial/)
[The React.js Way: Flux Architecture with Immutable.js](https://blog.risingstack.com/the-react-js-way-flux-architecture-with-immutable-js/)
[Pros and Cons of using immutability with React.js - React Kung Fu](http://reactkungfu.com/2015/08/pros-and-cons-of-using-immutability-with-react-js/)
[The Dao of Immutability — JavaScript Scene — Medium](https://medium.com/javascript-scene/the-dao-of-immutability-9f91a70c88cd)
[React.js the simple way — Medium](https://medium.com/@arqex/react-the-simple-way-cabdf1f42f12) (Freezer.js)

[Immutability in JavaScript](http://www.sitepoint.com/immutability-javascript/)
[Introduction to Immutable.js | Zsolt Nagy](http://www.zsoltnagy.eu/introduction-to-immutable-js/)
[Immutable Data Structures and JavaScript](http://jlongster.com/Using-Immutable-Data-Structures-in-JavaScript)

## Workflow

[The Hitchhiker's Guide to Modern JavaScript Tooling - React Kung Fu](http://reactkungfu.com/2015/07/the-hitchhikers-guide-to-modern-javascript-tooling/)
[addyosmani/es6-tools](https://github.com/addyosmani/es6-tools)
[Choose ES6 modules Today! -Telerik Developer Network](http://developer.telerik.com/featured/choose-es6-modules-today/) uses jspm
[DailyJS: Transpilers: This Time It's Different](http://dailyjs.com/2015/02/26/babel/)
[How to Use ES6 for Universal JavaScript Apps — JavaScript Scene — Medium](https://medium.com/javascript-scene/how-to-use-es6-for-isomorphic-javascript-apps-2a9c3abe5ea2)
[Practical Workflows for ES6 Modules](http://guybedford.com/practical-workflows-for-es6-modules)
[Setting up an ES6 Project Using Babel and Browserify](http://www.sitepoint.com/setting-up-es6-project-using-babel-browserify/)
[Traceur, Gulp, Browserify and ES6 - Matt Greer](http://www.mattgreer.org/articles/traceur-gulp-browserify-es6/)
[Using ES6 with npm today — Mammal](http://mammal.io/articles/using-es6-today/)
[Why Babel Matters](http://codemix.com/blog/why-babel-matters)
[How to Write a JavaScript Library - Introduction - JavaScript Video Tutorial #free @eggheadio](https://egghead.io/lessons/javascript-how-to-write-a-javascript-library-introduction?series=how-to-write-an-open-source-javascript-library)

### Transpilers

[esnext - Tomorrow’s JavaScript syntax today](http://esnext.github.io/esnext/#)

[google/traceur-compiler](https://github.com/google/traceur-compiler)
[facebook/jstransform](https://github.com/facebook/jstransform)

#### Babel

[Babel · The transpiler for writing next generation JavaScript](http://babeljs.io/)
[6.0.0 Released · Babel](https://babeljs.io/blog/2015/10/29/6.0.0/)
[Setting up Babel 6 · Babel](https://babeljs.io/blog/2015/10/31/setting-up-babel-6/)
[Quick guide: how to update Babel 5.x -> 6.x — Medium](https://medium.com/@malyw/how-to-update-babel-5-x-6-x-d828c230ec53#.gn96ozsm4)

[results for babel-plugin](https://www.npmjs.com/search?q=babel-plugin)
[codemix/babel-plugin-closure-elimination](https://github.com/codemix/babel-plugin-closure-elimination)
[ooflorent/babel-plugin-graphql](https://github.com/ooflorent/babel-plugin-graphql)
[chocolateboy/babel-plugin-source-map-support](https://github.com/chocolateboy/babel-plugin-source-map-support)
[zloirock/core-js](https://github.com/zloirock/core-js) es6 shim used in Babel

```json
{
  "name": "wsi-viewer",
  "version": "1.0.0",
  "description": "",
  "main": "bundle.js",
  "scripts": {
    "build": "browserify src/index.js --debug | exorcist public/bundle.js.map | uglifyjs -cm > public/bundle.js",
    "watch": "watchify src/index.js -d -o public/bundle.js -v",
    "test": "tape test/*.js",
    "coverage": "covert test/*.js"
  },
  "author": "KY LEE <kylee@astri.org>",
  "browserify": {
    "transform": [
      "browserify-shim",
      "babelify"
    ]
  },
  "browserify-shim": {
    "openseadragon": "global:OpenSeadragon"
  },
  "babel": {
    "presets": [
      "es2015",
      "react"
    ]
  },
  "devDependencies": {
    "babel-preset-es2015": "^6.1.18",
    "babel-preset-react": "^6.1.18",
    "babelify": "^7.2.0",
    "browserify": "^12.0.1",
    "browserify-shim": "^3.8.11",
    "covert": "^1.1.0",
    "exorcist": "^0.4.0",
    "tape": "^4.2.2",
    "uglify-js": "^2.6.1",
    "watchify": "^3.6.1"
  },
  "dependencies": {}
}
```

### See `browserify.md`

### Webpack

[webpack](http://webpack.github.io/docs/)
[Backend Apps with Webpack (Part I)](http://jlongster.com/Backend-Apps-with-Webpack--Part-I)
[Backend Apps with Webpack: Driving with Gulp (Part II)](http://jlongster.com/Backend-Apps-with-Webpack--Part-II)
[Live Editing JavaScript with Webpack (Part III)](http://jlongster.com/Backend-Apps-with-Webpack--Part-III)

## ES6

> TODO: digest these articles and put them into the above categories
> Refer to categorization here:
> [A guide to 2ality’s posts on the JavaScript language](http://www.2ality.com/2012/08/guide-jslang.html)
> [A guide to 2ality’s posts on ECMAScript.next/ECMAScript 6](http://www.2ality.com/2012/11/guide-esnext.html)
> [What are your favorite JavaScript ES6 features?](http://www.2ality.com/2015/07/favorite-es6-features.html)
> [zloirock/core-js](https://github.com/zloirock/core-js)
> Add these to `commonroom/es6/`

[Using ES6 Harmony with NodeJS](https://www.airpair.com/javascript/posts/using-es6-harmony-with-nodejs)
[Six Steps for Approaching the Next JavaScript -Telerik Developer Network](http://developer.telerik.com/featured/six-steps-for-approaching-the-next-javascript/)
[Learn ECMAScript6 by doing it](http://es6katas.org/)

[ES6 In Depth Articles ✩ Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/category/es6-in-depth/)
[ES6 Overview in 350 Bullet Points](https://ponyfoo.com/articles/es6)
[Articles tagged "es6-in-depth"](http://ponyfoo.com/articles/tagged/es6-in-depth)
[Learn Harmony -- Home](http://learnharmony.org/)
[Learn ES2015 · Babel](https://babeljs.io/docs/learn-es2015/)
[Tagtree course: Expert ES6](http://tagtree.tv/courses/expert-es6)
[jQuery UK - EcmaScript 6 - Google Slides](https://docs.google.com/presentation/d/1PvAHvODY_L3AiumgyjNFl4IPr82dq74vJxmMPOeU8uE/edit#slide=id.p)
[ES6: What are the benefits of the new features in practice? | CodeUtopia](http://codeutopia.n## ES6et/blog/2015/01/06/es6-what-are-the-benefits-of-the-new-features-in-practice/)
[ECMAScript 6 Power Tutorial - Tuts+ Code Tutorials](http://code.tutsplus.com/series/ecmascript-6-power-tutorial--cms-833)
[Porting your Javascript to ES6 — Lexical Labs Engineering — Medium](https://medium.com/lexical-labs-engineering/porting-your-javsascript-to-es6-d820520e900d)

[A guide to 2ality’s posts on ECMAScript.next/ECMAScript 6](http://www.2ality.com/2012/11/guide-esnext.html)
[Using ECMAScript 6 today](http://www.2ality.com/2014/08/es6-today.html)
[ECMAScript.next: for-of, iterators, generators](http://www.2ality.com/2012/06/for-of-ff13.html)
[ECMAScript 6: new OOP features besides classes](http://www.2ality.com/2014/12/es6-oop.html)
[Idiomatic ES6](https://blog.logentries.com/2015/06/idiomatic-es6/)

[You searched for ecmascript 6 - SitePoint](http://www.sitepoint.com/?s=ecmascript+6)

### features

[ECMAScript 6: New Features: Overview and Comparison](http://es6-features.org/)
[lukehoban/es6features](https://github.com/lukehoban/es6features#readme)
[sindresorhus/esnext-showcase](https://github.com/sindresorhus/esnext-showcase)
[hemanth/paws-on-es6](https://github.com/hemanth/paws-on-es6)
[help.wtf ECMAScript 6 Cheatsheet](http://help.wtf/es6)
[ECMAScript 6 compatibility table](http://kangax.github.io/compat-table/es6/)
 
## ES7

[Taming the asynchronous beast with ES7](http://pouchdb.com/2015/03/05/taming-the-async-beast-with-es7.html)

## CSP

[CSP and transducers in JavaScript](http://phuu.net/2014/08/31/csp-and-transducers.html)
[ubolonton/js-csp](https://github.com/ubolonton/js-csp)

## Pitfalls

[JavaScript Not Working? Here are 10 Common JavaScript Problems | Toptal](http://www.toptal.com/javascript/10-most-common-javascript-mistakes)

[Top 10 Mistakes Node.js Developers Make](https://www.airpair.com/node.js/posts/top-10-mistakes-node-developers-make)

[An interesting kind of JavaScript memory leak - Meteor](https://www.meteor.com/blog/2013/08/13/an-interesting-kind-of-javascript-memory-leak)

[Major and minor JavaScript pitfalls and ECMAScript 6](http://www.2ality.com/2012/02/js-pitfalls.html)

[JS Comparison Table](http://dorey.github.io/JavaScript-Equality-Table/)

## Tricks

> maybe a new post?

[7 Essential JavaScript Functions](http://davidwalsh.name/essential-javascript-functions?utm_source=javascriptweekly&utm_medium=email)

### padding

```js
//pads left
String.prototype.lpad = function(padChar, length) {
  var str = this;
  var padString = (length > str.length)?
    // limit padding char to 1 character
    Array(length-str.length+1).join(padChar[0]) : '';
  return (padString + str);
};

//pads right
String.prototype.rpad = function(padChar, length) {
  var str = this;
  var padString = (length > str.length)?
    // limit padding char to 1 character
    Array(length-str.length+1).join(padChar[0]) : '';
  return (str + padString);
};

// usage
var str = "5";
console.log(str.lpad(" ", 3)); //result "  5"
console.log(str.rpad("0", 3)); //result "500"

var str = "56789";
console.log(str.lpad(" ", 3)); //result "56789"
console.log(str.rpad("0", 3)); //result "56789"
```

### debounce

```js
// Returns a function, that, as long as it continues to be invoked, will not
// be triggered. The function will be called after it stops being called for
// N milliseconds. If `immediate` is passed, trigger the function on the
// leading edge, instead of the trailing.
function debounce(func, wait, immediate) {
    var timeout;
    return function() {
        var context = this, args = arguments;
        var later = function() {
            timeout = null;
            if (!immediate) func.apply(context, args);
        };
        var callNow = immediate && !timeout;
        clearTimeout(timeout);
        timeout = setTimeout(later, wait);
        if (callNow) func.apply(context, args);
    };
};

// Usage
var myEfficientFn = debounce(function() {
    // All the taxing stuff you do
}, 250);
window.addEventListener('resize', myEfficientFn);
```

### information hiding (private member)

http://www.crockford.com/javascript/private.html

// proper inheritance  
http://metaduck.com/08-module-pattern-inheritance.html

## functions

function become method automatically  
bound method: instance method  
unbound method: class method

