title: "Linux Desktop"
date: 2014-12-12 16:06:50
categories:
- linux
tags:
- desktop
- xinput
- xdg-utils
- gjs
toc: true
---

This post is about using GNU/Linux with [desktop environment](http://www.wikiwand.com/en/Desktop_environment) for daily use.

[Main Linux problems on the desktop, 2015 edition](http://linuxfonts.narod.ru/why.linux.is.not.ready.for.the.desktop.current.html)

[Getting Started with Linux: The Complete Guide](http://lifehacker.com/5778882/getting-started-with-linux-the-complete-guide)
[Introduction to Linux](http://www.tldp.org/LDP/intro-linux/html/index.html)
[The Linux System Administrator's Guide](http://www.tldp.org/LDP/sag/html/index.html)
[The UNIX Hater's Handbook](http://web.mit.edu/~simsong/www/ugh.pdf) (PDF)

## GNU and Linux

To distinguish GNU and Linux, and why it is not "correct" to say Linux system, read: [Linux and GNU](http://www.gnu.org/gnu/linux-and-gnu.html) and 
[GNU/Linux FAQ](http://www.gnu.org/gnu/gnu-linux-faq.html#why)

[GNU Userland | Linux.org](http://www.linux.org/threads/gnu-userland.7429/)
[List of GNU packages - Wikiwand](http://www.wikiwand.com/en/List_of_GNU_packages)
[GNU-Binutils | Linux.org](http://www.linux.org/threads/gnu-binutils.6544/)
[GNU Toolchain Explained | Linux.org](http://www.linux.org/threads/gnu-toolchain-explained.6469/)

[Stephen Bourne: Early days of Unix and design of sh - YouTube](https://www.youtube.com/watch?v=2kEJoWfobpA)

## Distros

[Linux distribution - Wikiwand](http://www.wikiwand.com/en/Linux_distribution)
[List of Linux distributions - Wikiwand](http://www.wikiwand.com/en/List_of_Linux_distributions)
[GNU/Linux Distribution Timeline](http://upload.wikimedia.org/wikipedia/commons/1/1b/Linux_Distribution_Timeline.svg)
Well, Android is also a [Linux distro](http://www.linux.org/threads/android-and-its-derivatives.6145/) with its own forks.

[DistroWatch.com: Put the fun back into computing. Use Linux, BSD.](http://distrowatch.com/)

### Check distro

```sh
cat /etc/issue
cat /etc/lsb-release
```

[Linux Command: Show Linux Version](http://www.cyberciti.biz/faq/command-to-show-linux-version/)
[Commands to check the Linux Version, Release name & Kernel version. | Symantec Connect](http://www.symantec.com/connect/articles/commands-check-linux-version-release-name-kernel-version)

### Check system install time

[How do I find how long ago a Linux system was installed? - Unix & Linux Stack Exchange](http://unix.stackexchange.com/questions/9971/how-do-i-find-how-long-ago-a-linux-system-was-installed)

We need several tools:  
- `df` to look up the device path of `/`  
- `tune2fs` to query the file system's info  
- GNU tools for command line magic ;-)

**Vanilla commands**

    $ df /
    Filesystem      Size  Used Avail Use% Mounted on
    /dev/sdb3       184G   18G  164G  10% /
    $ sudo tune2fs -l /dev/sdb3
    ...
    <fs info>
    Filesystem created:       Tue Aug 25 18:15:09 2015
    <fs info>
    ...

**Apply command line magic**

    $ sudo tune2fs -l $(df / | sed -n '2 p' | cut -d' ' -f1) | grep 'Filesystem created:'
    Filesystem created:       Tue Aug 25 18:15:09 2015

## Resources

[The Linux Documentation Project](http://www.tldp.org/)
[Beyond Linux® From Scratch](http://www.linuxfromscratch.org/blfs/view/svn/index.html)
[Linux and Life ~ daily Linux - Ubuntu news, reviews and tutorials](http://www.linuxandlife.com/)
[Tyrant's Arch Linux](http://arch.acgtyrant.com/)
[iTech - 博客园](http://www.cnblogs.com/itech/)

<!-- more -->

## Desktop Environment

> explains Linux desktop architecture
> bootloader, X, Mir, desktop environment, package manager

[WTF Desktop Environments: GNOME, KDE, and More Explained](http://lifehacker.com/5762081/wtf-desktop-environments-gnome-kde-and-more-explained)
[A Guide to Window Managers and Desktops for Unix and Linux](http://www.techopedia.com/2/28684/software/operating-systems/a-guide-to-window-managers-and-desktops-for-unix-and-linux)
[How-to: Picking a desktop environment in Linux](http://www.engadget.com/2012/11/30/how-to-pick-a-desktop-environment-in-linux/)

[Desktop environment - ArchWiki](https://wiki.archlinux.org/index.php/Desktop_environment)
[Display manager - ArchWiki](https://wiki.archlinux.org/index.php/Display_manager)
[Comparison of X Window System desktop environments - Wikiwand](http://www.wikiwand.com/en/Comparison_of_X_Window_System_desktop_environments)
[X Window System - Wikiwand](http://www.wikiwand.com/en/X_Window_System)
[AIGLX - Wikiwand](http://www.wikiwand.com/en/AIGLX)

[A Memory Comparison of Light Linux Desktops | l3net – a layer 3 networking blog](https://l3net.wordpress.com/2013/03/17/a-memory-comparison-of-light-linux-desktops/)
[A Memory Comparison of Light Linux Desktops – Part 2 | l3net – a layer 3 networking blog](https://l3net.wordpress.com/2013/04/09/a-memory-comparison-of-light-linux-desktops-part-2/)
[A Memory Comparison of Light Linux Desktops – Part 3 | l3net – a layer 3 networking blog](https://l3net.wordpress.com/2014/02/15/a-memory-comparison-of-light-linux-desktops-part-3/)

[字體及其渲染 | Tyrant's Arch Linux](http://arch.acgtyrant.com/2015/01/03/Fonts-and-its-rendering/)

## Display Manager

Upon login the Display Manager allows a user can choose the session (DE) to login to.
The available sessions are in `/usr/share/xsessions/`.

## Boot

> TODO: link to boot.md

## File Systems

> TODO: link to file-systems.md

## Kernel

[Linux Inside](http://0xax.gitbooks.io/linux-insides/content/)
[Linux Kernel in a Nutshell](http://www.kroah.com/lkn/)

## Freezes

[Bug #159356 “System freeze on high memory usage” : Bugs : linux package : Ubuntu](https://bugs.launchpad.net/ubuntu/+source/linux/+bug/159356)

Some suggested adding this to `/etc/rc.local`:
```
sysctl vm.vfs_cache_pressure=100000
```

## Microcode

[Microcode - ArchWiki](https://wiki.archlinux.org/index.php/Microcode)
[Microcode - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Microcode)

## `man` pages

Manpages are written in roff/mandoc/mdoc languages.
There are tools to convert Markdown to manpages:
- [Ronn](https://rtomayko.github.io/ronn/)
- [md2man](http://sunaku.github.io/md2man/man/man0/README.html)
- [Mantastic - manpage generator and manager](http://mantastic.herokuapp.com/)

It's [recommended](http://askubuntu.com/questions/244809/how-do-i-manually-install-a-man-page) to install manpage to `/usr/local/share/man/man[0-9]`.
It is [save](http://apple.stackexchange.com/questions/1393/are-my-permissions-for-usr-local-correct) to `sudo chown -R $(whoami) /usr/local` for single person machine.

```sh
sudo cp examplecommand.1 /usr/local/share/man/man1/
sudo mandb
man 1 examplecommand
```

[Making Man Pages | Linux.org](http://www.linux.org/threads/making-man-pages.6601/)

## Clipboard

[ClipboardsWiki](http://www.freedesktop.org/wiki/Specifications/ClipboardsWiki/)
[Clipboard Access from the Command Line with xsel/xclip - TerminalMage dot NET](http://terminalmage.net/2011/10/18/clipboard-access-from-the-command-line.html)
[Command Line to Clipboard | Linuxtidbits](https://linuxtidbits.wordpress.com/2008/02/22/command-line-to-clipboard/)

X11 has not one, not two, but _three_ clipboards. They are called:

* **PRIMARY** - Also known as the "primary selection" or the "primary
clipboard". This clipboard is populated whenever you highlight text with the
mouse. If you've ever highlighted text and noticed that you can paste it by
clicking the middle button on your mouse, this is the clipboard being used.
* **SECONDARY** - This clipboard is very rarely used anymore, but exists to
provide a "secondary selection" clipboard to accompany the primary selection.
* **CLIPBOARD** - This is the clipboard you are likely most familiar with. It
is the one used when you copy text from an application such as a web browser,
or a GUI text editor like **gedit**.

## "Standards"

[freedesktop.org](http://www.freedesktop.org/wiki/)
[Specifications](http://www.freedesktop.org/wiki/Specifications/) or [here](
http://standards.freedesktop.org/)

[Linux Standard Base (LSB) | The Linux Foundation](http://www.linuxfoundation.org/collaborate/workgroups/lsb)
[Linux Standard Base (LSB) | Linux.org](http://www.linux.org/threads/linux-standard-base-lsb.5113/)
[Linux Standard Base - Wikiwand](https://www.wikiwand.com/en/Linux_Standard_Base)
[Linux Filesystem Hierarchy](http://www.tldp.org/LDP/Linux-Filesystem-Hierarchy/html/index.html)

[X org / Desktop | Linux.org](http://www.linux.org/forums/x-org-desktop.50/)

[xdg-utils](http://portland.freedesktop.org/xdg-utils-1.0/)

### File Hierarchy

[Filesystem Hierarchy Standard - Wikiwand](https://www.wikiwand.com/en/Filesystem_Hierarchy_Standard)

[What are those /dev/ Files? | Linux.org](http://www.linux.org/threads/what-are-those-dev-files.4713/)
[Procfs and the Proc Directory | Linux.org](http://www.linux.org/threads/procfs-and-the-proc-directory.4928/)
[Sysfs and Configfs | Linux.org](http://www.linux.org/threads/sysfs-and-configfs.4956/)

### Base Directory

[XDG Base Directory Specification](http://standards.freedesktop.org/basedir-spec/basedir-spec-latest.html)
[sindresorhus/xdg-basedir](https://github.com/sindresorhus/xdg-basedir)

### Desktop files

[Desktop Entry Specification](http://standards.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html)
[desktop-file-utils](http://www.freedesktop.org/wiki/Software/desktop-file-utils/)
[Desktop files: putting your application in the desktop menus](https://developer.gnome.org/integration-guide/stable/desktop-files.html.en)

#### `.desktop` folders

```
/usr/share/applications
/usr/local/share/applications
~/.local/share/applications
```

#### Autotools

[Autotools Mythbuster](https://autotools.io/index.html)

#### `pkg-config`

[pkg-config](http://www.freedesktop.org/wiki/Software/pkg-config/)
[Guide to pkg-config](http://people.freedesktop.org/~dbn/pkg-config-guide.html)
[pkg config - PKG_CONFIG_PATH environment variable - Ask Ubuntu](http://askubuntu.com/questions/210210/pkg-config-path-environment-variable)
```
pkg-config --variable pc_path pkg-config
```

### Autostart

[Desktop Application Autostart Specification](http://standards.freedesktop.org/autostart-spec/autostart-spec-latest.html)

```
/etc/xdg/autostart/
~/.config/autostart/
```

### File Association

[shared-mime-info-spec](http://www.freedesktop.org/wiki/Specifications/shared-mime-info-spec/)
[Association between MIME types and applications](http://standards.freedesktop.org/mime-apps-spec/mime-apps-spec-latest.html)
[Default applications - ArchWiki](https://wiki.archlinux.org/index.php/Default_applications)
[Create Your Own File Types in Ubuntu with assoGiate | Ubuntu Genius's Blog](https://ubuntugenius.wordpress.com/2009/11/19/create-your-own-file-types-in-ubuntu-with-assogiate/)
[mimeo](http://xyne.archlinux.ca/projects/mimeo/) can find `.desktop` and change association.
[march-linux/mimi](https://github.com/march-linux/mimi)
[File-Openers and Xdg-utils | Linux.org](http://www.linux.org/threads/file-openers-and-xdg-utils.6600/)

How to set `gpicview` to default image viewer? Use following command line:
```sh
xdg-mime default gpicview.desktop `grep 'MimeType=' /usr/share/applications/gpicview.desktop | sed -e 's/.*=//' -e 's/;/ /g'`
```

NOTE: [xdg-utils](http://portland.freedesktop.org/wiki/XdgUtils) is needed here. It's a tool released by Portland project of Freedesktop.org. Most modern Linux distros have this tool installed by default.

#### Open folder with

```sh
vi ~/.local/share/applications/mimeapps.list
```

Add this to `[Added Associations]`
```
inode/directory=sublime_text.desktop
```

### Icon theme

[Icon Theme Specification](http://standards.freedesktop.org/icon-theme-spec/icon-theme-spec-latest.html)
[Icon Naming Specification](http://standards.freedesktop.org/icon-naming-spec/icon-naming-spec-latest.html)

#### GNOME

[Icon Naming Specification](https://developer.gnome.org/icon-naming-spec/)
[GNOME Desktop icons - Wikimedia Commons](https://commons.wikimedia.org/wiki/GNOME_Desktop_icons)

```
/usr/share/themes
/usr/share/icons
```

## dconf

This is the "registry" for GNOME DE. It replaces the XML based gconf with binary database optimized for faster loop ups.

gconf => XML database
dconf = GSetting API => binary database

[Projects/dconf - GNOME Wiki!](https://wiki.gnome.org/action/show/Projects/dconf)
[dconf: dconf Reference Manual](https://developer.gnome.org/dconf/unstable/dconf-overview.html)
[dconf - Wikiwand](http://www.wikiwand.com/en/Dconf)

```sh
gsettings list-schemas
gsettings list-keys org.cinnamon.desktop.screensaver
gsettings set org.cinnamon.desktop.lockdown disable-lock-screen true
gsettings set org.cinnamon.desktop.lockdown disable-lock-screen false

dconf dump /org/cinnamon/desktop/screensaver/
dconf write /org/cinnamon/desktop/screensaver/lock-enabled false
```

[gsettings - What is dconf, what is its function, and how do I use it? - Ask Ubuntu](http://askubuntu.com/questions/22313/what-is-dconf-what-is-its-function-and-how-do-i-use-it)
[What are the differences between gconf and dconf? - Ask Ubuntu](http://askubuntu.com/questions/34490/what-are-the-differences-between-gconf-and-dconf)
[Gconf, Dconf, Gsettings and the relationship between them - Ask Ubuntu](http://askubuntu.com/questions/249887/gconf-dconf-gsettings-and-the-relationship-between-them)

## Font

[Fonts - ArchWiki](https://wiki.archlinux.org/index.php/fonts)
[Fixing Missing Characters and Font Issues | Linux.org](http://www.linux.org/threads/fixing-missing-characters-and-font-issues.7644/)
[GNU Unifont Glyphs](http://unifoundry.com/unifont.html)

[Hanazono fonts](http://fonts.jp/hanazono/)
[BabelStone Fonts : BabelStone Han](http://www.babelstone.co.uk/Fonts/Han.html)

[Debian 8 (jessie) 安裝筆記 中文環境篇 - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/31556973.html)

[I stared into the fontconfig, and the fontconfig stared back at me / fuzzy notepad](http://eev.ee/blog/2015/05/20/i-stared-into-the-fontconfig-and-the-fontconfig-stared-back-at-me/)

## `xinput`

```
xinput list
xinput test <id>/<name>
xinput list-props <id>/<name>
xinput set-prop <id>/<name> <prop id>/<prop name> <value>
```

Settings are put in:
- `/etc/X11/xorg.conf.d` (Arch)
- `/usr/share/X11/xorg.conf.d` (Debian)

Look up with `locate xorg.conf.d | grep d$`

## X stuffs

http://linux.die.net/man/1/xprop
[Extended Window Manager Hints](http://standards.freedesktop.org/wm-spec/wm-spec-latest.html)

[X and ModeLines](http://howto-pages.org/ModeLines/)

## UI stack

[Xplain](http://magcius.github.io/xplain/article/)
[The Linux Graphics Stack | Clean Rinse](http://blog.mecheye.net/2012/06/the-linux-graphics-stack/)
[Wayland](http://wayland.freedesktop.org/)

[X Window System - Wikiwand](http://www.wikiwand.com/en/X_Window_System)
[Display server - Wikiwand](http://www.wikiwand.com/en/Display_server)
[Windowing system - Wikiwand](http://www.wikiwand.com/en/Windowing_system)

[![Free and open-source-software display servers and UI toolkits.svg - Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7b/Free_and_open-source-software_display_servers_and_UI_toolkits.svg/1280px-Free_and_open-source-software_display_servers_and_UI_toolkits.svg.png)](https://en.wikipedia.org/wiki/File:Free_and_open-source-software_display_servers_and_UI_toolkits.svg)

My `~/.xsession`:

```sh
#!/bin/sh

#
# ~/.xsession
#
# Executed by xdm/gdm/kdm at login
#

/bin/bash --login -i ~/.xinitrc
```

My `~/.xinitrc`:

```sh
#!/bin/sh

#
# ~/.xinitrc
#
# Executed by startx (run your window manager from here)
#

exec cinnamon-session
```


## GNOME

[Projects-GObjectIntrospection - GNOME Wiki!](https://wiki.gnome.org/Projects/GObjectIntrospection)
[Projects-Vala - GNOME Wiki!](https://wiki.gnome.org/Projects/Vala/)

[Develop for the GNOME Platform](https://developer.gnome.org/platform-overview/stable/)
[Tutorials, code samples and platform demos in Python](https://developer.gnome.org/gnome-devel-demos/unstable/py.html.en)

[woGue](http://worldofgnome.org/)
[Making Fancy GNOME Apps with NodeJS, MongoDB and WebKit! | woGue](http://worldofgnome.org/making-fancy-gnome-apps-with-nodejs-mongodb-and-webkit/)
[Scaffolding a modern GNOME 3.10 Gtk Gjs-Python App! | woGue](http://worldofgnome.org/scaffolding-a-modern-gnome-3-10-gtkgjs-app/)

### Gjs

[Projects/Gjs - GNOME Wiki!](https://wiki.gnome.org/action/show/Projects/Gjs?action=show&redirect=Gjs)
[Tutorials, code samples and platform demos in JavaScript](https://developer.gnome.org/gnome-devel-demos/unstable/js.html.en)

[HowTo run commands from Gjs | woGue](http://worldofgnome.org/howto-run-commands-from-gjs/)

[石頭閒語:JavaScript分類文章簡文 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/cat_242544.html)
[JavaScript 與 Desktop - WebKit - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/14282187.html)
[JavaScript 與 Desktop - Desktop and WebKit - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/14456843.html)
[JavaScript 與 Desktop - DBus - 石頭閒語 - 樂多日誌](http://blog.roodo.com/rocksaying/archives/14229429.html)

## mount `.iso` without root

[Script: mountiso « IgnorantGuru's Blog](https://igurublog.wordpress.com/downloads/script-mountiso/)

[HOW TO: Allow Mounting Of ISO Files By A Regular User « IgnorantGuru's Blog](https://igurublog.wordpress.com/2011/01/22/how-to-allow-mounting-of-iso-files-by-a-regular-user/)

## Wine

[WineHQ - Run Windows applications on Linux, BSD, Solaris and Mac OS X](https://www.winehq.org/)
[轉子男: [Ubuntu] 使用 Wine 安裝 Office 2010 於 Ubuntu 12.04](http://open-rotorman.blogspot.com/2012/11/ubuntu-wine-office-2010-ubuntu-1204.html)
