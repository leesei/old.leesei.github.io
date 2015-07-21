title: Trackball
categories:
  - comp.hardware
toc: true
date: 2015-06-15 12:47:32
tags:
- logitech
- adesso
- kensington
- sanwa
---

[Trackball - Wikiwand](http://www.wikiwand.com/en/Trackball)
[軌跡球不死！10款軌跡球介紹，羅技、Kensington、SANWA 登場 | T客邦 - 我只推薦好東西](http://www.techbang.com/posts/11369-trackball-does-not-die-8-trackball-kensington-introduced-logitech-trackball)
[轨迹球_淘宝搜索](http://s.taobao.com/search?q=轨迹球)
[Kensington Expert Mouse Trackball Review - All Things Ergo Blog](http://allthingsergo.com/blog/reviews/kensington-expert-mouse-trackball/)
[Advantages & Disadvantages of a Trackball | eHow](http://www.ehow.com/facts_7579911_advantages-disadvantages-trackball.html)

[TrackballWorld](http://www.trackballworld.com/)
[Deskthority wiki](http://deskthority.net/wiki/Main_Page)

<!-- more -->

## [Logitech Trackman Marble](http://www.logitech.com/en-ca/product/trackman-marble)

This is the first trackball I bought in Nov 2011.

Pros:
- cheap, < HK$200
- finger-operated
- hence symmetric design, can be used with both hands [1]

Cons:
- **no scroll**
- button is fragile, misfires or fails altogether

I setup key 3 as middle key, and emulate scroll wheel by holding it and moving the trackball.
But this setup puts stress to my thumb, so I look for trackball with hardware scroll.
[Logitech M570 Wireless Trackball](http://www.logitech.com/en-ca/product/wireless-trackball-m570) was not considered for being wireless and thumb-operated. 

### Linux setting

[Logitech_Marblemouse_USB - Community Help Wiki](https://help.ubuntu.com/community/Logitech_Marblemouse_USB)
[Logitech Marble Mouse - ArchWiki](https://wiki.archlinux.org/index.php/Logitech_Marble_Mouse)

Put this file in `locate xorg.conf.d | grep d$`:

```
# - - - Logitech Marble Mouse Settings - - -
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

### Windows setting

[Scroll modifier for mouse/trackball in windows - Super User](http://superuser.com/questions/498198/scroll-modifier-for-mouse-trackball-in-windows)
~~[Marble Mouse Scroll Wheel](http://simans.net/marble/)~~ (dead), home for `marbleinst.exe`
[MarbleScroll for Logitech Trackman Marble – Primož's Few Projects](http://www.fewprojects.com/marblescroll-for-logitech-trackman-marble/)
[X-Mouse Button Control](http://www.highrez.co.uk/downloads/XMouseButtonControl.htm)

fn1. with little practice, one can actually use any pointing device with both hands

## [Adesso iMouse T1](http://www.adesso.com/products/product-detail-137.html)

I got this thingy from [Taobao](http://s.taobao.com/search?&q=adesso+T1). Turns out it copied the design of [Sanwa MA-TB41](http://direct.sanwa.co.jp/ItemPage/MA-TB41S).

It has a scroll wheel on the left hand side of the device. It wasn't bulked outwards enough so it cannot be reached by the thumb when you are using the trackball naturally. And pressing middle button is difficult and quite often trigger scroll.

Pros:
- cheap, < HK$250
- finger-operated
- with scroll wheel

Cons:
- scroll wheel is hard to reach, thumb movement needed
- scroll wheel is too close to the trackball, usually have to bent thumb to reach the wheel
- pressing middle button will trigger scroll, and vice versa

### Linux setting

```sh
xinput --get-feedbacks "Trackball Mouse"
xinput --list-props "Trackball Mouse"

xinput --set-ptr-feedback "Trackball Mouse" 10 5 10
# Evdev Wheel Emulation Inertia (285):    30
```

```
# for 800dpi Adesso iMouse T1 trackball

Section "InputClass"
    Identifier "Trackball Mouse"
    MatchUSBID "195d:1009"
    MatchIsPointer "yes"

# set the following to 1 1 0 respectively to disable acceleration.
# trigger acceleration of 2 after 5 units
    Option "AccelerationThreshold" "7"
    Option "AccelerationNumerator" "1"
    Option "AccelerationDenominator" "2"

# some curved deceleration
    Option "AdaptiveDeceleration" "1"
# linear deceleration (mouse speed reduction)
    Option "ConstantDeceleration" "1"
EndSection
```

## [Kensington SlimBlade](http://www.kensington.com/us/hk/4493/k72327us/slimblade™-trackball)

Then I turned to the one in consumer market who still innovates in trackballs: Kensington.

[Hands-on: the Kensington Slimblade trackball | Ars Technica](http://arstechnica.com/gadgets/2010/09/hands-on-kensington-slimblade-trackball/)

[Trackballs | Trackball Mouse | Wireless Mouse - Kensington - Kensington](http://www.trackballworks.com)

Pros:
- dual laser sensors
- hence can scroll by twisting the trackball
- finger-operated

Cons:
- expensive, official price at HK$1000, HK$600 at [Taobao](http://s.taobao.com/search?q=Kensington+k72327)

[Orbit Scroll Ring](http://www.kensington.com/en/sa/4493/k72337eu/orbit™-scroll-ring-trackball) was not considered for having only two buttons. Middle button is crucial for me.
[Orbit Wireless Mobile](http://www.kensington.com/us/hk/4493/k72352us/orbit™-wireless-mobile-trackball) was not considered for being too small and wireless, but that may be a reason for you to choose it.
The tilting angle for [Expert Mouse](http://www.kensington.com/en/sa/4493/64325/expert-mouse-optical-trackball) is too high. It seems that it would cause wrist pain for prolonged usage.

### Linux setting

[kensington slimblade trackball linux - Google Search](https://www.google.com.hk/search?espv=2&biw=1147&bih=672&q=kensington+slimblade+trackball+linux&oq=kensington+trackball+slimblade+lin&gs_l=serp.3.0.0i22i30l2.25137.26212.0.27205.4.4.0.0.0.0.104.387.3j1.4.0....0...1c.1.64.serp..0.4.384.oka5IK0BCl4)
[Living and Programming - YJPark's Blog: Using Trackball on Linux](http://yjpark.blogspot.com/2010/04/using-trackball-on-linux.html)

```sh
# enable wheel emulation
xinput set-int-prop "Kensington Kensington Slimblade Trackball" "Evdev Wheel Emulation" 8 1

# use button 8 (upper right button) as the emulation button 
xinput set-int-prop "Kensington Kensington Slimblade Trackball" "Evdev Wheel Emulation Button" 8 8

# use for vertical and horizontal scrolling
xinput set-int-prop "Kensington Kensington Slimblade Trackball" "Evdev Wheel Emulation Axes" 8 6, 7, 4, 5

# button 8 don't work as "back"
xinput set-button-map "Kensington Kensington Slimblade Trackball" 1 2 3 4 5 6 7 10 9 8 11 12

# wheel emulation by toggling, not holding
# requires driver patch
xinput set-int-prop "Kensington Kensington Slimblade Trackball" "Evdev Wheel Emulation Button Toggle" 8 1
```

## Honorable Mentions

[优鼠 手握式轨迹球](http://s.taobao.com/search?q=%E8%BD%A8%E8%BF%B9%E7%90%83&cps=yes&ppath=20000%3A6094839)
[日本三和 轨迹球](http://s.taobao.com/search?q=轨迹球&cps=yes&ppath=20000%3A13003727)
[価格.com - タイプ:トラックボール サンワサプライ(SANWA SUPPLY)のマウス](http://kakaku.com/pc/mouse/itemlist.aspx?pdf_ma=345&pdf_Spec101=4)

## Linux X configs

[evdev - man page](https://www.mankier.com/4/evdev)
[vmmouse - man page](https://www.mankier.com/4/vmmouse)
[mousedrv(4) - Special file - Linux man page](https://www.mankier.com/4/mousedrv)
[xorg.conf - man page](https://www.mankier.com/5/xorg.conf)

[xinput - man page](https://www.mankier.com/1/xinput)
[xev - man page](https://www.mankier.com/1/xev)
[imwheel - ArchWiki](https://wiki.archlinux.org/index.php/Imwheel)
[Manpage of IMWheel](http://imwheel.sourceforge.net/imwheel.1.html)

### buttons

[ManyButtonsMouseHowto - Community Help Wiki](https://help.ubuntu.com/community/ManyButtonsMouseHowto)
[All Mouse Buttons Working - ArchWiki](https://wiki.archlinux.org/index.php/All_Mouse_Buttons_Working)
[Remapping mouse buttons :: wiki.mbirth.de](http://wiki.mbirth.de/know-how/software/linux/remapping-mouse-buttons.html)

1 2    : L/R button
3      : Middle button
4 5 6 7: scroll down/up/left/right
8 9    : back/forward

### scroll wheel

[Bug #124440 “[enhancement] Ubuntu needs a way to set mouse scrol...” : Bugs : GTK+](https://bugs.launchpad.net/gtk/+bug/124440)
[[ubuntu] Scroll (wheel) speed, mouse acceleration, threshold, sensivity - Page 2](http://ubuntuforums.org/showthread.php?t=1179448&page=2&p=10406312#post10406312)

### smooth scrolling

[Who-T: What's new in XI 2.1 - smooth scrolling](http://who-t.blogspot.de/2011/09/whats-new-in-xi-21-smooth-scrolling.html)
[Why no smooth scrolling on Linux? : linux](http://www.reddit.com/r/linux/comments/2qd564/why_no_smooth_scrolling_on_linux/)
[Does no one care about smooth scrolling? : elementaryos](http://www.reddit.com/r/elementaryos/comments/29pvtz/does_no_one_care_about_smooth_scrolling/)
[958868 – Support true smooth scrolling on X11/Linux with XInput 2.1](https://bugzilla.mozilla.org/show_bug.cgi?id=958868)

### acceleration

[Mouse acceleration - ArchWiki](https://wiki.archlinux.org/index.php/Mouse_acceleration)
[Lowering Mouse Sensitivity in Ubuntu and Fedora](https://patrickmn.com/blog/lowering-gaming-mouse-sensitivity-in-ubuntu-9-10/)
[High DPI mice and Linux / Kernel & Hardware / Arch Linux Forums](https://bbs.archlinux.org/viewtopic.php?id=104742)

