title: "Linux setup"
date: 2015-01-23 13:47:38
categories:
- linux
tags:
- desktop
toc: true
---

Arch Linux has IMO the best Linux [wiki](https://www.archlinux.org/).
Most of the Linux tricks can be found there.

<!-- more -->

> add [linux-installs.md](https://gist.github.com/leesei/65bf019431fc418f8ce3) here

## Distros

> explains Linux desktop architecture
> bootloader, X, Mir, desktop environment, package manager

## Bootable USB key

Creating a bootable USB key in Linux is [stright forward](https://wiki.archlinux.org/index.php/USB_flash_installation_media).

```
dd if=[iso] of=[usb device] bs=4M
```

Note [some utils](http://antergos.com/wiki/article/create-a-working-live-usb/) modify the partition lable of the ISO, that can cause problem during bootup.

- UNetbootin
- Linux Live USB Creator
- Universal USB Installer
- Live USB Creator
- [Rufus - Create bootable USB drives the easy way](https://rufus.akeo.ie/)

## Marbele Mouse

[Logitech_Marblemouse_USB - Community Help Wiki](https://help.ubuntu.com/community/Logitech_Marblemouse_USB)
[Logitech Marble Mouse - ArchWiki](https://wiki.archlinux.org/index.php/Logitech_Marble_Mouse)

```
# - - - Logitech Marble Mouse Settings - - -
#
# put this file in `locate xorg.conf.d | grep d$`
#
# For the sake of comments below, a Logitech Marble Mouse has buttons
# labeled from left to right: A (large), B, C, D (large).

# Preferred options for right-handed usage are:
# Left to right: A=1,normal click B=2,middle-click C=2,middle-click D=3,right-click
# Press button B (hold button while rolling trackball) to emulate wheel-scrolling.

# Preferred options for left-handed usage (saying 'alternate-click' instead of 'right click'):
# Left to right: A=3,alternate-click B=2,middle-click C=2,middle-click D=1,normal click
# Press button C (hold button while rolling trackball) to emulate wheel-scrolling.

# The trackball can scroll in two-axes, unlike a typical wheel mouse. Adjust the
# settings to constrain the scroll action to vertical-axis-only if you prefer.

# Pressing both large buttons simultaneously (b) produces a "back" action (=8). Finally,
# pressing and holding button B while rolling the trackball emulates wheel-rolling action.

Section "InputClass"
    Identifier "Marble Mouse"
    MatchProduct "Logitech USB Trackball"
    MatchIsPointer "on"
    MatchDevicePath "/dev/input/event*"
    Driver "evdev"

    # Physical button #s: A b D - - - - B C b = A & D simultaneously; - = no button
    Option "ButtonMapping" "1 8 3 4 5 6 7 2 2"
    # Option "ButtonMapping" "1 8 3 4 5 6 7 2 2" # For right-hand placement
    # Option "ButtonMapping" "3 8 1 4 5 6 7 2 2" # For left-hand placement

    # EmulateWheel refers to emulating a mouse wheel using Marble Mouse trackball.
    Option "EmulateWheel" "true"
    # Option "EmulateWheelButton" "8" # Factory default; use "9" for left-side placement.
    Option "EmulateWheelButton" "8"
    # Option "ZAxisMapping" "4 5"
    Option "ZAxisMapping" "4 5"
    # Option "XAxisMapping" "6 7" # Disable this for vertical-only scrolling.
    Option "XAxisMapping" "6 7"
    # Emulate3Buttons refers to the act of pressing buttons A and D
    # simultaneously to emulate a middle-click or wheel click.
    Option "Emulate3Buttons" "true"
EndSection
```

## Adesso iMouse T1

https://wiki.archlinux.org/index.php/Mouse_acceleration
http://www.x.org/archive/X11R7.7/doc/man/man5/xorg.conf.5.xhtml
http://www.x.org/archive/X11R7.7/doc/man/man4/mousedrv.4.xhtml

```
# for 800dpi Adesso iMouse T1 trackball

Section "InputClass"
    Identifier "Trackball Mouse"
    MatchUSBID "195d:1009"
    MatchIsPointer "yes"

# set the following to 1 1 0 respectively to disable acceleration.
# trigger acceleration of 2 after 5 units
    Option "AccelerationNumerator" "2"
    Option "AccelerationDenominator" "1"
    Option "AccelerationThreshold" "5"

# some curved deceleration
#   Option "AdaptiveDeceleration" "1"
# linear deceleration (mouse speed reduction)
    Option "ConstantDeceleration" "2"

EndSection
```

## XBox360 gamepad

### Wired gamepad

Wired XBox360 pad should work out of the box using `xpad` driver

### Wireless gamepad (using `xboxdrv`)

http://pingus.seul.org/~grumbel/xboxdrv/

```bash
sudo add-apt-repository ppa:grumbel/ppa
sudo apt-get update
sudo apt-get install xboxdrv
```

```bash
xboxdrv -L
xboxdrv --daemon
```

http://pingus.seul.org/~grumbel/xboxdrv/xboxdrv.html

[Xbox360Controller - Community Help Wiki](https://help.ubuntu.com/community/Xbox360Controller)
