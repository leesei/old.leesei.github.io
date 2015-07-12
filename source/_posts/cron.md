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

# remove your crontab file and start fresh
crontab -r   ## !! dangerous !!
```

```
#min hour dom month dow command
30 8-18/2 * * 1-5 ./path/to/backup_wiki.sh
# Minutes [0-59]
# Hour [0-23]
# Day of Month [1-31]
# Month [1-12] - January is 1, obviously
# Day of Week [0-6] - Sunday is 0
# Command to run (can have spaces)
```

Logs for `cron` can usually be found in `/var/log/cron.log` or `/var/log/messages`

## anacron

[Cron Vs Anacron: How to Setup Anacron on Linux (With an Example)](http://www.thegeekstuff.com/2011/05/anacron-examples/)

anacron is for PCs that are not running 24*7.
