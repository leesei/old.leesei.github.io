---
title: "Window Manager"
date: 2014-12-12 11:43:59
categories:
  - linux
tags:
  - shell-tool
  - desktop
  - wmctrl
  - window-tiling
  - x11
  - windows-manager
toc: true
---

[Window manager - ArchWiki](https://wiki.archlinux.org/index.php/Window_Manager)
[Window manager - Wikiwand](https://www.wikiwand.com/en/Window_manager)
[Dynamic window manager - Wikiwand](https://www.wikiwand.com/en/Dynamic_window_manager)
[Extended Window Manager Hints](http://standards.freedesktop.org/wm-spec/wm-spec-latest.html)

[How-to: Picking a Window Manager in Linux](http://www.engadget.com/2012/10/30/how-to-picking-a-window-manager-linux/)
[What are the best window managers for Linux? - Slant](https://www.slant.co/topics/390/~window-managers-for-linux)

[Adding Glue To a Desktop Environment](https://venam.nixers.net/blog/unix/2019/01/07/win-automation.html)

[Way Cooler](http://way-cooler.org/) awesomewm on Wayland, Rust, with Lua integrated

## Tiling WM

[10 Best Tiling Window Managers for Linux](https://www.tecmint.com/best-tiling-window-managers-for-linux/amp/)

[i3 - improved tiling wm](https://i3wm.org/)
[i3: i3 User’s Guide](https://i3wm.org/docs/userguide.html)

[baskerville/bspwm: A tiling window manager based on binary space partitioning](https://github.com/baskerville/bspwm)
[https://stumpwm.github.io](https://stumpwm.github.io/)
[conformal/spectrwm: A small dynamic tiling window manager for X11.](https://github.com/conformal/spectrwm)
[Bluetile - full-featured tiling for the GNOME desktop environment](https://bluetile.org/)
[xmonad | the tiling window manager that rocks](http://xmonad.org/) Haskell
[Qtile – A hackable tiling window manager written in Python | Qtile.org](http://www.qtile.org/)

['Material Shell' is an Impressive Tiling GNOME Shell Extension - OMG! Ubuntu!](https://www.omgubuntu.co.uk/2019/07/material-shell-tiling-gnome-shell-extension/amp)

[Sway](http://swaywm.org/) i3 on Wayland
[Sway - A Tiling Wayland i3-Compatible Compositor](https://www.fossmint.com/sway-a-tiling-wayland-i3-compatible-compositor/)

## awesome window manager

[awesome window manager](https://awesomewm.org/) Lua

[My first Awesome](https://awesomewm.org/apidoc/documentation/07-my-first-awesome.md.html)
[Default configuration file documentation](https://awesomewm.org/doc/api/documentation/05-awesomerc.md.html)
[awesome API documentation](https://awesomewm.org/doc/api/)

## Window Tiling on X

| Package       | Remark       |
| ------------- | ------------ |
| [gTile][]     | For Cinnomon |
| [xtile][]     |
| [ctrlwm][]    |
| [PyGrid][]    |
| [pytyle3][]   |
| [QuickTile][] | no UI        |
| [wumwum][]    |

See also [WinSplit Revolution][] (Windows), [Divvy][] (Mac).

[gtile]: https://github.com/shuairan/gTile
[quicktile]: https://github.com/ssokolow/quicktile
[xtile]: http://www.giuspen.com/x-tile/
[ctrlwm]: http://gtk-apps.org/content/show.php/ctrlwm?content=114565
[wmctrl]: http://tomas.styblo.name/wmctrl/
[pygrid]: https://github.com/pkkid/pygrid
[pytyle3]: https://github.com/BurntSushi/pytyle3
[wumwum]: http://wumwum.sourceforge.net/
[winsplit revolution]: http://winsplit-revolution.com/screenshots
[divvy]: http://alternativeto.net/software/divvy/

## `wmctrl`

[wmctrl - man page - ManKier](https://www.mankier.com/1/wmctrl)
http://tomas.styblo.name/wmctrl/
http://spiralofhope.com/wmctrl-examples.html
http://www.linuxjournal.com/magazine/hack-and-automate-your-desktop-wmctrl
http://ubuntuforums.org/showthread.php?t=1282386

[stiler](https://github.com/TheWanderer/stiler/tree/grid), [forum](https://bbs.archlinux.org/viewtopic.php?id=64100)

[Tiling in XFCE | Sjaak van den Berg](https://svdb.co/articles/2015/07/19/tiling-in-xfce/)

```sh
#!/bin/sh

# Single window to 66% width
set -- $(xwininfo -root| awk -F '[ :]+' '/ (Width|Height):/ { print $3 }')
width=$1
height=$2

wmctrl -r :ACTIVE: -e 0,0,0,$((width*2/3)),$height
```

```sh
#!/bin/sh

# Two windows each to 50% width
set -- $(xwininfo -root| awk -F '[ :]+' '/ (Width|Height):/ { print $3 }')
width=$1
height=$2

win1=$(xwininfo| awk '/^xwininfo: W/ { print $4 }')
win2=$(xwininfo| awk '/^xwininfo: W/ { print $4 }')

wmctrl -i -r $win1 -e 0,0,0,$((width/2)),$height
wmctrl -i -r $win2 -e 0,$((width/2)),0,$((width/2)),$height
```

## Node X11 interface

[sidorares/node-x11](https://github.com/sidorares/node-x11/)
[AirWM/AirWM](https://github.com/AirWM/AirWM)
[Airblader/node-tinywm](https://github.com/Airblader/node-tinywm)
[anko/basedwm](https://github.com/anko/basedwm)
[bu/OdieWM](https://github.com/bu/OdieWM)
[dominictarr/tiles](https://github.com/dominictarr/tiles)
[santigimeno/node-ewmh](https://github.com/santigimeno/node-ewmh)

## Python X11 interface

[BurntSushi/xpyb: A clone of xorg-xpyb.](https://github.com/BurntSushi/xpyb) inactive
[tych0/xcffib: A drop-in replacement for xpyb based on cffi](https://github.com/tych0/xcffib#installation)
