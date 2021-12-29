---
title: Adblocking
categories:
  - web
tags:
  - null
toc: true
date: 2018-07-27 09:35:02
---

[uBlock Origin - Chrome Web Store](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=en)
[gorhill/uBlock: uBlock Origin - An efficient blocker for Chromium and Firefox. Fast and lean.](https://github.com/gorhill/uBlock)

[uBlock Origin - Wikiwand](https://www.wikiwand.com/en/UBlock_Origin)
[Home · gorhill/uBlock Wiki](https://github.com/gorhill/uBlock/wiki)
[uBlock vs. ABP: efficiency compared · gorhill/uBlock Wiki](https://github.com/gorhill/uBlock/wiki/uBlock-vs.-ABP:-efficiency-compared)

## Nano Adblocker

> WARNING: DO NOT USE THIS
> Content keep here for historical purposes

[Nano Adblocker & Nano Defender was sold and should now be considered malware. : Adblock](https://www.reddit.com/r/Adblock/comments/jc447f/nano_adblocker_nano_defender_was_sold_and_should/)

I ditched the Adblock/Adblock Plus family and turned to Nano Adblocker for the anti adblock feature. The lighter footprint is a plus.

[Nano Adblocker - Chrome Web Store](https://chrome.google.com/webstore/detail/nano-adblocker/gabbbocakeomblphkmmnoamkioajlkfo) uBlock Origin fork that integrates better with Nano Defender
[Nano Defender - Chrome Web Store](https://chrome.google.com/webstore/detail/nano-defender/ggolfgbegefeeoocgjbmkembbncoadlb)
[NanoAdblocker/NanoCore: Just another adblocker](https://github.com/NanoAdblocker/NanoCore)

Edit: Nano Adblocker's rules seems to break some site (Viu.com), I fall back to uBlock Origin + Nano Defender

[Nano Defender](https://jspenguin2017.github.io/uBlockProtector/#extra-installation-steps-for-ublock-origin)
[Integrate Nano Defender with uBlock Origin to block Anti-Adblocker - gHacks Tech News](https://www.ghacks.net/2019/02/15/integrate-nano-defender-with-ublock-origin-to-block-anti-adblocker/)
Add `https://gitcdn.xyz/repo/NanoAdblocker/NanoFilters/master/NanoFilters/NanoResources.txt` to `userResourcesLocation` of Advanced settings.

## Custom Filter

[Static filter syntax · gorhill/uBlock Wiki](https://github.com/gorhill/uBlock/wiki/Static-filter-syntax)
[Adblock Plus filters explained](https://adblockplus.org/filter-cheatsheet)
[Writing Adblock Plus filters](https://adblockplus.org/en/filters)

Snippets that can be added to filter (like Userscript)
[Resources Library · gorhill/uBlock Wiki](https://github.com/gorhill/uBlock/wiki/Resources-Library)
[NanoFilters/NanoResources.txt at master · NanoAdblocker/NanoFilters](https://github.com/NanoAdblocker/NanoFilters/blob/master/NanoFiltersSource/NanoResources.txt)

[Dynamic filtering · gorhill/uBlock Wiki](https://github.com/gorhill/uBlock/wiki/Dynamic-filtering)
[Dynamic filtering: rule syntax · gorhill/uBlock Wiki](https://github.com/gorhill/uBlock/wiki/Dynamic-filtering:-rule-syntax)

## Pi-hole

[Pi-hole®: A black hole for Internet advertisements – curl -sSL https://install.pi-hole.net | bash](https://pi-hole.net/)
[Pi-hole Userspace](https://discourse.pi-hole.net/)

- Enable Pi-hole as DHCP server (remember to turn off router's) to seamlessly use Pi-hole's DNS
- Set router's DNS to Pi-hole

[Pi-Hole Raspberry Pi Network Ad Blocker | Make:](https://makezine.com/projects/raspberry-pi-network-ad-blocker/)
[Block ads at home using Pi-hole and a Raspberry Pi - Raspberry Pi](https://www.raspberrypi.org/blog/pi-hole-raspberry-pi/)
[Pi-hole: A Raspberry Pi Ad-Blocker with DNS Caching (Ultra-fast) – Jacob Salmela](https://jacobsalmela.com/2014/06/11/raspberry-pi-block-ads-adtrap/)
[Pi-hole: Raspberry Pi Ad-Blocker [Advanced Setup] – Jacob Salmela](https://jacobsalmela.com/2014/09/26/raspberry-pi-ad-blocker-advanced-setup/)
[Complete Pi Hole setup guide: Ad-free better internet in 15 minutes](https://www.smarthomebeginner.com/pi-hole-setup-guide/)
[Pi-Hole Setup Tutorial - LTT Official - Linus Tech Tips](https://linustechtips.com/main/topic/1094810-pi-hole-setup-tutorial/)
[Block EVERY Online Ad with THIS - Pi-Hole on Raspberry Pi - YouTube](https://www.youtube.com/watch?v=KBXTnrD_Zs4)
[Overview | Pi Hole Ad Blocker with Pi Zero W | Adafruit Learning System](https://learn.adafruit.com/pi-hole-ad-blocker-with-pi-zero-w?view=all)

[roots84/DNS-Swapper: A handy little tool to quickly switch between two DNS-Servers](https://github.com/roots84/DNS-Swapper)

[Blocking YouTube Ads and Why It’s a Losing Battle | by Julius Uy | Medium](https://medium.com/@julius.uy/blocking-youtube-ads-and-why-its-a-losing-battle-cd9f1caff9ca)

## Anti Adblock Blocker

[BlockAdblock | Stop Losing Ad Revenue](https://www.blockadblock.com/)

[Nano Defender](https://jspenguin2017.github.io/uBlockProtector/)
[jspenguin2017/uBlockProtector: An anti-adblock defuser for Nano Adblocker and uBlock Origin](https://github.com/jspenguin2017/uBlockProtector)

[Detecting Adblocker Blockers - Schneier on Security](https://www.schneier.com/blog/archives/2018/01/detecting_adblo.html)
[TNR: How To Bypass Websites that Block "AdBlock" (e.g. Forbes)](http://technewsreporter.blogspot.com/2015/12/how-to-bypass-websites-that-block-ad.html)

## Discussion

[Ad Blocking Experiments | FT Labs](https://labs.ft.com/2017/02/ad-blocking-experiments)
[Where Will the Ad versus Ad Blocker Arms Race End? - Scientific American](https://www.scientificamerican.com/article/where-will-the-ad-versus-ad-blocker-arms-race-end/)
[Publishers Need to Stop Whining About Adblock](https://www.makeuseof.com/tag/publishers-need-stop-whining-adblock/)
