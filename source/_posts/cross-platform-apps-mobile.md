title: "Cross Platform Apps"
date: 2015-04-03 13:01:12
categories:
- app
tags:
- cordova
- phonegap
- ionic
- crosswalk
- nativescript
- titanium
- react-native
toc: true
---

[Cross-platform - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Cross-platform)

It is difficult to develop and maintain apps which support multiple mobile platforms. Luckily there are abstraction layers which developers can write code on and deploy to multiple platforms.

```
     |================|================|
  web apps       hybrid apps      native apps
```

With "hybrid apps", we can use the abstraction layer for fast development and the native SDK for performance critical modules to get the best of both world.

The abstraction layer is *usually* HTML5 which is to be run on a browser. There will also be API's on the abstraction SDK to call native APIs.

<!-- more -->

> TODO: merge `md-wiki/mobile-html5-app.md` here
> TODO: merge `Cross-platform App Tools for Consumer and Enterprise Market.ppt` here

[Pros and Cons of the Top 5 Cross-Platform Tools - Developer Economics](http://www.developereconomics.com/pros-cons-top-5-cross-platform-tools/)
[Tools to Build your Mobile App | Developer Economics](http://www.developereconomics.com/search/tools/to/build/#q//sector/47/license//technology//platform//app_category//p/1)
[Native vs HTML5 - You're Asking The Wrong Question](http://blogs.telerik.com/platform/posts/14-02-21/native-vs-html5---you're-asking-the-wrong-question)
[Hybrid vs. Native: Choosing a Mobile Strategy](http://www.infoq.com/presentations/hybrid-native-mobile-strategy)
[android - Struggling between native and phonegap, simple app requirements - Stack Overflow](http://stackoverflow.com/questions/14065610/struggling-between-native-and-phonegap-simple-app-requirements)
[Web vs. native: let’s concede defeat - QuirksBlog](http://www.quirksmode.org/blog/archives/2015/05/web_vs_native_l.html)

[Cross-Platform Developer Tools 2012 - VisionMobile](http://www.visionmobile.com/blog/2012/02/crossplatformtools/)

## In the Wild

[How photo app Polarr topped the App Store the uncommon way - CNET](http://www.cnet.com/news/how-photo-app-polarr-topped-the-app-store-the-uncommon-way/)
[HTML5 is dead. Long live HTML5! - CNET](http://www.cnet.com/news/html5-is-dead-long-live-html5/)

## PhoneGap/Cordova

[PhoneGap API Documentation](http://docs.phonegap.com/en/edge/index.html)
[apache/cordova-cli](https://github.com/apache/cordova-cli)

[Phonegap/Cordova Workshop](http://wrenr.github.io/cordova-workshop/#/)
[JS.LA - Native Mobile Apps in JS - Just Add Cordova!](http://wrenr.github.io/jsla-cordova-2015-08/#/)

[Phonegap/Cordova vs Native Application](http://www.slideshare.net/hakimrie/phonegapcordova-vs-native-application)
[Phonegap vs Native - A 12 Month Review » Chel Ramsey Productions](http://chelramsey.com/series/phonegap-vs-native-a-12-month-review/) (2013)
[Cordova : Devgirl's Weblog](http://devgirl.org/category/cordova/)
[2 Quick Tips When Adding PhoneGap/Cordova Plugins : Devgirl's Weblog](http://devgirl.org/2014/07/15/2-quick-tips-when-adding-phonegapcordova-plugins/)

[Verified Plugins Marketplace | Cordova/PhoneGap Plugins](http://plugins.telerik.com/cordova)

### Adobe PhoneGap v Apache Cordova

PhoneGap was purchased by Adobe in 2011. Adobe donated PhoneGap to Apache Foundation and it was renamed to Cordova.
Adobe retained the trademark of PhoneGap and provide service around it.

[The Last Word on Cordova and PhoneGap | The Official Ionic Blog](http://blog.ionic.io/what-is-cordova-phonegap/)
[Cordova and PhoneGap Insights](http://www.slideshare.net/monaca_mobi/cordova-and-phone-gap)
[Cordova/PhoneGap Version Confusion : Devgirl's Weblog](http://devgirl.org/2014/11/07/cordovaphonegap-version-confusion/)
[cordova-coho/versioning-and-release-strategy.md at master · apache/cordova-coho](https://github.com/apache/cordova-coho/blob/master/docs/versioning-and-release-strategy.md)

### Ionic Framework

[Ionic: Advanced HTML5 Hybrid Mobile App Framework](http://ionicframework.com/)
[Learn Ionic](http://learn.ionicframework.com/)

Ionic Framework includes
- UI widget (can also be used for web apps)
- Angular seed
- `ionic`: CLI program for testing and deploy (`cordova` wrapper)
- [ngCordova](http://ngcordova.com/): Angular binding to common Cordova Plugins

The Ionic Framework Team has good relation with Angular Team and will support Angular 2 with Ionic 2.

### Manifold

[Manifold JS](http://www.manifoldjs.com/)

Converts your website to an "app", uses Cordova/Crosswalk as polyfill if needed.

[Simplify Android Development Using manifoldJS With Crosswalk - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/simplify-android-development-using-manifoldjs-with-crosswalk--cms-24790)

### Crosswalk

Embedding the latest Chromium WebView to your app instead of using the system's WebView.

[Crosswalk - Cordova](https://crosswalk-project.org/documentation/cordova.html)

## React Native

Write React JSX and deploy to iOS abd Android.
[React Native | A framework for building native apps using React](http://facebook.github.io/react-native/)
[facebook/react-native](https://github.com/facebook/react-native)

[Use React Native: site and newsletter](http://www.reactnative.com/)
[First Impressions using React Native - James Long](http://jlongster.com/First-Impressions-using-React-Native)
[Introducing React Native: Building Apps with JavaScript](http://www.raywenderlich.com/99473/introducing-react-native-building-apps-javascript)
[React Native for Android: How we built the first cross-platform React Native app | Engineering Blog | Facebook Code | Facebook](https://code.facebook.com/posts/1189117404435352/)
[zmxv: What I learned from building a React Native app](http://blog.zmxv.com/2015/09/what-i-learned-from-building-react.html)
[Why React Native is Different](http://jlongster.com/Why-React-Native-is-Different)

## NativeScript

[Cross-Platform Native Development with Javascript](https://www.nativescript.org/)
[Docs](http://docs.nativescript.org/) [source](https://github.com/NativeScript/docs)
[Docs: Android](http://docs.nativescript.org/runtimes/android/)
[Docs: iOS](http://docs.nativescript.org/runtimes/ios)

[Creating Mobile Native Apps in JavaScript with NativeScript](http://www.infoq.com/news/2015/03/nativescript)
[Building a Native App with JavaScript Using NativeScript](http://www.sitepoint.com/building-native-app-javascript-using-nativescript)

[NativeScript – a Technical Overview - Telerik Developer NetworkTelerik Developer Network](http://developer.telerik.com/featured/nativescript-a-technical-overview/)
[On NativeScript for Android - Telerik Developer NetworkTelerik Developer Network](http://developer.telerik.com/featured/nativescript-android/)
[How NativeScript Works -Telerik Developer Network](http://developer.telerik.com/featured/nativescript-works/)
[Styling Native Apps with CSS -Telerik Developer Network](http://developer.telerik.com/featured/styling-native-apps-css/)
[Getting Started with NativeScript -Telerik Developer Network](http://developer.telerik.com/featured/getting-started-nativescript/)
[Building Your Own NativeScript Modules for npm -Telerik Developer Network](http://developer.telerik.com/featured/building-your-own-nativescript-modules-for-npm/)

## Haxe

[Haxe - The Cross-platform Toolkit](http://haxe.org/)

> Haxe is an open source toolkit based on a modern, high level, strictly typed programming language, a cross-compiler, a complete cross-platform standard library and ways to access each platform's native capabilities.

The language itself is similar to JavaScript. The `.hx` can be compiled to [multiple targets](http://haxe.org/documentation/introduction/compiler-targets.html).
[Standard libraries](http://haxe.org/documentation/introduction/stdlib-introduction.html) are separated to three categories: standard, system and target specific. A package manager [Haxelib](http://lib.haxe.org/) is available.
[Haxe Manual](http://haxe.org/manual/)
[Haxe API](http://api.haxe.org/)

[haxe: compile time macros](http://notes.underscorediscovery.com/haxe-compile-time-macros/)
[Haxe from 1000ft](http://notes.underscorediscovery.com/haxe-from-1000ft/)
[Haxe Entry Point](http://notes.underscorediscovery.com/haxe-entry-point/)
[Learn Haxe](http://haxe.us/haxe_tutorial.html)

[OpenFL - Creative expression for desktop, mobile, web and console platforms](http://www.openfl.org/)

## Qt

[Qt - Product - Qt Quick](http://www.qt.io/qt-quick/)
[Qt - Qt for Mobile App Development](http://www.qt.io/mobile-app-development/)

[Qt Quick 5.4](http://doc.qt.io/qt-5/qtquick-index.html)
[Qt QML 5.4](http://doc.qt.io/qt-5/qtqml-index.html)
[QML Applications | Qt 5.4](http://doc.qt.io/qt-5/qmlapplications.html)

Paypal's Seif App binds Node.js to Qt
[The Seif Project - Douglas Crockford - YouTube](https://youtu.be/FHRXPlq9XNw?t=306)

## Xamarin

[Mobile Application Development to Build Apps in C# - Xamarin](http://xamarin.com/platform)

[Under The Hood - Xamarin](http://developer.xamarin.com/guides/android/under_the_hood/)
[iOS Under The Hood - Xamarin](http://developer.xamarin.com/guides/ios/under_the_hood/)

## Appcelerator

[Products | Appcelerator Inc.](http://www.appcelerator.com/product/)

[Getting To Know Alloy (Part One)](http://www.appcelerator.com/blog/2012/11/gtka-one/)
[Getting To Know Alloy (Part Two)](http://www.appcelerator.com/blog/2012/11/gtka-two/)

## Honorable Mentions

[MoSync](http://www.mosync.com/)
[RhoMobile Suite](http://rhomobile.com/)
