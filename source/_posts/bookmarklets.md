---
title: "Bookmarklets"
date: 2014-12-08 14:19:53
categories:
  - web
tags:
  - bookmarklet
  - browser
toc: true
---

Bookmarklets are bookmark of JavaScript code as the link (with protocol `javascript:`) that can be used to implement custom features inside browser.
They are simple ways to extend browser without resorting to browser extensions and plugins.
You can access `document` and `window` of the current page in the bookmarklet.
Useful properties includes:

- title
- URL
- DOM

[Bookmarkleteer: Create and Share Bookmarklets Online](http://bookmarkleteer.com/) (down), [source](https://github.com/coolaj86/bookmarkleteer)
[How To Make a Bookmarklet For Your Web Application | BetterExplained](http://betterexplained.com/articles/how-to-make-a-bookmarklet-for-your-web-application/)
[Implementing bookmarklets in JavaScript](http://www.2ality.com/2011/06/implementing-bookmarklets.html)

<!-- more -->

### Repository

[Bookmarklets | Bookmarklet Search Engine](http://marklets.com/)
[Ben Alman » Bookmarklets](http://benalman.com/projects/bookmarklets/)
[janmoesen/bookmarklets](https://github.com/janmoesen/bookmarklets)
[Bookmarklets](http://linkstore.ru/book/index-en.jsp)
[Jesse's Bookmarklets Site](https://www.squarefree.com/bookmarklets/)
[Bookmarklets - Tool Categories](http://www.bookmarklets.com/tools/categor.html)

### Creating bookmarklets

- Create any bookmark, edit it to change the title and paste the `javascript:` link as the url.
- Some services allows you to drag and drop a link to your bookmark bar to create the bookmarklet (the `javascript:` link is url-escaped).
- You may organize bookmarklets in fully documented `.js`
  - URL encode and minifiy it
  - use this to generate the link: (FIXME)

```sh
echo -n "javascript:"; uglifyjs --no-copyright file.js ; echo
```

- put them in Gist and use a loader, see [here](https://gist.github.com/ttscoff/5834741)

[Bookmarklets construction set - Create bookmarklets online](http://js.do/blog/bookmarklets/)
[Bookmarklet Crunchinator](http://ted.mielczarek.org/code/mozilla/bookmarklet.html)
[bookmarkleteer - Matt Gauger's bookmarklet maker](http://blog.mattgauger.com/bookmarkleteer/)

---

## Email Link

Generates a `mailto:` link with the webpage's URL and title.
I use this frequently to share links.
I registered Gmail to handle `mailto:` according to [this](http://webapps.stackexchange.com/a/33951).

```js Email Link
javascript: void window.open(
  "mailto:?SUBJECT=" + document.title + "&BODY=" + escape(location.href),
  "_blank",
  "width=628,left=" +
    screen.width * 0.5 +
    ",height=600,top=" +
    screen.height * 0.1 +
    ",resizable,scrollbars=no"
);
```

## Markdown Link

Creates a Markdown link `[]()` for the current page. Copy and paste to Markdown documents.

```js Markdown Link
javascript: prompt(
  "Markdown link for this page:",
  "[" + document.title + "](" + window.location.href + ")"
);
```

## Duplicate Tab

Duplicates this tab, useful for when you wish to change the url manually.

```js Duplicate Tab
javascript: void window.open(location.href);
```

## Up a Directory

I miss the "Up" button in file manager so I bring it to browser.

```js Up a Directory
javascript: void (location.href = location.href.substring(
  0,
  location.href.substring(0, location.href.length - 1).lastIndexOf("/") + 1
));
```

## Proxy via GAE

Sometime, someone blocks my access to website.
[mirrorrr](https://github.com/bslatkin/mirrorrr) to the rescue.

```js Proxy via GAE
javascript: void (location.href =
  "https://leesei-proxy.appspot.com/?url=" +
  encodeURIComponent(window.location.href));
```

## jQuerify

Loads [jQuery](http://jquery.com/) (from [Google CDN](https://developers.google.com/speed/libraries/devguide#jquery)) on any website, use Dev Console to play with it.

```js jQuerify
javascript:(function()%7B"use strict";function t()%7Bconsole.log("jQuery loaded!")%7Dvar e;e=document.createElement("script");e.addEventListener("load",t);e.src="//ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js";document.head.appendChild(e)%7D())
```

## GrabLinks

> Note: this is auto updateing as the bookmarklet loads the gist every time it is clicked.

List all the links in Markdown contained in the hovered portion of the page.
[GrabLinks - BrettTerpstra.com](http://brettterpstra.com/projects/grablinks/), [gist](https://gist.github.com/ttscoff/5834741).

Bookmarklet on website.

## Read Cookie

This is rudimentary, could have parsed it a little bit.
But why need this if we have DevTool?

```js Read Cookie
javascript: if (document.cookie.length < 1) {
  alert("No cookie for this site.");
} else {
  alert("Cookie for this site:\n" + document.cookie);
}
```

## Pocket

[Pocket: How to Save](https://getpocket.com/add)
[Pocket | Using the Pocket Bookmarklet](http://help.getpocket.com/customer/portal/articles/483627-using-the-pocket-bookmarklet)

Bookmarklet on website (click "install the bookmarklet").

## Google Bookmark

[Google Bookmarks - Chrome Help](https://support.google.com/chrome/answer/100215?hl=en)

Bookmarklet on website.

## BrowserPad

HTML5 `<contenteditable>` is a makeshift cross platform Notepad replacement.
A little styling makes it better.

```js BrowserPad
javascript: void window.open(
  "data:text/html, <html style='height: 100%'> <head> <title>BrowserPad</title><head> <body contenteditable style='background-color:#333; color: #ddd; font-family: courier; font-weight: bold'> </body> </html>",
  "_blank",
  "width=800,height=600"
);
```

## Transforming page

### Google Mobile View

This is an undocumented transformer by Google.

```js GWT
javascript: void window.open(
  "http://www.google.com/gwt/x?u=" + encodeURIComponent(window.location.href)
);
```

### Readability

[Readability](https://readability.com/) is a service that let you focus on the content of the webpage.
[heckyesmarkdown](http://heckyesmarkdown.com/#bookmarklets) provides wrapper around Readability's [API](https://readability.com/developers/api).

Bookmarklet on website.
Use "Readability→Markdown" for clean HTML or "Readability→Markdown (raw)" for Markdown.

### Print Friendly

[Print Friendly](http://www.printfriendly.com/) is a service provides a "print friendly" version of the webpage. It grabs the content intelligently, allow you to remove the unneed parts and save the result as PDF.

Bookmarklet on website.

## Video

### KeepVid

[KeepVid](http://keepvid.com/) is a service for downloading videos from various sites.
Personally I use [youtube-dl](http://rg3.github.io/youtube-dl/), but this is for non-technical people.

[KeepVid / Extensions](http://keepvid.com/extensions)

[KeepVid Bookmarklet | Bookmarklet Search Engine](http://marklets.com/KeepVid.aspx)

Bookmarklet on website.

### Extract Audio from video

[Dirpy](http://www.dirpy.com/) and [YouTube to mp3 Converter](http://www.youtube-mp3.org/) both do the job.

[Dirpy Bookmarklet | Bookmarklet Search Engine](http://marklets.com/Dirpy.aspx)

[Youtube MP3 Downloader Bookmarklet | Bookmarklet Search Engine](http://marklets.com/Youtube%20MP3%20Downloader.aspx)

Bookmarklet on website.

### YouTube Frames as Storyboard

Gernerate a storyboard of thumbnails of the video.

[How to Print a YouTube Video - Storyboard Bookmarklet](http://www.labnol.org/internet/print-youtube-video/28217/)
[YouTube Frames as Storyboard - YouTube](https://www.youtube.com/watch?v=Y6yfGGxXyHw)

Bookmarklet on website.

### YouTube Popup

[Open YouTube Videos in PopUp Window with a Bookmark · Amr Eldib](http://www.amreldib.com/blog/OpenYouTubeVideosInPopUpWindowWithBookmark/)
[Embed videos and playlists - YouTube Help](https://support.google.com/youtube/answer/171780)

```js
javascript: (function () {
  var url = window.location;
  if (url.origin.indexOf("www.youtube.com") == -1) {
    alert("Sorry, this is not a YouTube page! URL: " + url.href);
  } else {
    var width = "width=" + 600;
    var height = "height=" + 480;
    var left = "left=" + (screen.width - width) / 2;
    var top = "top=" + (screen.height - height) / 2;

    var query = window.location.search.substring(1);
    var vars = query.split("&");
    for (var i = 0; i < vars.length; i++) {
      var pair = vars[i].split("=");
      if (pair[0] == "v") {
        var videoId = pair[1];
      }
    }

    window.open(
      "http://www.youtube.com/embed/" + videoId,
      document.title,
      "location=no, directories=no, menubar=no, toolbar=no, scrollbars=no, status=no, resizable=yes, " +
        width +
        ", " +
        height +
        ", " +
        left +
        ", " +
        top
    );
  }
})();
```

### URL shortener

[is.gd - a URL shortener. Mmmm, tasty URLs!](http://is.gd/)
Bookmarklet on [FAQ](http://is.gd/faq.php#bookmarklet).

[硬是要縮 - 比 PPT 短網址更安全的縮網址服務](http://4fun.tw/)

[2lo.ng4.me - short urls](http://2lo.ng4.me/)

Bookmarklet on website.
