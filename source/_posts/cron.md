---
title: "Cron"
date: 2015-01-14 12:48:30
categories:
- app
tags:
- shell-tool
- cron
- anacron
toc: true
---

## cron

[Learning Cron by Example](http://www.marksanborn.net/linux/learning-cron-by-example/)
[Linux Crontab: 15 Awesome Cron Job Examples](http://www.thegeekstuff.com/2009/06/15-practical-crontab-examples/)
[A visual crontab editor - create your custom crontab syntax to use with the cron scheduling application on your Linux server](http://www.corntab.com/pages/crontab-gui)

```sh
# view our crontab entries without editing them
crontab -l

# view our crontab entries without editing them
crontab -e

# specify user
crontabl -u user

# remove your crontab file and start fresh
crontab -r   ## !! dangerous !!
crontab -ri

# load from file
# !! current crontab entries will be overwritten !!
crontab file
```

```
# min hour dom month dow command
30 8-18/2 * * 1-5 ./path/to/backup_wiki.sh
# Minutes [0-59]
# Hour [0-23]
# Day of Month [1-31]
# Month [1-12] - January is 1, obviously
# Day of Week [0-7] - Sunday is 0 or 7
# Command to run (can have spaces)
```

When you specify */5 in minute field means every 5 minutes.
When you specify 0-10/2 in minute field mean every 2 minutes in the first 10 minute.
Thus the above convention can be used for all the other 4 fields.

```
# use bash
SHELL=/bin/bash

# m h  dom mon dow   command

# show env of cron shell
#* * * * * env > /tmp/cron-env.output

# backup crontab every Monday
0 13 * * 1 crontab -l > ${HOME}/crobtab.bak
```

Logs for `cron` can usually be found in `/var/log/cron.log` or `/var/log/messages`

## anacron

[Cron Vs Anacron: How to Setup Anacron on Linux (With an Example)](http://www.thegeekstuff.com/2011/05/anacron-examples/)

`anacron` is for PCs that are not running 24*7.
