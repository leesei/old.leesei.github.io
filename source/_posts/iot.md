---
title: "Internet of things"
categories:
  - maker
tags:
  - iot
toc: true
date: 2018-06-12 13:35:14
---

> see `electronics.md`

[Internet of things - Wikiwand](http://www.wikiwand.com/en/Internet_of_things)
[Embedded system - Wikiwand](http://www.wikiwand.com/en/Embedded_system)
[Microcontroller - Wikiwand](http://www.wikiwand.com/en/Microcontroller)

[Mesh networking extends IoT reach - O'Reilly Radar](http://radar.oreilly.com/2014/07/mesh-networking-extends-iot-reach.html)
[Extracting value from the IoT - O'Reilly Radar](http://radar.oreilly.com/2014/06/extracting-value-from-the-iot.html)

[How Arduino is open-sourcing imagination | Massimo Banzi - YouTube](https://www.youtube.com/watch?v=UoBUXOOdLXY)

## IDE, Platforms and Frameworks

> see `learn-to-code-kids.md#physical-programming-with-blocks`

### Firmata

[Main Page - Firmata](http://firmata.org/wiki/Main_Page)
Firmata is a generic protocol for communicating with microcontrollers from software on a host computer. Allows for controlling the MCU from different languages.

[firmata/arduino: Firmata firmware for Arduino](https://github.com/firmata/arduino)
[firmata/protocol: Documentation of the Firmata protocol.](https://github.com/firmata/protocol)

### Arduino IDE

Arduino IDE can be used for Arduino-compatible boards. It provides a compile toolchain, editor, standard libraries and libraries convention for embedded system programming.

[Arduino - ArchWiki](https://wiki.archlinux.org/index.php/Arduino)
`pacman -Sy arduino`

[Arduino IDE: Creating Custom Boards - Hackster.io](https://www.hackster.io/wallarug/arduino-ide-creating-custom-boards-89f7a6)
[Unofficial list of 3rd party boards support urls · arduino/Arduino Wiki](https://github.com/arduino/Arduino/wiki/Unofficial-list-of-3rd-party-boards-support-urls)
[Arduino IDE 1.5 3rd party Hardware specification · arduino/Arduino Wiki](https://github.com/arduino/Arduino/wiki/Arduino-IDE-1.5-3rd-party-Hardware-specification)

[Arduino Editor](https://create.arduino.cc/editor/) Web version, account required
[Getting Started with Arduino Web Editor on Various Platforms - Arduino Project Hub](https://create.arduino.cc/projecthub/Arduino_Genuino/getting-started-with-arduino-web-editor-on-various-platforms-4b3e4a)

[Arduino - Hacking](https://www.arduino.cc/en/Hacking/HomePage)
[Build Process · arduino/Arduino Wiki](https://github.com/arduino/Arduino/wiki/Build-Process)

`Ctrl+U` to upload

There are two important folders Sketchbook location (`~/ardiono/sketchbook`):

- `hardware/`
- `libaries/`

[Arduino Blog » Announcing the Arduino Command Line Interface (CLI)](https://blog.arduino.cc/2018/08/24/announcing-the-arduino-command-line-interface-cli/)
[arduino/arduino-cli: Arduino command line interface](https://github.com/arduino/arduino-cli)
[Announcing the New Arduino Command Line Interface – Hackster Blog](https://blog.hackster.io/announcing-the-new-arduino-command-line-interface-cfc4c49e103b)
[Arduino Command Line Interface Is Here! | Open Electronics](https://www.open-electronics.org/arduino-command-line-interface-is-here/)

[The \$2 32-Bit Arduino (with Debugging) | Hackaday](https://hackaday.com/2017/03/30/the-2-32-bit-arduino-with-debugging/)

#### Libraries

[All Libraries - Arduino Libraries](https://www.arduinolibraries.info/libraries)
[Arduino Libraries | Arduino Tips, Tricks, and Techniques | Adafruit Learning System](https://learn.adafruit.com/arduino-tips-tricks-and-techniques/arduino-libraries?view=all#arduino-libraries)
[Arduino Libraries | All About Arduino Libraries | Adafruit Learning System](https://learn.adafruit.com/adafruit-all-about-arduino-libraries-install-use)
[Arduino Libraries! What they are, how they work and how to install them – Brainy-Bits](https://www.brainy-bits.com/arduino-libraries-tutorial/)

"Sketch" -> "Add Library" -> select file -> done

Manually add libraries:
Windows: `%USERPROFILE%\Documents\Arduino\libraries\`
Mac OSX: `~/Documents/Arduino/libraries/`
Linux: `~/Documents/Arduino/libraries/`

[Adafruit Industries](https://github.com/adafruit) many libraries for Adafruit board/components, use for reference
[knolleary/pubsubclient: A client library for the Arduino Ethernet Shield that provides support for MQTT.](https://github.com/knolleary/pubsubclient)
[Makeblock-official/Makeblock-Libraries: Arduino Library for Makeblock Electronic Modules, learn more from Makeblock official website](https://github.com/Makeblock-official/Makeblock-Libraries)

[Arduino Reference - Keyboard](https://www.arduino.cc/reference/en/language/functions/usb/keyboard/)
[Arduino - MIDIUSB](https://www.arduino.cc/en/Reference/MIDIUSB)
[Get The App](https://labz.makeymakey.com/d/) by Makey Makey, actually just keyboard events

[Technoblogy - Minimal Tiny I2C Routines](http://www.technoblogy.com/show?24R7)
[technoblogy/tiny-i2c: Minimal I2C master routines for ATtiny processors with a USI.](https://github.com/technoblogy/tiny-i2c)
[Technoblogy - Tiny Graphics Library](http://www.technoblogy.com/show?23OS)

#### Writing Library

[Arduino - LibraryTutorial](https://www.arduino.cc/en/Hacking/LibraryTutorial)

[#71 How to create an Arduino Library - easy! - YouTube](https://www.youtube.com/watch?v=fE3Dw0slhIc)

#### Plugins

[esp8266/arduino-esp8266fs-plugin: Arduino plugin for uploading files to ESP8266 file system](https://github.com/esp8266/arduino-esp8266fs-plugin)
[me-no-dev/arduino-esp32fs-plugin: Arduino plugin for uploading files to ESP32 file system](https://github.com/me-no-dev/arduino-esp32fs-plugin)

### XOD

[XOD](https://xod.io/)
[XOD is a cool way to program Arduino without coding – Boing Boing](https://boingboing-net.cdn.ampproject.org/v/s/boingboing.net/2019/06/04/xod-is-a-cool-way-to-program-a.html/amp)

### Platform.io

[An open source ecosystem for IoT development · PlatformIO](https://platformio.org/)
[PlatformIO is an open source ecosystem for IoT development — PlatformIO documentation](http://docs.platformio.org/en/latest/)

[PlatformIO IDE: The next-generation integrated development environment for IoT · PlatformIO](https://platformio.org/platformio-ide)
[PlatformIO IDE - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide)
[PlatformIO IDE for VSCode — PlatformIO documentation](https://docs.platformio.org/en/latest/ide/vscode.html#quick-start)

[Embedded Boards · PlatformIO](https://platformio.org/boards)

### Control over Serial

[Visualizing Data with Arduino](https://www.electroschematics.com/13439/visualizing-data-arduino/) Processing
[Arduino Playground - Python](https://playground.arduino.cc/interfacing/python)

### Frameworks

[NodeUp #73](http://nodeup.com/seventythree)
[#177: Cylon.js, Gobot, Artoo, and IoT with Ron Evans from The Hybrid Group - Changelog](https://changelog.com/177/)

[Nitrogen: A platform for connecting devices and applications.](http://nitrogen.io/index.html) authority framework
[nitrogenjs](https://github.com/nitrogenjs)
[nitrogen](https://www.npmjs.com/package/nitrogen)

[Node-RED](http://nodered.org/) A visual tool for wiring the Internet of Things
[Node-Red 簡介與快速安裝](https://www.arthurtoday.com/2016/10/node-red-introduction-and-installation.html)

[NodeBots - The Rise of JS Robotics](http://nodebots.io/)
[Cylon.js - JavaScript framework for robotics, physical computing, and the Internet of Things using Node.js](https://cylonjs.com/)
[Gobot - Golang framework for robotics, physical computing, and the Internet of Things (IoT)](https://gobot.io/)
[Artoo - Ruby framework for robotics, physical computing, and the Internet of Things](http://artoo.io/)
[JavaScript Robotics Platform Support (Johnny-Five)](http://johnny-five.io/platform-support/) execute JS on host for some board

### Partition Size

ESP32 with Bluetooth Classic may need a expand to the partition

[Change partition size (PlatformIO) – Bernd's development stuff](https://desire.giesecke.tk/index.php/2018/04/20/change-partition-size-platformio/)
[Change partition size (Arduino IDE) – Bernd's development stuff](https://desire.giesecke.tk/index.php/2018/04/20/change-partition-size-arduino-ide/)

[Add BluetoothSerial library by copercini · Pull Request #1144 · espressif/arduino-esp32](https://github.com/espressif/arduino-esp32/pull/1144)

## Python on SoC

[Ah! I see you have the machine that goes "BING"! - Dr. Graeme Cross - YouTube](https://www.youtube.com/watch?v=nzCvomTixzU)

[PyMite - Python Wiki](https://wiki.python.org/moin/PyMite)
[MicroPython - Python for microcontrollers](https://micropython.org/)
[What is CircuitPython? | Welcome to CircuitPython! | Adafruit Learning System](https://learn.adafruit.com/welcome-to-circuitpython/what-is-circuitpython?view=all)
[A Coming of Age for CircuitPython? – Hackster Blog](https://blog.hackster.io/a-coming-of-age-for-circuitpython-efb1b9c61aa3)
[Pyxie -- A Little Python to C++ Compiler](http://www.sparkslabs.com/pyxie/index.html)

[Using MicroPython in the wild - YouTube](https://www.youtube.com/watch?v=WI-nTf5iM84)
[GOTO 2016 • MicroPython & the Internet of Things • Damien George - YouTube](https://www.youtube.com/watch?v=EvGhPmPPzko)
[arduino vs micropython (Comparison) - YouTube](https://www.youtube.com/watch?v=LqBmnIF9y_s)

[How to Load MicroPython on a Microcontroller Board - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/how-to-load-micropython-on-a-microcontroller-board/all)
[Welcome to Micropython on ESP8266 Workshop’s documentation! — Micropython on ESP8266 Workshop 1.0 documentation](https://micropython-on-wemos-d1-mini.readthedocs.io/en/latest/)
[Getting Started with MicroPython on ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/getting-started-micropython-esp32-esp8266/)
[Python on ESP32: easy for beginners, powerful for professionals | Open Electronics](https://www.open-electronics.org/python-on-esp32-easy-for-beginners-powerful-for-professionals/)
[Programming an Arduino using Python, rather than C/C++ - Arduino Stack Exchange](https://arduino.stackexchange.com/questions/105/programming-an-arduino-using-python-rather-than-c-c)

[User Guide — Pumbaa documentation](https://pumbaa.readthedocs.io/en/latest/user-guide.html) MicroPython on Simba

## JavaScript for SoC

> see `espressif#espruino`

[Johnny-Five: The JavaScript Robotics & IoT Platform](http://johnny-five.io/)

[Duktape](http://duktape.org/)

[Platform for Internet of Things with JavaScript](http://iotjs.net/)
[JavaScript engine for Internet of Things](http://jerryscript.net/)
[jerryscript-project/jerryscript: Ultra-lightweight JavaScript engine for the Internet of Things.](https://github.com/jerryscript-project/jerryscript)
[Samsung/iotjs](https://github.com/Samsung/iotjs)
[JerryScript & IoT.js: JavaScript for IoT from Samsung](http://www.infoq.com/news/2015/08/iotjs-jerryscript-samsung)

### Espruino

[JavaScript On Microcontrollers - YouTube](https://www.youtube.com/watch?v=MuZfdmcplQA)
[Espruino - JavaScript for Microcontrollers](https://www.espruino.com/)
[Espruino Web IDE](https://www.espruino.com/ide/)

[Espruino on ESP8266 WiFi](http://www.espruino.com/EspruinoESP8266)
[Espruino on ESP32](http://www.espruino.com/ESP32)
[BBC micro:bit - Espruino](http://www.espruino.com/MicroBit)

[How to Flash/Install Espruino on an ESP8266 Dev Board/Microcontroller (MacOS) - YouTube](https://www.youtube.com/watch?v=j9xwgeE9u8E)

## Connectivity

> see `bluetooth.md`
> see `wifi.md`

http://wsnblog.com/tag/dash7/

http://en.wikipedia.org/wiki/DASH7
http://en.wikipedia.org/wiki/ZigBee
http://en.wikipedia.org/wiki/Z-Wave
http://en.wikipedia.org/wiki/FM-UWB

Rasberry Pi Zero W has Wifi and Bluetooth built-in.

ESP8266 is a common Wifi chipset. ESP32 is the next generation with Bluetooth and Wifi builtin.

[LoRa Module VS nRF24 VS Generic RF Module || Range & Power Test - YouTube](https://www.youtube.com/watch?v=nP6YuwNVoPU)

### Wifi

ESP8266
ESP32 (Bluetooth + Wifi)

### Bluetooth

ESP32 (Bluetooth + Wifi)

Arduino requires an external BT module.
HC-05/HC-06/HC-10 are common Wifi modules using ESP8266
[Arduino - ArduinoBoardBT](https://www.arduino.cc/en/Main/ArduinoBoardBT)

[Connect Arduino Uno to Android Via Bluetooth: 6 Steps](https://www.instructables.com/id/Connect-Arduino-Uno-to-Android-via-Bluetooth/)
[Bluetooth Basics: How to Control an LED Using a Smartphone and Arduino  | Arduino | Maker Pro](https://maker.pro/arduino/tutorial/bluetooth-basics-how-to-control-led-using-smartphone-arduino)
[Communicate with Your Arduino Through Android](https://www.allaboutcircuits.com/projects/communicate-with-your-arduino-through-android/)

### LPWAN/LoRA/6LoWPAN

[LPWAN](https://www.wikiwand.com/en/LPWAN): Low Power Wide Area Network
[LoRa](https://www.wikiwand.com/en/LoRa): Long Range
[6LoWPAN](https://www.wikiwand.com/en/6LoWPAN): IPv6 over Low-Power Wireless Personal Area Networks

[Low Power Wide Area Network Personal Area Networks | Microchip Technology Inc. | Microchip Technology Inc.](http://www.microchip.com/pagehandler/en-us/technology/personalareanetworks/technology/lora.html)

[#112 LoRa / LoRaWAN De-Mystified / Tutorial - YouTube](https://www.youtube.com/watch?v=hMOwbNUpDQA)

[nRF5 IoT SDK: 6LoWPAN over BLE](https://developer.nordicsemi.com/nRF5_IoT_SDK/doc/0.9.0/html/a00011.html)
[Connecting the Nordic nRF52 chip to IPv6 networks via 6LoWPAN | VisualGDB Tutorials](https://visualgdb.com/tutorials/arm/nrf51/6lowpan/)

### CSR

[Wireless Technology Solutions for the Consumer Electronics Market](http://www.csr.com/)
[CSRmesh - csr](https://wiki.csr.com/wiki/CSRmesh)
[CSRmesh Advantages and Applications - YouTube](https://www.youtube.com/watch?v=XRL0jH4v3zE)

### Modulation

[Modulation - Wikiwand](https://www.wikiwand.com/en/Modulation)
[Frequency-shift keying - Wikiwand](https://www.wikiwand.com/en/Frequency-shift_keying) FSK, GFSK
[Minimum-shift keying - Wikiwand](https://www.wikiwand.com/en/Minimum-shift_keying) MSK, GmSK

[Software Radio Basics - YouTube](https://www.youtube.com/watch?v=BK9QkHxeYQI)
[Understanding MSK, GMSK, FSK, GFSK Modulator and Demodulator with BER Scientech 2809 - YouTube](https://www.youtube.com/watch?v=Su0--12TfFE)
[#170: Basics of IQ Signals and IQ modulation & demodulation - A tutorial - YouTube](https://www.youtube.com/watch?v=h_7d-m1ehoY)

## Edge Computing

[Kubeedge](https://kubeedge.netlify.com/)
[kubeedge/website: KubeEdge website and documentation repo:](https://github.com/kubeedge/website)

## Wireless Control

[RadioHead: RadioHead Packet Radio library for embedded microprocessors](http://www.airspayce.com/mikem/arduino/RadioHead/index.html)

[nRF24L01 Wireless Joystick for Arduino Robot Car | DroneBot Workshop](https://dronebotworkshop.com/nrf24l01-wireless-joystick/)

[RBController - Apps on Google Play](https://play.google.com/store/apps/details?id=com.tassadar.rbcontroller)
[RoboticsBrno/RB3201-RBProtocol-library: Library implementing the RBController protocol by RoboticsBrno.](https://github.com/RoboticsBrno/RB3201-RBProtocol-library)

### PS2 Controller

Taobao has cheap wireless controller for PS2 ([PS2 无线手柄](https://s.taobao.com/search?q=ps2+%E6%89%8B%E6%9F%84+%E7%84%A1%E7%B7%9A&ie=utf8)), with the spec available, we can use it for controlling.
[Interfacing a PS2 (PlayStation 2) Controller - CuriousInventor Tutorials](http://store.curiousinventor.com/guides/PS2)
[PlayStation 2 Controller Arduino Library v1.0 « The Mind of Bill Porter](http://www.billporter.info/2010/06/05/playstation-2-controller-arduino-library-v1-0/)
[madsci1016/Arduino-PS2X: Read a Playstation 2 Gamepad or Guitar Hero Controller using an Arduino](https://github.com/madsci1016/Arduino-PS2X/)

[Interfacing PS2 Wireless Controller With Arduino](http://www.rhydolabz.com/wiki/?p=12663)
[Using A Playstation 2 Controller with your Arduino Project](http://www.techmonkeybusiness.com/using-a-playstation-2-controller-with-your-arduino-project.html)
[Control Anything With Ps2 Controller and Arduino (wirelessly): 6 Steps](https://www.instructables.com/id/Control-anything-with-ps2-controller-and-Arduino-/)

[PlayStation 2 Compatible Controller - COM-10330 - SparkFun Electronics](https://www.sparkfun.com/products/retired/10330)

### Bluetooth

PS3/PS4 controller is a slave device in Bluetooth Classic. None of the embedded SOC supports Bluetooth Classic master mode at the moment. We need to use an USB host shield and USB dongle.
http://wiki.ps2dev.org/ps3:hardware:sixaxis
[TKJ Electronics » PS4 controller now supported by the USB Host library](http://blog.tkjelectronics.dk/2014/01/ps4-controller-now-supported-by-the-usb-host-library/)

[nintendo switch pro controller bluetooth - Google Search](https://www.google.com.hk/search?q=nintendo+switch+pro+controller+bluetooth)

### Blue Dot

[Blue Dot — bluedot Documentation](https://bluedot.readthedocs.io/en/latest/#)

[Blue Dot - Apps on Google Play](https://play.google.com/store/apps/details?id=com.stuffaboutcode.bluedot)
[Blue Dot Python App — bluedot 1 Documentation](https://bluedot.readthedocs.io/en/latest/bluedotpythonapp.html)

### Bitty Controller

[Bitty Software](http://www.bittysoftware.com/apps/bitty_controller.html)

### Blynk

[Blynk](https://www.blynk.cc/)
[docs.blynk.cc](http://docs.blynk.cc/)

[Blynk server](http://docs.blynk.cc/#blynk-server)

[01Blynk+Arduino 搭配 USB 上網 - 阿玉 maker 研究區](https://sites.google.com/site/wenyumaker/14blynk-ce-shi/01blynk-arduino-usb)

## MagicMirror

[MagicMirror²](https://magicmirror.builders/)
[MichMich/MagicMirror: MagicMirror² is an open source modular smart mirror platform. With a growing list of installable modules, the MagicMirror² allows you to convert your hallway or bathroom mirror into your personal assistant.](https://github.com/MichMich/MagicMirror)
[Make Your Own Smart Mirror for Under \$80 Using Raspberry Pi - Hackster.io](https://www.hackster.io/SrivishnuTech/make-your-own-smart-mirror-for-under-80-using-raspberry-pi-a87460)
[Xonay Labs | Michael Teeuw](http://michaelteeuw.nl/tagged/magicmirror)

[Smart Wall Calendar: 5 Steps](https://www.instructables.com/id/Smart-Wall-Calendar/)

---

# OS

## SBC OS

[How To Install An Operating System To Your Raspberry Pi](https://www.makeuseof.com/tag/install-operating-system-raspberry-pi/)
[The Always-Up-to-Date Guide to Setting Up Your Raspberry Pi](https://lifehacker.com/the-always-up-to-date-guide-to-setting-up-your-raspberr-1781419054)

[The best Raspberry Pi distros in 2018 | TechRadar](https://www.techradar.com/news/best-raspberry-pi-distro)
[10 Operating Systems You Can Run With Raspberry Pi](https://www.makeuseof.com/tag/7-operating-systems-you-can-run-with-raspberry-pi/)
[The Best Operating Systems for Your Raspberry Pi Projects](https://lifehacker.com/the-best-operating-systems-for-your-raspberry-pi-projec-1774669829)
[Top 8 Raspberry Pi Distros - YouTube](https://www.youtube.com/watch?v=_rfZ9FW19hI&t=5s)

[BerryBoot v2.0 - bootloader / universal operating system installer [BerryTerminal]](https://www.berryterminal.com/doku.php/berryboot)

[NOOBS for Raspberry Pi](https://www.raspberrypi.org/downloads/noobs/) New Out Of the Box Software
[Download Raspbian for Raspberry Pi](https://www.raspberrypi.org/downloads/raspbian/)
[Buster - the new version of Raspbian - Raspberry Pi](https://www.raspberrypi.org/blog/buster-the-new-version-of-raspbian/)
[Ubuntu MATE for the Raspberry Pi 2 and Raspberry Pi 3 | Ubuntu MATE](https://ubuntu-mate.org/raspberry-pi/)
[pi-top | pi-topOS](https://www.pi-top.com/products/os#download)
[Armbian – Linux for ARM development boards](https://www.armbian.com/)

[Home Edition Download — Neverware](https://www.neverware.com/freedownload) formerly Flint OS
[FydeOS - 面向未来的云驱动操作系统 | 为中国用户打造的 Chrome OS](https://fydeos.com/) formerly Flint OS, Chinese fork

[LibreELEC – Just enough OS for KODI](https://libreelec.tv/)
[OpenELEC - Wikiwand](https://www.wikiwand.com/en/OpenELEC)

## MCU OS

[FreeRTOS - Market leading RTOS (Real Time Operating System) for embedded systems with Internet of Things extensions](https://www.freertos.org/)
[FreeRTOS - Quick start guide](https://www.freertos.org/FreeRTOS-quick-start-guide.html)

[Welcome to Simba’s documentation! — Simba master documentation](https://simba-os.readthedocs.io/en/latest/index.html)

[Arduino FreeRTOS | feilipu](https://feilipu.me/2015/11/24/arduino_freertos/)
[FreeRTOS - Arduino Libraries](https://www.arduinolibraries.info/libraries/free-rtos)
[feilipu/Arduino_FreeRTOS_Library: A FreeRTOS Library for all Arduino AVR Devices (Uno, Leonardo, Mega, etc)](https://github.com/feilipu/Arduino_FreeRTOS_Library)
[feilipu/avrfreertos: AVR ATmega port of freeRTOS](https://github.com/feilipu/avrfreertos)
[How to use FreeRTOS with Arduino - Real time operating system](https://microcontrollerslab.com/use-freertos-arduino/)
[Using FreeRTOS multi-tasking in Arduino - Arduino Project Hub](https://create.arduino.cc/projecthub/feilipu/using-freertos-multi-tasking-in-arduino-ebc3cc)
[Using FreeRTOS Semaphores in Arduino IDE - Hackster.io](https://www.hackster.io/feilipu/using-freertos-semaphores-in-arduino-ide-b3cd6c)

[Mynewt Documentation — Apache Mynewt latest documentation](https://mynewt.apache.org/latest/index.html)
[Hosting Embedded Rust apps on Apache Mynewt with STM32 Blue Pill](https://medium.com/@ly.lee/hosting-embedded-rust-apps-on-apache-mynewt-with-stm32-blue-pill-c86b119fe5f)

[Using FreeRTOS multi-tasking in Arduino - Hackster.io](https://www.hackster.io/feilipu/using-freertos-multi-tasking-in-arduino-ebc3cc)
[Battery Powered Arduino Applications through FreeRTOS - Hackster.io](https://www.hackster.io/feilipu/battery-powered-arduino-applications-through-freertos-3b7401)

[Amazon FreeRTOS - IoT operating system for microcontrollers - AWS](https://aws.amazon.com/freertos/)
[A peek inside Amazon FreeRTOS | Embedded](https://www.embedded.com/electronics-blogs/say-what-/4460619/A-peek-inside-Amazon-FreeRTOS)
[aws/amazon-freertos: Cloud-native IoT operating system for microcontrollers.](https://github.com/aws/amazon-freertos)

[Home | Mbed](https://www.mbed.com/en/) ARM mbed
[What is Mbed? | Mbed](https://www.mbed.com/en/about-mbed/what-mbed/)

[General RTOS Concepts](http://dev.ti.com/tirex/content/simplelink_academy_cc2640r2sdk_1_14_02_04/modules/rtos_concepts/rtos_concepts.html)

---

# Software Platforms

[Mozilla IoT](https://iot.mozilla.org/)
[Mozilla IoT - WebThings Gateway](https://iot.mozilla.org/gateway/)
[Mozilla IoT - WebThings Framework](https://iot.mozilla.org/framework/)
[Introducing Mozilla WebThings - Mozilla Hacks - the Web developer blog](https://hacks.mozilla.org/2019/04/introducing-mozilla-webthings/)

---

# Hardware Platforms

[System on a chip - Wikiwand](https://www.wikiwand.com/en/System_on_a_chip)
[Microprocessor - Wikiwand](https://www.wikiwand.com/en/Microprocessor)
[Microcontroller - Wikiwand](https://www.wikiwand.com/en/Microcontroller)

There are SBC (single board computer) and MCU (micro controller unit). MCU also acts as co-processor of other system.

[ExplainingComputers.com: Single Board Computers](https://www.explainingcomputers.com/sbc.html)
[Raspberry Pi Alternatives | Linux Journal](https://www.linuxjournal.com/content/raspberry-pi-alternatives)
[Downsides to Raspberry Pi Alternatives | Linux Journal](https://www.linuxjournal.com/content/downsides-raspberry-pi-alternatives)
[Raspberry Pi Alternatives: Top Single Board Computers [2019]](https://itsfoss.com/raspberry-pi-alternatives/)
[Best Raspberry Pi alternatives (April 2019) | ZDNet](https://www.zdnet.com/google-amp/pictures/best-raspberry-pi-alternatives-april-2019/)
[10 Best Raspberry Pi Alternatives Comparison: x86 And ARM SBCs For 2019](https://fossbytes-com.cdn.ampproject.org/v/s/fossbytes.com/best-raspberry-pi-alternatives-x86-arm/amp/)

[The Future of Single Board Computers - YouTube](https://www.youtube.com/watch?v=Kajlrr5ybpU)
[Single Board Computer Benchmarks - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/single-board-computer-benchmarks)
[The Single Board Computer Database](https://www.board-db.org/)
[sbc-bench/Results.md at master · ThomasKaiser/sbc-bench](https://github.com/ThomasKaiser/sbc-bench/blob/master/Results.md)

[Ringing in 2018 with 103 hacker-friendly SBCs](http://linuxgizmos.com/ringing-in-2018-with-103-hacker-friendly-sbcs/)
[2018 reader survey of 116 open-spec Linux/Android SBCs](http://linuxgizmos.com/2018-reader-survey-of-116-open-spec-linux-android-sbcs/)
[Six SBC Benchmark: ODROID XU4, ROCKPro64 & More! - YouTube](https://www.youtube.com/watch?v=k4kMEbeORLo)

[When to Use Micro Processors vs. Micro Controllers - YouTube](https://www.youtube.com/watch?v=Rai8dAkcDLk)
[The Next Generation of High-Powered Microcontrollers « Adafruit Industries – Makers, hackers, artists, designers and engineers!](https://blog.adafruit.com/2018/06/26/the-next-generation-of-high-powered-microcontrollers/)

[You know you have a memory problem when... | Memories of an Arduino | Adafruit Learning System](https://learn.adafruit.com/memories-of-an-arduino?view=all)

[Neil Kolban](https://leanpub.com/u/kolban)

## GPIO Libraries

Many of them uses sysfs interface

> see `kernel.md#gpio`

[Welcome to wiringX documentation!](https://manual.wiringx.org/) framework for multiple platforms, Python 2 binding
[wiringX/wiringX: Modular GPIO interface](https://github.com/wiringX/wiringX)
[radxa/wiringX: Modular GPIO interface](https://github.com/radxa/wiringX) for RK3188

[kplindegaard/smbus2: A drop-in replacement for smbus-cffi/smbus-python in pure Python](https://github.com/kplindegaard/smbus2)
[tomstokes/python-spi: Pure Python SPI interface using spidev](https://github.com/tomstokes/python-spi)

[adafruit/Adafruit_Python_GPIO: Library to provide a cross-platform GPIO interface on the Raspberry Pi and Beaglebone Black using the RPi.GPIO and Adafruit_BBIO libraries.](https://github.com/adafruit/Adafruit_Python_GPIO) with bitbang implementation for I2C and SPI

[radxa/pyRock: Python GPIO module for rockchip platform](https://github.com/radxa/pyRock) RK3188

Firefly RK3288
[zhansb/pyFireflyP](https://github.com/zhansb/pyFireflyP)
[shawn-github/rk3288-gpio-control: rk3288 游戏机，gpio 作为输出和按键](https://github.com/shawn-github/rk3288-gpio-control)
[tjCFeng/GoRK3288: golang RK3288](https://github.com/tjCFeng/GoRK3288)

[TinkerBoard/gpio_lib_python](https://github.com/TinkerBoard/gpio_lib_python) TinkerBoard RK3288

## Firmata protocol

[Arduino - Firmata](https://www.arduino.cc/en/Reference/Firmata)
[firmata/protocol: Documentation of the Firmata protocol.](https://github.com/firmata/protocol)

## Raspberry Pi

> see `raspberry-pi.md`

## AllWinner

[Banana Pi - BPI Single Board Computers Official Website](http://www.banana-pi.org/)

[Orange Pi - Orangepi](http://www.orangepi.org/)

[PINE64 – 64-bit Single Board Computer](https://www.pine64.org/)
[longsleep/build-pine64-image: Pine64 Linux build scripts, tools and instructions](https://github.com/longsleep/build-pine64-image)

## Sony Spresense

[Multicore Arduino, the Easy Way – Hackster Blog](https://blog.hackster.io/multicore-arduino-the-easy-way-ec8b0c73c5ae)
[Spresense boards (main & extension)'s projects](https://www.hackster.io/sony/products/spresense-boards-main-extension)

## Rockchip

> see `rockchip.md`

## Espressif (ESP)

> see `espressif.md`

## Apollo3 Blue

[Apollo Ultra-Low Power MCU](https://ambiqmicro.com/mcu/)
[SparkFun Edge Development Board - Apollo3 Blue - DEV-15170 - SparkFun Electronics](https://www.sparkfun.com/products/15170) An MCU that runs TensorFlow, with built in microphones, a 3-axis accelerometer and CSI for camera
[SparkFun Edge Hookup Guide - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/sparkfun-edge-hookup-guide/all)
[Introducing the SparkFun Edge - Hackster Blog](https://blog.hackster.io/introducing-the-sparkfun-edge-34c9eb80a000)

## STM

STM32F103
ARM Cortex-M3 @72MHz 3.3V
some pins are 5V tolerant
2 12-bit ADC
16-bit PWM, frequency up to 32MHz
15 interrupts
[STM32F103C8 - Mainstream Performance line, ARM Cortex-M3 MCU with 64 Kbytes Flash, 72 MHz CPU, motor control, USB and CAN - STMicroelectronics](https://www.st.com/en/microcontrollers/stm32f103c8.html)

STM32F030
ARM Cortex-M0 @45MHz 3.3V
some pins are 5V tolerant
1 12-bit ADC
2 I2C
entry-level model
[STM32F030C8 - Mainstream ARM Cortex-M0 Value line MCU with 64 Kbytes Flash, 48 MHz CPU - STMicroelectronics](https://www.st.com/en/microcontrollers/stm32f030c8.html)
[Datasheet Review of an STM32 Microcontroller (Blog + Video) | PREDICTABLE DESIGNS](https://predictabledesigns.com/stm32-microcontroller-datasheet-review/)

[Blue Pill - STM32duino wiki](http://wiki.stm32duino.com/index.php?title=Blue_Pill)
[LeafLabs Documentation Index — Maple Documentation](http://docs.leaflabs.com/static.leaflabs.com/pub/leaflabs/maple-docs/latest/index-2.html)

[Arduino for STM32 - Index page](http://www.stm32duino.com/)
[Boards Manager package - STM32duino wiki](http://wiki.stm32duino.com/index.php?title=Boards_Manager_package)
[Libraries · rogerclarkmelbourne/Arduino_STM32 Wiki](https://github.com/rogerclarkmelbourne/Arduino_STM32/wiki/Libraries)

[Let's code with STM32 NUCLEO | Open Electronics](https://www.open-electronics.org/lets-code-with-stm32-nucleo/)
[Easy & Powerful Arduino Alternative? STM32 Beginner's Guide - YouTube](https://www.youtube.com/watch?v=EaZuKRSvwdo)

## nRF52

[nRF52832 / Bluetooth Low Energy / Products / Home - Ultra Low Power Wireless Solutions from NORDIC SEMICONDUCTOR](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF52832)
[nRF52832 Breakout Board Hookup Guide - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/nrf52832-breakout-board-hookup-guide)
[Starting up with the Nordic NRF52 BLE chip | Primal Cortex's Weblog](https://primalcortex.wordpress.com/2017/11/06/starting-up-with-the-nordic-nrf52-ble-chip/)

[sandeepmistry/arduino-nRF5: Arduino Core for Nordic Semiconductor nRF5 based boards](https://github.com/sandeepmistry/arduino-nRF5)

## Arduino

> see `arduino.md`

### Beaglebone

[BeagleBoard.org - community supported open hardware computers for making](https://beagleboard.org/)

The CPU used includes two Programmable Realtime Units (PRUs), which have access to all of the IO that a Linux application has, but is accessible without the interference of the non-realtime Linux OS.

[adafruit/adafruit-beaglebone-io-python: Adafruit's BeagleBone IO Python Library](https://github.com/adafruit/adafruit-beaglebone-io-python/)

## Tessel

[Tessel 2](https://tessel.io/) development platform with Node ecosystem
[Tessel 2 - Tessel - Seeed Studio](https://www.seeedstudio.com/depot/Tessel-2-p-2622.html?ref=tessel.io)

## Micro:bit

> see `micro-bit.md`

## Webduino

[Webduino Bit - 最 HOT 的物聯網開發板！](https://bit.webduino.io/site/zh_tw/index.html)
micro:bit clone using ESP32

## Blocks with SoC

### EV3/NXT

[Lego Mindstorms NXT - Wikiwand](https://www.wikiwand.com/en/Lego_Mindstorms_NXT)
[Nine alternative programming languages for LEGO MINDSTORMS – LEGO Engineering](http://www.legoengineering.com/alternative-programming-languages/)

[LEGO Mindstorms | Mindstorms Robots](http://www.mindstormsrobots.com/lego-mindstorms/)
[Home - Mindstorms LEGO.com](https://www.lego.com/en-us/mindstorms)
[LEGO EV3 & NXT hacks and robots](http://www.philohome.com/nxt.htm)
[The NXT STEP is EV3 - LEGO® MINDSTORMS® Blog](http://www.thenxtstep.com/)

[LEGO Mindstorms NXT / EV3 Cable & Crimping Tool DIY - YouTube](https://www.youtube.com/watch?v=p1rhdOg9sVc) file your crimping tool
[Lego Mindstorms EV3 Review - A lack of enthusiasm - YouTube](https://www.youtube.com/watch?v=wLupj65qJHg) RCX (1998) -> NXT (2006) -> RV3 (2013)

[mindboards/ev3sources: LEGO MINDSTORMS EV3 source code](https://github.com/mindboards/ev3sources)
[NXT/LEGO-MINDSTORMS-MINDdroid: LEGO MINDSTORMS Android Apps](https://github.com/NXT/LEGO-MINDSTORMS-MINDdroid)

[TechnicBRICKs: WeDo 2.0 - The future of PF](http://www.technicbricks.com/2016/01/wedo-20-future-of-pf.html)
[TechnicBRICKs: WeDo 2.0 - the new parts](http://www.technicbricks.com/2016/01/wedo-20-new-parts.html)

[Top 5 LEGO Compatible Electronics - YouTube](https://www.youtube.com/watch?v=lLzTM2w1SM4)
[适用乐高 EV3/NXT 主控马达传感器连接线 乐高 lego 连接线 数据线-淘宝网](https://item.taobao.com/item.htm?id=554185937877)

### SoC

[robo8080/ESP32_LegoMotor_RCWC: ESP32 + TB6612 モータードライバー + RCWController で、LEGO Power Functions Motor と Servo Motor を制御します。](https://github.com/robo8080/ESP32_LegoMotor_RCWC) ESP32 + TB6612, !important

[FATCATLAB](http://fatcatlab.com/product/evb/) Beaglebone Black + EVB cape to replace EV3

[ev3dev Home](https://www.ev3dev.org/)
[gpio - How can I control Lego motors? - Raspberry Pi Stack Exchange](https://raspberrypi.stackexchange.com/questions/682/how-can-i-control-lego-motors)
[Motor Lego NXT nxt output input wiring tacho signal](http://trivox.tripod.com/lego-nxt-motor-input-output.html)

[Lego Technic Servo Motor - 9V PWM - Arduino Stack Exchange](https://arduino.stackexchange.com/questions/16904/lego-technic-servo-motor-9v-pwm)
[piece information - At what voltage do the c1 and c2 lines run at when controlling a lego servo motor? - Bricks](https://bricks.stackexchange.com/questions/6620/at-what-voltage-do-the-c1-and-c2-lines-run-at-when-controlling-a-lego-servo-moto)

**Arduino**

[Arduino Playground - PwmFrequency](http://playground.arduino.cc/Code/PwmFrequency)

```
The base frequency for pins 3, 9, 10, and 11 is 31250 Hz.
The base frequency for pins 5 and 6 is 62500 Hz.
Divisors:
The divisors available on pins 5, 6, 9 and 10 are: 1, 8, 64, 256, and 1024.
The divisors available on pins 3 and 11 are: 1, 8, 32, 64, 128, 256, and 1024.
```

[Take Control Over Lego Power Functions - Arduino Project Hub](https://create.arduino.cc/projecthub/Notthemarsian/take-control-over-lego-power-functions-ee0bfa)
[Notthemarsian/Lego-car-Arduino: arduino Lego car model bluetooth controlled with android app developed with MIT app inventor](https://github.com/Notthemarsian/Lego-car-Arduino)

[Lego Hacking | Scuttlebots](https://scuttlebots.com/lego-hacking/)

[BTBox – LEGO Power Functions Bluetooth Controller | PlastiBots](http://www.plastibots.com/index.php/2017/09/01/btbox-lego-power-functions-bluetooth-controller/)

[Adafruit customer service forums • View topic - How to use Adafruit Motor Shield V2 with Lego Servo Motor?](https://forums.adafruit.com/viewtopic.php?f=31&t=62325)

[IoT Dune Buggy - Control it from Anywhere! - Hackster.io](https://www.hackster.io/Satyavrat/iot-dune-buggy-control-it-from-anywhere-84b921)

[【图片】「乐高(pin)遇上 arduino」之荒神小钢炮 moc【国产积木吧】\_百度贴吧](https://tieba.baidu.com/p/4981594749)
[Front Page - Microduino](https://microduinoinc.com/) mCookies are modules with magnets
[d4rks70rm/ArduinoLegoTrain: Control a Lego Train with Arduino](https://github.com/d4rks70rm/ArduinoLegoTrain)

[Arduino Controlling LEGO Power Functions Motor Part 1: Wired Control - YouTube](https://www.youtube.com/watch?v=ArEt9RWPbhE) !important, PWM frequencies
[Arduino Controlling LEGO Power Functions Motor Part 2: IR Remote Control - YouTube](https://www.youtube.com/watch?v=D7kQCJIeM6c)

**Raspberry Pi**

[BrickPi - Dexter Industries](https://www.dexterindustries.com/brickpi/)
[BrickPi3 Tutorials and Documentation: Get Started with the BrickPi3 and the Raspberry Pi](https://www.dexterindustries.com/brickpi3-tutorials-documentation/)
[DexterInd/BrickPi: The BrickPi Project Combining the Raspberry Pi and LEGO MINDSTORMS](https://github.com/DexterInd/BrickPi)
[BrickPi - YouTube](https://www.youtube.com/playlist?list=PLGXEJ4Ye1qCOIk6PdUMxePiYP6Y34hOux)
[LEGO MINDSTORMS Motors with Raspberry Pi (BrickPi 0.1) - Dexter Industries](https://www.dexterindustries.com/howto/lego-mindstorms-motors-with-raspberry-pi-brickpi-0-1/)
[Controlling a LEGO Mindstorms EV3 Robot with a Raspberry Pi GPIO Pin](http://www.mindstormsrobots.com/lego-mindstorms/controlling-mindstorms-ev3-with-a-raspberry-pi/)

[LEGO Power Functions 8293 Motor Set - Raspberry Pi Forums](https://www.raspberrypi.org/forums/viewtopic.php?t=31421)
[Paul's Geek Dad Blog: Raspberry Pi Powered Lego Car](http://pdwhomeautomation.blogspot.com/2012/11/raspberry-pi-powered-lego-car.html)
[Paul's Geek Dad Blog: Raspberry Pi Powered Lego Car 2.0](http://pdwhomeautomation.blogspot.com/2013/11/raspberry-pi-powered-lego-car-20.html)

**SoC + Infrared**

[jurriaan/Arduino-PowerFunctions: Lego Power Functions Infrared Control for Arduino](https://github.com/jurriaan/Arduino-PowerFunctions)
[iConor/lego-pf-arduino: Control LEGO Power Functions with an Arduino and an IR LED.](https://github.com/iConor/lego-pf-arduino)
[iConor/lego-lirc: Control LEGO Power Functions with a Raspberry Pi and an IR LED, using LIRC (Linux Infrared Remote Control).](https://github.com/iConor/lego-lirc)
[quantenProjects/LegoPowerFunctionsIR: A Python libeary and C programm to control Lego Powerfunctions via IR on a Raspberry Pi](https://github.com/quantenProjects/LegoPowerFunctionsIR)
[Zchander/RPi-PowerFunctions: A project to send commands over IR to a LEGO PowerFunctions receiver using an Raspberry Pi, I2C and an ATtiny2313](https://github.com/Zchander/RPi-PowerFunctions)
[dspinellis/lego-power-scratch: Control Lego power functions from Scratch](https://github.com/dspinellis/lego-power-scratch)

[Replace Lego’s $190 Intelligent Brick with MIT’s Scratch and a $40 Raspberry Pi - IEEE Spectrum](https://spectrum.ieee.org/geek-life/hands-on/replace-legos-190-intelligent-brick-with-mits-scratch-and-a-40-raspberry-pi)
[Controlling LEGO Power Function trains and models with Raspberry Pi | Freetronics](https://www.freetronics.com.au/blogs/news/17338609-controlling-lego-power-function-trains-and-models-with-raspberry-pi)
[Wii Nunchuk Analog Stick Controlling LEGO Power Functions Tank by Arduino - YouTube](https://www.youtube.com/watch?v=v7NJNDcBFE4)
[Raspberry Pi Lego Robot - Computerphile - YouTube](https://www.youtube.com/watch?v=nZHOclcOB2k)

### Seeed Studio

[Seeed Wiki](http://wiki.seeedstudio.com/)
Seeed Studio produces custom make component boards with "Grove Connectors" (actually PH 2.0 4pins)

[Grove System](http://wiki.seeedstudio.com/Grove_System/)
[Grove 专区-武汉零度智控科技有限公司-淘宝网](https://shop289628642.taobao.com/category-1365889245.htm)
[Grove 传感器外壳 Stem 教育 兼容乐高积木 红 黄 蓝 绿 四色可选-淘宝网](https://item.taobao.com/item.htm?id=566415709625) t also produces LEGO compatible racks for Grove modules

### DFRobot

Gravity system (actually PH 2.0 3pins)

[Oxford 传感器-小氪机器人官方店-淘宝网](https://shop137769920.taobao.com/category-1324924875.htm)

### UBTECH

Pieces are little bit smaller than LEGO pieces, so _not compatible_

[UBTECH Robotics - Humanoid intelligent & programmed robots for family](https://ubtrobot.com/)
[优必选官方旗舰店-天猫 Tmall.com](https://ubtech.tmall.com/)
[优必选得烨专卖店-天猫 Tmall.com](https://ubtechdeye.tmall.com/shop/view_shop.htm)
[【优必选变形工程车（卡卡&卡力）】优必选（UBTECH）智能机器人 stem 教育编程早教益智儿童积木遥控拼装玩具礼物变形工程车 卡卡卡力【行情 报价 价格 评测】-京东](https://item.jd.com/7398404.html)

### VEX IQ

[艾博士机器人创客家园-淘宝网](https://shop443346547.taobao.com/shop/view_shop.htm)
[淼淼积木-淘宝网](https://mmjm.taobao.com/)
[东北智能生活数码港-淘宝网](https://shop125955852.taobao.com/shop/view_shop.htm)

[VEX-皇岗 360-淘宝网](https://szhg360.taobao.com/search.htm?orderType=&viewType=grid&keyword=VEX&lowPrice=&highPrice=)

[VEX IQ Super Kit - Do you want to build a robot? - YouTube](https://www.youtube.com/watch?v=sohekAXc8UY)

### abilix

[abilix 能力风暴旗舰店-天猫 Tmall.com](https://abilix.tmall.com/shop/view_shop.htm)

### CocoRobo

[COCOROBO](https://cocorobo.hk/online/)
[COCOROBO 課程中心](https://cocorobo.hk/online/curriculumKit/0)

### 酷比克機器人 Cubic

[ScratchPi](https://www.bettertree.com.tw/)

- Micro USB connectors
- LEGO compatible

[酷比克三代電子積木基礎版 :: ScratchPi](https://www.bettertree.com.tw/l/%e9%85%b7%e6%af%94%e5%85%8b%e4%b8%89%e4%bb%a3%e9%9b%bb%e5%ad%90%e7%a9%8d%e6%9c%a8%e5%9f%ba%e7%a4%8e%e7%89%88/)
[酷比克三代電子積木高級版 :: ScratchPi](https://www.bettertree.com.tw/l/%e9%85%b7%e6%af%94%e5%85%8b%e4%b8%89%e4%bb%a3%e9%9b%bb%e5%ad%90%e7%a9%8d%e6%9c%a8%e9%ab%98%e7%b4%9a%e7%89%88/)

### Makeblock

> see `makeblock.md`
> see `learn-to-code-kids.md#mblock`

### Witcat

[首页-机智猫少儿创客机器人-淘宝网](https://shop150832632.taobao.com/index.htm)

### Mitu

[米兔积木机器人 - 小米商城](https://www.mi.com/toyblock/)
[米兔积木机器人 - 小米社区官方论坛](http://bbs.xiaomi.cn/f-479)
[米兔积木机器人非官方编程手册 - 小米社区官方论坛](http://bbs.xiaomi.cn/t-13524032)

[积木世界](http://www.mitubuilder.com/)
[米兔开发板开发板米兔米兔积木机器人传感器开发板 开源 DIY 设计-淘宝网](https://item.taobao.com/item.htm?id=557218028022) interface with the Mitu core
[自己动手扩展红外避障传感器-米兔积木机器人传感器开发板-积木世界](http://www.mitubuilder.com/?thread-527.htm)

[深度解密米兔积木机器人八大黑科技 - 知乎](https://zhuanlan.zhihu.com/p/29548231)
[米兔积木机器人主控盒拆解丨智能设备丨数字尾巴](http://www.dgtle.com/thread-782327-1-1.html)

[499 元小米積木機械人與樂高機械人有何區別？ - 每日頭條](https://kknews.cc/zh-hk/tech/2aqk5ke.html)
[如何评价小米新出的「米兔积木机器人」？ - 知乎](https://www.zhihu.com/question/52239880/answer/131735620) Hardware review

[米兔积木机器人履带机甲视频大测评 - YouTube](https://www.youtube.com/watch?v=POHChVGh4LQ)
[视频 | 益智烧脑，趣比乐高：米兔积木机器人履带机甲上手体验 - 知乎](https://zhuanlan.zhihu.com/p/28093955)
[米兔积木机器人简单自平衡测试教程 - 小米社区官方论坛](http://bbs.xiaomi.cn/t-13253395)

## Projects

[Maker Pro | Electronics Projects, From Concept to Creation](https://maker.pro/)
[Hackster.io - The community dedicated to learning hardware.](https://www.hackster.io/feed)
[Arduino – Hackster Blog](https://blog.hackster.io/tagged/arduino)
[Home | Free Platform for Coding, Making and Inventing | Make | Tech Will Save Us](https://make.techwillsaveus.com/)
[Open source electronic projects](https://www.open-electronics.org/)
[Hackaday | Fresh hacks every day](https://hackaday.com/)

[TUTORIALS – Brainy-Bits](https://www.brainy-bits.com/tutorials/)
[200+ Free Electronics Projects and Tutorials - Maker Advisor](https://makeradvisor.com/200-free-electronics-projects/)

[机器人学习资料教程专区 - DF 创客社区 - DF 创客社区 - 分享创造的喜悦 -](http://www.dfrobot.com.cn/community/portal.php?mod=topic&topicid=3)

[Suspense Courtesy of Arduino, Mess of Wires | Hackaday](https://hackaday.com/2018/11/06/suspense-courtesy-of-arduino-mess-of-wires/)
[Defusable alarm clock – wastes wire but fun for the kids | Hackaday](https://hackaday.com/2011/09/07/defusable-alarm-clock-wastes-wire-but-fun-for-the-kids/)

[MickMake - YouTube](https://www.youtube.com/channel/UC7GMT3ohvYEAJFDenzj9EMQ)
[8 Bits and a Byte - YouTube](https://www.youtube.com/channel/UCsxNFv5K7ZdeTBDwh6D-ukQ?app=desktop)
