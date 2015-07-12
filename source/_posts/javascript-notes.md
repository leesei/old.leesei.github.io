title: "JavaScript notes"
date: 2014-12-11 17:04:13
categories:
- comp.lang
tags:
- javascript
- notes
toc: true
---

## tricks

```javascript
// delete n elements at index i, insert args at that position
[].splice(i, n, [, arg1[, arg2[, ...]]])

// convert arguments to true Array
[].slice.call(arguments);

// bind() returns a new function
f2 = f1.bind(thisArg[, arg1[, arg2[, ...]]])
f1.call(thisArg[, arg1[, arg2[, ...]]])
```

[Apply and arrays: three tricks](http://www.2ality.com/2012/07/apply-tricks.html)

[7 Essential JavaScript Functions](http://davidwalsh.name/essential-javascript-functions?utm_source=javascriptweekly&utm_medium=email)

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

[A guide to 2ality’s posts on the JavaScript language](http://www.2ality.com/2012/08/guide-jslang.html)
> refer to its categorization

[plainJS - The Vanilla JavaScript Repository](http://plainjs.com/)

## pitfalls

[JavaScript Not Working? Here are 10 Common JavaScript Problems | Toptal](http://www.toptal.com/javascript/10-most-common-javascript-mistakes)

[An interesting kind of JavaScript memory leak - Meteor](https://www.meteor.com/blog/2013/08/13/an-interesting-kind-of-javascript-memory-leak)

## style

[Brace styles and JavaScript](http://www.2ality.com/2013/01/brace-styles.html)
[Video: JavaScript coding tips](http://www.2ality.com/2014/08/javascript-coding-tips.html)

[Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)

## types

[12 JavaScript quirks](http://www.2ality.com/2013/04/12quirks.html)
[JavaScript’s type system](http://www.2ality.com/2013/09/types.html)
[Categorizing values in JavaScript](http://www.2ality.com/2013/01/categorizing-values.html)
[JavaScript: fixing categorization](http://www.2ality.com/2013/02/isinstance.html)
[Coercing objects to primitives](http://www.2ality.com/2012/11/coercing-objects.html)

[Statically typed JavaScript via Microsoft TypeScript, Facebook Flow and Google AtScript](http://www.2ality.com/2014/10/typed-javascript.html)

Objects are like map, but see [The pitfalls of using objects as maps in JavaScript](http://www.2ality.com/2012/01/objects-as-maps.html).

[ECMAScript 6: maps and sets](http://www.2ality.com/2015/01/es6-maps-sets.html)
[ECMAScript 6 sets: union, intersection, difference](http://www.2ality.com/2015/01/es6-set-operations.html)

## syntax

[Expressions versus statements in JavaScript](http://www.2ality.com/2012/09/expressions-vs-statements.html)

## scoping

[JavaScript variable scoping and its pitfalls](http://www.2ality.com/2011/02/javascript-variable-scoping-and-its.html)
[Variable declarations: three rules you can break](http://www.2ality.com/2012/11/var-statement-rules.html)

## flow control

[Asynchronous programming and continuation-passing style in JavaScript](http://www.2ality.com/2012/06/continuation-passing-style.html)

> add promise and generator

## runtime and VM

[Philip Roberts: What the heck is the event loop anyway? | JSConf EU 2014 - YouTube](https://www.youtube.com/watch?v=8aGhZQkoFbQ) (Recommanded)
[mö.js - explaining js vm in js - YouTube](https://www.youtube.com/watch?v=y8hVeKMD_oM)

## CSP

[CSP and transducers in JavaScript](http://phuu.net/2014/08/31/csp-and-transducers.html)
[ubolonton/js-csp](https://github.com/ubolonton/js-csp)

## promise

[calvinmetcalf/lie](https://github.com/calvinmetcalf/lie)
[petkaantonov-bluebird · GitHub](https://github.com/petkaantonov/bluebird)
[duereg-songbird · GitHub](https://github.com/duereg/songbird)
[nodegit/promisify-node](https://github.com/nodegit/promisify-node)

[async-to-q.js](https://gist.github.com/wavded/6116786)
[Asynchronous JavaScript Interfaces](http://medikoo.com/asynchronous-javascript-interfaces/)
[JavaScript Promises: There and back again - HTML5 Rocks](http://www.html5rocks.com/en/tutorials/es6/promises/)
[Making Change.org — Promises and Error Handling](http://making.change.org/post/69613524472/promises-and-error-handling)
[Promise nuggets](http://promise-nuggets.github.io/)
[Promises and design patterns in AngularJS | Xebia Blog](http://blog.xebia.com/2014/02/23/promises-and-design-patterns-in-angularjs/)
[Promises in Node.js with Q – An Alternative to Callbacks - StrongLoop](http://blog.strongloop.com/promises-in-node-js-with-q-an-alternative-to-callbacks/)
[How-to Compose Node.js Promises with Q - StrongLoop](http://blog.strongloop.com/how-to-compose-node-js-promises-with-q/)
[Why I am switching to promises](http://spion.github.io/posts/why-i-am-switching-to-promises.html)
[Promises + FP = Beautiful Streams - Tech.pro](http://tech.pro/blog/6888/promises--fp--beautiful-streams)
[From callback to (Future -> Functor -> Monad) - Tech.pro](http://tech.pro/blog/6742/callback-to-future-functor-applicative-monad)

## generators

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

## strict mode

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/Strict_mode
http://howardabrams.com/presentations/?use-strict
http://stackoverflow.com/a/15251160/665507

## ES6

[Six Steps for Approaching the Next JavaScript -Telerik Developer Network](http://developer.telerik.com/featured/six-steps-for-approaching-the-next-javascript/)

[ES6 In Depth Articles ✩ Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/category/es6-in-depth/)
[ECMAScript 6: New Features: Overview and Comparison](http://es6-features.org/)
[Learn Harmony -- Home](http://learnharmony.org/)
[Exploring ES6: Upgrade to the next version of JavaScript](http://exploringjs.com/)
[Learn ES2015 · Babel](https://babeljs.io/docs/learn-es2015/)
[Tagtree course: Expert ES6](http://tagtree.tv/courses/expert-es6)
[jQuery UK - EcmaScript 6 - Google Slides](https://docs.google.com/presentation/d/1PvAHvODY_L3AiumgyjNFl4IPr82dq74vJxmMPOeU8uE/edit#slide=id.p)
[ES6: What are the benefits of the new features in practice? | CodeUtopia](http://codeutopia.n## ES6et/blog/2015/01/06/es6-what-are-the-benefits-of-the-new-features-in-practice/)
[ECMAScript 6 Power Tutorial - Tuts+ Code Tutorials](http://code.tutsplus.com/series/ecmascript-6-power-tutorial--cms-833)

[Using ECMAScript 6 today](http://www.2ality.com/2014/08/es6-today.html)
[A guide to 2ality’s posts on ECMAScript.next/ECMAScript 6](http://www.2ality.com/2012/11/guide-esnext.html)
[ECMAScript.next: for-of, iterators, generators](http://www.2ality.com/2012/06/for-of-ff13.html)
[ECMAScript 6: new OOP features besides classes](http://www.2ality.com/2014/12/es6-oop.html)
[Classes in ECMAScript 6 (final semantics)](http://www.2ality.com/2015/02/es6-classes-final.html)

[StrongLoop | Getting Started with JavaScript ES6 Object Notation](https://strongloop.com/strongblog/javascript-es6-object-notation/)
[StrongLoop | Getting Started with JavaScript ES6 Destructuring](https://strongloop.com/strongblog/getting-started-with-javascript-es6-destructuring/)
[Why Destructuring is a Terrible Idea in ES6 | Thomas R Alexander](http://teeohhem.com/why-destructuring-is-a-terrible-idea-in-es6/)

[You searched for ecmascript 6 - SitePoint](http://www.sitepoint.com/?s=ecmascript+6)

[lukehoban/es6features](https://github.com/lukehoban/es6features#readme)
[sindresorhus/esnext-showcase](https://github.com/sindresorhus/esnext-showcase)

[Standard ECMA-262](http://www.ecma-international.org/publications/standards/Ecma-262.htm)

[ECMAScript 6 compatibility table](http://kangax.github.io/compat-table/es6/)

### Promise

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

[Introduction to ES6 Promises – The Four Functions You Need To Avoid Callback Hell | James K Nelson](http://jamesknelson.com/grokking-es6-promises-the-four-functions-you-need-to-avoid-callback-hell/)
[Promise - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
[We have a problem with promises](http://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html)
- don't use 2nd param of `then()`, trailing `catch()` is better in all cases
- passing `then()` non-function will cause the previous promise's result to fall through

```js
new Promise((function(resolve, reject){})
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

### workflow

[Traceur, Gulp, Browserify and ES6 - Matt Greer](http://www.mattgreer.org/articles/traceur-gulp-browserify-es6/)
[Practical Workflows for ES6 Modules](http://guybedford.com/practical-workflows-for-es6-modules)
[addyosmani/es6-tools](https://github.com/addyosmani/es6-tools)
[DailyJS: Transpilers: This Time It's Different](http://dailyjs.com/2015/02/26/babel/)
[Choose ES6 modules Today! -Telerik Developer Network](http://developer.telerik.com/featured/choose-es6-modules-today/)

[Setting up an ES6 Project Using Babel and Browserify](http://www.sitepoint.com/setting-up-es6-project-using-babel-browserify/)

### transpilers

[Babel · The transpiler for writing next generation JavaScript](http://babeljs.io/)
[google/traceur-compiler](https://github.com/google/traceur-compiler)
[facebook/jstransform](https://github.com/facebook/jstransform)
[esnext - Tomorrow’s JavaScript syntax today](http://esnext.github.io/esnext/#)
[ECMAScript 6 compatibility table](http://kangax.github.io/compat-table/es6/)

[Setting up an ES6 Project Using Babel and Browserify](http://www.sitepoint.com/setting-up-es6-project-using-babel-browserify/)

### template strings

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

### class and inheritance 

[Simple JavaScript Inheritance: What You Need to Know - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/simple-javascript-inheritance-what-you-need-to-know--cms-24144)
[Understanding ECMAScript 6: Class and Inheritance](http://www.sitepoint.com/understanding-ecmascript-6-class-inheritance/)

[christianalfoni - Think twice about ES6 classes](http://www.christianalfoni.com/articles/2015_01_01_Think-twice-about-ES6-classes)

## ES7

[Taming the asynchronous beast with ES7](http://pouchdb.com/2015/03/05/taming-the-async-beast-with-es7.html)

## modules

[Declaring module exports (Node.js, AMD)](http://www.2ality.com/2012/04/declaring-module-exports.html)
[Understanding ES6 Modules](http://www.sitepoint.com/understanding-es6-modules/)
[ECMAScript 6 modules: the final syntax](http://www.2ality.com/2014/09/es6-modules-final.html)
[JavaScript Modules the ES6 Way ◆ 24 ways](http://24ways.org/2014/javascript-modules-the-es6-way/)
[Choose ES6 modules Today! -Telerik Developer Network](http://developer.telerik.com/featured/choose-es6-modules-today/)
[JavaScript Module Pattern: In-Depth](http://www.adequatelygood.com/JavaScript-Module-Pattern-In-Depth.html)

## functional programming

[Functional Programming in Javascript === Garbage « Thomas Reynolds](http://awardwinningfjords.com/2014/04/21/functional-programming-in-javascript-equals-garbage.html)
[functional js](http://fogus.github.io/lemonad/)
[baconjs/bacon.js](https://github.com/baconjs/bacon.js)
[FredyC/promised-land](https://github.com/FredyC/promised-land/)
[Understanding recursion in functional JavaScript programming](http://www.integralist.co.uk/posts/js-recursion.html)
[jussi-kalliokoski/trine](https://github.com/jussi-kalliokoski/trine)

## property, prototypal inheritance

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

[Object Playground: The Definitive Guide to Object-Oriented JavaScript](http://www.objectplayground.com/)

[JavaScript: __proto__](http://www.2ality.com/2012/10/proto.html)
[Object properties in JavaScript](http://www.2ality.com/2012/10/javascript-properties.html)
[Properties in JavaScript: definition versus assignment](http://www.2ality.com/2012/08/property-definition-assignment.html)
[JavaScript terminology: the two prototypes](http://www.2ality.com/2013/01/two-prototypes.html)
[JavaScript properties: inheritance and enumerability](http://www.2ality.com/2011/07/js-properties.html)
[JavaScript inheritance by example](http://www.2ality.com/2012/01/js-inheritance-by-example.html)
[JavaScript inheritance: beyond the basics (video)](http://www.2ality.com/2012/11/js-inheritance-beyond-basics.html)
[Property assignment and the prototype chain](http://www.2ality.com/2012/11/property-assignment-prototype-chain.html)
[A closer look at _.extend and copying properties](http://www.2ality.com/2012/08/underscore-extend.html)

[Learning Javascript with Object Graphs (Part I) - How To Node - NodeJS](http://howtonode.org/object-graphs)
[Learning Javascript with Object Graphs (Part II) - How To Node - NodeJS](http://howtonode.org/object-graphs-2)
[Learning Javascript with Object Graphs (Part III) - How To Node - NodeJS](http://howtonode.org/object-graphs-3)
[Prototypal Inheritance - How To Node - NodeJS](http://howtonode.org/prototypical-inheritance)

[Inheritance and the prototype chain - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
[Prototypal Inheritance](http://javascript.crockford.com/prototypal.html)
[Learning JavaScript Design Patterns](http://addyosmani.com/resources/essentialjsdesignpatterns/book/#prototypepatternjavascript)

http://ejohn.org/blog/simple-javascript-inheritance/
http://phrogz.net/JS/classes/OOPinJS.html  
http://phrogz.net/JS/classes/OOPinJS2.html  
http://metaduck.com/05-dump-this.html

## information hiding (private member)

http://www.crockford.com/javascript/private.html

// proper inheritance  
http://metaduck.com/08-module-pattern-inheritance.html

## functions

function become method automatically  
bound method: instance method  
unbound method: class method

