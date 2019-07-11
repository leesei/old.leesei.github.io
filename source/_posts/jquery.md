---
title: jQuery
categories:
  - comp.lang
tags:
  - jquery
toc: true
date: 2016-04-12 11:09:37
---

[jQuery](https://jquery.com/)

[alvarotrigo jquery](http://alvarotrigo.com/blog/category/jquery/)

## Alternatives

[Zepto.js: the aerogel-weight jQuery-compatible JavaScript library](http://zeptojs.com/)
[Miq JavaScript library](http://www.bitstorm.org/javascript/miq/)

[You Might Not Need jQuery](http://youmightnotneedjquery.com/)
[oneuijs/You-Dont-Need-jQuery: Examples of how to do query, style, dom, ajax, event etc like jQuery with plain javascript.](https://github.com/oneuijs/You-Dont-Need-jQuery)
[jQuery considered harmful | Lea Verou](http://lea.verou.me/2015/04/jquery-considered-harmful/)
[You Don't Need jQuery! – Free yourself from the chains of jQuery by embracing and understanding the modern Web API and discovering various directed libraries to help you fill in the gaps.](http://blog.garstasio.com/you-dont-need-jquery/)

## Plugins

[jQuery Plugin Registry](http://plugins.jquery.com/) read-only mode
[npm "jquery-plugin"](https://www.npmjs.com/browse/keyword/jquery-plugin)

### layout

[kudago/waterfall: Waterfall layout. Extremely fast lightweight version of fluid columns masonry layout of isotope.](https://github.com/kudago/waterfall)

[Isotope v2](https://isotope.metafizzy.co/v2/)

### widgets

[wiringtheworld/Snarl: Growl style notifications for your web app.](https://github.com/wiringtheworld/Snarl)
[Modaal is a WCAG 2.0 Level AA accessible modal plugin](http://humaan.com/modaal/)
[jQuery Animated Typing with Typed.js | by Matt Boldt](http://www.mattboldt.com/demos/typed-js/)

## Tips and Tricks

### Move cursor to end of input

```js
//usage
moveCursorToEnd($('input'));
 
//function
function moveCursorToEnd(input) {
    var originalValue = input.val();
    input.val('');
    input.blur().focus().val(originalValue);
}
```
