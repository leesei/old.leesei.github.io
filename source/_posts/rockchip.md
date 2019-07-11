---
title: Rockchip
  - comp.hardware
tags:
  - iot
  - rk3288
toc: true
date: 2018-10-20 09:22:17
---

# Rockchip

[Firefly | 让科技更简单，让生活更智能](http://www.t-firefly.com/index.html)
[论坛首页 - Firefly 开源社区论坛首页](http://dev.t-firefly.com/portal.php?mod=topic&topicid=11)
Firefly are Rockchip dev boards

## Firefly RK3288

[Firefly-RK3288](http://www.t-firefly.com/product/rk3288.html)
[Firefly-RK3288 Wiki](http://en.t-firefly.com/doc/product/index/id/4.html)

[Firefly-RK3288 中文](http://www.t-firefly.com/product/rk3288.html)
[Firefly Wiki 中文](http://wiki.t-firefly.com/zh_CN/Firefly-RK3288/start_guide.html)

[Firefly-RK3288 - Firefly Open Source Community](http://bbs.t-firefly.com/forum-126-1.html)
[Firefly-RK3288 - Firefly 开源社区](http://dev.t-firefly.com/forum-284-1.html)

[Rockchip 3288 & 3328 - Armbian forum](https://forum.armbian.com/forum/21-rockchip-3288-3328/)

[Linux SDK - Rockchip open source Document](http://opensource.rock-chips.com/wiki_Linux_SDK)
[RK3288 - Rockchip open source Document](http://opensource.rock-chips.com/wiki_RK3288)

rk tool 2.22+
[Boot Ubuntu (Linux) or Android from an SD Card on Rockchip RK3288 Devices](https://www.cnx-software.com/2014/12/11/boot-ubuntu-linux-or-android-from-an-sd-card-on-rockchip-rk3288-devices/)
[Leon Anavi - Mobile & Embedded - Booting Ubuntu from microSD Card on Firefly-RK3288](https://www.anavi.org/article/172/)
[Linux Users Guide - Rockchip Wiki](http://rockchip.wikidot.com/linux-user-guide#toc20)
[How to apply Firefly Rk3288 · Planet15/linux Wiki](https://github.com/Planet15/linux/wiki/How-to-apply-Firefly-Rk3288)
[linux-build/overclocking.md at master · ayufan-rock64/linux-build](https://github.com/ayufan-rock64/linux-build/blob/master/recipes/overclocking.md)

[FireflyTeam/docker-rockchip: Docker image for rockchip linux sdk](https://github.com/FireflyTeam/docker-rockchip)

## Resources Download

[资料下载](http://www.t-firefly.com/doc/download/page/id/4.html)
[Download](http://en.t-firefly.com/doc/download/page/id/4.html)
[Ubuntu\_免费高速下载|百度网盘-分享无限制](https://pan.baidu.com/s/1g1OVtmDQsNeWMx4MVFz5ng#list/path=%2FPublic%2FDevBoard%2FFirefly-RK3288%2FFirmware%2FFirefly-RK3288%2FUbuntu&parentPath=%2FPublic%2FDevBoard%2FFirefly-RK3288%2FFirmware%2FFirefly-RK3288)

[Firefly-RK3288 - Google Drive](https://drive.google.com/drive/folders/0B7HO8lbGgAqAMDk1OGxZdkhrNlU)
[Firefly-RK3288 Firmware - Google Drive](https://drive.google.com/drive/folders/0B7HO8lbGgAqALVhOYUZSNVpxME0)

```
解决存储空间不足问题
sudo /sbin/resize2fs /dev/mmcblk2p3

解决firefox奔溃问题：
sudo apt update
sudo apt remove firefox
sudo apt-cache madison firefox // 查看firefox可用的版本
sudo apt install firefox=45.0.2+build1-0ubuntu1  // 安装旧版本
（谁有更好的解决办法，烦请告知，谢谢～）

解决ParoleMediaPlay的GStreamer错误：
[Tools]->[Preferences]->[Display]，将Video Output设置为No Xv
```

[tlgimenes/archlinux-firefly: This is a repository teaching how to install ArchLinux ARM on the Firefly-rk3288](https://github.com/tlgimenes/archlinux-firefly)

## Flashing

[Firefly | Flashing Image](http://en.t-firefly.com/doc/product/info/id/231.html)
[升级固件 — Firefly Wiki](http://wiki.t-firefly.com/zh_CN/Firefly-RK3288/download_firmware.html)
[Linux 升级固件 — Firefly Wiki](http://wiki.t-firefly.com/zh_CN/Firefly-RK3288/upgrade_firmware-linux.html)

`rkflash.sh`

```sh
# single image
sudo upgrade_tool uf <update.img>

# separate partitions
sudo upgrade_tool ul rk3399_loader_v1.09.112.bin
sudo upgrade_tool di -p parameter.txt
sudo upgrade_tool di -u uboot.img
sudo upgrade_tool di -t trust.img
sudo upgrade_tool di -re resource.img
sudo upgrade_tool di -k kernel.img
sudo upgrade_tool di -rootfs rootfs.img
sudo upgrade_tool rd
```

[Tools - Rockchip open source Document](http://opensource.rock-chips.com/wiki_Tools)
[Upgradetool - Rockchip open source Document](http://opensource.rock-chips.com/wiki_Upgradetool)
[Rkdeveloptool - Rockchip open source Document](http://opensource.rock-chips.com/wiki_Rkdeveloptool)

[rockchip-linux/tools: Rockchip Develop tools](https://github.com/rockchip-linux/tools)

[Rockusb - Rockchip open source Document](http://opensource.rock-chips.com/wiki_Rockusb) the protocol
[Boot option - Rockchip open source Document](http://opensource.rock-chips.com/wiki_Boot_option)
[Firefly | Boot mode](http://en.t-firefly.com/doc/product/info/id/233.html)

[Partitions - Rockchip open source Document](http://opensource.rock-chips.com/wiki_Partitions)
[Firefly RK3288 'parameter' File Generator - Firefly-RK3288 - Firefly Open Source CommunityFirefly RK3288 'parameter' File Generator](http://bbs.t-firefly.com/forum.php?mod=viewthread&tid=609&extra=page%3D1)

[How to Update Any Rockchip Android Box Full Tutorial 2017 Using the NT N8 - YouTube](https://www.youtube.com/watch?v=6A_-ataMLus)
[Video: How to easily flash firmware on Rikomagic V5 RK3288 Android TV Stick ~ China Gadgets Reviews](http://chinagadgetsreviews.blogspot.com/2015/01/video-how-to-easily-flash-firmware-on.html)

```sh
# 解决存储空间不足问题
sudo /sbin/resize2fs /dev/mmcblk2p3
```

## Compiling Kernel

[RK3288 使用 kernel4.4+ubuntu16.04，纯 linux 下升级包制作 - Firefly-RK3288 - Firefly 开源社区](http://dev.t-firefly.com/thread-12393-1-1.html)

[luwanjia/linux-kernel](https://github.com/luwanjia/linux-kernel)
[T-Firefly / linux-kernel · GitLab](https://gitlab.com/TeeFirefly/linux-kernel)
[T-Firefly / prebuilts · GitLab](https://gitlab.com/TeeFirefly/prebuilts) tool chain

## GPIO

[RK3288 的 gpio 设置 - keleming1 的博客 - CSDN 博客](https://blog.csdn.net/keleming1/article/details/51034766) !important
`/kernel/drivers/pinctrl/pinctrl-rockchip.c`
`/kernel/arch/arm/boot/dts/rk3288-pinctrl.dtsi`

`ls /dev/*spi*`, `ls /dev/*i2c*`

[RK3288 开发板 GPIO 介绍 - 一块钢板 - CSDN 博客](https://blog.csdn.net/limin2928/article/details/63252725)
[how to use GPIO ? - Firefly-RK3288 - Firefly Open Source Community](http://bbs.t-firefly.com/forum.php?mod=viewthread&tid=731)
[Gpio-int-test.c - RidgeRun Developer Connection](https://developer.ridgerun.com/wiki/index.php/Gpio-int-test.c).

[rk3128 控制 GPIO - lzpdz 的博客 - CSDN 博客](https://blog.csdn.net/lzpdz/article/details/51853725)
[RK3399 用户空间 IO 控制 - zhuyong006 的博客 - CSDN 博客](https://blog.csdn.net/zhuyong006/article/details/80907718?utm_source=blogxgwz0)
[Renegade 3328 GPIO not working - Rockchip 3288 & 3328 - Armbian forum](https://forum.armbian.com/topic/8376-renegade-3328-gpio-not-working/)

[zhansb/pyFireflyP](https://github.com/zhansb/pyFireflyP)
[[fireflyP] GPIO 使用 - Firefly-RK3288 - Firefly 开源社区[fireflyP] GPIO 使用](http://dev.t-firefly.com/thread-10588-1-1.html)
[[fireflyP] PWM 使用 - Firefly-RK3288 - Firefly 开源社区[fireflyP] PWM 使用](http://dev.t-firefly.com/thread-10606-1-1.html)
[[fireflyP] SPI 使用 - Firefly-RK3288 - Firefly 开源社区[fireflyP] SPI 使用](http://dev.t-firefly.com/thread-10636-1-1.html)

[shawn-github/rk3288-gpio-control: rk3288 游戏机，gpio 作为输出和按键](https://github.com/shawn-github/rk3288-gpio-control)
[tjCFeng/GoRK3288: golang RK3288](https://github.com/tjCFeng/GoRK3288)

## Asus Tinker Board

[Tinker Board | Single-board Computer | ASUS United Kingdom](https://www.asus.com/uk/Single-board-Computer/TINKER-BOARD/)
[Asus Tinker Board - YouTube](https://www.youtube.com/watch?v=CS66_BbalG8)

RK3288

Tinker Board S has built-in 16G eMMC flash

[GPIO - Tinker Board Wiki](https://tinkerboarding.co.uk/wiki/index.php/GPIO)
[TinkerBoard/gpio_lib_python](https://github.com/TinkerBoard/gpio_lib_python)
[GPIO - Tinker Board Wiki](https://tinkerboarding.co.uk/wiki/index.php?title=GPIO#Python)
[sabrigultekin/Asus-Tinker-Board: Asus Tinker Board Basic Applications](https://github.com/sabrigultekin/Asus-Tinker-Board)
[Using Python to control/test GPIO pins](https://tinkerboarding.co.uk/forum/thread-306.html)

## Fireduino

[Fireduino](http://www.t-firefly.com/doc/product/index/id/7.html) !important
RKNanoD
[Fireduino Arduino Compatible Board Features Rockchip RKnanoD Dual Core Cortex-M3 MCU (Crowdfunding)](https://www.cnx-software.com/2016/06/21/fireduino-arduino-compatible-board-features-rockchip-rknanod-dual-core-cortex-m3-mcu-crowdfunding/)
[Using the new Fireduino board with Linux - YouTube](https://www.youtube.com/watch?v=7ZgoaiY37m8) have to start IDE as root

## Radxa

[Radxa](https://wiki.radxa.com/Home)
[Rockpi4 - Radxa](https://wiki.radxa.com/Rockpi4)

[ROCK PI S – ALLNET China](https://shop.allnetchina.cn/collections/frontpage/products/rock-pi-s)

## FriendlyElec

[FriendlyElec](https://www.friendlyarm.com/)

[NanoPC & NanoPi](https://www.friendlyarm.com/index.php?route=product/category&path=69)
[NanoPi NEO4](https://www.friendlyarm.com/index.php?route=product/product&product_id=241)
[NanoPi NEO4 review: A powerful Raspberry Pi rival but with drawbacks - TechRepublic](https://www.techrepublic.com/article/nanopi-neo4-review-a-powerful-raspberry-pi-rival-but-with-drawbacks/)
