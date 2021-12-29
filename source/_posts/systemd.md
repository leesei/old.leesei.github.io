---
title: systemd
categories:
  - linux
tags:
  - desktop
toc: true
date: 2017-01-05 11:18:07
---

[systemd - Wikiwand](http://www.wikiwand.com/en/Systemd)
[systemd - freedesktop.org](http://www.freedesktop.org/wiki/Software/systemd/)
[systemd - ArchWiki](https://wiki.archlinux.org/index.php/systemd)
[systemd - Debian Wiki](https://wiki.debian.org/systemd)
[TipsAndTricks](http://www.freedesktop.org/wiki/Software/systemd/TipsAndTricks/)
[systemd.index](https://www.freedesktop.org/software/systemd/man/index.html)

[Rethinking PID 1](http://0pointer.de/blog/projects/systemd.html)
[The Biggest Myths](http://0pointer.de/blog/projects/the-biggest-myths.html) by author of `systemd`
[EWONTFIX - Broken by design: systemd](http://ewontfix.com/14/)

[Meet systemd, the controversial project taking over a Linux distro near you | PCWorld](http://www.pcworld.com/article/2841873/meet-systemd-the-controversial-project-taking-over-a-linux-distro-near-you.html)
[How To Use Systemctl to Manage Systemd Services and Units | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units)
[Systemd Essentials: Working with Services, Units, and the Journal | DigitalOcean](https://www.digitalocean.com/community/tutorials/systemd-essentials-working-with-services-units-and-the-journal)
[media.ccc.de - systemd in 2018](https://media.ccc.de/v/ASG2018-230-systemd_in_2018/oembed)

[Archlinux, systemd-free](http://systemd-free.org/)

## Unit files

Unit files are compiled to C code for faster bootup time.
`man 5 systemd.unit`, `systemctl cat <unit>`
`systemctl list-unit-files` - List all services in system

System services are written in unit files, located in:

- `/lib/systemd/system` (system, installed by package manager, read only)
- `/usr/lib/systemd/system/` (system, installed by package manager, read only)
- `/etc/systemd/system/` (custom, overrides `/usr`)
- `/run/systemd/system/` (temporary)

Drop-in unit file:
`/etc/systemd/system/httpd.service.d/myconf.conf`
`systemctl edit --full <service.unit>`

This is what `systemctl enable teamviewerd` does:

```sh
ln -s '/usr/lib/systemd/system/teamviewerd.service' '/etc/systemd/system/multi-user.target.wants/teamviewerd.service'
```

### Service units

[Running Node.js on Linux with systemd - via @codeship | via @codeship](https://blog.codeship.com/running-node-js-linux-systemd/)
[How to Run a Linux Program at Startup with systemd](https://www.howtogeek.com/687970/how-to-run-a-linux-program-at-startup-with-systemd/amp/)

!! Remember to `systemctl enable <service>` after adding service file. !!

[therootcompany/serviceman: Cross-platform service management for Mac, Linux, and Windows.](https://github.com/therootcompany/serviceman)
[Serviceman | webinstall.dev](https://webinstall.dev/serviceman/)

```sh
sudo env PATH="$PATH" \
    serviceman add --system --username $(whoami) --name caddy -- \
        caddy run --config ./Caddyfile
```

Docker service example:

```ini
[Unit]
Description=Redis container
Requires=docker.service
After=docker.service

[Service]
Restart=always
ExecStart=/usr/bin/docker start -a redis_server
ExecStop=/usr/bin/docker stop -t 2 redis_server

[Install]
WantedBy=local.target
```

```ini
# /etc/systemd/system/docker-compose-gogs.service

[Unit]
Description=Gogs Service (Docker Compose)
Requires=docker.service
After=docker.service

[Service]
Type=oneshot
RemainAfterExit=yes
WorkingDirectory=/home/git/gogs
ExecStart=/usr/local/bin/docker-compose up -d
ExecStop=/usr/local/bin/docker-compose down
TimeoutStartSec=10

[Install]
WantedBy=multi-user.target
```

### Timer units

`man 5 systemd.timer`
`man 7 systemd.time`
`systemctl list-timers` list all timers in system
`systemd-run --on-active=1m <cmd>` one shot timer

```ini
# timer.timer
[Unit]
Description=Timer to kick off timer service

[Timer]
# monotonic, every N seconds
OnBootSec=
OnUnitActiveSrc=

# realtime, akin to cron
OnCalendar=
Persistent=true # run on boot if last timer is missed

Unit= # unit name

[Install]
WantedBy=timer.target # run service of the same name by default
```

## systemd container

`systemd-nspawn`

1. place OS tree in /var/lib/machines/<container name>

```sh
machinectl pull-raw --verify=checksum <URL>
# set container root password
systemd-nspawn -D /var/lib/machines/<container name>
```

2. `systemd-nspawn -M <container name>`
3. `machinectl enable <container name>` or `systemctl enable systemd-nspawn@<container name>`

## systemctl

[systemctl command man page - systemd | ManKier](https://www.mankier.com/1/systemctl)

`systemctl` - List active services in system

`systemctl --all` - List all services in system

`systemctl start SERVICE.service` - Use it to start a service. Does not persist after reboot

`systemctl stop SERVICE.service` - Use it to stop a service. Does not persist after reboot

`systemctl restart SERVICE.service` - Use it to restart a service

`systemctl reload SERVICE.service` - If the service supports it, it will reload the config files related to it without interrupting any process that is using the service.

`systemctl status SERVICE.service` - Shows the status of a serviceTells whether a service is currently running.

`systemctl enable SERVICE.service` - Turns the service on, on the next reboot or on the next start event. It persists after reboot.

`systemctl disable SERVICE.service` - Turns the service off on the next reboot or on the next stop event. It persists after reboot.

`systemctl is-enabled SERVICE.service` - Check if a service is currently configured to start or not on the next reboot.

`systemctl is-active SERVICE.service` - Check if a service is currently active.

`systemctl show SERVICE.service` - Show all the information about the service.

`systemctl daemon-reload`: rewrite and reload all dependencies.

## tools

[systemd-cgls](https://www.freedesktop.org/software/systemd/man/systemd-cgls.html)

`systemd-ui`

[systemd-analyze command man page - systemd | ManKier](https://www.mankier.com/1/systemd-analyze) analyse boot time

```
systemd-analyze blame | head -5
```

systemd specific locale and timezone:
`localectl`
`timedatectl`

`hostnamectl`: `set-location`

`systemd-inhibit`: run command with suspending

## Lennart Poettering

[Why systemd?](http://0pointer.de/blog/projects/why.html)
[The Biggest Myths](http://0pointer.de/blog/projects/the-biggest-myths.html)
[systemd journal](https://docs.google.com/document/pub?id=1IC9yOXj7j6cdLLxWEBAGRL6wl97tFxgjLUEHIX3MSTs)

## systemd for Developers

[systemd for Developers I](http://0pointer.net/blog/projects/socket-activation.html)
[systemd for Developers II](http://0pointer.net/blog/projects/socket-activation2.html)
[systemd for Developers III](http://0pointer.net/blog/projects/journal-submit.html)

## systemd for Administrators

> TODO:
> http://0pointer.net/blog/archives.html
> select "systemd for Administrators" and generate links

[systemd for Administrators, Part 1](http://0pointer.net/blog/projects/systemd-for-admins-1.html)
[systemd for Administrators, Part II](http://0pointer.net/blog/projects/systemd-for-admins-2.html)
[systemd for Administrators, Part III](http://0pointer.net/blog/projects/systemd-for-admins-3.html)
....
[systemd For Administrators, Part XXI](http://0pointer.net/blog/systemd-for-administrators-part-xxi.html)

## journalctl

[journalctl command man page - systemd | ManKier](https://www.mankier.com/1/journalctl)
[journalctl](https://www.freedesktop.org/software/systemd/man/journalctl.html)
[journalctl: Query the systemd Journal | Reference | openSUSE Leap 42.3](https://doc.opensuse.org/documentation/leap/reference/html/book.opensuse.reference/cha.journalctl.html)
[Displaying Linux Log files with journalctl](http://landoflinux.com/linux_journalctl_examples.html)
[Using journalctl -The Ultimate Guide to Logging](https://www.loggly.com/ultimate-guide/using-journalctl/)
[How To Use Journalctl to View and Manipulate Systemd Logs | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs)

```sh
# clean logs
journalctl --disk-usage
sudo journalctl --vacuum-size=500M
```

```sh
# jump to end
journalctl -e
# show only this boot
journalctl -b
# reverse logs
journalctl -r
# follow journal
journalctl -f
# time filtering `--since` and `--until`
journalctl --since "2019-09-25 15:00"
# filter to `docker` service
journalctl -u docker.service
# add entry to journal
echo "here" | systemd-cat

# kernel logs (akin to dmesg)
journalctl -k

# formatting output
# man 7 system.journal-fields
journalctl -o verbose
journalctl -o json-pretty
```

## Binding

[python-systemd package — python-systemd documentation](https://www.freedesktop.org/software/systemd/python-systemd/)
[torfsen/python-systemd-tutorial: A tutorial for writing a systemd service in Python](https://github.com/torfsen/python-systemd-tutorial)
