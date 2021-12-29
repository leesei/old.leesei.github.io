---
title: Immutability
toc: true
date: 2015-12-04 12:13:25
categories:
  - web
tags:
  - immutability
  - javascript
  - web-dev
---

> Most of the study gears towards JavaScript/web development

## Immutability

Immutable app state probably will help you to enforce mutation from single component. Passing snapshot of the immutable state as props to child allows you to define your component as "pure" to boost performance.

A naive implementation of immutability is to a deep clone the original data, then return the mutated copy.  
A more performant implementation is to use [persistent data structure](https://www.wikiwand.com/en/Persistent_data_structure) (structural sharing), where only the mutated fields and the nodes reaching from the root to the field have to be updated.

[Immutable object - Wikiwand](https://www.wikiwand.com/en/Immutable_object)
[Persistent data structure - Wikiwand](https://www.wikiwand.com/en/Persistent_data_structure)
[Trie - Wikiwand](https://www.wikiwand.com/en/Trie)

[List of immutable libraries](https://gist.github.com/jlongster/bce43d9be633da55053f)
[immutable-data.md · markerikson/redux-ecosystem-links](https://github.com/markerikson/redux-ecosystem-links/blob/master/immutable-data.md#immutable-update-utilities)

[Immutable.js](https://facebook.github.io/immutable-js/) structural sharing
[arqex/freezer](https://github.com/arqex/freezer)
[rtfeldman/seamless-immutable](https://github.com/rtfeldman/seamless-immutable) no structural sharing
[kolodny/immutability-helper: mutate a copy of data without changing the original source](https://github.com/kolodny/immutability-helper) no structural sharing
[debitoor/dot-prop-immutable: Immutable version of dot-prop with some extensions](https://github.com/debitoor/dot-prop-immutable)
[mariocasciaro/object-path-immutable: Modify deep object properties without modifying the original object (immutability). Works great with React and Redux.](https://github.com/mariocasciaro/object-path-immutable)
[Gozala/typed-immutable](https://github.com/gozala/typed-immutable)
[mori](http://swannodette.github.io/mori/) structural sharing
[scottcorgan/immu](https://github.com/scottcorgan/immu)
[substantial/updeep: Easily update nested frozen objects and arrays in a declarative and immutable manner.](https://github.com/substantial/updeep) utilize `lodash`, no structural sharing

[Introduction to Immutable.js and Functional Programming Concepts](https://auth0.com/blog/2016/03/23/intro-to-immutable-js/)
[Introduction to Immutable.js | Zsolt Nagy](http://www.zsoltnagy.eu/introduction-to-immutable-js/)
[02-immutable.js](https://www.jfokus.se/jfokus16/preso/JavaScript-Immutability--Dont-Go-Changing.pdf) (PDF)

[Immutability is not enough](https://codewords.recurse.com/issues/six/immutability-is-not-enough) functional steps have dependency => effect systems
[The Dao of Immutability — JavaScript Scene — Medium](https://medium.com/javascript-scene/the-dao-of-immutability-9f91a70c88cd)
[Immutability in JavaScript](http://www.sitepoint.com/immutability-javascript/)
[Immutable Javascript using ES6 and beyond](https://wecodetheweb.com/2016/02/12/immutable-javascript-using-es6-and-beyond/)
[Immutable Data from Scratch - RYANFUNDUK.COM](https://ryanfunduk.com/articles/immutable-data-from-scratch/)
[Immutable Data Structures and JavaScript](http://jlongster.com/Using-Immutable-Data-Structures-in-JavaScript)

[React.js Conf 2015 - Immutable Data and React - YouTube](https://www.youtube.com/watch?v=I7IdS-PbEgI) use trie to implement the map and list interfaces
[Immutable User Interfaces (Lee Byron) - Full Stack Fest 2016 - YouTube](https://www.youtube.com/watch?v=pLvrZPSzHxo)
