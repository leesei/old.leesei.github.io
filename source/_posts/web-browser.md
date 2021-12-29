---
title: "Web Browser"
categories:
  - web
toc: true
date: 2017-06-16 11:03:02
tags:
---

[Google Chrome](http://www.google.com/chrome/)
[Google Chrome book](https://www.google.com/googlebooks/chrome/big_00.html)

[Firefox](https://www.mozilla.org/en-US/firefox/products/)

[W3M Homepage](http://w3m.sourceforge.net/) console browser

[mozilla/webextension-polyfill: A lightweight polyfill library for Promise-based WebExtension APIs in Chrome](https://github.com/mozilla/webextension-polyfill)

[graysky2/profile-sync-daemon: Symlinks and syncs browser profile dirs to RAM thus reducing HDD/SDD calls and speeding-up browsers.](https://github.com/graysky2/profile-sync-daemon)

[web-platform-tests dashboard](https://wpt.fyi/results/?label=experimental&label=master&aligned)

## Profile sync

[Profile-sync-daemon - ArchWiki](https://wiki.archlinux.org/title/Profile-sync-daemon)
[How To Sync Browser Profile Into Tmpfs (RAM) In Linux](https://ostechnix.com/how-to-sync-browser-profile-into-tmpfs-ram-in-linux/)

```sh
psd preview

# add `user ALL=(ALL) NOPASSWD: /usr/bin/psd-overlay-helper` to
sudo visudo -f /etc/sudoers.d/psd

# such that this command does not requires password
sudo -n /usr/bin/psd-overlay-helper
```

## Chrome

[Here's how Google's Chrome browser does updates](http://www.computerworld.com/article/3208345/web-browsers/how-googles-chrome-browser-does-updates.html)
[How to Use Google Chrome’s Hidden Reader Mode](https://www.howtogeek.com/423643/how-to-use-google-chromes-hidden-reader-mode/)

[Chrome Flags that will improve your browsing experience](https://www.androidauthority.com/chrome-flags-1009941/)
[One tweak for a more pain-free Google Chrome browsing experience | ZDNet](https://www.zdnet.com/article/one-tweak-for-a-more-pain-free-google-chrome-browsing-experience/) reduce notification

`chrome://network-internals`
`chrome://webrtc-internals`
`chrome://media-internals` (while streaming)

### Extension

[What are extensions? - Google Chrome](https://developer.chrome.com/extensions)
[How to use React.js to create a Chrome extension in 5 minutes](https://levelup.gitconnected.com/how-to-use-react-js-to-create-chrome-extension-in-5-minutes-2ddb11899815)
[Create your own Chrome Extension in 5 minutes | by Harsha Vardhan | JavaScript In Plain English | Oct, 2020 | Medium](https://medium.com/javascript-in-plain-english/create-your-own-chrome-extension-in-5-minutes-a43b24d6652e)

[Writing a Chrome extension in Kotlin (Part 1) – Ramon Rivas – Medium](https://medium.com/@rivasdiaz/writing-a-chrome-extension-in-kotlin-part-1-e013d431b63f)
[Writing a Chrome extension in Kotlin — Using Coroutines (Part 2)](https://medium.com/@rivasdiaz/writing-a-chrome-extension-in-kotlin-using-coroutines-part-2-29175f4d1739)
[Writing a Chrome extension in Kotlin — Supporting Firefox and Chrome (Part 3)](https://medium.com/@rivasdiaz/writing-a-chrome-extension-in-kotlin-supporting-firefox-and-chrome-part-3-a5ab0ae58bb4)
[rivasdiaz/helloworld-chrome-extension-kotlin: Simple Chrome Extension from Google Chrome Developer Portal in Kotlin](https://github.com/rivasdiaz/helloworld-chrome-extension-kotlin)

## Firefox

[Servo, the parallel browser engine](https://servo.org/)
[servo/servo: The Servo Browser Engine](https://github.com/servo/servo)
[Servo (layout engine) - Wikiwand](https://www.wikiwand.com/en/Servo_(layout_engine%29)

[How to Backup and Restore Firefox Profile On Linux](https://www.fossmint.com/backup-and-restore-a-firefox-profile-on-linux/)

### Extension

[Firefox Extension Workshop | Get help creating & publishing Firefox extensions.](https://extensionworkshop.com/)
[Browser Extensions - Mozilla | MDN](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions)
[Getting started with web-ext - Mozilla | MDN](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Getting_started_with_web-ext)

[How to Write Your Own Browser Extension [Example Project Included]](https://www.freecodecamp.org/news/write-your-own-browser-extensions/)
[Developing your web extension with the best tools – Eric Masseran – Medium](https://medium.com/@Morikko/developing-your-web-extension-with-the-best-tools-213207c2b6b5)

[Your first Firefox (Web)extension in Kotlin – Kirill Rakhman – Medium](https://medium.com/@Cypressious/your-first-firefox-web-extension-in-kotlin-348fc907915)
[Your second Firefox extension in Kotlin – Kirill Rakhman – Medium](https://medium.com/@Cypressious/your-second-firefox-extension-in-kotlin-bafd91d87c41)
[KotlinConf 2018 - Building a Browser Extension with Kotlin by Kirill Rakhman - YouTube](https://www.youtube.com/watch?v=QaPMKZay_Ig)
[cypressious/second-firefox-extension-kotlin: Porting https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Your_second_WebExtension to Kotlin](https://github.com/cypressious/second-firefox-extension-kotlin)

## Brave

[Secure, Fast & Private Web Browser with Adblocker | Brave Browser](https://brave.com/)
[Welcome to Brave Docs — Brave Browser documentation](https://brave-browser.readthedocs.io/en/latest/index.html)
[Installing Brave — Brave Browser documentation](https://brave-browser.readthedocs.io/en/latest/installing-brave.html#linux)

## How it works

> see `css-notes#css-houdini`

[Quantum – Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/category/quantum/)
[Entering the Quantum Era—How Firefox got fast again and where it’s going to get faster – Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/2017/11/entering-the-quantum-era-how-firefox-got-fast-again-and-where-its-going-to-get-faster/)
[Inside a super fast CSS engine: Quantum CSS (aka Stylo) – Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/2017/08/inside-a-super-fast-css-engine-quantum-css-aka-stylo/)
[The whole web at maximum FPS: How WebRender gets rid of jank – Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/2017/10/the-whole-web-at-maximum-fps-how-webrender-gets-rid-of-jank/)
[Fearless Concurrency in Firefox Quantum | Rust Blog](https://blog.rust-lang.org/2017/11/14/Fearless-Concurrency-In-Firefox-Quantum.html)
[Image Inconsistencies: How and When Browsers Download Images – CSS Wizardry – CSS Architecture, Web Performance Optimisation, and more, by Harry Roberts](https://csswizardry.com/2018/06/image-inconsistencies-how-and-when-browsers-download-images/)
[Firefox 61 – Quantum of Solstice – Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/2018/06/firefox-61-quantum-of-solstice/)
[RenderingNG - Chrome Developers](https://developer.chrome.com/blog/renderingng/)

[V8 JavaScript engine](https://v8.dev/)
[Indicium: V8 runtime tracer tool · V8](https://v8.dev/blog/system-analyzer)

Sparkplug is positioned as a “super-fast” non-optimizing compiler. Sparkplug is part of a compiler pipeline, nestled between the Ignition interpreter and the TurboFan optimizing compiler.

[How do browsers really work? These 5 videos will show you their inner workings](https://medium.freecodecamp.org/the-inner-workings-of-the-browser-for-javascript-web-developers-course-d26f11270f41)
[How browser rendering works — behind the scenes – LogRocket](https://blog.logrocket.com/how-browser-rendering-works-behind-the-scenes-6782b0e8fb10)
[WebKit for Developers - Paul Irish](http://www.paulirish.com/2013/webkit-for-developers/) 2013
[How browsers work internally - Tali Garsiel - Front-Trends 2012 on Vimeo](https://vimeo.com/44182484)
[How browser rendering works — behind the scenes – LogRocket](https://blog.logrocket.com/how-browser-rendering-works-behind-the-scenes-6782b0e8fb10)
[JavaScript: from Downloading Scripts to Execution (Part 1)](https://www.telerik.com/blogs/journey-of-javascript-downloading-scripts-to-execution-part-i)
[JavaScript: from Downloading Scripts to Execution (Part 2)](https://www.telerik.com/blogs/journey-of-javascript-downloading-scripts-to-execution-part-ii)
[V8, Advanced JavaScript, & the Next Performance Frontier (Google I/O '17) - YouTube](https://www.youtube.com/watch?v=EdFDJANJJLs)
[Jake Archibald: In The Loop - JSConf.Asia 2018 - YouTube](https://www.youtube.com/watch?v=cCOL7MC4Pl0)

[Rendering on the Web | Google Developers](https://developers.google.com/web/updates/2019/02/rendering-on-the-web)
[How browser engines work?](http://www.slideshare.net/haricot/how-browser-engines-work/) 2012
[How WebKit Works - Google Drive](https://docs.google.com/presentation/d/1ZRIQbUKw9Tf077odCh66OrrwRIVNLvI_nhLm2Gi__F0/embed?start=false&loop=false&delayms=3000#slide=id.p) 2012
[How Browsers Work: Behind the scenes of modern web browsers - HTML5 Rocks](http://www.html5rocks.com/en/tutorials/internals/howbrowserswork/) 2011
[your webkit port is special (just like every other port)](http://ariya.ofilabs.com/2011/06/your-webkit-port-is-special-just-like-every-other-port.html) 2011
[How browsers work](http://taligarsiel.com/Projects/howbrowserswork1.htm) Tali Garsiel 2009
[Performance Calendar » Rendering: repaint, reflow/relayout, restyle](http://calendar.perfplanet.com/2009/rendering-repaint-reflow-relayout-restyle/) 2009
2007:
[WebCore Rendering I – The Basics | WebKit](https://webkit.org/blog/114/webcore-rendering-i-the-basics/)
[WebCore Rendering II – Blocks and Inlines | WebKit](https://webkit.org/blog/115/webcore-rendering-ii-blocks-and-inlines/)
[WebCore Rendering III – Layout Basics | WebKit](https://webkit.org/blog/116/webcore-rendering-iii-layout-basics/)
[WebCore Rendering IV – Absolute/Fixed and Relative Positioning | WebKit](https://webkit.org/blog/117/webcore-rendering-iv-absolutefixed-and-relative-positioning/)
[WebCore Rendering V – Floats | WebKit](https://webkit.org/blog/118/webcore-rendering-v-floats/)

[WebAssembly and Back Again: Fine-Grained Sandboxing in Firefox 95 - Mozilla Hacks - the Web developer blog](https://hacks.mozilla.org/2021/12/webassembly-and-back-again-fine-grained-sandboxing-in-firefox-95/)

## DevTools

[DevTools in 2016: Accelerate your workflow - Google I/O 2016 - YouTube](https://www.youtube.com/watch?v=x8u0n4dT-WI)
[Cool Chrome DevTools tips and tricks you wish you knew already](https://medium.freecodecamp.org/cool-chrome-devtools-tips-and-tricks-you-wish-you-knew-already-f54f65df88d2)
[Introduction | Down and Dirty with Chrome Developer Tools](http://blittle.github.io/chrome-dev-tools/)

[Developer Edition Devtools Update: Now with Photon UI - Mozilla Hacks - the Web developer blog](https://hacks.mozilla.org/2017/09/developer-edition-devtools-update-now-with-photon-ui/)

[𝗛𝗼𝘄 𝘁𝗼 𝗳𝗶𝗻𝗱 "UNUSED" 𝗝𝗔𝗩𝗔𝗦𝗖𝗥𝗜𝗣𝗧 𝗮𝗻𝗱 𝗖𝗦𝗦 𝗰𝗼𝗱𝗲 𝗼𝗻 𝘆𝗼𝘂𝗿 𝗽𝗮𝗴𝗲? 🤔 - DEV Community](https://dev.to/varunprashar5/unused-3688)

[VisBug](https://visbug.web.app/)
[VisBug - Chrome Web Store](https://chrome.google.com/webstore/detail/visbug/cdockenadnadldjbbgcallicgledbeoc?hl=en)
[Day 1 Keynote (Chrome Dev Summit 2018) - YouTube](https://www.youtube.com/watch?v=zPHyxvPT0gg&t=1374)

## Debugging

[JavaScript Debugging Reference | Tools for Web Developers | Google Developers](https://developers.google.com/web/tools/chrome-devtools/javascript/reference)
[Get Started with Remote Debugging Android Devices | Web | Google Developers](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/)

[Debug Progressive Web Apps | Tools for Web Developers | Google Developers](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps)
[Debugging Modern Web Applications – Mozilla Hacks – the Web developer blog](https://hacks.mozilla.org/2018/05/debugging-modern-web-applications/)

[iOS Safari](https://developer.apple.com/library/content/documentation/AppleApplications/Conceptual/Safari_Developer_Guide/GettingStarted/GettingStarted.html)
[Debug on iOS Devices and the iOS Simulator – Adaptive.js Docs](http://adaptivejs.mobify.com/v2.0/docs/debug-on-ios-devices-and-the-ios-simulator/)

[Introducing the Microsoft Edge DevTools Protocol - Microsoft Edge Dev BlogMicrosoft Edge Dev Blog](https://blogs.windows.com/msedgedev/2018/05/11/introducing-edge-devtools-protocol/)

[weinre - Home](http://people.apache.org/~pmuellr/weinre/docs/latest/Home.html)
[Debug on Legacy Android with the Stock Browser (and on Other Devices) – Adaptive.js Docs](http://adaptivejs.mobify.com/v2.0/docs/debug-on-legacy-android-with-the-stock-browser-and/) with weinre

## Snippets

[DevTools Snippets](http://bgrins.github.io/devtools-snippets/)

[Run Snippets Of Code From Any Page | Tools for Web Developers | Google Developers](https://developers.google.com/web/tools/chrome-devtools/snippets)
[Scratchpad - Firefox Developer Tools | MDN](https://developer.mozilla.org/en-US/docs/Tools/Scratchpad)

## Video policy

[New <video> Policies for iOS | WebKit](https://webkit.org/blog/6784/new-video-policies-for-ios/) 2016-07
[Muted Autoplay on Mobile: Say Goodbye to Canvas Hacks and Animated GIFs! | Web | Google Developers](https://developers.google.com/web/updates/2016/07/autoplay) 2016-07
[HTML5 video autoplay on mobile revisited – Walter Ebert](http://walterebert.com/blog/html5-video-autoplay-mobile-revisited/) 2016-11
[Unsolved HTML5 video issues on iOS | Blog | Miller Medeiros](http://blog.millermedeiros.com/unsolved-html5-video-issues-on-ios/) 2011-04
[Getting HTML5 video to work with iOS Mobile Safari | fdiv.net](http://fdiv.net/2013/05/17/getting-html5-video-work-ios-mobile-safari) 2013-05
[Five Tips for Using Self Signed SSL Certificates with iOS | HttpWatch BlogHttpWatch Blog](https://blog.httpwatch.com/2013/12/12/five-tips-for-using-self-signed-ssl-certificates-with-ios/)

[HTMLMediaElement - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement)
[HTMLAudioElement - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAudioElement)
[HTMLVideoElement - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/HTMLVideoElement)
[Media formats supported by the HTML audio and video elements - HTML | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats)

## Bug Tracker

[Issues - chromium - An open-source project to help move the web forward. - Monorail](crbug.com)
[Bugzilla Main Page](https://bugzilla.mozilla.org/)chrome
[Microsoft Connect (IE Feedback)](https://connect.microsoft.com/IE/Feedback)
[EdgeHTML issue tracker - Report or search issues, such as problems with site rendering or standards compliance](https://developer.microsoft.com/en-us/microsoft-edge/platform/issues/)

## Browsersync

[Browsersync - Time-saving synchronised browser testing](https://browsersync.io/)
[Browsersync (@Browsersync) | Twitter](https://twitter.com/browsersync/)

[Browsersync API](https://browsersync.io/docs/api/)
[Browsersync options](https://browsersync.io/docs/options/)
[BrowserSync/recipes: Fully working project examples showing how to use BrowserSync in various ways.](https://github.com/BrowserSync/recipes)

[SPA routing in BrowserSync without hashes](http://thomastuts.com/blog/browsersync-spa-routing-pretty-urls)
[Browsersync - time saving features you didn’t know about - JH](http://wearejh.com/news/browsersync-time-saving-features-you-didnt-know-about/)
[How I speed up my web development process by 34% — Medium](https://medium.com/@nejcrodosek/how-i-speed-up-my-web-development-process-by-34-3fa6265aa7#.lamo325vb)

## Installed Chrome Extensions

Goto chrome://extensions/shortcuts to set shortcuts

[Augmented Steam - Chrome Web Store](https://chrome.google.com/webstore/detail/augmented-steam/dnhpnfgdlenaccegplpojghhmaamnnfp)
[Copycat - Chrome Web Store](https://chrome.google.com/webstore/detail/copycat/jdjbiojkklnaeoanimopafmnmhldejbg)

- Ctrl+Shift+D to copy Markdown link
- PR: add notification after copy

[Explain and Send Screenshots - Chrome Web Store](https://chrome.google.com/webstore/detail/explain-and-send-screensh/mdddabjhelpilpnpgondfmehhcplpiin)
[Enhanced Steam - Chrome Web Store](https://chrome.google.com/webstore/detail/enhanced-steam/okadibdjfemgnhjiembecghcbfknbfhg)
[FasterChrome - Chrome Web Store](https://chrome.google.com/webstore/detail/fasterchrome/nmgpnfccjfjhdenioncabecepjcmdnjg)
[FreshStart - Cross Browser Session Manager - Chrome Web Store](https://chrome.google.com/webstore/detail/freshstart-cross-browser/nmidkjogcjnnlfimjcedenagjfacpobb)
[Honey - Chrome Web Store](https://chrome.google.com/webstore/detail/honey/bmnlcjabgnpnenekpadlanbbkooimhnj)
[HTTP Indicator - Chrome Web Store](https://chrome.google.com/webstore/detail/http-indicator/hgcomhbcacfkpffiphlmnlhpppcjgmbl)
[Ivacy VPN: Best Chrome VPN Proxy Extension - Chrome Web Store](https://chrome.google.com/webstore/detail/ivacy-vpn-best-chrome-vpn/lblebdecfhdegbeoejplcpmhibbkbkin)
[LastPass: Free Password Manager - Chrome Web Store](https://chrome.google.com/webstore/detail/lastpass-free-password-ma/hdokiejnpimakedhajhdlcegeplioahd)
[Link to Text Fragment - Chrome Web Store](https://chrome.google.com/webstore/detail/link-to-text-fragment/pbcodcjpfjdpcineamnnmbkkmkdpajjg)
[Make Medium Readable Again - Chrome Web Store](https://chrome.google.com/webstore/detail/make-medium-readable-agai/kljjfejkagofbgklifblndjelgabcmig)
[Markdown Here - Chrome Web Store](https://chrome.google.com/webstore/detail/markdown-here/elifhakcjgalahccnjkneoccemfahfoa)

- change shortcut to <kbd>Alt</kbd> + <kbd>M</kbd>

[Medium Unlimited](https://manojvivek.github.io/medium-unlimited/)
[Mercury Reader - Chrome Web Store](https://chrome.google.com/webstore/detail/mercury-reader/oknpjjbmpnndlpmnhmekjpocelpnlfdi)
[Moly HaH - Chrome Web Store](https://chrome.google.com/webstore/detail/moly-hah/pjoacnohgednppackhamgfalpkffeeek)

- E, Shift-E to enter HaH
- Charset: ASDZXC
- PR: sync option

[Petapator - Chrome Web Store](https://chrome.google.com/webstore/detail/petapator/eapjillhmgpcgfelagikhjeiboocofcm)
[PlantUML Viewer - Chrome Web Store](https://chrome.google.com/webstore/detail/plantuml-viewer/legbfeljfbjgfifnkmpoajgpgejojooj) disabled
[Reader View - Chrome Web Store](https://chrome.google.com/webstore/detail/reader-view/ecabifbgmdmgdllomnfinbmaellmclnh)
[Reedy - Chrome Web Store](https://chrome.google.com/webstore/detail/reedy/ihbdojmggkmjbhfflnchljfkgdhokffj)
[Screenshot YouTube - Chrome Web Store](https://chrome.google.com/webstore/detail/screenshot-youtube/gjoijpfmdhbjkkgnmahganhoinjjpohk/related)
[Smart Websocket Client - Chrome Web Store](https://chrome.google.com/webstore/detail/smart-websocket-client/omalebghpgejjiaoknljcfmglgbpocdp)
[Steam Database - Chrome Web Store](https://chrome.google.com/webstore/detail/steam-database/kdbmhfkmnlmbkgbabkdealhhbfhlmmon)
[Tampermonkey - Chrome Web Store](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)
[TunnelBear VPN - Chrome Web Store](https://chrome.google.com/webstore/detail/tunnelbear-vpn/omdakjcmkglenbhjadbccaookpfjihpa)
[Unblock Youku - Chrome Web Store](https://chrome.google.com/webstore/detail/unblock-youku/pdnfnkhpgegpcingjbfihlkjeighnddk)
[Video Speed Controller - Chrome Web Store](https://chrome.google.com/webstore/detail/video-speed-controller/nffaoalbilbmmfgbnbgppjihopabppdk?hl=en)

- PR: sync option
- Preferred Speed: 1.8
- Remember Playback Speed

[Web Archiver - Chrome Web Store](https://chrome.google.com/webstore/detail/web-archiver/gjpgpobcdndcdcidmgcmlphbomllapjp)
[Wikiwand: Wikipedia Modernized - Chrome Web Store](https://chrome.google.com/webstore/detail/wikiwand-wikipedia-modern/emffkefkbkpkgpdeeooapgaicgmcbolj)
[YT Anti Translate - Chrome Web Store](https://chrome.google.com/webstore/detail/yt-anti-translate/ndpmhjnlfkgfalaieeneneenijondgag)

[百度网盘直接下载助手 直链加速版](https://greasyfork.org/zh-CN/scripts/39504-%E7%99%BE%E5%BA%A6%E7%BD%91%E7%9B%98%E7%9B%B4%E6%8E%A5%E4%B8%8B%E8%BD%BD%E5%8A%A9%E6%89%8B-%E7%9B%B4%E9%93%BE%E5%8A%A0%E9%80%9F%E7%89%88)

### Adblocker

> see `adblocker.md`

### Raspberry Pi

Chromium, `h264ify`, and `rpi-chromium-mods` are preinstalled since [2016-09](https://www.raspberrypi.org/blog/introducing-pixel/)

[Pi3 internet browsing and Youtube performance - Raspberry Pi Forums](https://www.raspberrypi.org/forums/viewtopic.php?t=138025)
[[HowTo!] Smooth youtube 1080p in Chromium - Raspberry Pi Forums](https://lb.raspberrypi.org/forums/viewtopic.php?f=66&t=199543&sid=ba57433f962277aea45c1aa252056d4d&start=50#p1442955) `config.txt`, `00-rpi-vars`, `chromiummod.sh` 2018
[How to get smooth youtube/flash video playback on Raspberry Pi (updated 25-03-2019)](https://www.linkedin.com/pulse/how-get-smooth-youtubeflash-video-playback-raspberry-pi-kovalenko)
[RPi-youtube - Chrome Web Store](https://chrome.google.com/webstore/detail/rpi-youtube/laacchpjldmpbhkcjfmfcjijaekhhlgn?hl=en)
[RaspberryCast - Chrome Web Store](https://chrome.google.com/webstore/detail/raspberrycast/aikmhmnmlebhcjjdbjilohbpfljioeak?hl=en)
[Create Your Own Chrome Cast With Raspicast - YouTube](https://www.youtube.com/watch?v=QQ2vlfWY-R8)
[h264ify - Chrome Web Store](https://chrome.google.com/webstore/detail/h264ify/aleakchihdccplidncghkekgioiakgal?hl=en)

### Watchlist

[The Best Browser Extensions That’ll Save You Money (and Which to Skip)](https://twocents.lifehacker.com/the-best-browser-extensions-that-ll-save-you-money-and-1702736679)
[How to Use Pushbullet to Bridge the Gap Between All Your Devices](https://lifehacker.com/how-to-use-pushbullet-to-bridge-the-gap-between-all-you-1548595270)
[Just Read - Chrome Web Store](https://chrome.google.com/webstore/detail/just-read/dgmanlpmmkibanfdgjocnabmcaclkmod?hl=en)

### DevTools

[Apollo Client Developer Tools - Chrome Web Store](https://chrome.google.com/webstore/detail/apollo-client-developer-t/jdkknkkbebbapilgoeccciglkfbmbnfm)
[DOMListener - Chrome Web Store](https://chrome.google.com/webstore/detail/domlistener/jlfdgnlpibogjanomigieemaembjeolj)
[JSONView - Chrome Web Store](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc) disabled
[JWT Analyzer & Inspector - Chrome Web Store](https://chrome.google.com/webstore/detail/jwt-analyzer-inspector/henclmbnehmcpbjgipaajbggekefngob)
[React Developer Tools - Chrome Web Store](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)
[Redux DevTools - Chrome Web Store](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd)
[Set Character Encoding - Chrome Web Store](https://chrome.google.com/webstore/detail/set-character-encoding/bpojelgakakmcfmjfilgdlmhefphglae)
[Smart Websocket Client - Chrome Web Store](https://chrome.google.com/webstore/detail/smart-websocket-client/omalebghpgejjiaoknljcfmglgbpocdp)
[Vue.js devtools - Chrome Web Store](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
[XState DevTools - Chrome Web Store](https://chrome.google.com/webstore/detail/xstate-devtools/aamnodipnlopbknpklfoabalmobheehc)

### GitHub

[bitHound - Chrome Web Store](https://chrome.google.com/webstore/detail/bithound/jemefagecbkdhddocooihfhhgolbccan)
[npmhub - Chrome Web Store](https://chrome.google.com/webstore/detail/npmhub/kbbbjimdjbjclaebffknlabpogocablj)
[Octo Mate - Chrome Web Store](https://chrome.google.com/webstore/detail/octo-mate/baggcehellihkglakjnmnhpnjmkbmpkf)
[Octotree - Chrome Web Store](https://chrome.google.com/webstore/detail/octotree/bkhaagjahfmjljalopjnoealnfndnagc)
[Refined GitHub - Chrome Web Store](https://chrome.google.com/webstore/detail/refined-github/hlepfoohegkhhmjieoechaddaejaokhf)

## Installed Firefox Extensions

[Video Speed Controller – Add-ons for Firefox](https://addons.mozilla.org/en-US/firefox/addon/videospeed/)
[uBlock Origin – Add-ons for Firefox](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/)
[Tabboo - Session Manager – Add-ons for Firefox](https://addons.mozilla.org/en-US/firefox/addon/tabboo-session-manager/?src=search)
