---
title: Espressif
  - maker
tags:
  - iot
  - espressif
  - esp32
  - esp8266
toc: true
date: 2018-10-20 09:22:17
---

# Espressif (ESP)

[ESP32 vs ESP8266 - Pros and Cons - Maker Advisor](https://makeradvisor.com/esp32-vs-esp8266/)

[Development Board | Espressif Systems](https://www.espressif.com/en/products/hardware/development-boards)
[开发板 | 乐鑫](https://www.espressif.com/zh-hans/products/hardware/development-boards)
[Documents | Espressif Systems](https://www.espressif.com/en/support/download/documents)

Board bringup
[Installing ESP32 in Arduino IDE Mac OS X and Linux | Random Nerd Tutorials](https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-mac-and-linux-instructions/)
[How to Install the ESP8266 Board in Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/how-to-install-esp8266-board-arduino-ide/)
[ESP32 Dual Core with Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-dual-core-arduino-ide/)

1. Go to _File -> Preference_ of Arduino IDE, enter these to _Additional Board Manager URLs_  
   `https://dl.espressif.com/dl/package_esp32_index.json, http://arduino.esp8266.com/stable/package_esp8266com_index.json`
2. Go to _Tools -> Board Manager_, install esp32 and esp8266

[ESP-SDK | Espressif Systems](https://www.espressif.com/en/products/software/esp-sdk/overview)
[espressif/esp-idf: Espressif IoT Development Framework. Official development framework for ESP32.](https://github.com/espressif/esp-idf)
[espressif/esp-iot-soluion: Espressif IoT Library. IoT Device Drivers, Documentations And Solutions.](https://github.com/espressif/esp-iot-solution)
[espressif/esptool: ESP8266 and ESP32 serial bootloader utility](https://github.com/espressif/esptool)
[espressif/ESP8266_NONOS_SDK: ESP8266 nonOS SDK](https://github.com/espressif/ESP8266_NONOS_SDK)
[espressif/ESP8266_RTOS_SDK: Latest ESP8266 SDK based on FreeRTOS, esp-idf style.](https://github.com/espressif/ESP8266_RTOS_SDK)
[plerup/makeEspArduino: A makefile for ESP8266 and ESP32 Arduino projects](https://github.com/plerup/makeEspArduino)
[Backup & Restore an ESP8266](https://steve.fi/Hardware/backup-and-restore/)
[A Beta Release for ESP Bluetooth Mesh – Hackster Blog](https://blog.hackster.io/a-beta-release-for-esp-bluetooth-mesh-6eb8998334e6)

[MicroPython Programming Basics with ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/micropython-programming-basics-esp32-esp8266/)
[Flash/Upload MicroPython Firmware to ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/flash-upload-micropython-firmware-esp32-esp8266/)
[ESP32/ESP8266 Analog Readings with MicroPython | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-esp8266-analog-readings-micropython/)

[ESPlorer – esp8266](https://esp8266.ru/esplorer/)
[ESPlorer — Next Generation IDE for ESP8266 developers - Everything ESP8266](https://www.esp8266.com/viewtopic.php?f=22&t=882)
Includes Lua and MicroPython IDE

[Coding is easy – Start now!](http://easycoding.tn/) Block programming for ESP board
[ESP32](http://easycoding.tn/esp32/demos/code/)
[ESP8266](http://www.easycoding.tn/tuniot/demos/code/)

## Vendors

Most vendor will market both ESP8266 and ESP32 boards

[ESP32-DevKitC | Espressif Systems](https://www.espressif.com/en/products/hardware/esp32-devkitc/overview)
[An ESP32-Based Arduino Lookalike – Hackster Blog](https://blog.hackster.io/an-esp32-based-arduino-lookalike-b5523c6f54b0)

[NodeMcu -- An open-source firmware based on ESP8266 wifi-soc.](http://www.nodemcu.com/index_en.html)
[Overview - NodeMCU Documentation](https://nodemcu.readthedocs.io/en/master/)
[nodemcu/nodemcu-devkit-v1.0](https://github.com/nodemcu/nodemcu-devkit-v1.0)
[nodemcu/nodemcu-firmware: lua based interactive firmware for mcu like esp8266](https://github.com/nodemcu/nodemcu-firmware)
[nodemcu/nodemcu-flasher: A firmware Flash tool for nodemcu](https://github.com/nodemcu/nodemcu-flasher)
[Flashing NodeMCU Firmware on the ESP8266 using Windows | Random Nerd Tutorials](https://randomnerdtutorials.com/flashing-nodemcu-firmware-on-the-esp8266-using-windows/)

[Home - WEMOS.CC](https://www.wemos.cc/) LOLIN

[Doctors of Intelligence & Technology](http://en.doit.am/)
[Home · SmartArduino/SZDOITWiKi Wiki](https://github.com/SmartArduino/SZDOITWiKi/wiki)
[ESP8266 ESP32 · SmartArduino/SZDOITWiKi Wiki](https://github.com/SmartArduino/SZDOITWiKi/wiki/ESP8266---ESP32)
[Nicholas3388/LuaNode: Esp32/esp8266 lua sdk](https://github.com/Nicholas3388/LuaNode) DoIT

## ESP32

[ESP32 Overview | Espressif Systems](https://www.espressif.com/en/products/hardware/esp32/overview)
[ESP32 - Wikiwand](https://www.wikiwand.com/en/ESP32)
[ESP32 WROOM Overview | Espressif Systems](https://www.espressif.com/en/products/hardware/esp-wroom-32/overview)
[ESP32 Overview | Espressif Systems](https://www.espressif.com/en/products/hardware/esp32/overview)
[ESP32-DevKitC V4 Getting Started Guide — ESP-IDF Programming Guide v3.2-dev-1385-g129d327 documentation](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/get-started-devkitc.html)
[espressif/arduino-esp32: Arduino core for the ESP32](https://github.com/espressif/arduino-esp32)

[ESP-IDF Programming Guide — ESP-IDF Programming Guide v3.2-dev-1385-g129d327 documentation](https://docs.espressif.com/projects/esp-idf/en/latest/index.html)

160/240Mhz
Bluetooth 4.2, BLE, 802.11bgn
16 LED PWN, 18 ADC, 2 12C, 4 SPI (shares pin with GPIO)
D0WDQ6 is the standard package, D0WD is smaller
10.8x25.5mm, requires CP2102 USB to Serial
28.3x51.4mm, embedded mini-usb

> To use the Bluetooth or BLE functionality of the ESP32, you will need to use the Espressif IDF not the Arduino IDE. ?

[ESP32 Development Boards Review and Comparison - Maker Advisor](https://makeradvisor.com/esp32-development-boards-review-comparison/)
[Getting Started with the ESP32 Development Board | Random Nerd Tutorials](https://randomnerdtutorials.com/getting-started-with-esp32/) !important

[#147 Introduction into ESP32 with first tests: PWM, Servo, Web, Touch Sensors (Tutorial) - YouTube](https://www.youtube.com/watch?v=SBG7ccW5gpA)
[#179 Was it worth waiting for Bluetooth? How Much Current Needs the ESP32 Bluetooth in BLE? - YouTube](https://www.youtube.com/watch?v=nyWMaAF4dRQ)

[#159 Big ESP32 Boards Review and Test - YouTube](https://www.youtube.com/watch?v=3O_vrKAmshA)
[ESP32 Boards Comparison - Google Sheets](https://docs.google.com/spreadsheets/d/1Mu-bNwpnkiNUiM7f2dx8-gPnIAFMibsC2hMlWhIHbPQ/edit#gid=0)

Board bringup
[ESP32 Thing Hookup Guide - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/esp32-thing-hookup-guide)
[ESP32 — Getting Started the Easy Way!](https://www.electroschematics.com/13312/esp32-easy-play/) DOIT board
[ESP32 Troubleshooting Guide | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-troubleshooting-guide/)
[How to power up ESP32-DevKitC without USB port? - ESP32 Forum](http://bbs.esp32.com/viewtopic.php?t=3416) 5V input via AMS1117-3.3 LDO

https://pan.baidu.com/s/1ycfadOAvoBZxL1R_L1MY-A 密码 bwle

[esp32, esp32 tutorial,ESP32 Arduino Tutorial Overview](https://www.dfrobot.com/blog-964.html)
[ESP32 - YouTube](https://www.youtube.com/playlist?list=PL3XBzmAj53RnZPeWe799F-uoXERBldhn9)

[ESP32 Hardware Reference — ESP-IDF Programming Guide documentation](https://esp-idf.readthedocs.io/en/latest/hw-reference/)
[The Internet of Things with ESP32](http://esp32.net/)
[espressif/arduino-esp32: Arduino core for the ESP32](https://github.com/espressif/arduino-esp32)
[nkolban/ESP32_BLE_Arduino: The library source for the ESP32 BLE support for Arduino.](https://github.com/nkolban/ESP32_BLE_Arduino)

[ESP32 Built-In Hall Effect Sensor | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-hall-effect-sensor/)
[ESP32 Flash Memory - Save Permanent Data | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-flash-memory/)
[problem with MCPWM below 15 Hz frequency · Issue #2255 · espressif/esp-idf](https://github.com/espressif/esp-idf/issues/2255)

[#147 Introduction into ESP32 with first tests: PWM, Servo, Web, Touch Sensors (Tutorial) - YouTube](https://www.youtube.com/watch?v=SBG7ccW5gpA)
[ESP32 PWM with Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-pwm-arduino-ide/)

### ESP32-CAM

[ESP32-CAM - Maker Advisor](https://makeradvisor.com/tools/esp32-cam/)

[ESP32-CAM Troubleshooting Guide: Most Common Problems Fixed | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-cam-troubleshooting-guide/)
[ESP32-CAM Video Streaming and Face Recognition with Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-cam-video-streaming-face-recognition-arduino-ide/)
[ESP32-CAM Video Streaming Web Server (works with Home Assistant) | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-cam-video-streaming-web-server-camera-home-assistant/)
[ESP32-CAM Take Photo and Save to MicroSD Card | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-cam-take-photo-save-microsd-card/)

[Using a Camera with the ESP32 – Hackster Blog](https://blog.hackster.io/using-a-camera-with-the-esp32-9d6994b34a2b)
[ESP32+OV7670 — WebSocket Video Camera – Mudassar Tamboli – Medium](https://medium.com/@mudassar.tamboli/esp32-ov7670-websocket-video-camera-26c35aedcc64)

### `esp-who`

[espressif/esp-who: Face detection and recognition framework](https://github.com/espressif/esp-who)
[Face Detection and Recognition on the ESP32 – Hackster Blog](https://blog.hackster.io/face-detection-and-recognition-on-the-esp32-3b4b9a35c765)

### Pinout

[ESP32 Pinout Reference: Which GPIO pins should you use? | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-pinout-reference-gpios/) !important
LuaNode/Doit ESP-WROOM32 30pins

## ESP32-S2

[New Part Day: Espressif Announces ESP32-S2 With USB | Hackaday](https://hackaday.com/2019/05/21/new-part-day-espressif-announces-esp32-s2-with-usb/) no Bluetooth, USB OTG
[The ESP32-S2, Is It Almost Ready? – Hackster Blog](https://blog.hackster.io/the-esp32-s2-is-it-almost-ready-aa62f2d6b916)

## ESP8266

[ESP-WROOM-02 Overview | Espressif Systems](https://www.espressif.com/en/products/hardware/esp-wroom-02/overview)
[ESP8266_RTOS_SDK/docs/en at master · espressif/ESP8266_RTOS_SDK](https://github.com/espressif/ESP8266_RTOS_SDK/tree/master/docs/en)

[Welcome to ESP8266 Arduino Core’s documentation! — ESP8266 Arduino Core documentation](https://arduino-esp8266.readthedocs.io/en/latest/)
[Boards — ESP8266 Arduino Core documentation](https://arduino-esp8266.readthedocs.io/en/latest/boards.html)
[Best ESP8266 Wi-Fi Development Board - Buying Guide 2018](https://makeradvisor.com/best-esp8266-wi-fi-development-board/)
[Comparison of ESP8266 NodeMCU development boards • my2cents](https://frightanic.com/iot/comparison-of-esp8266-nodemcu-development-boards/)

[esp8266/Arduino: ESP8266 core for Arduino](https://github.com/esp8266/Arduino)
[Welcome to ESP8266 Arduino Core’s documentation!](https://arduino-esp8266.readthedocs.io/en/latest/)

[ESP8266 Thing Hookup Guide - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/esp8266-thing-hookup-guide/all)
[Getting Started with ESP8266 WiFi Transceiver (Review) | Random Nerd Tutorials](https://randomnerdtutorials.com/getting-started-with-esp8266-wifi-transceiver-review/) !important
[ESP8266 Pinout Reference: Which GPIO pins should you use? | Random Nerd Tutorials](https://randomnerdtutorials.com/esp8266-pinout-reference-gpios/)
[Getting Started with the ESP8266 – Alasdair Allan – Medium](https://medium.com/@aallan/getting-started-with-the-esp8266-270e30feb4d1)
[ESP8266 - Beginner Tutorial + Project - Hackster.io](https://www.hackster.io/Niv_the_anonymous/esp8266-beginner-tutorial-project-6414c8)

[spacehuhn/esp8266_deauther: Scan for WiFi devices, block selected connections, create dozens of networks and confuse WiFi scanners!](https://github.com/spacehuhn/esp8266_deauther)

## Low Power

[ESP8266 Deep Sleep with Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/esp8266-deep-sleep-with-arduino-ide/)
[MicroPython: ESP8266 Deep Sleep and Wake Up Sources | Random Nerd Tutorials](https://randomnerdtutorials.com/micropython-esp8266-deep-sleep-wake-up-sources/)

- Connect RST (RESET) pin to GPIO 16 (WAKE)
- RST is high when ESP8266 is on, and RTC interrupt can pull GPIO 16 to low
- so ESP8266 will reset based on timer and deep sleep again
- use `deepSleep(0)` to let other input to pull RST switch to low
  [Low-energy ESP8266-based Board Sleeps Like a Log Until Triggered | Hackaday](https://hackaday.com/2018/11/13/low-energy-esp8266-based-board-sleeps-like-a-log-until-triggered/)
  [Low Power Weather Station Datalogger using ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/low-power-weather-station-datalogger-using-esp8266-bme280-micropython/)

[ESP32 Deep Sleep with Arduino IDE and Wake Up Sources | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-deep-sleep-arduino-ide-wake-up-sources/)
[MicroPython: ESP32 Deep Sleep and Wake Up Sources | Random Nerd Tutorials](https://randomnerdtutorials.com/micropython-esp32-deep-sleep-wake-up-sources/)
[ESP32 Timer Wake Up from Deep Sleep | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-timer-wake-up-deep-sleep/)
[ESP32 Touch Wake Up from Deep Sleep | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-touch-wake-up-deep-sleep/)
[ESP32 External Wake Up from Deep Sleep | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-external-wake-up-deep-sleep/)

## SPIFFS

ESPlorer?

[pellepl/spiffs: Wear-leveled SPI flash file system for embedded devices](https://github.com/pellepl/spiffs)
[me-no-dev/arduino-esp32fs-plugin: Arduino plugin for uploading files to ESP32 file system](https://github.com/me-no-dev/arduino-esp32fs-plugin)

[Install ESP32 Filesystem Uploader on Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/install-esp32-filesystem-uploader-arduino-ide/)
[ESP32 Web Server using SPIFFS (SPI Flash File System) | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-web-server-spiffs-spi-flash-file-system/)

## MicroPython

[Step by Step Install - MicroPython Forum](https://forum.micropython.org/viewtopic.php?f=18&t=5085)

[Getting Started with Thonny MicroPython (Python) IDE for ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/getting-started-thonny-micropython-python-ide-esp32-esp8266/)
[Getting Started with MicroPython on ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/getting-started-micropython-esp32-esp8266/)
[Flash/Upload MicroPython Firmware to ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/flash-upload-micropython-firmware-esp32-esp8266/) with uPyCraft
[Flashing MicroPython Firmware with esptool.py on ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/flashing-micropython-firmware-esptool-py-esp32-esp8266/) with esptool

[Install uPyCraft IDE - Linux Ubuntu | Random Nerd Tutorials](https://randomnerdtutorials.com/install-upycraft-ide-linux-ubuntu-instructions/)
[MicroPython with ESP32 and ESP8266: Interacting with GPIOs | Random Nerd Tutorials](https://randomnerdtutorials.com/micropython-gpios-esp32-esp8266/)
[MicroPython: Interrupts with ESP32 and ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/micropython-interrupts-esp32-esp8266/)

## Projects

[ESP32 Access Point (AP) for Web Server | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-access-point-ap-web-server/)
[ESP32/ESP8266 MicroPython Web Server | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-esp8266-micropython-web-server/)
[ESP32 Static/Fixed IP Address | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-static-fixed-ip-address-arduino-ide/)
[Control ESP32 with Command Line Interface Over the Internet - Hackster.io](https://www.hackster.io/donowak/control-esp32-with-command-line-interface-over-the-internet-fa9634)

[30+ ESP8266 Projects and Tutorials | Random Nerd Tutorials](https://randomnerdtutorials.com/projects-esp8266/)
[20+ ESP32 Projects and Tutorials | Random Nerd Tutorials](https://randomnerdtutorials.com/projects-esp32/)
[ESP32 Bluetooth Low Energy (BLE) on Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-bluetooth-low-energy-ble-arduino-ide/)
[ESP32 with PIR Motion Sensor using Interrupts and Timers | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-pir-motion-sensor-interrupts-timers/)
[Build an ESP8266 Web Server - Code and Schematics | Random Nerd Tutorials](https://randomnerdtutorials.com/esp8266-web-server/) + NodeMCU's Lua
[ESP32 Web Server with BME280 – Mini Weather Station | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-web-server-with-bme280-mini-weather-station/)
[DIY Weather Station & WiFi Sensor Station || ESP8266, Nextion LCD - YouTube](https://www.youtube.com/watch?v=daS2CE-zFNo)
[MicroPython: ESP32/ESP8266 with DHT11/DHT22 Web Server | Random Nerd Tutorials](https://randomnerdtutorials.com/micropython-esp32-esp8266-dht11-dht22-web-server/)
[ESP32/ESP8266 RGB LED Strip with Color Picker Web Server | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-esp8266-rgb-led-strip-web-server/)
[ESP32 MQTT Publish Subscribe with Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-mqtt-publish-subscribe-arduino-ide/)
[MicroPython - Getting Started with MQTT on ESP32/ESP8266 | Random Nerd Tutorials](https://randomnerdtutorials.com/micropython-mqtt-esp32-esp8266/)
[A Robust ESP8266 RFID Access Control System | Hackaday](https://hackaday.com/2019/04/15/a-robust-esp8266-rfid-access-control-system/)
[ESP32 Capacitive Touch Sensor Pins with Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-touch-pins-arduino-ide/)
[MicroPython on Cheap \$3 ESP8266 WeMos D1 Mini for 2x Temperature Logging, Wifi and Mobile Stats: 4 Steps](https://www.instructables.com/id/MicroPython-on-Cheap-3-ESP8266-WeMos-D1-Mini-for-T/)

[ESP32 Micro Robot Arm - Electron Dust](https://electrondust.com/2018/11/11/esp-32-micro-robot-arm/)

[esp32 projects, esp32, esp32 review,The Best 14 ESP32 Projects Overview](https://www.dfrobot.com/blog-699.html)

OTA
[scottchiefbaker/ESP-WebOTA](https://github.com/scottchiefbaker/ESP-WebOTA)
[ESP32 Over-the-air (OTA) Programming | Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-over-the-air-ota-programming/)
[Library Makes ESP Over the Air Updates Easy | Hackaday](https://hackaday.com/2019/03/21/library-makes-esp-over-the-air-updates-easy/)
[Running the IOTA CClient library on ESP32 – IOTA](https://blog.iota.org/running-the-iota-cclient-library-on-esp32-4a1a5191afad)

Andreas Spiess, the guy with Sweden accent
[ESP8266 - YouTube](https://www.youtube.com/playlist?list=PL3XBzmAj53Rlu3Byy_GkqG6b-nwEpWku0)
[IOT Framework with ESP8266 - YouTube](https://www.youtube.com/playlist?list=PL3XBzmAj53Rl2vNyL9ucv87xnbUHzpSPw)
[ESP32 - YouTube](https://www.youtube.com/playlist?list=PL3XBzmAj53RnZPeWe799F-uoXERBldhn9)

[Hardware-Related Content](https://steve.fi/Hardware/)
[skx/esp8266: Collection of projects for the WeMos Mini D1](https://github.com/skx/esp8266) OLED, WifiManage, Web server, MQTT client
[gbafana25/esp8266_honeypot: THE ESP8266 HONEYPOT: A PROJECT TO TRAP SCRIPT KIDDIES EVERYWHRE!!](https://github.com/gbafana25/esp8266_honeypot)

[An ESP8266 Sundial For Your Wall | Hackaday](https://hackaday.com/2019/03/20/an-esp8266-sundial-for-your-wall/)
[dheera/shadow-clock: a wall clock](https://github.com/dheera/shadow-clock)

[AM Radio Transmitter – bitluni's lab](http://bitluni.net/am-radio-transmitter/)
[ESP32 Composite Video – bitluni's lab](http://bitluni.net/esp32-composite-video/)
[ESP32 VGA – bitluni's lab](http://bitluni.net/esp32-vga/)
