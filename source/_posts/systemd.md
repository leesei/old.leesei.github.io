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

[Rethinking PID 1](http://0pointer.de/blog/projects/systemd.html)
[The Biggest Myths](http://0pointer.de/blog/projects/the-biggest-myths.html) by author of `systemd`

[Meet systemd, the controversial project taking over a Linux distro near you | PCWorld](http://www.pcworld.com/article/2841873/meet-systemd-the-controversial-project-taking-over-a-linux-distro-near-you.html)
[How To Use Systemctl to Manage Systemd Services and Units | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units)
[Systemd Essentials: Working with Services, Units, and the Journal | DigitalOcean](https://www.digitalocean.com/community/tutorials/systemd-essentials-working-with-services-units-and-the-journal)
[media.ccc.de - systemd in 2018](https://media.ccc.de/v/ASG2018-230-systemd_in_2018/oembed)

System services are written in `.service` files, located in:
`/usr/lib/systemd/system` (enabled) and `/usr/lib/systemd/system/` (available).

This is what `systemctl enable teamviewerd` does:

```sh
ln -s '/usr/lib/systemd/system/teamviewerd.service' '/etc/systemd/system/graphical.target.wants/teamviewerd.service'
```

`/etc/systemd/system/display-manager.service` symlinks to the DM (or `plymouth` wrapper).

[Archlinux, systemd-free](http://systemd-free.org/)

`systemd-ui`

[systemctl command man page - systemd | ManKier](https://www.mankier.com/1/systemctl)
[systemd-analyze command man page - systemd | ManKier](https://www.mankier.com/1/systemd-analyze)

```
systemd-analyze blame | head -5
```

[Running Node.js on Linux with systemd - via @codeship | via @codeship](https://blog.codeship.com/running-node-js-linux-systemd/)

Docker service example:

```
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

## systemctl

`systemctl` - List active services in system

`systemctl list-unit-files` - List all services in system

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
# reverse logs
journalctl -r
# follow journal
journalctl -f
# filter to `docker` service
journalctl -u
```

## Binding

[torfsen/python-systemd-tutorial: A tutorial for writing a systemd service in Python](https://github.com/torfsen/python-systemd-tutorial)
