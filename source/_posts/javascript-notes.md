title: Javascript notes
date: 2014-12-11 17:04:13
categories:
- comp.lang
tags:
- javascript
- notes
toc: true
---

### tricks

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

[A guide to 2ality’s posts on the JavaScript language](http://www.2ality.com/2012/08/guide-jslang.html)
> refer to its categorization

### style

[Brace styles and JavaScript](http://www.2ality.com/2013/01/brace-styles.html)
[Video: JavaScript coding tips](http://www.2ality.com/2014/08/javascript-coding-tips.html)

### types

[12 JavaScript quirks](http://www.2ality.com/2013/04/12quirks.html)
[JavaScript’s type system](http://www.2ality.com/2013/09/types.html)
[Categorizing values in JavaScript](http://www.2ality.com/2013/01/categorizing-values.html)
[JavaScript: fixing categorization](http://www.2ality.com/2013/02/isinstance.html)
[Coercing objects to primitives](http://www.2ality.com/2012/11/coercing-objects.html)

[Statically typed JavaScript via Microsoft TypeScript, Facebook Flow and Google AtScript](http://www.2ality.com/2014/10/typed-javascript.html)

Objects are like map, but see [The pitfalls of using objects as maps in JavaScript](http://www.2ality.com/2012/01/objects-as-maps.html).

[ECMAScript 6: maps and sets](http://www.2ality.com/2015/01/es6-maps-sets.html)
[ECMAScript 6 sets: union, intersection, difference](http://www.2ality.com/2015/01/es6-set-operations.html)


### syntax

[Expressions versus statements in JavaScript](http://www.2ality.com/2012/09/expressions-vs-statements.html)

### scoping

[JavaScript variable scoping and its pitfalls](http://www.2ality.com/2011/02/javascript-variable-scoping-and-its.html)
[Variable declarations: three rules you can break](http://www.2ality.com/2012/11/var-statement-rules.html)

### flow control

[Asynchronous programming and continuation-passing style in JavaScript](http://www.2ality.com/2012/06/continuation-passing-style.html)

> add promise and generator

### CSP

[CSP and transducers in JavaScript](http://phuu.net/2014/08/31/csp-and-transducers.html)
[ubolonton/js-csp](https://github.com/ubolonton/js-csp)

### promise

[Asynchronous JavaScript Interfaces](http://medikoo.com/asynchronous-javascript-interfaces/)
[async-to-q.js](https://gist.github.com/wavded/6116786)
[duereg-songbird · GitHub](https://github.com/duereg/songbird)
[FredyC-promised-land · GitHub](https://github.com/FredyC/promised-land/)
[How-to Compose Node.js Promises with Q - StrongLoop](http://blog.strongloop.com/how-to-compose-node-js-promises-with-q/)
[JavaScript Promises: There and back again - HTML5 Rocks](http://www.html5rocks.com/en/tutorials/es6/promises/)
[Making Change.org — Promises and Error Handling](http://making.change.org/post/69613524472/promises-and-error-handling)
[petkaantonov-bluebird · GitHub](https://github.com/petkaantonov/bluebird)
[Promise nuggets](http://promise-nuggets.github.io/)
[Promises and design patterns in AngularJS | Xebia Blog](http://blog.xebia.com/2014/02/23/promises-and-design-patterns-in-angularjs/)
[Promises in Node.js with Q – An Alternative to Callbacks - StrongLoop](http://blog.strongloop.com/promises-in-node-js-with-q-an-alternative-to-callbacks/)
[Why I am switching to promises](http://spion.github.io/posts/why-i-am-switching-to-promises.html)
[JavaScript Promises: There and back again - HTML5 Rocks](http://www.html5rocks.com/en/tutorials/es6/promises/)

### generators

[The Definitive Guide to the JavaScript Generators](http://gajus.com/blog/2/the-definetive-guide-to-the-javascript-generators)
[Analysis of generators and other async patterns in node](http://spion.github.io/posts/analysis-generators-and-other-async-patterns-node.html)
[ES6 Generators Deliver Go Style Concurrency](http://swannodette.github.io/2013/08/24/es6-generators-and-csp/)
[Generators: the Gnarly Bits](http://updates.html5rocks.com/2014/10/Generators-the-Gnarly-Bits)
[Generators vs Fibers - How To Node - NodeJS](http://howtonode.org/generators-vs-fibers)
[How should I format the ECMAScript 6 generator asterisk?](http://www.2ality.com/2014/08/formatting-generator-asterisk.html)
[Introduction to Generators & Koa.js - Tuts+ Code Tutorials](http://code.tutsplus.com/series/introduction-to-generators-koajs--cms-690)
[StrongLoop | Generators in Node.js: Common Misconceptions and Three Good Use Cases](http://strongloop.com/strongblog/how-to-generators-node-js-yield-use-cases/)
[Generators Are Like Arrays](https://gist.github.com/jkrems/04a2b34fb9893e4c2b5c)


### ES6

[ECMAScript 6 compatibility table](http://kangax.github.io/compat-table/es6/)
[A guide to 2ality’s posts on ECMAScript.next/ECMAScript 6](http://www.2ality.com/2012/11/guide-esnext.html)
[Video: An overview of ECMAScript 6](http://www.2ality.com/2013/06/video-es6.html)
[Four talks on ECMAScript 6/ECMAScript.next](http://www.2ality.com/2012/11/es6-talks.html)
[ECMAScript.next: for-of, iterators, generators](http://www.2ality.com/2012/06/for-of-ff13.html)
[ECMAScript 6: new OOP features besides classes](http://www.2ality.com/2014/12/es6-oop.html)
[sindresorhus/esnext-showcase](https://github.com/sindresorhus/esnext-showcase)


#### workflow

[Traceur, Gulp, Browserify and ES6 - Matt Greer](http://www.mattgreer.org/articles/traceur-gulp-browserify-es6/)
[Practical Workflows for ES6 Modules](http://guybedford.com/practical-workflows-for-es6-modules)
[addyosmani/es6-tools](https://github.com/addyosmani/es6-tools)

#### transpilers

[google/traceur-compiler](https://github.com/google/traceur-compiler)
[6to5 · Turn ES6+ code into readable vanilla ES5](http://6to5.org/)
[esnext - Tomorrow’s JavaScript syntax today](http://esnext.github.io/esnext/#)
[ECMAScript 6 compatibility table](http://kangax.github.io/compat-table/es6/)

#### template strings

[Using ES6 template strings for regular expressions](http://www.2ality.com/2012/12/template-strings-xregexp.html)
[HTML templating with ES6 template strings](http://www.2ality.com/2015/01/template-strings-html.html)
[Template strings: embedded DSLs in ECMAScript 6](http://www.2ality.com/2011/09/quasi-literals.html)
[A closer look at Underscore templates](http://www.2ality.com/2012/06/underscore-templates.html)
[Getting Literal With ES6 Template Strings](http://updates.html5rocks.com/2015/01/ES6-Template-Strings)

### modules

[Declaring module exports (Node.js, AMD)](http://www.2ality.com/2012/04/declaring-module-exports.html)

### functional programming

[Functional Programming in Javascript === Garbage « Thomas Reynolds](http://awardwinningfjords.com/2014/04/21/functional-programming-in-javascript-equals-garbage.html)
[Read JavaScript Allongé | Leanpub](https://leanpub.com/javascript-allonge/read)

### property, protoypal inheritance

[JavaScript: __proto__](http://www.2ality.com/2012/10/proto.html)
[Object properties in JavaScript](http://www.2ality.com/2012/10/javascript-properties.html)
[Properties in JavaScript: definition versus assignment](http://www.2ality.com/2012/08/property-definition-assignment.html)
[JavaScript terminology: the two prototypes](http://www.2ality.com/2013/01/two-prototypes.html)
[JavaScript properties: inheritance and enumerability](http://www.2ality.com/2011/07/js-properties.html)
[JavaScript inheritance by example](http://www.2ality.com/2012/01/js-inheritance-by-example.html)
[JavaScript inheritance: beyond the basics (video)](http://www.2ality.com/2012/11/js-inheritance-beyond-basics.html)
[Property assignment and the prototype chain](http://www.2ality.com/2012/11/property-assignment-prototype-chain.html)
[A closer look at _.extend and copying properties](http://www.2ality.com/2012/08/underscore-extend.html)

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain
http://javascript.crockford.com/prototypal.html
http://addyosmani.com/resources/essentialjsdesignpatterns/book/#prototypepatternjavascript
http://ejohn.org/blog/simple-javascript-inheritance/
http://howtonode.org/prototypical-inheritance
http://www.2ality.com/2012/01/js-inheritance-by-example.html
http://phrogz.net/JS/classes/OOPinJS.html  
http://phrogz.net/JS/classes/OOPinJS2.html  
http://metaduck.com/05-dump-this.html

### information hiding (private member)

http://www.crockford.com/javascript/private.html

// proper inheritance  
http://metaduck.com/08-module-pattern-inheritance.html

### functions

function become method automatically  
bound method: instance method  
unbound method: class method

# references

[Resources – JS Central](http://www.jscentral.org/resources.html)
