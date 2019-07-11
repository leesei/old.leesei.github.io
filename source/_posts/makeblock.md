---
title: "Makeblock"
categories:
  - comp.hardware
tags:
  - iot
  - makeblock
  - mbot
  - mcore
  - orion
toc: true
date: 2019-06-12 21:49:59
---

[Makeblock - Wikiwand](https://www.wikiwand.com/en/Makeblock)
[Makeblock: Global STEAM Education Solution Provider](https://www.makeblock.com/)
[Makeblock HK | STEM Education Robotics Platform](http://makeblock.hk/)
[Makeblock 官网-全球 STEAM 教育解决方案领导者](https://www.makeblock.com/cn)
[軟體下載 · Issue #1 · MakeblockMacau/Reference](https://github.com/MakeblockMacau/Reference/issues/1)

- RJ25 connectors
- [official adapter](https://item.taobao.com/item.htm?id=554185937877) [1](https://item.taobao.com/item.htm?id=548612116793) [2](https://item.taobao.com/item.htm?id=570704363022)
- [official cable](https://detail.tmall.com/item.htm?id=560659474412) [1](https://item.taobao.com/item.htm?id=541962558126)
- [mBridge 水晶头接口 RJ25 转接板 Robotbit 扩展板 支持 micro:bit-淘宝网](https://item.taobao.com/item.htm?id=595667433688)
- support I2C devices/2 IO pins per port
- LEGO compatible
- PH2.0 3.7V/DC 3.5mm 6V
- [Lithium batteries' options for mBot-Blue - Makeblock Products / mBot - Makeblock Forum](https://forum.makeblock.com/t/lithium-batteries-options-for-mbot-blue/4629/4)

[STEAM Kits | Makeblock – Let Creation Be a Way of Life](https://www.makeblock.com/steam-kits)

[Student E-learn | Makeblock HK](http://makeblock.hk/stu_elearn/)

## Shops

[首页-咖咖创客官方店-淘宝网](https://kakachuangke.taobao.com/)
[makeblock 旗舰店-天猫 Tmall.com](https://makeblock.tmall.com/)
[首页-makeblock 咖咖创客专卖店-天猫 Tmall.com](https://makeblockkkck.tmall.com/)
[首页-Maker 体验店-淘宝网](https://mbot.world.taobao.com/)
[makeblock 兼容系列-HoneySense(和信创客)makerclock 兼容 makeblock-淘宝网](https://honeysense.world.taobao.com/category-1429586360.htm) Makeblock compatible
[首页-小氪机器人官方店-淘宝网](https://shop137769920.taobao.com/index.htm) Makeblock compatible

## Makeblock internal

[Makeblock-official/Makeblock-Libraries: Arduino Library for Makeblock Electronic Modules, learn more from Makeblock official website](https://github.com/Makeblock-official/Makeblock-Libraries) [doc](http://learn.makeblock.com/cn/Makeblock-library-for-Arduino/index.html)
[Learning Arduino Programming – Open-source Arduino Robot Building Platform|Makeblock Learning Resource](http://learn.makeblock.com/en/learning-arduino-programming/)

[xeecos/python-for-mbot: A Python interface to control and communicate with mBot robot kit](https://github.com/xeecos/python-for-mbot)

[Interactive MBot With JavaScript: 4 Steps](https://www.instructables.com/id/Interactive-mBot-with-JavaScript/)
[Makeblock-official/mbot_nodebots](https://github.com/Makeblock-official/mbot_nodebots)

[Getting Started: Wire up Your Creation - Makeblock](https://www.makeblock.com/project/step-1-wiring-color-marker-show-the-modules-connection-for-correct)
[Advanced Makeblock Sensors (DIY): 32 Steps (with Pictures)](https://www.instructables.com/id/Advanced-Makeblock-Sensors-DIY/) !important
[Me RJ25 Adapter - Makeblock](https://www.makeblock.com/project/me-rj25-adapter)

[mBot Serial Port Protocol - Makeblock](https://www.makeblock.com/project/mbot-serial-port-protocol)

Port Coloring:

Red: Output voltage of Vin (6-12 Volt), one or two digital ports.
Black: Single analog port or two analog ports.
Blue: Two digital ports.
Yellow: Single digital port.
White: I2C Port
Grey: Hardware serial port.

RJ25 Dupont Cable Coloring:

blue SCL I2C clock bus
yellow SDA I2C data bus
green GND Grounding
red VCC 5 Volt  
black S1 Digital/analog port
white S2 Digital/analog port

## mCore

[mCore - Makeblock](https://www.makeblock.com/project/mcore)
[mCore – Open-source Arduino Robot Building Platform|Makeblock Learning Resource](http://learn.makeblock.com/en/mcore/)

mCore board is used by [mBot](#mbot)

### Pins

```
Port_1    { 11 , 12 } = RJ25 port 1
Port_2    {  9 , 10 } = RJ25 port 2
Port_3    { A2 , A3 } = RJ25 port 3
Port_4    { A0 , A1 } = RJ25 port 4
Port_5    { NC , NC }  (Not Connected)
Port_6    {  8 , A6 } = Buzzer, Light sensor
Port_7    { A7 , 13 } = Button, two WS2812 LEDs
Port_8    {  8 , A6 } = Buzzer, Light sensor
Port_9    {  6 ,  7 } = PWM motor 2, DIR Motor 2
Port_10   {  5 ,  4 } = PWM motor 1, DIR Motor 1

2   = IR Receiver
3   = IR emitter LED
5   = light sensor
13  = Blue LED
```

## Orion

[Makeblock Orion - Makeblock](https://www.makeblock.com/project/makeblock-orion)
[Makeblock Orion | Makeblock HK](http://makeblock.hk/sensors-makeblock-orion/)
[Makeblock 電子模組手冊－Makeblock Orion - 軟硬體開源區 - 圓創力科技.MakeBlock TW -](http://magiccar.let-do.com/forum.php?mod=viewthread&tid=410)

Orion board is used by mBot Start and mBot Ultimate
It is also known as Baseboard
[Why Baseboard is Better? - YouTube](https://www.youtube.com/watch?v=21Q-RYDYnak)

## mBot

[Robot Kits for Kids : mBot | Makeblock - Global STEAM Education Solution Provider](https://www.makeblock.com/steam-kits/mbot)
[mBot – Open-source Arduino Robot Building Platform|Makeblock Learning Resource](http://learn.makeblock.com/en/mbot/)
[mBot Docs · GitBook](http://docs.makeblock.com/mbot/en/) mBlock 5

[值得拥有——mBot 机器人正式版开箱评测（2.4G 版本） | mBot 机器人学习中心](http://www.mbot.cc/?p=297)
[让每一个孩子拥有自己的机器人——mBot 开箱评测 - 模型手办 - Chiphell - 分享与交流用户体验](https://www.chiphell.com/thread-1282876-1-1.html)
[mBot 怎么玩？mBot 官方中文说明书，mbot 中文使用手册 - Makeblock](https://www.makeblock.com/cn/mbot/212197.html)
[mBot Tutorials - GitBook](http://docs.makeblock.com/mbot/en/)
[Cheat Sheet / Getting started - mBot (more) - General Discussion - Makeblock Forum](https://forum.makeblock.com/t/cheat-sheet-getting-started-mbot-more/2960)

[mBot 教育资源页 - makeblock education](http://education.makeblock.com/zh-hans/mbot/)
[home - makeblock education](http://education.makeblock.com/)

[Technology-at-school/Robots/Makeblock at master · Tauvic/Technology-at-school](https://github.com/Tauvic/Technology-at-school/tree/master/Robots/Makeblock)
[機器人齊步走 mBlock5 mbot*ver8*探奇邱信仁](https://www.slideshare.net/renchiou/mblock5-mbotver8)
[2017 探奇 mBot mblock 機器人齊步走 15 小時課程講義 v7](https://www.slideshare.net/renchiou/2017-mbot-mblock-15-v7)
[[mbot] 我的 mbot 教學記錄 II (2018~已完成) @zfang の科學小玩意](http://n.sfs.tw/content/index/12238) !important
[[合集] mBot 教學 - makeblock education](http://education.makeblock.com/zh-hans/resource/%E5%90%88%E9%9B%86-mbot-%E6%95%99%E5%AD%B8/) [吳錫修](https://www.slideshare.net/sshiouwu/presentations) !important, 2018 version
[Programming With Scratch X for Makeblock MBot : 4 Steps](https://www.instructables.com/id/Programming-With-Scratch-X-for-Makeblock-MBot/)

[mBot - YouTube](https://www.youtube.com/playlist?list=PL0SbEqiUD3gxR2nv5ZcHzFudksPz6e2tc) 粤語
[Makeblock - mBot 小學堂珊子姊姊教學影片 - YouTube](https://www.youtube.com/playlist?list=PL9SylZdGlmQNQYK1f5qXW0Ump8hGbEYuz)
[Makeblock Inventor Kit: STEM project 搭建示範 - YouTube](https://www.youtube.com/playlist?list=PLRw4p7Et1ltSyGiB-agMCsUfnGM8z-sb_)
[mBot 教學影片 - YouTube](https://www.youtube.com/playlist?list=PL23zUR4ndfavuldG3my8UNCCYX6wADuT7)
[mBot Tutorials - YouTube](https://www.youtube.com/playlist?list=PLuuf1TKEkEqQ9_2hGTHx5XRxlyTOVUJzS)

[進學國小資訊組 - mBot 如何使用 Gyroscope (陀螺儀) 自行走直線](https://class.tn.edu.tw/modules/tad_web/news.php?WebID=1384&NewsID=11921) + Micro:bit

[【SE 組裝教學】亞洲機器人大賽 mBot CNY70 組裝 - YouTube](https://www.youtube.com/watch?v=7QSqkYAZmz0&list=PL23zUR4ndfateJmKmzPzKPcsNI0LDDCIa&index=2)

## Codey Rocky

[程小奔机器人介绍*程小奔机器人拆解评测*入门编程使用指南-Makeblock](https://www.makeblock.com/cn/info/codey) Codey Rocky
[编程机器人程小奔有什么新功能？程小奔可编程益智机器人评测 - makeblock](https://www.makeblock.com/cn/codey/207165.html)
