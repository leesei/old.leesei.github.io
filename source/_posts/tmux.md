---
title: "Tmux"
date: 2014-12-11 17:59:04
categories:
- app
tags:
- shell-tool
- tmux
- tmuxifier
toc: true
---

[tmux](http://tmux.github.io/) is a terminal multiplexer, which creates windows (tab) and panels (split in a tab) in a single terminal. The session lives in the server so you can restore your session even if you were disconnected from the server.

[rothgar/awesome-tmux: A list of awesome resources for tmux](https://github.com/rothgar/awesome-tmux)
[tmux-plugins/tpm: Tmux Plugin Manager](https://github.com/tmux-plugins/tpm)

[Terminal Multiplexers: Screen, Tmux - Hyperpolyglot](http://hyperpolyglot.org/multiplexers)
[A Gentle Introduction to tmux – Hacker Noon](https://hackernoon.com/a-gentle-introduction-to-tmux-8d784c404340)
[A minimalist guide to tmux – Actualize – Medium](https://medium.com/actualize-network/a-minimalist-guide-to-tmux-13675fb160fa)
[tmux-plugins/tmux-sensible: basic tmux settings everyone can agree on](https://github.com/tmux-plugins/tmux-sensible)

<!-- more -->

## Troubleshooting

### tmux not loading bashrc 

tmux includes `.bash_profile`/`.profile` but not `.bashrc`

You can add this line to `.bash_profile`/`.profile`:

```sh
$echo case $- in *i*) . ~/.bashrc;; esac >> .bash_profile 
```

## reference

http://www.openbsd.org/cgi-bin/man.cgi?query=tmux
https://wiki.archlinux.org/index.php/tmux
https://markmcb.com/2016/05/23/tmux-introduction-configuration-boot-time-setup/
http://www.rdegges.com/tools-i-use-tmux/
http://mutelight.org/practical-tmux
http://robots.thoughtbot.com/a-tmux-crash-course
http://tangosource.com/blog/a-tmux-crash-course-tips-and-tweaks/
http://blog.hawkhost.com/2010/06/28/tmux-the-terminal-multiplexer/
http://blog.hawkhost.com/2010/07/02/tmux-%E2%80%93-the-terminal-multiplexer-part-2/
[screen - Send command to all window in tmux - Stack Overflow](http://stackoverflow.com/questions/9250884/send-command-to-all-window-in-tmux)

## key bindings/cheatsheet

[dayid's screen and tmux cheat sheet](http://www.dayid.org/os/notes/tm.html)
[tmux cheatsheet](https://gist.github.com/andreyvit/2921703)
[tmux cheatsheet](https://gist.github.com/henrik/1967800)
[Tmux Quick Reference & Cheat sheet - 2 column format for less scrolling!](https://gist.github.com/afair/3489752)
[tmux shortcuts & cheatsheet](https://gist.github.com/MohamedAlaa/2961058)

## theme

[jimeh/tmux-themepack: A pack of various Tmux themes.](https://github.com/jimeh/tmux-themepack)

## .tmux.conf

https://gist.github.com/snuggs/800936/raw
http://files.floriancrouzat.net/dotfiles/.tmux.conf
https://gist.github.com/napcs/1147532
http://justinlilly.com/dotfiles/tmux.html
http://zanshin.net/2013/09/05/my-tmux-configuration/
http://tonkersten.com/2011/07/104-switching-to-tmux/
[tmux Tutorial](http://blog.victorquinn.com/tmux-tutorial)
[docwhat/homedir-tmux: Configuration and tools to make working with TMux easier](https://github.com/docwhat/homedir-tmux)

[jimeh/tmux-themepack](https://github.com/jimeh/tmux-themepack)

`bind -n (-n: no prefix)`

### my `.tmux.conf`

```sh
#!rcfile for tmux

# ---------------------
# SERVER OPTIONS
# ---------------------
# shorten command delay
# not available in old version (1.1)
set -sg escape-time 50
# ---------------------
# SERVER OPTIONS
# ---------------------

# ---------------------
# WINDOW OPTIONS
# ---------------------
# causes tmux to resize a window based on the smallest client actually
# viewing it, not on the smallest one attached to the entire session.
setw -g aggressive-resize on

# 1-based index
setw -g pane-base-index 1

# utf8 support
setw -g utf8 on
# ---------------------
# WINDOW OPTIONS
# ---------------------

# ---------------------
# Copy & Paste
# ---------------------
# emacs selection key (^+space) conflicts with gcin
setw -g mode-keys vi
# add 'y'ank binding
# bind-key -t vi-copy y copy-pipe "reattach-to-user-namespace xclip -selection clipboard"
# default 'Enter' also pipe to clipboard
# unbind -t vi-copy Enter
# bind-key -t vi-copy Enter copy-pipe "reattach-to-user-namespace xclip -selection clipboard"
# ---------------------
# Copy & Paste
# ---------------------

# set shell
#set -g default-shell /usr/bin/zsh

# 1-based index
set -g base-index 1

# fixes most rendering issues
# gnome-terminal needs to export TERM=screen-256color, or use `tmux -2`
set -g default-terminal "screen-256color"

# default is 2000
set -g history-limit 100000

# highlight active pane
# not available in old version (1.1)
set -g pane-active-border-bg default
set -g pane-active-border-fg red
set -g pane-border-bg default
set -g pane-border-fg cyan
set -g display-panes-colour red

# do not renumber other windows when a window is closed in a session
set -g renumber-windows off

# sane scrolling
set -g terminal-overrides 'xterm*:smcup@:rmcup@'

# ---------------------
# MOUSE MODE
# ---------------------
# !! this interferes with mouse selection !!
# setw -g mode-mouse copy-mode
# set -g mouse-resize-pane on
# set -g mouse-select-pane on
# set -g mouse-select-window on
# set -g mouse-utf8 on
# ---------------------
# MOUSE MODE
# ---------------------

# ---------------------
# TITLE
# ---------------------
set -g set-titles on
# #T is very long
set -g set-titles-string '#S:#I:#P [#W]'
# ---------------------
# TITLE
# ---------------------

# ---------------------
# STATUS BAR
# ---------------------
# Reference for color:
# http://misc.flogisoft.com/bash/tip_colors_and_formatting
#
set -g status on
set -g status-utf8 on

# colors
set -g status-bg green
set -g status-fg black

## Left side of status bar, hostname and the session number
set -g status-left-length 20
#set -g status-left '#[fg=green][#[bg=black,fg=cyan]#S#[bg=black,fg=blue,dim]:#H#[fg=green]]'
set -g status-left ' #[fg=cyan,bright]#10H#[fg=green]:#[fg=white]#S#[default] | '

## Right side of status bar, date time
set -g status-right '| #[fg=yellow,bright]%y-%m-%d %H:%M '

## Middle of status bar, window list
set -g status-justify centre
# Inactive windows in status bar
#setw -g window-status-format '#[fg=cyan,dim]#I#[fg=blue]:#[default]#W#[fg=grey,dim]#F'
# Current or active window in status bar
#setw -g window-status-current-format '#[bg=blue,fg=cyan,bold]#I#[bg=blue,fg=cyan]:#[fg=white]#W#[fg=dim]#F'
# Alerted window in status bar. Windows which have an alert (bell, activity or content).
# setw -g window-status-alert-fg red
# setw -g window-status-alert-bg white

# TMUX_COLOUR_BORDER="colour237"
# TMUX_COLOUR_ACTIVE="colour231"
# TMUX_COLOUR_INACTIVE="colour16"
# not available in old version
# setw -g window-status-activity-bg $TMUX_COLOUR_BORDER
# setw -g window-status-activity-fg $TMUX_COLOUR_ACTIVE
# remove formatting
# setw -g window-status-current-format "#I:#W"
# setw -g window-status-format "#[fg=$TMUX_COLOUR_INACTIVE]#I:#W#F"
setw -g window-status-current-attr italics

setw -g monitor-activity on
setw -g window-status-activity-attr blink
# ---------------------
# STATUS BAR
# ---------------------

# ---------------------
# KEY BINDINGS
# ---------------------
# change key binding to ctrl+z, not the send-prefix for nested session
# set -g prefix C-z
# unbind-key C-b
# bind-key z send-prefix

# quit tmux
unbind-key C-q         ; bind-key C-q kill-session

# reload config
unbind-key r           ; bind-key r source-file ~/.tmux.conf\; display-message "Config reloaded"

# logging
unbind-key -n M-l      ; bind-key -n M-l pipe-pane "exec cat >>$HOME/'#W-tmux.log'" \; display-message 'Started logging to $HOME/#W-tmux.log'
unbind-key l           ; bind-key l pipe-pane \; display-message 'Ended logging to $HOME/#W-tmux.log'

# promt for a hostname
unbind-key S           ; bind-key S command-prompt -p ssh: "new-window -n %1 'ssh %1'"

# easier split window
unbind-key h           ; bind-key h split-window -h
unbind-key v           ; bind-key v split-window -v

# set up resize-pane keys
unbind-key -           ; bind-key - resize-pane -U 3
unbind-key +           ; bind-key + resize-pane -D 3
unbind-key /           ; bind-key / resize-pane -L 3
unbind-key *           ; bind-key * resize-pane -R 3
# unbind-key -n M-z      ; bind-key -n M-z   resize-pane -Z

# pane selection
unbind-key -n M-q      ; bind-key -n M-q   select-pane -t :.+

# window selection, alt+N, alt+page{up,down}
unbind-key -n M-1      ; bind-key -n M-1   select-window -t 1
unbind-key -n M-2      ; bind-key -n M-2   select-window -t 2
unbind-key -n M-3      ; bind-key -n M-3   select-window -t 3
unbind-key -n M-4      ; bind-key -n M-4   select-window -t 4
unbind-key -n M-5      ; bind-key -n M-5   select-window -t 5
unbind-key -n M-6      ; bind-key -n M-6   select-window -t 6
unbind-key -n M-7      ; bind-key -n M-7   select-window -t 7
unbind-key -n M-8      ; bind-key -n M-8   select-window -t 8
unbind-key -n M-9      ; bind-key -n M-9   select-window -t 9
unbind-key -n M-0      ; bind-key -n M-0   select-window -t 10
unbind-key -n M-Pageup ; bind-key -n M-Pageup previous-window
unbind-key -n M-PageDown ; bind-key -n M-PageDown next-window

# move window
unbind-key -n C-S-Left ; bind-key -n C-S-Left swap-window -t -1
unbind-key -n C-S-Right ; bind-key -n C-S-Right swap-window -t +1
# ---------------------
# KEY BINDINGS
# ---------------------
```

## Session Management

[Tmux scripting | Htbaa blogs?](https://blog.htbaa.com/news/tmux-scripting)
Simple script:

```sh
#!/bin/sh

SESSION=${0##*/}  # use file name as session name
SESSION=${SESSION%.*}  # remove 1 extension

tmux has-session -t ${SESSION} || {
    # create session if not exist
    tmux new-session -d -s ${SESSION}

    # reuse the first window
    tmux rename-window 'server'
    tmux send-keys 'ssh user@server' 'C-m'
    # this can be executed on server if using passwordless login
    tmux send-keys 'free' 'C-m'

    # `-c` cannot expand `~/`
    tmux new-window -n 'wip' -c "${HOME}/wip"

    tmux new-window -n 'project'
    # can use shell expansion here
    tmux send-keys 'cd ~/project' 'C-m'

    tmux select-window -t ${SESSION}:server
}
tmux -2 attach-session -t ${SESSION}
```

[iasj/IniTmux: Initializer for Tmux](https://github.com/iasj/IniTmux) requires Python
[tmuxinator/tmuxinator: Manage complex tmux sessions easily](https://github.com/tmuxinator/tmuxinator) requires Ruby

### tmuxifier

[jimeh/tmuxifier](https://github.com/jimeh/tmuxifier) allows you to define layout files (in `~/.tmuxifier-layouts` by default) in plain Bash scripts.

```sh
git clone https://github.com/jimeh/tmuxifier.git ~/.tmuxifier
```
