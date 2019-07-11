---
title: Gamepad
categories:
  - comp.hardware
tags:
  - null
toc: true
date: 2016-09-25 22:05:50
---

[Gamepad - ArchWiki](https://wiki.archlinux.org/index.php/Gamepad)

[Glossary:Controller - PCGamingWiki PCGW - bugs, fixes, crashes, mods, guides and improvements for every PC game](http://pcgamingwiki.com/wiki/Glossary:Controller#XInput_Plus)

[XInput and DirectInput (Windows)](https://msdn.microsoft.com/en-us/library/windows/desktop/ee417014(v=vs.85%29.aspx)
[DirectInput - Wikiwand](https://www.wikiwand.com/en/DirectInput#/DirectInput_vs_XInput)

[手柄哥子俊 - YouTube](https://www.youtube.com/channel/UC24bt5d-Gg5m8Gdu7daaQVQ)

## 小雞 Gamesir

### G3

[GameSir G3w USB Controller Joystick for PC/Android Devices/PS3 – GameSir Official Store](https://gamesir.hk/collections/gamepads/products/gamesir-g3w)
Bought from Taobao at ¥45 201609
Supports PC (XInput, DInput) and Android
Great value for the cost
- Long press HOME button for 5 seconds to toggle between XInput and DInput (1 LED and 2 LED)

[Tutorial: upgrading firmware for G3 - YouTube](https://www.youtube.com/watch?v=DenbKDHOCxc)

### T4

[GameSir T4 2.4 GHz Wireless Controller – GameSir Official Store](https://gamesir.hk/collections/gamepads/products/gamesir-t4)
Taobao ¥115 (with ¥30 coupon), ¥248 for 2 (with ¥20 coupon) 201812
[兼容多平台的震动游戏手柄：GameSir 盖世小鸡 T4 无线游戏手柄开箱\_\_什么值得买](https://post.smzdm.com/p/773469/)
[入门级 switch 游戏手柄体验—盖世小鸡 T4 手柄体验\_\_什么值得买](https://post.smzdm.com/p/769576/)
[它支持switch！小雞T4遊戲手柄上手體驗 - 每日頭條](https://kknews.cc/zh-hk/digital/82nvo3e.html)
[【手柄哥测评】小雞T4遊戲手柄測評 高性價比PC遊戲手柄 - YouTube](https://www.youtube.com/watch?v=URWk6gyfs4Q)

- Long press HOME button for 5 seconds to switch mode  
  XInput: LED1+LED4
  XInput Wired: LED2+LED3
  DInput: LED1+LED3
- turn on "Pro Controller wired Communication" to use in Switch
- 長按LT,RT,R3再通過按壓方向鍵上下來調光
- Long press LB,RB 5 seconds to turn off LED
- 長按Turbo鍵，再通過按壓方向鍵上下來調節馬達振動強度

## 北通

[游戏伴我行之这些年用过的手柄\_\_什么值得买](https://post.smzdm.com/p/425023/)
[北通蝙蝠 3 钢翼版 游戏手柄 简单开箱\_\_什么值得买](https://post.smzdm.com/p/532658/)
[Betop 北通 阿修罗 2 有线手柄（黑色）开箱\_\_什么值得买](https://post.smzdm.com/p/571176/)
[有惊无喜的阿修罗 2 蓝牙版手柄评测*值友评测*什么值得买](https://test.smzdm.com/pingce/p/37454/)

## Microsoft

Xbox One Classic + Li-ion battery RMB240
PC wireless adapter RMB102

Xbox One S + Li-ion battery RMB343
connect to Windows 10 via Bluetooth

## Key Mapping

[Xpadder vs PGP vs J2K](http://www.xpadder-vs-pgp-vs-j2k.com/)
[Xpadder or Pinnacle Game Profiler or other? (control-mapping program) :: Off Topic](https://steamcommunity.com/discussions/forum/12/46476145543038473/)

### Xinput Plus

XInput -> DInput, buttons remapping, SHIFT key

[XInput Plus - 0dd14 lab](https://sites.google.com/site/0dd14lab/xinput-plus)
[Xinput Plus tutorial - Play-Old-PC-Games.com](http://www.play-old-pc-games.com/compatibility-tools/xinput-plus-tutorial/)
[Steam Community :: Guide :: True Solution for all XInput Controller Problems](http://steamcommunity.com/sharedfiles/filedetails/?id=755970152)

### ARPG Gamepad Controller

[ARPG Gamepad Controller | Cute Kick Studio](http://cutekickstudio.com/tools/arpg-gamepad-controller/)

### x360ce

XInput -> DInput, buttons remapping

[x360ce/x360ce: Primary repository for the x360ce library, front-end and tools.](https://github.com/x360ce/x360ce)
[Xbox 360 Controller Emulator - PCGamingWiki PCGW - bugs, fixes, crashes, mods, guides and improvements for every PC game](http://pcgamingwiki.com/wiki/Xbox_360_Controller_Emulator)

### Pinnacle Game Profiler

[Download - Pinnacle Game Profiler](http://pinnaclegameprofiler.com/download)
[How To Register Pinnacle Game Profiler For Free LifeTime Use 1000% Works - YouTube](https://youtu.be/pyLmiSMTug4?t=195)

Disconnect from Internet when submitting the info:

```
name: quintan corder
password: ragzzz51181
unlock key: GINLW-R9NI-DIP7N-N3SN-N9LHY
magic color: YELLOW
magic word: PINEAPPLE
checkmarks: C4-G6-G8-H2-H3
```

`regedit`, set `HKLM\SOFTWARE\PowerUp Software\Pinnacle Game Profiler\(Default)` to `5/66/66`

### XPadder

[Xpadder](http://xpadder.com/)
[Download Xpadder (Last freeware version) 5.3](<http://www.majorgeeks.com/mg/getmirror/xpadder_(last_freeware_version),1.html>)
[Steam Community :: Guide :: Working Controller guide.](https://steamcommunity.com/sharedfiles/filedetails/?id=509137138) Xpadder

### InputMapper

[InputMapper - Home](https://inputmapper.com/)

---

## Linux

[How to configure your gamepad on Ubuntu](https://www.howtoforge.com/tutorial/how-to-configure-your-gamepad-on-ubuntu/)

```sh
# from joyutils
jscal -c /dev/input/js0
```

### XBox360 Wired

Wired XBox360 pad should work out of the box using `xpad` driver

### XBox360 Wireless (using `xboxdrv`)

http://pingus.seul.org/~grumbel/xboxdrv/

```sh
sudo add-apt-repository ppa:grumbel/ppa
sudo apt-get update
sudo apt-get install xboxdrv
```

```sh
xboxdrv -L
xboxdrv --daemon
```

http://pingus.seul.org/~grumbel/xboxdrv/xboxdrv.html

[Xbox360Controller - Community Help Wiki](https://help.ubuntu.com/community/Xbox360Controller)

### Tester

[jstest-gtk - A joystick testing and configuration tool for Linux](http://pingus.seul.org/~grumbel/jstest-gtk/)
[HTML5 Gamepad Tester](http://html5gamepad.com/)

```sh
# invoke Window's Control Panel to test joystick
wine control joy.cpl

# from joyutils
jstest /dev/input/js0
```
