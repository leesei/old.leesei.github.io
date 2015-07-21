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

[nginx - ArchWiki](https://wiki.archlinux.org/index.php/Nginx)
[Nginx Community](http://wiki.nginx.org/Main)
[GettingStarted - Nginx Community](http://wiki.nginx.org/GettingStarted)
[Pitfalls - Nginx Community](http://wiki.nginx.org/Pitfalls)

[Nginx开发从入门到精通 — Nginx开发从入门到精通](http://tengine.taobao.org/book/index.html)
[agentzh's Nginx Tutorials](http://openresty.org/download/agentzh-nginx-tutorials-en.html) [download](http://openresty.org/#eBooks) [source](https://github.com/openresty/nginx-tutorials)
[Nginx Guide - Tuts+ Code Tutorials](http://code.tutsplus.com/series/nginx-guide--cms-792)
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

[Nginx Configuration Primer](http://blog.martinfjordvald.com/2010/07/nginx-primer/)
[Nginx Primer 2: From Apache to Nginx](https://blog.martinfjordvald.com/2011/02/nginx-primer-2-from-apache-to-nginx/)
[Understanding the Nginx Configuration Inheritance Model](https://blog.martinfjordvald.com/2012/08/understanding-the-nginx-configuration-inheritance-model/)
[Debugging Nginx Errors](https://blog.martinfjordvald.com/2013/06/debugging-nginx-errors/)

Main config filer (`nginx.conf`) sits in the Nginx config folder (e.g. `/etc/nginx`).  
There are `sites-available/` and `sites-enabled/`, default setting file includes `sites-enabled/*`.  
Server files are usually put in `sites-available/` and symlinked to `sites-enabled/`.

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
server {
    listen   80;
    server_name  domain.com www.domain.com;
    access_log   /var/log/nginx/static_server.log combined;
    root   /home/www;
    location / {
            index  index.php index.html index.htm;
    }
    # Directory listing
    location /www {
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

Setup group and ownership of www folder

```sh
sudo -v
usermod -a -G www-data ${USER}
chown -R www-data:www-data /home/www
chmod -R g+w /home/www
```

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
