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
toc: true
---

It is difficult to develop and maintain apps which support multiple mobile platforms. Luckily there are abstraction layers which developers can write code on and deploy to multiple platforms.

```
     |================|================|
  web apps       hybrid apps      native apps
```

With "hybrid apps", we can use the abstraction layer for fast development and the native SDK for performance critical modules to get the best of both world.

The abstraction layer is *usually* HTML5 which is to be run on a browser. There will also be API's on the abstraction SDK to call native APIs.

[Pros and Cons of the Top 5 Cross-Platform Tools - Developer Economics](http://www.developereconomics.com/pros-cons-top-5-cross-platform-tools/)
[Tools to Build your Mobile App | Developer Economics](http://www.developereconomics.com/search/tools/to/build/#q//sector/47/license//technology//platform//app_category//p/1)
[Native vs HTML5 - You're Asking The Wrong Question](http://blogs.telerik.com/platform/posts/14-02-21/native-vs-html5---you're-asking-the-wrong-question)
[android - Struggling between native and phonegap, simple app requirements - Stack Overflow](http://stackoverflow.com/questions/14065610/struggling-between-native-and-phonegap-simple-app-requirements)

## PhoneGap/Cordova

[PhoneGap API Documentation](http://docs.phonegap.com/en/edge/index.html)
[apache/cordova-cli](https://github.com/apache/cordova-cli)

[Phonegap/Cordova vs Native Application](http://www.slideshare.net/hakimrie/phonegapcordova-vs-native-application)
[Phonegap vs Native - A 12 Month Review » Chel Ramsey Productions](http://chelramsey.com/series/phonegap-vs-native-a-12-month-review/) (2013)
[Cordova : Devgirl's Weblog](http://devgirl.org/category/cordova/)
[2 Quick Tips When Adding PhoneGap/Cordova Plugins : Devgirl's Weblog](http://devgirl.org/2014/07/15/2-quick-tips-when-adding-phonegapcordova-plugins/)

### Adobe PhoneGap v Apache Cordova

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

### Crosswalk

Embedding the latest Chromium WebView to your app instead of using the system's WebView.

[Crosswalk - Cordova](https://crosswalk-project.org/documentation/cordova.html)

## NativeScript

[Cross-Platform Native Development with Javascript](https://www.nativescript.org/)

[Creating Mobile Native Apps in JavaScript with NativeScript](http://www.infoq.com/news/2015/03/nativescript)

## Appcelerator Titanium

[Products | Appcelerator Inc.](http://www.appcelerator.com/product/)
