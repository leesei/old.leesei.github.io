---
title: "Cinnamon setup"
date: 2015-05-04 13:23:07
categories:
  - linux
tags:
  - desktop
  - cinnamon
toc: true
---

## Settings

### "Font Selection"

Default Font: Noto Sans CJK HK Regular 10
Document Font: Noto Sans Regular 10
Document Font: Noto Sans Regular 11
Mono Font: Fira Code Regular 11
Window Title Font: Noto Sans CJK HK Black 10

Text scaling factor: 1.2
Hinting: Full

## "Themes"

[Spices : Cinnamon (Themes)](http://cinnamon-spices.linuxmint.com/themes)

`~/.themes/`

Windows borders: Arc-Dark
Icons: Arc-X-D
Controls: Arc-Dark
Mouse Pointer: Adwaita
Desktop: Arc-Dark

Also: Zukitwo for Mac-like feeling

Uncheck "Show icons in menus"
Uncheck "Show icons on buttons"

## "Applets"

[Spices : Cinnamon (Applets)](http://cinnamon-spices.linuxmint.com/applets)

`~/.local/share/cinnamon/applets/`

Upper panel (left-to-right):

- Menu
- Panel launchers
  - Chrome
  - Firefox
  - Terminal
- Spacer
- Multi-Core System Monitor
- Keyboard
- Display
- Notifications
- Sound/Sound With Apps Volume
- ScreenShot+Record Desktop
- Removable Drives
- Network Manager
- Calendar

Lower panel (left-to-right):

- Scale
- Expo
- Window List
- Force Quit/Force Quit II
- Workspace switcher

[Force Quit II](http://cinnamon-spices.linuxmint.com/applets/view/218) (white)
[Force Quit](http://cinnamon-spices.linuxmint.com/applets/view/4) (red)
[Multi-Core System Monitor](http://cinnamon-spices.linuxmint.com/applets/view/79)
[ScreenShot+Record Desktop](https://cinnamon-spices.linuxmint.com/applets/view/41)

### [Sound With Apps Volume](http://cinnamon-spices.linuxmint.com/applets/view/150)

Check "Volume 150%"
Uncheck "Mute with middle click"

### [Timer With Notifications](http://cinnamon-spices.linuxmint.com/applets/view/68)

### Calender

Check "Show week numbers"
Custom date format: "%Y-%m-%d (%a) | %H:%M"

### Menu

Check "Enable file system path in search box"

### Notification

Uncheck "Show empty tray"

## Date & Time

"Use 24h Clock": on
"Display the date": on
"Display Seconds": off
"First day of week": Monday

## "Desklets"

[Spices : Cinnamon (Desklets)](http://cinnamon-spices.linuxmint.com/desklets)

`~/.local/share/cinnamon/desklets/`

### Time and Date Desklets

```json
{
  "description": "A fork desklet that displays the time and date",
  "dateSize": "20pt",
  "dangerous": false,
  "dateFormat": "%A, %e %B",
  "name": "Time and Date Desklet",
  "timeSize": "50pt",
  "last-edited": "1371648230",
  "timeFormat": "%H:%M",
  "prevent-decorations": true,
  "uuid": "TimeAndDate@nightflame"
}
```

## "Extensions"

[Spices : Cinnamon (Extensions)](http://cinnamon-spices.linuxmint.com/extensions)

```sh
cinnamon-settings extensions
```

`~/.local/share/cinnamon/extensions/`

### gTile

<Super>space
2x2, 3x3, 4x3, 4x4
check "Auto-Close"
uncheck "Animation"

## "Panel"

2 Panels

## "Preferred Applications"

Google Chrome
Text Editor

### Settings

Lock when put to sleep
Lock when screen turn off
Don't ask for custom message

### Date

Use custom date and time format

## "Startup Applications"

Disable:

- EndeavourOS Update Notifier
- Desktop Sharing
- User folder update
- Zeitgeist Datahub

Add:

- Guake
- overGrive

## "Windows"

### Titlebar

Action on titlebar middle click: None

### Alt-Tab

Coverflow (3d)
off
delay 50ms

## "Keyboard" > "Keyboard Shortcuts"

Generally delete unused shortcuts.
Disable NumLock to use keypad keys.

```sh
gsettings list-schema org.cinnamon.desktop.keybindings.wm
dconf dump /org/cinnamon/desktop/keybindings/wm/
```

"General":

- "Show the window selection screen" (Scale): <kbd>Super</kbd>+<kbd>Q</kbd>
- "Show the workspace selection screen" (Expo): none
- "Show Desktop": <kbd>Super</kbd>+<kbd>D</kbd>
- "Cycle Windows Backwards": <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>Tab</kbd>
- "Cycle Same App": <kbd>Alt</kbd>+<kbd>\`</kbd>
- "Run": <kbd>Super</kbd>+<kbd>r</kbd>
- "Looking Glass": <kbd>Super</kbd>+<kbd>F12</kbd>

"Windows":

- "Minimize window": <kbd>Super</kbd>+<kbd>KP_1</kbd>
- "Toggle maximization state": <kbd>Super</kbd>+<kbd>KP_9</kbd>

"Window > Tiling and Snapping":

- "Push tile left": <kbd>Super</kbd>+<kbd>Left</kbd>
- "Push tile right": <kbd>Super</kbd>+<kbd>Right</kbd>
- "Push tile up": <kbd>Super</kbd>+<kbd>Up</kbd>
- "Push tile down": <kbd>Super</kbd>+<kbd>Down</kbd>
- "Push snap left": <kbd>Ctrl</kbd>+<kbd>Super</kbd>+<kbd>Left</kbd>
- "Push snap right": <kbd>Ctrl</kbd>+<kbd>Super</kbd>+<kbd>Right</kbd>
- "Push snap up": <kbd>Ctrl</kbd>+<kbd>Super</kbd>+<kbd>Up</kbd>
- "Push snap down": <kbd>Ctrl</kbd>+<kbd>Super</kbd>+<kbd>Down</kbd>

"Window > Inter-workspace":

- "Move window to left workspace": <kbd>Super</kbd>+<kbd>,</kbd>
- "Move window to right workspace": <kbd>Super</kbd>+<kbd>.</kbd>

"Window > Inter-workspace":

- "Move window to left monitor": <kbd>Shift</kbd>+<kbd>Super</kbd>+<kbd>Left</kbd>
- "Move window to right monitor": <kbd>Shift</kbd>+<kbd>Super</kbd>+<kbd>Right</kbd>
- "Move window to up monitor": <kbd>Shift</kbd>+<kbd>Super</kbd>+<kbd>Up</kbd>
- "Move window to down monitor": <kbd>Shift</kbd>+<kbd>Super</kbd>+<kbd>Down</kbd>

"Workspace > Direct Navigation":

- "Switch to workspace 1": <kbd>Super</kbd>+<kbd>1</kbd>
- "Switch to workspace 2": <kbd>Super</kbd>+<kbd>2</kbd>

"System":

- "Lock screen": <kbd>Super</kbd>+<kbd>L</kbd>

"System > Hardware":

- "Re-detect display devices": None

"System > Screenshots and Recordings":

- "Take a screenshot of an area": <kbd>Shift</kbd>+<kbd>Print</kbd>
- "Copy a screenshot of an area to clipblard": <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Print</kbd>
- "Take a screenshot": <kbd>Print</kbd>
- "Copy a screenshot to clipblard": <kbd>Ctrl</kbd>+<kbd>Print</kbd>
- "Take a screenshot of a window": <kbd>Alt</kbd>+<kbd>Print</kbd>
- "Copy a screenshot of a window to clipblard": <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Print</kbd>

"Launchers":

- "Launch terminal": <kbd>Super</kbd>+<<kbd>T</kbd>
- "WWW browser": <kbd>Homepage</kbd> (<kbd>Fn</kbd>+<kbd>F1</kbd>)
- "Home folder": <kbd>Super</kbd>+<kbd>E</kbd>

## Nemo

### "Views"

Default: "List View"
List View zoom: "66%"

### "Behavior"

Check "Ignore per-folder view preferences"
Automatically close when media unmounted

### "Display"

Date format: ISO
Check "Show full path"
Check "Show advanced permissions"

### "List Columns"

Check "Owner", "Permissions"

### "Preview"

Disable Text in icons
Show thumbnails for < 10MB
Enable tooltips

### "Toolbar"

Check "computer", "terminal"

## Debugging

Toggle Looking Glass with <kbd>Super</kbd>+<kbd>F12</kbd>
Looking Glass log: `~/.cinnamon/glass.log`
Xsession error: `~/.xsession-errors`
