---
title: Raspberry Pi
categories:
  - maker
tags:
  - iot
  - raspberry-pi
  - rpi
toc: true
date: 2018-09-12 23:56:12
---

> on Rasp Pi 3, 4 and on

[Inside the Raspberry Pi: The story of the \$35 computer that changed the world - TechRepublic](https://www.techrepublic.com/article/inside-the-raspberry-pi-the-story-of-the-35-computer-that-changed-the-world/)

[Raspberry Pi - Teach, Learn, and Make with Raspberry Pi](https://www.raspberrypi.org/)
[Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/)
[Raspberry Pi hardware - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/hardware/raspberrypi/)
[utils/raspinfo at master · raspberrypi/utils](https://github.com/raspberrypi/utils/blob/master/raspinfo/raspinfo)
[Raspberry Pi Downloads - Software for the Raspberry Pi](https://www.raspberrypi.org/downloads/)

[The MagPi Magazine - The official Raspberry Pi magazine](https://www.raspberrypi.org/magpi/)
[Hello World](https://helloworld.raspberrypi.org/) magazine for educators
[Custom PC magazine](https://custompc.raspberrypi.com/)
[Online training - Raspberry Pi](https://www.raspberrypi.org/training/online/)

[thibmaek/awesome-raspberry-pi: 📝 A curated list of awesome Raspberry Pi tools, projects, images and resources](https://github.com/thibmaek/awesome-raspberry-pi)
[RPi Hub - eLinux.org](https://elinux.org/RPi_Hub)
[Kolban's Book on the Raspberry… by Neil Kolban [PDF/iPad/Kindle]](https://leanpub.com/pi)
[Raspberry Pi: The Unofficial Tutorial](https://www.makeuseof.com/tag/great-things-small-package-your-unofficial-raspberry-pi-manual/)
[Inside the Raspberry Pi: The story of the \$35 computer that changed the world - TechRepublic](https://www.techrepublic.com/article/inside-the-raspberry-pi-the-story-of-the-35-computer-that-changed-the-world/)
[Lifehacker's Complete Guide to Raspberry Pi](https://lifehacker.com/s/raspberrypiguide)
[The Always-Up-to-Date Guide to Setting Up Your Raspberry Pi](https://lifehacker.com/the-always-up-to-date-guide-to-setting-up-your-raspberr-1781419054)
[ARM/RaspberryPi - Ubuntu Wiki](https://wiki.ubuntu.com/ARM/RaspberryPi#Packages)

[RasPi.TV – Raspberry Pi, Electronics & Making](https://raspi.tv/)

[Why Every Tech Geek Should Own a Raspberry Pi](https://www.tomshardware.com/news/why-own-raspberry-pi,38809.html)

[Setting up your Raspberry Pi - Introduction | Raspberry Pi Projects](https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up)
[Setting up your Raspberry Pi - Introduction | Raspberry Pi Projects](https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up)
[How to Set Up a Raspberry Pi for the First Time](https://www.tomshardware.com/reviews/raspberry-pi-set-up-how-to,6029.html)

[Give Your Raspberry Pi SD Card a Break: Log to RAM | Hackaday](https://hackaday.com/2019/04/08/3give-your-raspberry-pi-sd-card-a-break-log-to-ram/)
[Log2Ram: Extending SD Card Lifetime for Raspberry Pi LoRaWAN Gateway | MCU on Eclipse](https://mcuoneclipse.com/2019/04/01/log2ram-extending-sd-card-lifetime-for-raspberry-pi-lorawan-gateway/)

[Python Programming Tutorial: Getting Started with the Raspberry Pi - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/python-programming-tutorial-getting-started-with-the-raspberry-pi/configure-your-pi)
[How to Set Up a Headless Raspberry Pi, No Monitor Needed | Tom's Hardware](https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html)

[Headless Raspberry Pi Setup - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/headless-raspberry-pi-setup)
[Ansible Playbook to create a minimal headless raspberry pi – Stineblog](http://www.stinebaugh.info/ansible-playbook-to-create-a-minimal-headless-raspberry-pi/)
[PiBakery - The blocks based, easy to use setup tool for Raspberry Pi](https://www.pibakery.org/)
[Configure Your Raspberry Pi Installation With PiBakery](https://www.makeuseof.com/tag/configure-raspberry-pi-installation-pibakery/)

[Raspberry Pi And The IoT In C](https://www.iot-programmer.com/index.php/books/17-raspberry-pi-and-the-iot-in-c)
[9 Best Pi Programming Resources to Put Your Raspberry Pi to Use](https://www.makeuseof.com/tag/best-raspberry-pi-programming-resources/)

ExplainingComputers:
[Raspberry Pi 3 - YouTube](https://www.youtube.com/playlist?list=PL2m2YvnrOYxKWlCkoSZXfkLtgDAMev9oN)
[Raspberry Pi 3 Model B+ - YouTube](https://www.youtube.com/playlist?list=PL2m2YvnrOYxIABPXD2YY-ilcy_quyyEbT)
[Raspberry Pi 4 Model B - YouTube](https://www.youtube.com/watch?v=CXCjpJasvG0)
[Raspberry Pi Robotics - YouTube](https://www.youtube.com/playlist?list=PL2m2YvnrOYxLOZG0TGQgm9LAEYuvaglzY)

[Raspberry Pi 4 Benchmarks: Processor And Network Performance Makes It A Real Desktop Contender | Hackaday](https://hackaday.com/2019/07/10/raspberry-pi-4-benchmarks-processor-and-network-performance-makes-it-a-real-desktop-contender/)
[Benchmarked: Raspberry Pi 4 Hits 2 GHz with New Firmware - Tom's Hardware](https://www.tomshardware.com/reviews/raspberry-pi-4-overclock-2-ghz,6254.html)

[Robotics and the Raspberry Pi - sentdex - YouTube](https://www.youtube.com/user/sentdex/playlists?sort=dd&view=50&shelf_id=20)
[Robotics with Python Raspberry Pi and GoPiGo - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDcG4wbhhCv_XTnexvWfjlBy)

## updating

[Raspberry Pi 4 Firmware Update: All You Need to Know | All3DP](https://m.all3dp.com/2/raspberry-pi-4-firmware-update-tutorial/)

[Updating and upgrading Raspberry Pi OS - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/raspbian/updating.md)
[rpi-update - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/raspbian/applications/rpi-update.md)

```sh
sudo apt update
sudo apt upgrade
sudo rpi-update # update your Raspberry Pi OS kernel and VideoCore firmware to the latest pre-release versions

sudo apt full-upgrade # this upgrade firmware too
```

Firmware

```sh
unzip vl805_update_0137a8.zip
chmod a+x vl805
sudo ./vl805 -w vl805_fw_0137a8.bin
sudo reboot

# to revert
sudo ./vl805 -w vl805_fw_013701.bin
sudo reboot
```

### RPi4 issues

[Raspberry Pi 4 Rev 1.2 Fixes USB-C Power Issues, Improves SD Card Resilience](https://www.cnx-software.com/2020/02/24/raspberry-pi-4-rev-1-2-fixes-usb-c-power-issues-improves-sd-card-resilience/)

[Pi4 not working with some chargers (or why you need two cc resistors) – The blog of Tyler Ward (aka scorpia)](https://www.scorpia.co.uk/2019/06/28/pi4-not-working-with-some-chargers-or-why-you-need-two-cc-resistors/)
[The Raspberry Pi Foundation messed up its first USB-C device - The Verge](https://www.theverge.com/platform/amp/2019/7/10/20688655/raspberry-pi-4-usb-c-port-bug-e-marked-cables-audio-accessory-charging)
[Exploring The Raspberry Pi 4 USB-C Issue In-Depth | Hackaday](https://hackaday.com/2019/07/16/exploring-the-raspberry-pi-4-usb-c-issue-in-depth/) USB-C standard

[Thermal testing Raspberry Pi 4 - Raspberry Pi](https://www.raspberrypi.org/blog/thermal-testing-raspberry-pi-4/) 2019-11-28, beta firmware
[Overclocking the Raspberry Pi 4 - Tom's Hardware | Tom's Hardware](https://www.tomshardware.com/reviews/raspberry-pi-4-b-overclocking,6188.html) 2019-10
[Raspberry Pi 4 Firmware Updates Tested: A Deep Dive Into Thermal Performance and Optimization - Hackster.io](https://www.hackster.io/news/raspberry-pi-4-firmware-updates-tested-a-deep-dive-into-thermal-performance-and-optimization-2f22c78e7089)

## USB booting

USB boot mode is stored on chip
[USB mass storage boot - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bootmodes/msd.md)
[documentation/hardware/raspberrypi/bootmodes at master · raspberrypi/documentation](https://github.com/raspberrypi/documentation/tree/master/hardware/raspberrypi/bootmodes)

### <= Raspberry Pi 3

[Pi 3 booting part I: USB mass storage boot beta - Raspberry Pi](https://www.raspberrypi.org/blog/pi-3-booting-part-i-usb-mass-storage-boot/)
[Install Raspbian on a USB Flash drive from MacOS or Linux](https://www.stewright.me/2017/06/install-raspbian-usb-flash-drive-macos-linux/)

[documentation/booteeprom.md at master · raspberrypi/documentation](https://github.com/raspberrypi/documentation/blob/master/hardware/raspberrypi/booteeprom.md)

### Raspberry Pi 4

> EEPROM update in 2020-05 enabled this

[Booting my Raspberry Pi 4 from a USB device | ZDNet](https://www.zdnet.com/google-amp/article/booting-my-raspberry-pi-4-from-a-usb-device/)
[How to Boot Raspberry Pi 4 From a USB SSD or Flash Drive | Tom's Hardware](https://www.tomshardware.com/how-to/boot-raspberry-pi-4-usb)
[raspberrypi/rpi-eeprom: This repository contains the scripts and pre-compiled binaries used to create the rpi-eeprom package which is used to update the Raspberry Pi4 bootloader EEPROM.](https://github.com/raspberrypi/rpi-eeprom)
[I'm booting my Raspberry Pi 4 from a USB SSD | Jeff Geerling](https://www.jeffgeerling.com/blog/2020/im-booting-my-raspberry-pi-4-usb-ssd)

## RPiconfig

[RPiconfig - eLinux.org](https://elinux.org/RPiconfig)

`sudo raspi-config` provides an interface to edit `config.txt`

SPI and I2C are disabled by default, it has to be enabled in RPiconfig to load the appropriate module

## Pinout/GPIO

[Raspberry Pi GPIO Pinout](https://pinout.xyz/)
[GPIO - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/hardware/raspberrypi/gpio/README.md)
[Raspberry Pi GPIO basics - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDdnpgDr1YZF9dI_4G334od6)
[Raspberry gPIo - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/raspberry-gpio)
[Everything You Need to Know About Raspberry Pi GPIO Pins](https://www.makeuseof.com/tag/raspberry-pi-gpio-pins-guide/)
[Raspberry Pi GPIO Pinout: What Each Pin Does - Tom's Hardware](https://www.tomshardware.com/reviews/raspberry-pi-gpio-pinout,6122.html)

[Ben Croston – RasPi.TV](https://raspi.tv/tag/ben-croston) GPIO series

[Raspberry Pi SPI and I2C Tutorial - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/raspberry-pi-spi-and-i2c-tutorial/all)
[How to set up i²c in Raspbian on the Raspberry Pi – RasPi.TV](https://raspi.tv/how-to-set-up-i2c-in-raspbian-on-the-raspberry-pi)
[SPI - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/hardware/raspberrypi/spi/README.md)
[Raspberry Pi GPIO Tutorial: The Basics Explained - Pi My Life Up](https://pimylifeup.com/raspberry-pi-gpio/)

[Using the Raspberry Pi Timer for Embedded Environments | Studica Blog](https://www.studica.com/blog/raspberry-pi-timer-embedded-environments)
[Behind The Pin: How The Raspberry Pi Gets Its Audio | Hackaday](https://hackaday.com/2018/07/13/behind-the-pin-how-the-raspberry-pi-gets-its-audio/)
[gpio - Driving PWM output frequency - Raspberry Pi Stack Exchange](https://raspberrypi.stackexchange.com/questions/53854/driving-pwm-output-frequency)

[Can a Raspberry Pi be used as an Arduino? || RPi GPIO Programming Guide 101 - YouTube](https://www.youtube.com/watch?v=tQEmtbaO2GY)
[Arduino vs Raspberry Pi - Which Board is Best For You? - YouTube](https://www.youtube.com/watch?v=v6mJUqtkXUM)

[What are the min/max voltage/current values the gpio pins can handle? - Raspberry Pi Stack Exchange](https://raspberrypi.stackexchange.com/questions/3209/what-are-the-min-max-voltage-current-values-the-gpio-pins-can-handle)

[raspberry-gpio-python download | SourceForge.net](https://sourceforge.net/projects/raspberry-gpio-python/) `RPi.GPIO`
[Welcome to RPIO’s documentation! — RPIO 0.10.0 documentation](https://pythonhosted.org/RPIO/)

### Emulator

[Raspberry Pi GPIO Emulator Simulates Physical Components | Tom's Hardware](https://www.tomshardware.com/amp/news/raspberry-pi-gpio-emulator-simulates-physical-components)

### gpiozero

[gpiozero — Gpiozero Documentation](https://gpiozero.readthedocs.io/en/stable/)
[RPi-Distro/python-gpiozero: A simple interface to GPIO devices with Raspberry Pi](https://github.com/RPi-Distro/python-gpiozero)

[GPIO Zero: a friendly Python API for physical computing - Raspberry Pi](https://www.raspberrypi.org/blog/gpio-zero-a-friendly-python-api-for-physical-computing/)
[GPIO Zero: Developing a new friendly Python API for Physical Computing - Ben Nuttall](https://bennuttall.com/gpio-zero-developing-a-new-friendly-python-api-for-physical-computing/)
[Updates to GPIO Zero, the physical computing API - Raspberry Pi](https://www.raspberrypi.org/blog/gpio-zero-update/) v1.4
[What's new in GPIO Zero v1.4? - Ben Nuttall](https://bennuttall.com/whats-new-gpio-zero-v1-4/)

[GPIO Zero Essentials - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/issues/essentials-gpio-zero-v1/)

[GPIO expander: access a Pi's GPIO pins on your PC/Mac - Raspberry Pi](https://www.raspberrypi.org/blog/gpio-expander/)
[4. Configuring Remote GPIO — Gpiozero 1.4.1 Documentation](https://gpiozero.readthedocs.io/en/stable/remote_gpio.html)

### pigpio

[pigpio library](http://abyz.me.uk/rpi/pigpio/)
[joan2937/pigpio: pigpio is a C library for the Raspberry which allows control of the General Purpose Input Outputs (GPIO).](https://github.com/joan2937/pigpio)

### WiringPi

[WiringPi](http://wiringpi.com/) Arduino's `wiring` API
[GPIO Access in C with Raspberry Pi: Traffic Lights - Simon Prickett - Medium](https://medium.com/@simon_prickett/gpio-access-in-c-with-raspberry-pi-traffic-lights-6b982e197d45)

### CircuitPython

> see `iot.md#circuitpython`
>
> [Overview | CircuitPython on Linux and Raspberry Pi | Adafruit Learning System](https://learn.adafruit.com/circuitpython-on-raspberrypi-linux?view=all)

## Modifying image

[Modify a disk image to create a Raspberry Pi-based homelab | Opensource.com](https://opensource.com/article/20/5/disk-image-raspberry-pi)

## Cross compilation

```sh
$ sudo git clone https://github.com/raspberrypi/tools --depth 1 /opt/rpi_tools
$ export PATH=$PATH:/opt/rpi_tools/arm-bcm2708/gcc-linaro-arm-linux-gnueabihf-raspbian/bin
$ > hello.c <<EOF
# include <stdio.h>
int main() {
    printf("%s\n", "Hello World");
    return 0;
}
EOF
$ arm-linux-gnueabihf-gcc -o hello hello.c
$ file hello
hello: ELF 32-bit LSB executable, ARM, EABI5 version 1 (SYSV), dynamically linked, interpreter /lib/ld-, for GNU/Linux 2.6.26, BuildID[sha1]=b5d2d491fea9afdf8259aea28f0e6c02929711dc, not stripped
```

Running on host:

```sh
$ sudo apt-get install qemu
$ export RPI_SYSROOT=$(arm-linux-gnueabihf-gcc --print-sysroot)
$ qemu-arm -L $RPI_SYSROOT ./hello
Hello World
```

- [Difference between native and cross compilation and how to compile simple program for x86 and ARM](https://www.lynxbee.com/difference-between-native-and-cross-compilation-and-how-to-compile-simple-program-for-x86-and-arm/)
- [How to cross compile for ARM](http://www.firmcodes.com/how-to-cross-compile-for-arm/)

### Cross Compile Qt5

[Raspberry Pi Beginners Guide - Qt Wiki](https://wiki.qt.io/Raspberry_Pi_Beginners_Guide)

1. Mounting RootFS

```sh
# destination mount point
$ sudo mkdir /mnt/rpi-rootfs
# download http://director.downloads.raspberrypi.org/raspbian_full/images/raspbian_full-2019-04-09/2019-04-08-raspbian-stretch-full.zip
# do not use NOOBS images
$ fdisk -l raspbian-full.img
Disk raspbian-full.img: 5 GiB, 5402263552 bytes, 10551296 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0x43c1e3bb

Device                                Boot Start      End  Sectors  Size Id Type
2019-04-08-raspbian-stretch-full.img1       8192    96042    87851 42.9M  c W95 FAT32 (LBA)
2019-04-08-raspbian-stretch-full.img2      98304 10551295 10452992    5G 83 Linux
# mount the image by using the sector size of `512` and start block number `98304`
$ sudo mount raspbian-full.img -o loop,offset=$(( 512 * 98304)) /mnt/rpi-rootfs/
# check the mounting point
$ ls /mnt/rpi-rootfs
```

```sh
# fix symlinks in rootfs
$ wget https://raw.githubusercontent.com/riscv/riscv-poky/master/scripts/sysroot-relativelinks.py
$ chmod +x sysroot-relativelinks.py./sysroot-relativelinks.py
$ sudo ./sysroot-relativelinks.py /mnt/rpi-rootfs
```

2. Setup toolchain

```sh
# download this on 64-bit system
$ sudo apt-get install lib32z1
```

Install QT (to `~/Qt/5.12.3/`)
Fix Qt `qmake` configuration bugs for `raspberrypi` which has different names for `EGL` libraries in new `stretch` version.
Search `./qtbase/mkspecs/devices/linux-rasp-pi-g++/qmake.conf` file, all references to `-IEGL` and `-LGLESv2` need to be substituted for `-lbrcmEGL` and `-lbrcmGLESv2` respectively.

```sh
$ git clone https://github.com/oniongarlic/qt-raspberrypi-configuration.git
$ cd qt-raspberrypi-configuration && make install DESTDIR=~/Qt/5.12.3/Src/
```

```sh
$ cd ~/Qt/5.12.3/Src/
$ export RPI_TOOLCHAIN=/opt/rpi-tools/arm-bcm2708/gcc-linaro-arm-linux-gnueabihf-raspbian-x64/bin/arm-linux-gnueabihf-
$ export RPI_SYSROOT=/mnt/rpi-rootfs
$ export RPI_QT5=/opt/rpi-qt5  # cross compiled libraries for RPi
$ export RPI_QT5_TOOLS=/opt/rpi-qt5-tools  # host tools for cross compilation
$ ./configure -release \
    -opensource -confirm-license \
    -opengl es2 \
    -device linux-rasp-pi-g++ \
    -device-option CROSS_COMPILE=$RPI_TOOLCHAIN \
    -sysroot $RPI_SYSROOT \
    -extprefix $RPI_QT5 \
    -hostprefix $RPI_QT5_TOOLS \
    -make libs \
    -skip qtwayland -skip qtlocation -skip qtscript -skip qtdatavis3d \
    -no-use-gold-linker -no-gbm -v
$ make -j(nproc) && make install
$ ll $RPI_QT5
# install to RPi
$ rsync -avz --rsync-path="sudo rsync" $RPI_QT5 pi@raspberrypi.local:/usr/local
```

3. Cross compiling QT app

```sh
$ cd TextFinder/build-rpi
$ $RPI_QT5_TOOLS/bin/qmake ../TextFinder.pro
$ ls
Makefile .qmake.stash
$ make -j$(nproc)
$ file TextFinder
TextFinder: ELF 32-bit LSB executable, ARM, EABI5 version 1 (SYSV), dynamically linked, interpreter /lib/ld-, for GNU/Linux 3.2.0, BuildID[sha1]=fcbc9b1ee203db6b9ae8ff4b9fe783d1183c9775, not stripped
```

To build a static linking Qt program, seeing [Linking to Static Builds of Qt](https://doc.qt.io/QtForDeviceCreation/qtee-static-linking.html)

[Cross-compile and deploy Qt 5.12 for Raspberry Pi](https://mechatronicsblog.com/cross-compile-and-deploy-qt-5-12-for-raspberry-pi/)
[How to cross compile QT for Raspberry Pi 3 on Linux (Ubuntu) for Beginners!](https://medium.com/@amirmann/how-to-cross-compile-qt-for-raspberry-pi-3-on-linux-ubuntu-for-beginners-75acf2a078c)
[Building Qt 5.12 LTS for Raspberry Pi on Debian Stretch](https://www.tal.org/tutorials/building-qt-512-raspberry-pi)
[OpenGL ES2 error while Cross Compiling Qt5.11 for Raspbian Stretch with desktop](https://www.raspberrypi.org/forums/viewtopic.php?t=227408)

## HATs

[Introducing Raspberry Pi HATs - Raspberry Pi](https://www.raspberrypi.org/blog/introducing-raspberry-pi-hats/)
[Tip of the HAT to the RasPi – A Discussion on the Pi HAT Hardware Specification](https://www.electroschematics.com/14036/tip-of-the-hat-to-the-raspi-a-discussion-on-the-pi-hat-hardware-specification/)

[Making Robot Friends with the Crickit HAT for Raspberry Pi - Raspberry Pi](https://www.raspberrypi.org/blog/making-robot-friends-with-the-crickit-hat-for-raspberry-pi/)

[Raspberry Pi machine learning HAT - Geeky Gadgets](https://www.geeky-gadgets.com/raspberry-pi-machine-learning-hat-07-08-2019/)

## GPU

[GPGPU hacking on the Pi - Raspberry Pi](https://www.raspberrypi.org/blog/gpgpu-hacking-on-the-pi/)
[Raspberry Pi VideoCore APIs - eLinux.org](https://elinux.org/Raspberry_Pi_VideoCore_APIs)
[hermanhermitage/videocoreiv-qpu: Fun and Games with the Videocoreiv Quad Processor Units](https://github.com/hermanhermitage/videocoreiv-qpu)

[RPI4 & Ubuntu MATE - How to enable video acceleration](https://www.dedoimedo.com/computers/rpi4-ubuntu-mate-hw-video-acceleration.html)

[Hacking The GPU For Fun And Profit (Pt. 1) | Raspberry Pi Playground](https://rpiplayground.wordpress.com/2014/05/03/hacking-the-gpu-for-fun-and-profit-pt-1/)
[Hacking The GPU For Fun And Profit (Pt. 2) | Raspberry Pi Playground](https://rpiplayground.wordpress.com/2014/05/06/hacking-the-gpu-for-fun-and-profit-pt-2/)
[Hacking The GPU For Fun And Profit (Pt. 3) | Raspberry Pi Playground](https://rpiplayground.wordpress.com/2014/05/13/hacking-the-gpu-for-fun-and-profit-pt-3/)
[Hacking The GPU For Fun And Profit (Pt. 4) | Raspberry Pi Playground](https://rpiplayground.wordpress.com/2014/05/21/hacking-the-gpu-for-fun-and-profit-pt-4/)

## Bluetooth

[Everything You Need to Set Up Bluetooth on the Raspberry Pi 3](https://lifehacker.com/everything-you-need-to-set-up-bluetooth-on-the-raspberr-1768482065)

## Camera

[Camera Module - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/hardware/camera/README.md)

[RPi Camera - Waveshare Wiki](http://www.waveshare.net/wiki/RPi_Camera)
[学习资料](https://www.yahboom.com/study_module/Camera-GJ)
[picamera — Picamera Documentation](https://picamera.readthedocs.io/en/)

Camera Module v1

- OV5647
- 5MP
- 1080p30, 720p60, 480p90

[raspicam commands - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/usage/camera/raspicam/README.md)
[Raspberry Pi Camera Module - Raspberry Pi Documentation](https://www.raspberrypi.org/documentation/raspbian/applications/camera.md)

```sh
sudo raspi-config -> Camera ->Enable

raspistill -o image.jpg -t 10000 -n # 10 sec timeout, no preview
raspistill -o image.jpg -t 2000 -p 100,100,300,200 # display with preview
raspistill -t 600000 -tl 10000 -o image_num_%d_today.jpg # one still every 10 sec, for 10 minutes

raspivid -o video.h264 -t 10000
raspivid -w 320 -h 240 -p 0 -t 10000 -o video.h264 # display to full screen
omxplayer -o hdmi video.h264 # plaback video
```

[Video Streaming Raspberry Pi Camera | Random Nerd Tutorials](https://randomnerdtutorials.com/video-streaming-with-raspberry-pi-camera/)
[How to Live Stream to YouTube With a Raspberry Pi](https://www.makeuseof.com/tag/live-stream-youtube-raspberry-pi/)
[Node-RED Raspberry Pi Camera (Take Photos) | Random Nerd Tutorials](https://randomnerdtutorials.com/node-red-with-raspberry-pi-camera-take-photos/)

## SBC

[Using a Raspberry Pi as a Desktop PC: 7 Things I Learned After a Week](https://www.makeuseof.com/tag/using-raspberry-pi-as-desktop-pc/)

[Use Your Raspberry Pi Like a Desktop PC](https://www.makeuseof.com/tag/use-your-raspberry-pi-like-a-desktop-pc/)
[How to Create Custom Keyboard Shortcuts for Raspberry Pi](https://www.tomshardware.com/news/raspberry-pi-custom-keyboard-shortcuts,40215.html) LXDE

[Build your own laptop in The MagPi #74 - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/build-laptop-magpi-74/)
[5 Ways to Turn Your Raspberry Pi Into a Laptop](https://www.makeuseof.com/tag/raspberry-pi-laptop/)
[4 Projects That Make Your Raspberry Pi Portable](https://www.makeuseof.com/tag/portable-raspberry-pi-projects/)
[NODE / Hardware - YouTube](https://www.youtube.com/playlist?list=PLBoRXNIahWlA6ZHYEqZxhthiQvVeqLZc1)

[DeskPi Pro Set-Top Box For Raspberry Pi 4 - SSD Support, Full Size HDMI, Ice Tower Cooler - YouTube](https://www.youtube.com/watch?v=MviNfqoukwo)
[Pi Case 40 by Cooler Master — Kickstarter](https://www.kickstarter.com/projects/coolermaster/pi-case-40)

### #perfmatters

[Effective Raspberry Pi ZRAM usage](https://www.linkedin.com/pulse/effective-raspberry-pi-ram-management-sergey-kovalenko/)

Changed the swap file to 2GB instead of 100MB:

```
sudo nano /etc/dphys-swapfile
CONF_SWAPSIZE=2048
sudo /etc/init.d/dphys-swapfile stop
sudo /etc/init.d/dphys-swapfile start
```

### OpenGL

[Raspberry Connect - Trying out OpenGL on Raspberry Pi 3](http://www.raspberryconnect.com/gamessoftware/item/314-trying_out_opengl_on_raspberry_pi_3)

`apt-get install -y mesa-utils mesa-vdpau-drivers`

Chrome settings (`chrome://flags`) or `00-rpi-vars`:

```
CHROMIUM_FLAGS="--disable-quic --enable-fast-unload --enable-tcp-fast-open --disable-gpu-compositing --enable-native-gpu-memory-buffers --use-gl=egl --gles --enable-gpu-rasterization --ignore-gpu-blacklist --enable-zero-copy"
```

```
CHROMIUM_FLAGS="--ignore-gpu-blacklist --enable-gpu-rasterization --enable-native-gpu-memory-buffers --enable-checker-imaging --disable-quic --enable-tcp-fast-open --disable-gpu-compositing --enable-fast-unload --enable-experimental-canvas-features --enable-scroll-prediction --enable-simple-cache-backend --answers-in-suggest --ppapi-flash-path=/usr/lib/chromium-browser/libpepflashplayer.so --ppapi-flash-args=enable_stage_stagevideo_auto=0 --ppapi-flash-version= --max-tiles-for-interest-area=512 --num-raster-threads=4 --default-tile-height=512"
```

```
CHROMIUM_FLAGS="${CHROMIUM_FLAGS} --purge-memory-button --smooth-scrolling --no-pings --disable-background-mode --dns-prefetch-disable --ignore-gpu-blacklist --enable-gpu-rasterization --enable-native-gpu-memory-buffers --enable-lazy-image-loading --enable-lazy-frame-loading --enable-checker-imaging --enable-quic --enable-resource-prefetch --enable-tcp-fast-open --disable-gpu-compositing --enable-fast-unload --enable-experimental-canvas-features --enable-scroll-prediction --enable-scroll-anchoring --enable-tab-audio-muting --disable-background-video-track --enable-simple-cache-backend --answers-in-suggest --ppapi-flash-path=/usr/lib/chromium-browser/libpepflashplayer.so --ppapi-flash-args=enable_stage_stagevideo_auto=0 --ppapi-flash-version= --max-tiles-for-interest-area=512 --num-raster-threads=4 --default-tile-height=512"
```

```
CHROMIUM_FLAGS="${CHROMIUM_FLAGS} --ignore-gpu-blacklist --enable-one-copy-rasterizer --enable-gpu-rasterization --enable-native-gpu-memory-buffers --enable-checker-imaging --enable-quic --site-per-process --enable-tcp-fastopen --disable-gpu-compositing --enable-fast-unload --enable-experimental-canvas-features --enable-scroll-prediction --answers-in-suggest --ppapi-flash-path=/usr/lib/chromium-browser/libpepflashplayer.so --ppapi-flash-args=enable_stagevideo_auto=0 --ppapi-flash-version= --max-tiles-for-interest-area=512 --num-raster-threads=4 --default-tile-height=512"
```

Expected `chrome://gpu`:

```
Graphics Feature Status
Canvas: Hardware accelerated
CheckerImaging: Disabled
Flash: Hardware accelerated
Flash Stage3D: Hardware accelerated
Flash Stage3D Baseline profile: Hardware accelerated
Compositing: Hardware accelerated
Multiple Raster Threads: Enabled
Native GpuMemoryBuffers: Hardware accelerated
Rasterization: Hardware accelerated on all pages
Video Decode: Hardware accelerated
```

### ExaGear Desktop

[ExaGear Desktop. Run x86 applications on ARM-based devices.](https://eltechs.com/product/exagear-desktop/)
[Run Google Chrome on Raspberry Pi | Linux.com | The source for Linux information](https://www.linux.com/blog/run-google-chrome-raspberry-pi)

## Gaming

> see `game-emulator.md#retroarch`

[Retro Gaming on the Raspberry Pi: Everything You Need to Know](https://www.makeuseof.com/tag/retro-gaming-on-the-raspberry-pi-everything-you-need-to-know-si/)
[How to Build a Raspberry Pi Retro Game Console](https://lifehacker.com/how-to-turn-your-raspberry-pi-into-a-retro-game-console-498561192)
[The Advanced Guide to Setting Up a DIY Game Console with a Raspberry Pi](https://lifehacker.com/the-advanced-guide-to-setting-up-a-diy-game-console-wit-1790381861)
[How to Play Almost Any Video Game on a Raspberry Pi](https://www.makeuseof.com/tag/play-video-games-raspberry-pi/)
[Retro Gaming in Style With RecalBox for the Raspberry Pi](https://www.makeuseof.com/tag/recalbox-raspberry-pi/)

Most are backed by RetroArch + EmulationStation

> see `game-emulator.md#lakka`

[RetroPie vs Recalbox vs Lakka for retro gaming on the Raspberry Pi](https://www.electromaker.io/blog/article/retropie-vs-recalbox-vs-lakka-for-retro-gaming-on-the-raspberry-pi)
[DIY Retro Game System Showdown: RetroPie vs. Recalbox](https://lifehacker.com/diy-retro-game-system-showdown-retropie-vs-recalbox-1787542021)

### RetroPie

[RetroPie - Retro-gaming on the Raspberry Pi](https://retropie.org.uk/)
[RetroPie Docs](https://retropie.org.uk/docs/)
[First Installation - RetroPie Docs](https://retropie.org.uk/docs/First-Installation/)
[Updating RetroPie - RetroPie Docs](https://retropie.org.uk/docs/Updating-RetroPie/)
[FAQ - RetroPie Docs](https://retropie.org.uk/docs/FAQ/)

[來自樹莓派界的傳奇工作室打造！【Insert Coin 茵絲可電玩工房】NESPI 4 / SSD / Raspberry 4b 套件 支援線上更新/Steam 串流/電視源播放 - YouTube](https://www.youtube.com/watch?v=LjkenDYheKU)

[How to Create a RetroPie on Raspberry Pi - Graphical Guide](https://davidwalsh.name/retropie-graphical-guide)
[Updating RetroPie · RetroPie/RetroPie-Setup Wiki](https://github.com/retropie/retropie-setup/wiki/updating-retropie)
[RetroPie 4.4. First Installation. A Beginner's Guide to Setting Up RetroPie on a Raspberry Pi - YouTube](https://www.youtube.com/watch?v=E1sbnPZ_A8w)
[Build a Raspberry Pi 4 Retro-Gaming Console with RetroPie (Complete Guide) - YouTube](https://www.youtube.com/watch?v=fsc3gYIYwV8)
[The ULTIMATE RetroPie 4.1 Raspberry Pi Setup Tutorial: 10 Steps (with Pictures)](https://www.instructables.com/id/The-ULTIMATE-RetroPie-41-Raspberry-Pi-Setup-Tutori/)
[How to Set Up RetroPie on Raspberry Pi 4 (or earlier) | Tom's Hardware](https://www.tomshardware.com/amp/how-to/install-retropie-raspberry-pi-4)
[RetroPie: Build your own Raspberry Pi retro gaming rig - howchoo](https://howchoo.com/g/n2qyzdk5zdm/build-your-own-raspberry-pi-retro-gaming-rig)
[How to Configure RetroPie and Install ROMs - YouTube](https://www.youtube.com/watch?v=HZFxSqXCx34)
[The Raspberry Pi Has Revolutionized Emulation](https://blog.codinghorror.com/the-raspberry-pi-has-revolutionized-emulation/)

[Web Browser On Emulation Station ! - RetroPie Forum](https://retropie.org.uk/forum/topic/3410/web-browser-on-emulation-station/10)
[zerojay/RetroPie-Extra: A collection of unofficial scripts for adding more emulators/ports/games to RetroPie.](https://github.com/zerojay/RetroPie-Extra)

[First Installation - RetroPie Docs](https://retropie.org.uk/docs/First-Installation/#transferring-roms)
[Running ROMs from a USB drive - RetroPie Docs](https://retropie.org.uk/docs/Running-ROMs-from-a-USB-drive/)
[How to Add Roms To RetroPie - YouTube](https://www.youtube.com/watch?v=f8_2Ij3b9iw) with Samba using IP, or `\\retropie`  
when prompted for password, use user `root` and password `pi`

#### Scraper

[Scraper - RetroPie Docs](https://retropie.github.io/RetroPie-Docs/Scraper/)

[sselph/scraper: A scraper for EmulationStation written in Go using hashing](https://github.com/sselph/scraper)
[How to Scrape Using Sselph Scraper: Tutorial with Command Examples - RetroPie Forum](https://retropie.org.uk/forum/topic/4227/how-to-scrape-using-sselph-scraper-tutorial-with-command-examples)

[Skraper](https://www.skraper.net/)
[SCREENSCRAPER - Base de données et téléchargement médias pour front-end gaming multi-systèmes](https://screenscraper.fr/index.php?action=changelangue&langue=en&gameid=0&plateforme=0)

### Streaming

> see `pc-games.md#streaming`

[Steam Link now available on Raspberry Pi :: Steam Link Raspberry Pi](https://steamcommunity.com/app/353380/discussions/6/2806204039992195182/)
[Steam Link Raspberry Pi Troubleshooting :: Steam Link Raspberry Pi](https://steamcommunity.com/app/353380/discussions/6/1743354432807054634/)
[Steam Link Raspberry Pi :: Steam Community](https://steamcommunity.com/app/353380/discussions/6/)
[Raspberry Pi Steam Link | Sam Brooks](https://sambrooks.net/raspberry-pi-steam-link/)
[How to Use a Raspberry Pi and Steam Link to Stream PC Games to Your TV | PCMag.com](https://www.pcmag.com/feature/370997/how-to-use-a-raspberry-pi-and-steam-link-to-stream-pc-games)

[How to Stream Steam Games to Raspberry Pi Without Moonlight](https://www.makeuseof.com/tag/stream-steam-games-raspberry-pi-diy-link-box/) with Parsec
[Setting Up On Raspberry Pi (Raspbian) – Parsec](https://support.parsecgaming.com/hc/en-us/articles/115002699012-Setting-Up-On-Raspberry-Pi-Raspbian-)
[How to Stream Any PC Game to TV Using a Raspberry Pi](https://www.makeuseof.com/tag/stream-pc-game-tv-raspberry-pi/) with Moonlight

### Native/Ports/Clones

[10+ Classic Games You Can Run on Raspberry Pi Without Emulators](https://www.makeuseof.com/tag/classic-games-raspberry-pi-without-emulators/)
[How to Run Doom on Your Raspberry Pi Without an Emulator](https://www.makeuseof.com/tag/run-doom-raspberry-pi/)
[STICKY: GAMES LIST: Games That Work On The Pi - Raspberry Pi Forums](https://www.raspberrypi.org/forums/viewtopic.php?t=51794)

## USB 3 Storage

[UASP makes Raspberry Pi 4 disk IO 50% faster | Jeff Geerling](https://www.jeffgeerling.com/blog/2020/uasp-makes-raspberry-pi-4-disk-io-50-faster)
[Faster USB Disk IO For Raspberry Pi | Tom's Hardware](https://www.tomshardware.com/amp/news/faster-usb-disk-io-for-raspberry-pi)
[Raspberry Pi 4 With an SSD: Dramatic Speed Improvements, Higher Price](https://www.tomshardware.co.uk/raspberry-pi-4-ssd-test,news-61094.html)

## NAS

[Build a Raspberry Pi NAS — The MagPi magazine](https://magpi.raspberrypi.org/articles/build-a-raspberry-pi-nas)

## CV/AI

> see "artificial-intelligence.md#edge-ai"

[piwheels - Home](https://www.piwheels.org/)

[pip install opencv - PyImageSearch](https://www.pyimagesearch.com/2018/09/19/pip-install-opencv/) object classification
[Raspberry Pi Face Recognition - PyImageSearch](https://www.pyimagesearch.com/2018/06/25/raspberry-pi-face-recognition/)
[Object detection with Raspberry Pi and Python - Data Driven Investor - Medium](https://medium.com/datadriveninvestor/object-detection-with-raspberry-pi-and-python-bc6b3a1d4972)
[Real Time Face Detection on the RaspberryPi-4: 6 Steps](https://www.instructables.com/id/Real-Time-Face-Detection-on-the-RaspberryPi-4/)

## Development

[How to Get Started With Rust on Raspberry Pi](https://www.makeuseof.com/tag/getting-started-rust-raspberry-pi/)

## Projects

[Pi My Life Up - 101+ DIY Raspberry Pi Projects & Guides](https://pimylifeup.com/)
[Projects | Raspberry Pi Projects](https://projects.raspberrypi.org/en/projects/)

[Best Raspberry Pi Projects for Kids](https://www.electromaker.io/blog/article/best-raspberry-pi-projects-for-kids)
[15 Practical Raspberry Pi Projects | Open Electronics](https://www.open-electronics.org/15-practical-raspberry-pi-projects/)
[Top 10 Raspberry Pi Projects for Beginners](https://lifehacker.com/top-10-raspberry-pi-projects-for-beginners-1791002723)
[Ten More Awesome Projects for Your Raspberry Pi](https://lifehacker.com/ten-more-awesome-projects-for-your-raspberry-pi-5978871)
[25 Raspberry Pi Projects Anyone Can Follow [2019]](https://itsfoss.com/raspberry-pi-projects/)

[Education - Training, resources, programmes and events](https://www.raspberrypi.org/education/)

[AWShome - Home automation using RPi + Alexa + IoT - Hackster.io](https://www.hackster.io/awshome/awshome-home-automation-using-rpi-alexa-iot-a3d3dc)
[How to Use Raspberry Pi as a VPN Gateway - Tom's Hardware](https://www.tomshardware.com/reviews/raspberry-pi-vpn-gateway,6103.html)

[GoPiGo Beginner Starter Kit: the Raspberry Pi Robot Car](https://www.dexterindustries.com/shop/gopigo-beginner-starter-kit/)

[Raspberry Pi Motion Detector with Photo Capture | Random Nerd Tutorials](https://randomnerdtutorials.com/raspberry-pi-motion-detector-photo-capture/)
[CCTV Raspberry Pi Based System with Storage using MotionEyeOS | Random Nerd Tutorials](https://randomnerdtutorials.com/cctv-raspberry-pi-based-system-storage-motioneyeos/)

[Build a car computer 'carputer' with Raspberry Pi - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/build-car-computer-raspberry-pi/)
[How to Build an Android TV Box With a Raspberry Pi](https://www.makeuseof.com/tag/build-android-tv-box-raspberry-pi/)

[Wiki | Raspberry Pi Dramble](https://www.pidramble.com/wiki) RPi Cluster

[Home Assistant - Home Assistant](https://www.home-assistant.io/hassio/)
[Installing Home Assistant - Home Assistant](https://www.home-assistant.io/hassio/installation/)
