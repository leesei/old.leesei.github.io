---
title: Apache
categories:
  - app
toc: true
date: 2015-06-21 18:58:50
tags:
  - apache
  - notes
---

[Apache 2 Advanced Configuration on Unix-Like Systems - Tuts+ Code Article](http://code.tutsplus.com/articles/apache-2-advanced-configuration-on-unix-like-systems--net-26244)

Apache Web server binary and package is called `httpd`.

## .htaccess

[Stupid htaccess Tricks | Perishable Press](https://perishablepress.com/stupid-htaccess-tricks/)
[What is .htaccess? - Apache .htaccess Guide, Tutorials & Examples](http://www.htaccess-guide.com/)
[Adding MIME types - Apache .htaccess Guide, Tutorials & Examples](http://www.htaccess-guide.com/adding-mime-types/)

[Search results for htaccess Tutorials](https://www.hostinger.com/tutorials/?s=htaccess)
[How do I disable directory listing | Hostinger Help Center](https://support.hostinger.com/en/articles/1583496-how-do-i-disable-directory-listing)

[How to Password Protect Joomla’s Administrator Directory](https://www.ostraining.com/blog/joomla-cms/how-to-password-protect-joomla-s-administrator-directory/)

## Rewrite

[RewriteRule examples and explanations - filkor.org Writings](http://dev.filkor.org/2014/01/09/dot-htaccess-examples-and-explanations/)

## HTTPS

```sh
# generate cert
> openssl genrsa -out privatekey.pem 1024
> openssl req -new -key privatekey.pem -x509 -days 7300 -out certificate.pem

Loading 'screen' into random state - done
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [AU]:tw
State or Province Name (full name) [Some-State]:Taiwan
Locality Name (eg, city) []:Taipei
Organization Name (eg, company) [Internet Widgits Pty Ltd]:MyCompany
Organizational Unit Name (eg, section) []:IT-Dept
Common Name (e.g. server FQDN or YOUR name) []:ssl.mycompany.com.tw
Email Address []:
```

Configure Apache:

```
<VirtualHost *:80>
       ServerAdmin                   # 電子郵件信箱，可任意填，但不能為空值
       DocumentRoot                  # 網站根目錄
       ServerName                    # 網站domain，需與前面的CommonName內容相同
       ErrorLog "logs/error_log"
       CustomLog "logs/access_log common"
       #SSLEngine on
       SSLCertificateFile            # server.crt的完整路徑
       SSLCertificateKeyFile         # server.key的完整路徑
</VirtualHost>
```

```sh
apache -D SSL
```

## Enabling PHP debug

In `php.ini`:

```
error_reporting = E_ALL | E_STRICT;
```

## `httpd.conf`

### DocumentRoot

```
DocumentRoot "path"

<Directory "path">
    # setting for DocumentRoot
</Directory>
```

### Hiding folder

```
<Directory ~ ".*\.sql*">
    Order allow,deny
    Deny from all
    Satisfy all
</Directory>
```

## WSGI

[RunningDeepZoomServerOnApache · openslide/openslide Wiki](https://github.com/openslide/openslide/wiki/RunningDeepZoomServerOnApache)
