title: Windows Manager
date: 2014-12-12 11:43:59
categories:
- linux
tags:
- shell-tool
- desktop
- wmctrl
- window-tiling
- x
- windows-manager
toc: true
---

[Window manager - ArchWiki](https://wiki.archlinux.org/index.php/Window_Manager)

## Window Tiling

Package       | Remark
--------      | -------
[gTile][]     | With UI, need [patch](https://github.com/shuairan/gTile/pull/16) for Cinnamon 1.8.8, close on [escape](https://github.com/shuairan/gTile/issues/2)
[QuickTile][] | no UI
[xtile][]     |
[ctrlwm][]    |
[pytyle3][]   |
[wumwum][]    |
See also [WinSplit Revolution][] (Windows), [Divvy][] (Mac).

[gTile]: https://github.com/shuairan/gTile
[QuickTile]: https://github.com/ssokolow/quicktile
[xtile]: http://www.giuspen.com/x-tile/
[ctrlwm]: http://gtk-apps.org/content/show.php/ctrlwm?content=114565
[wmctrl]: http://tomas.styblo.name/wmctrl/
[pytyle3]: https://github.com/BurntSushi/pytyle3
[wumwum]: http://wumwum.sourceforge.net/
[WinSplit Revolution]: http://winsplit-revolution.com/screenshots
[Divvy]: http://alternativeto.net/software/divvy/

## `wmctrl`

http://tomas.styblo.name/wmctrl/
http://linux.die.net/man/1/wmctrl
http://spiralofhope.com/wmctrl-examples.html
http://www.linuxjournal.com/magazine/hack-and-automate-your-desktop-wmctrl
http://ubuntuforums.org/showthread.php?t=1282386

[stiler](https://github.com/TheWanderer/stiler/tree/grid), [forum](https://bbs.archlinux.org/viewtopic.php?id=64100)

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

## X stuffs

http://linux.die.net/man/1/xprop
[Extended Window Manager Hints](http://standards.freedesktop.org/wm-spec/wm-spec-latest.html)

[X and ModeLines](http://howto-pages.org/ModeLines/)

## UI stack

[Xplain](http://magcius.github.io/xplain/article/)
[The Linux Graphics Stack | Clean Rinse](http://blog.mecheye.net/2012/06/the-linux-graphics-stack/)
[Wayland](http://wayland.freedesktop.org/)
