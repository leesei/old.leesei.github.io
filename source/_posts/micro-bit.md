---
title: "Micro:bit"
categories:
  - maker
tags:
  - iot
  - micro-bit
toc: true
date: 2018-09-12 21:11:59
---

[Micro:bit Educational Foundation | micro:bit](https://microbit.org/)
[Micro Bit - Wikiwand](http://www.wikiwand.com/en/Micro_Bit)

[carlosperate/awesome-microbit: A curated list of BBC micro:bit resources.](https://github.com/carlosperate/awesome-microbit)
[Welcome to micro:mag - micro:mag](https://micromag.cc/)

43x52mm, with builtin:

- 5x5 dot matrix
- bluetooth
- accelerometer
- magnetometer
- thermometer
- light sensor
- compass
- 2 buttons
- PH2.0 3-3.7V power
  [bbcmicrobit/hardware: Hardware designs for the BBC micro:bit](https://github.com/bbcmicrobit/hardware)
  [Micro:bit Hardware](https://tech.microbit.org/hardware/)
  [micro:bit Power Consumption | REUK.co.uk](http://www.reuk.co.uk/wordpress/microbit-power-consumption/)

[Getting Started with micro:bit - YouTube](https://www.youtube.com/playlist?list=PLBcrWxTa5CS0mWJrytvii8aG5KUqMXvSk) by SparkFun
[micro:bit Tutorial Series - YouTube](https://www.youtube.com/playlist?list=PL3bNyZYHcRSUl7Z5ruCPurJIx4fCtZ35D)
[智能学习-micro:bit 开发板](http://www.yahboom.com/study/micro-board)

[Bitty Software](http://www.bittysoftware.com/index.html)
[IchigonQuest for micro:bit - YouTube](https://www.youtube.com/watch?v=Zw0ON6jjoLA)

[micro:bit Power Consumption | REUK.co.uk](http://www.reuk.co.uk/wordpress/microbit-power-consumption/)

[microbit & accessories from Kitronik](https://www.kitronik.co.uk/microbit.html)
[Micro:bit 技術發展歷程觀察 – circuitcellar](https://www.circuitcellar.com.tw/?p=3882)

## Pinout/GPIO

![](./micro-bit/microbit_pinout.png)
[micro:bit pins](https://makecode.microbit.org/---docs#doc:device/pins)

- Pin #0 - large pad - analog in
- Pin #1 - large pad - analog in
- Pin #2 - large pad - analog in
- Pin #3 - analog in, also used for LED matrix
- Pin #4 - analog in, also used for LED matrix
- Pin #5 - also used for Button A
- Pin #6 - also used for LED matrix
- Pin #7 - also used for LED matrix
- Pin #8
- Pin #9 - also used for LED matrix
- Pin #10 - analog in, also used for LED matrix
- Pin #11 - also used for Button B
- Pin #12
- Pin #13 - also available as SPI clock
- Pin #14 - also available as SPI MISO
- Pin #15 - also available as SPI MOSI
- Pin #16 - also available as SPI Chip Select
- Pin #17 - +3.3V
- Pin #18 - +3.3V
- Pin #19 - also available as I2C clock (SCL)
- Pin #20 - also available as I2C data (SCA)

[Edge Connector Data Sheet](https://tech.microbit.org/hardware/edgeconnector_ds/)
Note different pins have different pull up/down resistance
Using shared pins will trigger unexpected behaviors. Avoid them if possible.

- Buttons (5, 11)
- LEDs (3, 4, 6, 7, 9, 10)  
  Disable LEDs with `led.enable(false)` before used the pins (light sensing will also be disabled)
- Accessibility (12)  
  Reserved for toggling the chip's accessibility mode and should not be used
- I2C (19, 20)  
  on board motion sensor is connected to I2C bus, do not use these other than for I2C  
  (otherwise micro:bit might fail to boot)

[Power Supply](https://tech.microbit.org/hardware/powersupply/)
max input current: 120mA
power usage: 30mA
max current for pins: 90mA

[BBC micro:bit pinout - Espruino](http://www.espruino.com/MicroBit#pinout)
[micro:bit Analog Inputs | The Meandering Pi and Friends](https://meanderingpi.wordpress.com/2017/08/05/microbit-analog-inputs/) using 1.2V as reference for ADC

[micro:bit IoT In C - First Steps With The GPIO](https://www.iot-programmer.com/index.php/books/27-micro-bit-iot-in-c/chapters-micro-bit-iot-in-c/46-micro-bit-iot-in-c-first-steps-with-the-gpio?showall=1)

[吉哥的分享 - micro:bit 的 P0 腳位按法](https://sites.google.com/jes.mlc.edu.tw/ljj/microbit開發板/microbit的p0腳位按法) the touch sensor response to touch and remove, do not touch and hold

> see `learn-to-code-kids.md#capacitive-touch-sensor`

## Education

[Intro to CS - Microsoft MakeCode](https://makecode.microbit.org/courses/csintro) !important, 14 week Introduction to Computer Science course
[From Getting Started to Games - starting Computer Science with the BBC micro:bit | micro:bit](https://microbit.org/en/2018-01-19-train_the_trainer/)
[Physical Computing with the Micro:Bit](http://www.launchcs.com/shop#!/Physical-Computing-with-the-Micro-Bit/p/106450337/category=29069031) 10 Lesson Unit on Physical Computing with the Micro:Bit
[microbit for primary schools – Schemes of work, lesson plans and resources for teachers](http://mb4ps.co.uk/)
[Lessons - Microsoft MakeCode](https://makecode.microbit.org/lessons)
[hastklass micro:bit of Things](https://sites.google.com/view/microbitofthings)

## Coding Environment

[Let's Code | micro:bit](https://microbit.org/code/) Web Editors

### `.hex` file format

[Intel HEX - Wikiwand](https://www.wikiwand.com/en/Intel_HEX)

[.HEX file format](https://tech.microbit.org/software/hex-format/)
Python source code is embedded at address `0x3E000`, source code in the above link.

[pxt/source-embedding.md at 437f53ca6311335c7f3f75a062ec1079b4e7806a · Microsoft/pxt · GitHub](https://github.com/Microsoft/pxt/blob/437f53ca6311335c7f3f75a062ec1079b4e7806a/docs/source-embedding.md)
JavaScript source is embedded as JSON at `0x20000000`.
[Locking and unlocking Javascript Blocks Editor .hex files : Support](https://support.microbit.org/support/solutions/articles/19000053218-locking-and-unlocking-javascript-blocks-editor-hex-files)

[Intel HEX file Viewer](http://www.dlwrr.com/electronics/tools/hexview/hexview.html)
[GitHub - bialix/intelhex: Python IntelHex library](https://github.com/bialix/intelhex)
[nrf-intel-hex | Yet another parser for “Intel HEX” files.](https://nordicsemiconductor.github.io/nrf-intel-hex/) JavaScript

### JavaScript

[Microsoft MakeCode for micro:bit](https://makecode.microbit.org/#)
[Reference - Microsoft MakeCode](https://makecode.microbit.org/reference)
Valid JavaScript can also be converted to blocks

[MakeCode (PXT) Documentation - Microsoft MakeCode](https://makecode.com/docs)
[Device - Microsoft MakeCode](https://makecode.microbit.org/device)

In JavaScript mode, the left panel have an "Explorer" tree in which you can see the source code of the modules (built-in and external) used in project. You can even delete Block mode in "Explorer".

[Microsoft/pxt-microbit: A Blocks / JavaScript code editor for the micro:bit built on Microsoft MakeCode](https://github.com/Microsoft/pxt-microbit)

[Micro:bit offline App](https://makecode.microbit.org/offline-app)

[Makecode-Kittenbot](https://www.kittenbot.cn/newsinfo/969084.html)
[真·Makecode 离线版本下载，串口演示教程（201811111 更新 3.4 版本） - Micro:bit&Robot:bit - Kittenbot 小喵科技——专注图形化编程教育 - Powered by Discuz!](http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=156)

#### Sharable link

When you share the project, an unique ID will be generated:
https://makecode.microbit.org/_EzCf5hfdxif2

The ID can be used to embed the simulator in web site.

```html
<div style="position:relative;height:0;padding-bottom:81.97%;overflow:hidden;">
  <iframe
    style="position:absolute;top:0;left:0;width:100%;height:100%;"
    src="https://makecode.microbit.org/---run?id=_EzCf5hfdxif2"
    allowfullscreen="allowfullscreen"
    sandbox="allow-popups allow-forms allow-scripts allow-same-origin"
    frameborder="0"
  ></iframe>
</div>
```

#### PXT

[Microsoft/pxt: Microsoft MakeCode (PXT - Programming eXperience Toolkit)](https://github.com/Microsoft/pxt)
[Microsoft/pxt-microbit: A Blocks / JavaScript code editor for the micro:bit built on Microsoft MakeCode](https://github.com/Microsoft/pxt-microbit/)
[pxt-microbit - npm](https://www.npmjs.com/package/pxt-microbit)

> also depends on C Runtime

[kadok0520/pxt-microbit - Docker Hub](https://hub.docker.com/r/kadok0520/pxt-microbit/)
[趣味の電子工作: chibi:bit (micro:bit)の PXT 開発環境(Microsoft Make Code)を自宅に構築する](http://takafuminaka.blogspot.com/2017/04/chibibit-microbitpxtmicrosoft-make-code.html)

#### Extensions (libraries)

> they used to be called "Packages"

Use custom blocks for development
[Custom blocks - Microsoft MakeCode](https://makecode.microbit.org/blocks/custom)
[Defining blocks - Microsoft MakeCode](https://makecode.com/defining-blocks)
[MakeCode Playground](https://makecode.com/playground)

Then you can create Github repo and expose that as Extension
[Extensions - Microsoft MakeCode](https://makecode.microbit.org/extensions)
[Building your own extension - Microsoft MakeCode](https://makecode.com/extensions/getting-started)
[GitHub package authoring - Microsoft MakeCode](https://makecode.com/blog/github-packages)

Or install `pxt` locally

```sh
npm i -g pxt  # once
# for each project
mkdir microbit
cd microbit
pxt target microbit
pxt serve
```

[Building your own extension - Microsoft MakeCode](https://makecode.com/extensions/getting-started/vscode)

[吉哥的分享 - 如何製作 makecode 裡的 micro:bit 積木](https://sites.google.com/jes.mlc.edu.tw/ljj/microbit開發板/如何製作makecode裡的microbit積木)
[大榔頭的電腦隨筆: 自製 Makecode 拼塊(一)：製作拼塊檔案](http://hammer1007.blogspot.com/2018/02/makecode_89.html)
[大榔頭的電腦隨筆: 自製 Makecode 拼塊(二)：上傳及使用拼塊](http://hammer1007.blogspot.com/2018/02/makecode_54.html)

[pxt-microbit/libs/core at master · Microsoft/pxt-microbit](https://github.com/Microsoft/pxt-microbit/tree/master/libs/core)
[microbit-makecode-packages](https://github.com/microbit-makecode-packages)
[Tinkertanker](https://github.com/Tinkertanker)
[shaoziyang/microbit-lib: all kinds of microbit python drives, libs, examples, etc.](https://github.com/shaoziyang/microbit-lib)
[lioujj / Repositories](https://github.com/lioujj?tab=repositories&type=source)

[Microsoft/pxt-neopixel: A Neo-Pixel package for pxt-microbit](https://github.com/Microsoft/pxt-neopixel)
[Microsoft/pxt-sonar: A Microsoft MakeCode package to handle sonar sensors and pings](https://github.com/Microsoft/pxt-sonar)
[philipphenkel/pxt-powerfunctions: MakeCode package that turns your micro:bit and Calliope-Mini into a remote control for LEGO Power Functions](https://github.com/philipphenkel/pxt-powerfunctions)
[Microsoft/pxt-bluedot: A PXT package to support the BlueDot app - beta](https://github.com/Microsoft/pxt-bluedot)
[Tinkertanker/pxt-oled-ssd1306: Tinkercademy MakeCode package for using the SSD1306 OLED controller with micro:bit](https://github.com/Tinkertanker/pxt-oled-ssd1306)
[sparkfun/pxt-gamer-bit: SparkFun gamer:bit package for Microsoft MakeCode - beta](https://github.com/sparkfun/pxt-gamer-bit)
[MonadnockSystems/pxt-dht11](https://github.com/MonadnockSystems/pxt-dht11)

[microbit-lib/lcd/I2C_LCD1602 at master · shaoziyang/microbit-lib](https://github.com/shaoziyang/microbit-lib/tree/master/lcd/I2C_LCD1602)
[KittenBot/pxt-powerbrick](https://github.com/KittenBot/pxt-powerbrick)

Use code blocks

```
    "dependencies": {
        "core": "*",
        "ws2812b": "github:Microsoft/pxt-ws2812b#v0.0.4"
    },
```

Then you can use `pins` functions.

[吉哥的分享 - microbit 連接 LCM1602](https://sites.google.com/jes.mlc.edu.tw/ljj/microbit開發板/microbit連接lcm1602)
[吉哥的分享 - microbit 共陰極 RGB 積木](https://sites.google.com/jes.mlc.edu.tw/ljj/microbit開發板/microbit共陰極rgb積木)

#### Threading

[Serial not concurrency safe? · Issue #1157 · Microsoft/pxt-microbit](https://github.com/Microsoft/pxt-microbit/issues/1157)
Actually its the fiber yielding to other threads when blocked by serial IO.

`basic.forever()` vs `control.inBackground()`  
They're both fibers. `inBackground()` have a `fiberDone` callback to clean up after function exited.

https://github.com/Microsoft/pxt-microbit/blob/master/libs/core/basic.cpp#L117-L122
https://github.com/Microsoft/pxt-microbit/blob/master/libs/core/pxt.cpp#L654-L659

### Espruino

[BBC micro:bit - Espruino](http://www.espruino.com/MicroBit)

Another JavaScript runtime, no block programming support

### Scratch

[Scratch - micro:bit](https://scratch.mit.edu/microbit)
[首页 - Mind+ 重装归来 - Mind+官网](http://mindplus.cc/)

[Scratch cards for micro:bit | micro:bit](https://microbit.org/scratch/)
[EduMakerLab STEAM 實驗室: 小玩 Scratch 3.0 之 micro:bit 篇](https://edumakerlab.blogspot.com/2018/08/scratch-30-microbit.html)
[Micro:bit Scratch 課程系列介紹 :: Microbit & STEAM Shop](http://www.astar-tek.com.tw/micro%3abit-scratch-課程系列介紹/)

### MicroPython

> MicroPython API is synchronous and do not implement all of Python 3's feature

[Micro:bit - Python editor](https://python.microbit.org/)
[Code With Mu](https://codewith.mu/en/) offline MicroPython editor
[Mu editor(Micropython)-Kittenbot](https://www.kittenbot.cn/newsinfo/969085.html)

[MicroPython - Python for microcontrollers](http://micropython.org/)
[Overview — MicroPython documentation](https://docs.micropython.org/en/latest/index.html)
[BBC micro:bit MicroPython documentation](https://microbit-micropython.readthedocs.io/en/latest/index.html)
[whaleygeek/microbit_python: Various micro:bit python code examples](https://github.com/whaleygeek/microbit_python)

[Tour of MicroPython on BBC micro:bit with Tony D! @micropython @microbit_edu - YouTube](https://www.youtube.com/watch?v=g9dSOLBD1cg)
[MicroPython on the micro:bit in 60 minutes - RARESchool](http://www.rareschool.com/workshops/)

### MicroBlocks

[MicroBlocks: Small, Fast, Human Friendly](http://microblocks.fun/index.html)

### Over serial/network

[Serial - Microsoft MakeCode](https://makecode.microbit.org/device/serial)
[How do I use the serial port on Windows : Support](https://support.microbit.org/support/solutions/articles/19000022103-how-do-i-use-the-serial-port-with-a-micro-bit-on-windows)
[Mbed OS Documentation | Tutorials](https://os.mbed.com/docs/latest/tutorials/serial-comm.html)

The micro:bit should show up as `/tty/USB*` or `/tty/ACM` after plugging-in.
Add your user to the group of the device, e.g. `sudo usermod -G dialout -a ${USER}`
Baud rate: 115200, 8N1

[吉哥的分享 - micro:bit 數字鋼琴](https://sites.google.com/jes.mlc.edu.tw/ljj/microbit開發板/microbit數字鋼琴)
[吉哥的分享 - 序列埠和 micro:bit 溝通](https://sites.google.com/jes.mlc.edu.tw/ljj/microbit開發板/序列埠和microbit溝通)

[That IoT Thing: Pairing a BBC micro:bit with a Raspberry Pi using BlueZ](https://bluetooth-mdw.blogspot.com/2017/02/pairing-bbc-microbit-with-raspberry-pi.html)
[Raspberry 樹莓派 & Micro:bit :: Microbit & STEAM Shop](http://www.astar-tek.com.tw/raspberry-micro-bit/)

### C runtime

Used by upper layers, you can also use it directly.

[micro:bit runtime](https://lancaster-university.github.io/microbit-docs/)
[lancaster-university/microbit](https://github.com/lancaster-university/microbit) basic wrapper around the DAL
[lancaster-university/microbit-dal](https://github.com/lancaster-university/microbit-dal)
[lancaster-university/microbit-samples](https://github.com/lancaster-university/microbit-samples)

[micro:bit IoT In C](https://www.iot-programmer.com/index.php/books/26-micro-bit-iot-in-c)
[Micro:bit Programs](https://iopress.info/index.php/2-uncategorised/9-micro-bit-programs)
[Programming using C/C++ (Offline IDE Setup) | BBC Microbit - Hackster.io](https://www.hackster.io/weargenius/programming-using-c-c-offline-ide-setup-bbc-microbit-90a6e5)

[Home | Mbed](https://www.mbed.com/en/)
[yotta Documentation - yotta](http://docs.yottabuild.org/)

[QEMU 4.0 adds micro:bit emulation support - QEMU](https://www.qemu.org/2019/05/22/microbit/)

### Rust

[GitHub - therealprof/microbit: A Rust crate for BBC micro:bit development](https://github.com/therealprof/microbit)
[Rust on BBC micro:bit using Windows • Flames of Code](https://flames-of-code.netlify.com/blog/rust-microbit-windows/)

### Arduino IDE

[sandeepmistry/arduino-nRF5: Arduino Core for Nordic Semiconductor nRF5 based boards](https://github.com/sandeepmistry/arduino-nRF5/)
[Overview | Micro:bit with Arduino | Adafruit Learning System](https://learn.adafruit.com/use-micro-bit-with-arduino?view=all)

[08 利用 Blynk APP 控制 - 阿玉 micro:bit 研究區](https://sites.google.com/site/wenyumaker2/02micro-bit-yan-jiu/08li-yongblynk-app-kong-zhi)
[24 Micro:bit with Arduino - 阿玉 micro:bit 研究區](https://sites.google.com/site/wenyumaker2/02micro-bit-yan-jiu/23-micro-bit-with-arduino)

## Updating Firmware

[Troubleshooting downloads with WebUSB - Microsoft MakeCode](https://makecode.microbit.org/device/usb/webusb/troubleshoot)
[Upgrading the micro:bit firmware : Support](https://support.microbit.org/support/solutions/articles/19000019131-how-to-upgrade-the-firmware-on-the-micro-bit)
[DAPLink on micro:bit (KL26Z) | Mbed](https://www.mbed.com/en/platform/hardware/prototyping-production/daplink/daplink-on-kl26z/#Updating_your_DAPLink_firmware)

## Android test apps

[How to pair your BBC micro:bit with an Android phone or tablet - YouTube](https://www.youtube.com/watch?v=7hLBfdAGkZI)

[micro:bit Blue - Apps on Google Play](https://play.google.com/store/apps/details?id=com.bluetooth.mwoolley.microbitbledemo&rdid=com.bluetooth.mwoolley.microbitbledemo)
[microbit-foundation/microbit-blue](https://github.com/microbit-foundation/microbit-blue)

[bitty blue - Apps on Google Play](https://play.google.com/store/apps/details?id=com.bittysoftware.bittyblue.BittyBlue)
[Bitty Software](http://www.bittysoftware.com/downloads.html#bitty_blue)

## Networking

[Networking with the micro:bit - Nominet](https://www.nominet.blog/networking-with-the-microbit/)

## Extension boards

[microbit 转接板 microbit 扩展板 IOBIT KittenBot 小喵科技-淘宝网](https://item.taobao.com/item.htm?id=567838559503) v1 ¥29 (¥20.3), KittenBot, 20pins x 3, micro USB power, buzzer, LEGO compatible

[micro:bit 能量魔块扩展板 Armourbit 图形编程 兼容乐高 小喵科技-淘宝网](https://item.taobao.com/item.htm?id=593081651784) ¥139, KittenBot, 20pins x 8, 4pins PH 2.0 x 7, PH2.0 3-3.7V power, buzzer, LEGO compatible

[micro:bit 转接板 micro:bit 扩展板 IOBIT ittenBot 创客教育套件-淘宝网](https://item.taobao.com/item.htm?id=573067000645) ¥28 (¥18), HJduino, 20pins x 3, micro USB power, buzzer, LEGO compatible, ~= KittenBot IOBIT v1

[Micro:bit 3V 传感器扩展板 Sensor:bit-淘宝网](https://item.taobao.com/item.htm?id=572685991359) ¥49.9 (¥39.9), ElecFreaks Sensor:bit, 20pins x 3, buzzer, separate i2c pins, LEGO compatible

[BBC micro:bit GPIO 扩展板 B 直接插入方便使用-淘宝网](https://item.taobao.com/item.htm?id=559637644083) ¥14.85, 20pins face up, with 6+4 crocodile clip pins

[微雪 micro:bit 接口扩展板 microbit 转接板 IO 扩展板 模块-淘宝网](https://item.taobao.com/item.htm?id=566819104996) ¥44.5, 20pins x 2, with 3+2 crocodile clip holes

[micro：bit GPIO 扩展板 micro：bit 创客教育 Python 编程开发板-淘宝网](https://item.taobao.com/item.htm?id=576358788444) ¥35, 13+8pins face up, with 9+2 crocodile clip pins

[【YwRobot】英国 BBC Micro:bit 金手指扩展板转接板 Breakout MINI-淘宝网](https://item.taobao.com/item.htm?id=575760081889) ¥15, 13pins face up/down/side

[Microbit 开发板扩展板 Python 编程创客教育 micro:bit 转接板 T 型-淘宝网](https://item.taobao.com/item.htm?id=574480410787) ¥24.9, T-shaped for breadboard, _mini USB in, 5V out_
[【YwRobot】英国 BBC Micro:bit 扩展板 主板转接板面包板 Breakout-淘宝网](https://item.taobao.com/item.htm?id=567613131317) ¥32.76, T-shaped for breadboard, 20pins face up, with crocodile clip pins
[micro:bit T 型扩展板转接头 板载接口 micro:bit 全兼容 Python 编程-淘宝网](https://item.taobao.com/item.htm?id=572484338905) ¥23, T-shaped for breadboard, Keyes Red
[Micro:bit GPIO 扩展板 Breakout 转接板拓展板 microbit 亚博智能-淘宝网](https://item.taobao.com/item.htm?id=561758010873) 29.5, pins face down for breadboard

[DFROBOT 出品 Micro:Mate——超迷你的 micro:bit 多功能 I/O 扩展板-淘宝网](https://item.taobao.com/item.htm?id=565924031498) DFRobot Micro:Mate

- Gravity compatible
- 3.5/5V
- 3.5mm jack
- screw on top of Micro:bit

[microbit Octopus:bit 八爪鱼拓展板 breakout board Micro:bit-淘宝网](https://item.taobao.com/item.htm?id=564775918834) ¥83.90, Elecfreaks Octopus:bit

- Octopus connectors
- 3.5/5V

[BBC Micro:bit 扩展板 microbit 转接板拓展板 DIY 智能小车 亚博-淘宝网](https://item.taobao.com/item.htm?id=564678119175) ¥117.39, 亚博 Bitbot

- 2 RGB LED spotlight
- 3 RGB LED
- 2 DC, 3 servo
- buzzer
- LiPo with charging
- infrared receiver
- line tracking sensor
- distance sensor
- port for ultrasound sensor
- XH2.54 3.7V power
- mobile app
- [智能学习-microbit 扩展板（专业级）](http://www.yahboom.com/study/bitbot-board)
- [micro:bit expansion board](https://www.yahboom.net/study/breakout)
- [lzty634158/yahboom_mbit](https://github.com/lzty634158/yahboom_mbit)
- [lzty634158/yahboom_mbit_en: This is yahboom_mbit English version.](https://github.com/lzty634158/yahboom_mbit_en)
- better buy 智能小车 set (¥228)
- [智能学习-Mirco:bit 智能小车](http://www.yahboom.com/study/Bitbot) `h0zd`
- [micro:bit robot](https://www.yahboom.net/study/Bitbot)
- [micro：bit smart robot - YouTube](https://www.youtube.com/watch?v=y5QCgXlHN_I)

[Micro:bit 扩展板 积木电机舵机开发驱动板套件 microbit 传感器 GPIO-淘宝网](https://item.taobao.com/item.htm?id=590223678300) ¥99, 亚博 Super:bit

- crocodile clip pins
- 4 RGB LED
- 4 DC, 8 servo
- buzzer
- 18650 with charging
- Lego compatible
- [智能学习-Super:bit 多功能扩展板](https://www.yahboom.com/study/Super:bit) `4hnu`
- [Super:bit_expansion_board](https://www.yahboom.net/study/Super:bit)
- [lzty634158/SuperBit: microbit 多功能扩展板](https://github.com/lzty634158/SuperBit)

[micro:bit 扩展板 microbit 中小学入门 Robotbit V2.1 Python 编程-淘宝网](https://item.taobao.com/item.htm?id=559862615142) ¥99, Robot:bit

- 4 RGB LED
- 4 DC, 8 servo
- buzzer
- 18650 with charging
- Lego compatible
- [KittenBot/pxt-robotbit: Robotbit extension for makecode](https://github.com/KittenBot/pxt-robotbit)
- [Robotbit -robotics expansion board for micro:bit – KittenBot](https://www.kittenbot.cc/collections/frontpage/products/robotbit-robotics-expansion-board-for-micro-bit)
- [2. Robotbit V2.0 详解 — kittenbot docs 文档](https://kittenbot.readthedocs.io/zh_CN/latest/mainboards/Robotbitv2.0.html)

[MBot 拓展板 Micro:bit 电机扩展板-淘宝网](https://item.taobao.com/item.htm?id=574070307498) ¥190.9 Elecfreaks Robit

- Makeblock compatible
- 4 DC/2 step, 8 servo
- Octopus, RJ25 connectors

[Micro:bit Elecfreaks motor:bit Microbit 电机驱动板 扩展板-淘宝网](https://item.taobao.com/item.htm?id=564916191336) ¥89.90, Elecfreaks motor:bit

- 2 DC, 8 servo
- buzzer
- 3.5/5V
- Octopus connectors

[Microbit Micro:bit 扩展板机器人/品牌原装 Python 编程创客教育-淘宝网](https://item.taobao.com/item.htm?id=563435199195) ¥111.6, LOBOT

- 2 RGB LED
- 2 DC, 6+2 servo
- buzzer, mic
- port for ultrasound and color sensor
- 18650 with charging
- LEGO compatible

[microbit 可编程电子积木/DaDa:bit 套件/创客教育 micro:bit 机器人-淘宝网](https://item.taobao.com/item.htm?id=589922037484) ¥122, LOBOT

- 2 RGB LED
- 2 DC, 6 servo
- 4 pin x 6
- buzzer, mic
- serial port
- 18650 with charging
- LEGO compatible

[Microbit Micro:bit 机器人扩展板 Magishield 青少年创客教育-淘宝网](https://item.taobao.com/item.htm?id=566089463412) ¥129, Magishield

- 2 DC, 5 servo
- LiPo with charging
- battery hidden behind board
- LEGO compatible

### Kittenbot

[KittenBot](https://www.kittenbot.cc/)
[KittenBot/kittenbot-docs](https://github.com/KittenBot/kittenbot-docs)
[欢迎来到 Kittenbot 的文档与教程 — kittenbot docs 文档](https://kittenbot.readthedocs.io/zh_CN/latest/index.html)

[Micro:bit 教程汇总目录（20180710 更新） - Micro:bit&Robot:bit - Kittenbot 小喵科技——专注图形化编程教育 - Powered by Discuz!](http://kittenbot.cn/bbs/forum.php?mod=viewthread&tid=104)
[Micro:bit&Robot:bit - Kittenbot 小喵科技——专注图形化编程教育 - Powered by Discuz!](http://kittenbot.cn/bbs/forum.php?mod=forumdisplay&fid=37)

## Box sets

All of these are rip-offs

[智能学习-micro-bit 套件](http://www.yahboom.com/study/microbit)
¥306
[Micro:bit Microbit 入门初学者套件 Python 图形编程 中小学教育-tmall.com 天猫](https://detail.tmall.com/item.htm?id=568601231960)
[Micro:bit 开发板扩展板 青少年入门套件 图形编程 microbit 转接板-淘宝网](https://item.taobao.com/item.htm?id=575429498498)

## Projects

[Projects - Microsoft MakeCode](https://makecode.microbit.org/projects)
[The BBC micro:bit , lesson packs and accessories – ETC Educational Technology Connection (HK) Ltd](https://www.etchkshop.com/collections/bbc-micro-bit)

[BBC micro:bit | Free Platform for Coding, Making and Inventing | Make | Tech Will Save Us](https://make.techwillsaveus.com/microbit/)
[BBC micro:bit | Micro BMO | Free Platform for Coding, Making and Inventing | Make | Tech Will Save Us](https://make.techwillsaveus.com/microbit/activities/micro-bmo)
[BBC micro:bit | Micro Pet | Free Platform for Coding, Making and Inventing | Make | Tech Will Save Us](https://make.techwillsaveus.com/microbit/activities/micro-pet-advanced)
[Math Training Thru Micro:bit Icons (ClientVersion) - Hackster.io](https://www.hackster.io/philip-cua/math-training-thru-micro-bit-icons-clientversion-478758)

[BBC micro:bit | 101 Computing](https://www.101computing.net/category/bbc-microbit/)

[Micro:bit - Getting Started — UCL BBC micro:bit tutorial](https://microbit-challenges.readthedocs.io/en/latest/) MicroPython, good tutorial on built-in sensors

[micro:bit - Maker Education](http://www.makereducation.com/microbit.html)
[Microbit Project Ideas - YouTube](https://www.youtube.com/playlist?list=PLHC1XA0PhqHkBc3ErWVmcRQ8jB9sfS3aU)
[jffwferq (my scripts) - BBC micro:bit](https://www.microbit.co.uk/app/#list:installed-scripts:user:jffwferq:overview)
[智能学习-micro-bit 套件](http://www.yahboom.com/study/microbit)
[智能学习-Mirco:bit 智能小车](http://www.yahboom.com/study/Bitbot) `h0zd`
[micro:bit | Tutorials - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/tags/micro-bit)

[Micro:Bit 手柄试用+DF 电机驱动板体验：红汽车新生记（另附.....—Micro:bit 论坛—DF 创客社区 -](http://mc.dfrobot.com.cn/forum.php?mod=viewthread&tid=37934) Fix BlockyTalky clashing with MagicPad

[classic beatbox - Microsoft MakeCode](https://makecode.microbit.org/lessons/classic-beatbox)

[ElecFreaks Blog](https://www.elecfreaks.com/store/blog.html)
[How To Make A Six-feet Micro:bit Insect - Blog](https://www.elecfreaks.com/store/blog/post/how-to-make-a-six-feet-microbit-insect.html)

[ornberg/microbit-quiz](https://github.com/ornberg/microbit-quiz)

[Microbit Example | Scoop.it](https://www.scoop.it/t/microbit-edumakerlab/)
[阿玉 micro:bit 研究區](https://sites.google.com/site/wenyumaker2/)
[阿玉 MAKER 研究區(2018 年版)](https://sites.google.com/site/wenyumaker3/)
[嘰哩呱啦 ACE (2 代)](https://glglace.blogspot.com/search/label/micro:bit)
[擁有英國血統！BBC 強打的 Micro Bit！不容錯過！-INPLUS](http://inplus.tw/bbc-micro-bit)

[25 上音樂課了 - 阿玉 micro:bit 研究區](https://sites.google.com/site/wenyumaker2/02micro-bit-yan-jiu/25shang-yin-le-ke-le)
[29 電流急急棒 - 阿玉 micro:bit 研究區](https://sites.google.com/site/wenyumaker2/02micro-bit-yan-jiu/29dian-liu-ji-ji-bang)

[micro:bit plant water pump - YouTube](https://www.youtube.com/watch?v=jANCdtkJAKY)
[Make Your BBC Micro:Bit Talk Using MicroPython - micro:bit Projects](https://microbit.hackster.io/anish78/make-your-bbc-micro-bit-talk-using-micropython-7bdb10)
[Speech — BBC micro:bit MicroPython documentation](https://microbit-micropython.readthedocs.io/en/latest/tutorials/speech.html#)

[micro:bit - SparkFun Electronics](https://www.sparkfun.com/categories/284)
[Microbit 自动浇水套件水泵灌溉浇花模块土壤湿度检测自动 DIY 套装-淘宝网](https://item.taobao.com/item.htm?id=575157547280) ¥88
[Microbit 机器人套件/扩展板机械臂小车 Armbit/小 R 科技创客教育-淘宝网](https://item.taobao.com/item.htm?id=570576057974) ¥478
[Micro:bit 智能小车机器人套件 Microbit 图形化编程开发板 STEM 亚博-淘宝网](https://item.taobao.com/item.htm?id=564643202667) ¥228, 亚博 board
[Qbit/micro:bit 创客教育套件 microbit 编程机器人平衡小车 LOBOT-淘宝网](https://item.taobao.com/item.htm?id=575687772267) ¥279.84, balance car, LOBOT board
[BBC micro:bit 小车 Ringbit car 迷你智能小车 智能机器人-淘宝网](https://item.taobao.com/item.htm?id=573513759509) ¥138, servo as motor

亚博
[智能学习-Mirco:bit 智能小车](http://www.yahboom.com/study/Bitbot) ¥228/¥330
[智能学习-HelloBot 机器人](http://www.yahboom.com/study/HelloBot)

[首页-KittenBot-淘宝网](https://kittenbot.taobao.com/) expensive
[Kittenbot Home](http://kittenbot.cn/#/home)
[Kittenbot](http://www.kittenbot.cc/)
[2. Robotbit V2.0 详解 — kittenbot docs 文档](http://learn.kittenbot.cn/zh_CN/latest/)
[micro:bit Robotbit LEGO 乐高 伺服电机 舵机 makecode 编程 四个-淘宝网](https://item.taobao.com/item.htm?id=572085241353)

---

# CALLIOPE mini

Calliope mini is a micro:bit compatible board pushed by German government

[CALLIOPE | About mini](https://calliope.cc/en/idee/ueber-mini)
[The Little Computer That Could](https://global.handelsblatt.com/politics/the-little-computer-that-could-690080)
[Introducing the Calliope mini - YouTube](https://www.youtube.com/watch?v=YA5Kk5gdpX0)

# BPI:bit

[An ESP32-Based Micro:bit Clone – Hackster Blog](https://blog.hackster.io/an-esp32-based-micro-bit-clone-93c170d6c563)
[BPI-UNO32 - Banana Pi Wiki](http://wiki.banana-pi.org/BPI-UNO32)
