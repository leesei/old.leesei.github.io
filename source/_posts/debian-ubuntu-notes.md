title: Debian/Ubuntu notes
toc: true
date: 2014-12-08 13:04:28
categories:
- linux
tags:
- debian
- ubuntu
- desktop
- package-manager
- notes
---

[The Debian Administrator's Handbook](http://debian-handbook.info/browse/stable/)
[Ubuntu Desktop Guide](https://help.ubuntu.com/lts/ubuntu-help/index.html)
[CommunityHelpWiki - Community Help Wiki](https://help.ubuntu.com/community/CommunityHelpWiki)

<!-- more -->

## Package managers

[What is the difference between dpkg and aptitude/apt-get? - Ask Ubuntu](http://askubuntu.com/questions/309113/what-is-the-difference-between-dpkg-and-aptitude-apt-get)
[6.4. Frontends: aptitude, synaptic](http://debian-handbook.info/browse/stable/sect.apt-frontends.html)

list upgrades: `apt-get -s upgrade`

list installed: `aptitude search '~i!~M'`

[apt - How to list all installed packages? - Ask Ubuntu](http://askubuntu.com/questions/17823/how-to-list-all-installed-packages)

[Ubuntu Apps Directory](https://apps.ubuntu.com/cat/)

### repo source

```sh
inxi -r
cat /etc/apt/sources.list
ls /etc/apt/sources.list.d
```

## Init

### Debian/LSB-compliant

[LSB Referenced Specifications](http://refspecs.linuxfoundation.org/lsb.shtml)

https://github.com/Fleshgrinder/nginx-sysvinit-script  
https://github.com/JasonGiedymin/nginx-init-ubuntu  

```sh
$ sudo update-rc.d --help
update-rc.d: error: --help
usage: update-rc.d [-n] [-f] <basename> remove
       update-rc.d [-n] <basename> defaults [NN | SS KK]
       update-rc.d [-n] <basename> disable|enable [S|2|3|4|5]
        -n: not really
        -f: force
```

```sh
sudo update-rc.d -f nginx remove
sudo update-rc.d nginx defaults
sudo service nginx status
sudo service nginx start
sudo service nginx stop
```

### Ubuntu

Use `upstart` instead of `init.d` for Ubuntu:  
http://casear.chuto.tw/2013/05/31/upstart-setting-for-nginx-on-ubuntu/  
http://casear.chuto.tw/2013/05/31/upstart-setting-for-redis-on-ubuntu/

## Hacker setup

http://niftylettuce.com/posts/linux-mint-ubuntu-nodejs-hacker-setup/

## Timezone

```sh
$ date
Thu Mar 21 18:02:49 MST 2012
$ more /etc/timezone
US/Arizona

$ sudo dpkg-reconfigure tzdata
```

> http://www.christopherirish.com/2012/03/21/how-to-set-the-timezone-on-ubuntu-server/
