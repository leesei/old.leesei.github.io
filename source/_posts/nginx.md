---
title: "Nginx"
date: 2014-12-11 17:57:51
categories:
- web
tags:
- nginx
- notes
toc: true
---

## References

[nginx documentation](http://nginx.org/en/docs/)
[Beginner’s Guide](http://nginx.org/en/docs/beginners_guide.html)
[NGINX and NGINX Plus Admin Guide | NGINX](https://www.nginx.com/resources/admin-guide/)

[nginx - ArchWiki](https://wiki.archlinux.org/index.php/Nginx)
[Nginx Community](http://wiki.nginx.org/Main)
[GettingStarted - Nginx Community](http://wiki.nginx.org/GettingStarted)
[Pitfalls - Nginx Community](http://wiki.nginx.org/Pitfalls)

[Nginx开发从入门到精通 — Nginx开发从入门到精通](http://tengine.taobao.org/book/index.html)
[agentzh's Nginx Tutorials](http://openresty.org/download/agentzh-nginx-tutorials-en.html) [download](http://openresty.org/#eBooks) [source](https://github.com/openresty/nginx-tutorials)
[cNginx Guide - Tuts+ Code Tutorials](http://code.tutsplus.com/series/cnginx-guide--cms-792)
[The Architecture of Open Source Applications (Volume 2): nginx](http://www.aosabook.org/en/nginx.html)

[Use Nginx + SPDY, without compiling Nginx and without a recent OpenSSL - Phusion Blog](http://old.blog.phusion.nl/2013/08/21/use-nginx-spdy-without-compiling-nginx-and-without-a-recent-openssl/)

[Nginx Secure SSL Web Server @ Calomel.org](https://calomel.org/nginx.html)

## vs Apache

[Nginx vs. Apache - Michael Lustfield](https://michael.lustfield.net/nginx/nginx-vs-apache)

## Configuration

> https://github.com/h5bp/server-configs-nginx  
> https://github.com/Umkus/nginx-boilerplate  
> https://github.com/perusio/nginx_ensite  

[Configuration - Nginx Community](http://wiki.nginx.org/Configuration)

[Core functionality](http://nginx.org/en/docs/ngx_core_module.html)
[Module ngx_http_core_module](http://nginx.org/en/docs/http/ngx_http_core_module.html)

[Serving Static Content | NGINX](https://www.nginx.com/resources/admin-guide/serving-static-content/)

[Nginx Configuration Primer](http://blog.martinfjordvald.com/2010/07/nginx-primer/)
[Nginx Primer 2: From Apache to Nginx](https://blog.martinfjordvald.com/2011/02/nginx-primer-2-from-apache-to-nginx/)
[Nginx Library](http://nginxlibrary.com/)
[Debugging Nginx Errors](https://blog.martinfjordvald.com/2013/06/debugging-nginx-errors/)
[Understanding the Nginx Configuration Inheritance Model](https://blog.martinfjordvald.com/2012/08/understanding-the-nginx-configuration-inheritance-model/)

[Understanding the Nginx Configuration File Structure and Configuration Contexts | DigitalOcean](https://www.digitalocean.com/community/tutorials/understanding-the-nginx-configuration-file-structure-and-configuration-contexts)
[Understanding Nginx Server and Location Block Selection Algorithms | DigitalOcean](https://www.digitalocean.com/community/tutorials/understanding-nginx-server-and-location-block-selection-algorithms)
[How To Set Up Nginx Server Blocks (Virtual Hosts) on Ubuntu 14.04 LTS | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-server-blocks-virtual-hosts-on-ubuntu-14-04-lts)

Main config filer (`nginx.conf`) sits in the Nginx config folder (e.g. `/etc/nginx`).  
There are `sites-available/` and `sites-enabled/`, default setting file includes `sites-enabled/*`.  
Server files are usually put in `sites-available/` and symlinked to `sites-enabled/`.

Options are called *directives*. They can live inside blocks (contexts) which define the scope they apply. Contexts are hierarchical: `main`, (`http`, `mail`, `stream`), `server`, `location`.

### CORS

[enable cross-origin resource sharing](http://enable-cors.org/index.html)
[Example Nginx configuration for adding cross-origin resource sharing (CORS) support to reverse proxied APIs](https://gist.github.com/Stanback/7145487)
[Wide-open CORS config for nginx](https://gist.github.com/michiel/1064640)


### nginScript

[Launching nginScript and Looking Ahead - NGINX](https://www.nginx.com/blog/launching-nginscript-and-looking-ahead/)
[nginScript - why create our own JavaScript implementation?](https://www.nginx.com/blog/nginscript-why-our-own-javascript-implementation/)

### init (Debian/Ubuntu)

> https://github.com/JasonGiedymin/nginx-init-ubuntu  
> https://github.com/hulihanapplications/nginx-init-debian

```sh
$ sudo service nginx 
configtest    force-reload  reload        restart       start         status        stop 
```

### systemd

```sh
sudo systemctl enable nginx.service
sudo systemctl start nginx.service
```

## Static file serving

```nginx
user http;

server {
    listen   80;
    server_name  domain.com www.domain.com;
    access_log   /var/log/nginx/static_server.log combined;
    root   /home/www;
    location / {
        index  index.php index.html index.htm;
        # Directory listing
        autoindex on;
    }
    # Password protect a directory
    location ^~ /secret_folder/ {
        auth_basic            "Restricted Area";
        # relative to this config file
        # using Apache's `htpasswd -b htpasswd NewUser NewPassword` or
        # http://www.tools.dynamicdrive.com/password/
        auth_basic_user_file  conf/htpasswd;
    }
}
```

Setup group and ownership of `www` folder

```sh
sudo -v
mkdir /home/www
usermod -a -G http ${USER}
chown -R http:http /home/www
chmod -R g+w /home/www
```

## Internals

[Inside NGINX - NGINX](https://www.nginx.com/resources/library/infographic-inside-nginx/)
[Inside NGINX: Designed for Performance & Scalability](https://www.nginx.com/blog/inside-nginx-how-we-designed-for-performance-scale/)
[Boosting NGINX Performance 9x with Thread Pools](https://www.nginx.com/blog/thread-pools-boost-performance-9x/)

## Redirect to https

```nginx
server {
    server_name _;
    rewrite ^ https://example.com$request_uri permanent;
}
```

## Node/Nginx

Add this to `hosts`:

```
127.0.0.1   mynodeapp.dev
```

> Uses [upstream module](http://nginx.org/en/docs/http/ngx_http_upstream_module.html) for abstraction and load balancing

```nginx
# node.conf

upstream node {
    server http://127.0.0.1:3000
    server unix:/tmp/mynodeapp.socket;
}

server {
    listen 80;
    server_name mynodeapp.dev
    location / {
            proxy_pass node;
            proxy_set_header Host $http_host;
    }
}
```

## Reverse proxy api.github.com

Add this to `hosts`:

```
127.0.0.1   api.github.localhost
```

Add this to `/etc/nginx/sites-enabled/api.github`:

```nginx
server {
    listen 80;
    server_name api.github.localhost;

    location / {
        proxy_set_header Host api.github.com;
        proxy_pass https://api.github.com/;
    }

    access_log      /var/log/nginx/github_access.log combined;
    error_log       /var/log/nginx/github_error.log error;
}
```

## Nginx status page

```nginx
location /nginx_status {
    # Turn on nginx stats
    stub_status on;
    # I do not need logs for stats
    access_log   off;
    # Security: Only allow access from 192.168.1.100 IP #
    allow 192.168.1.100;
    # Send rest of the world to /dev/null #
    deny all;
}
```

## Modules

[OpenResty - a fast web app server by extending nginx](http://openresty.org/)
[3rdPartyModules - Nginx Community](http://wiki.nginx.org/3rdPartyModules)

Module        | Link
------        | -----
Auth Digest   | https://github.com/samizdatco/nginx-http-auth-digest
Echo          | https://github.com/agentzh/echo-nginx-module
Fancy Indexes | https://github.com/aperezdc/ngx-fancyindex
Log If        | https://github.com/cfsego/ngx_log_if/
Lua           | https://github.com/chaoslawful/lua-nginx-module
PageSpeeed    | http://ngxpagespeed.com/ngx_pagespeed_example/
MP4 streaming | http://nginx.org/en/docs/http/ngx_http_mp4_module.html
