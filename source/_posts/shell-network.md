---
title: "Shell Tools (Network)"
categories:
  - app
toc: true
date: 2015-09-15 13:55:34
tags:
- netcat
- nmap
- netstat
---

Network related shell tools

## Nmap

[Nmap: the Network Mapper - Free Security Scanner](https://nmap.org/)

## netcat

http://nc110.sourceforge.net/
http://www.catonmat.net/blog/unix-utilities-netcat/
http://blog.hawkhost.com/2009/12/12/using-netcat-as-an-intercepting-proxy/
http://www.g-loaded.eu/2006/11/06/netcat-a-couple-of-useful-examples/

## netstat

```sh
# list listening TCP ports
netstat -antlp
lsof -i udp:24000
lsof -i tcp:80
```

[oh-my-zsh/systemadmin.plugin.zsh at master · robbyrussell/oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh/blob/master/plugins/systemadmin/systemadmin.plugin.zsh)
