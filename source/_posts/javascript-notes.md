title: Javascript notes
toc: true
date: 2014-12-11 17:04:13
tags:
- javascript
- notes
---

```javascript
// delete n elements at index i, insert args at that position
[].splice(i, n, [, arg1[, arg2[, ...]]])

// convert arguments to true Array
[].slice.call(arguments);

// bind() returns a new function
f2 = f1.bind(thisArg[, arg1[, arg2[, ...]]])
f1.call(thisArg[, arg1[, arg2[, ...]]])
```

### protoypal inheritance

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
