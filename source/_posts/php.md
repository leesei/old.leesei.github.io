---
title: "PHP"
date: 2021-05-28 16:04:06
categories:
  - comp.lang
tags:
  - php
toc: true
---

[PHP: Hypertext Preprocessor](https://www.php.net/)
[PHP Scraper - An opinionated web-scraping library for PHP](https://phpscraper.de/)

[PHP - ArchWiki](https://wiki.archlinux.org/title/PHP)

[How to Learn PHP](https://code.tutsplus.com/articles/how-to-learn-php--cms-37726)

[Difference between PHP-CGI and PHP-FPM | BaseZap](https://www.basezap.com/difference-php-cgi-php-fpm/)
[The Definitive PHP 5.6, 7.0, 7.1, 7.2, 7.3, 7.4, and 8.0 Benchmarks (2021)](https://kinsta.com/blog/php-benchmarks/)

[Is PHP Dead? No! At Least Not According to PHP Usage Statistics](https://kinsta.com/blog/is-php-dead/)
[PHP in decline: The rise and fall of a programming language - JAXenter](https://jaxenter.com/php-tiobe-sept-2019-162096.html)

## Config

[PHP: Description of core php.ini directives - Manual](https://www.php.net/manual/en/ini.core.php)

```sh
$ php --ini
Configuration File (php.ini) Path: /etc/php7
Loaded Configuration File:         /etc/php7/php.ini
Scan for additional .ini files in: /etc/php7/conf.d
Additional .ini files parsed:      (none)
```

## PHP-FPM

[PHP: FastCGI Process Manager (FPM) - Manual](https://www.php.net/manual/en/install.fpm.php) `php-fpm`
[PHP: Configuration - Manual](https://www.php.net/manual/en/install.fpm.configuration.php)

[PHP-FPM - HTTPD - Apache Software Foundation](https://cwiki.apache.org/confluence/display/httpd/PHP-FPM)

Use `cgi-fcgi` for testing your PHP FPM endpoints.  
[inanzzz | Testing PHP-FPM without having a web server](http://www.inanzzz.com/index.php/post/653v/testing-php-fpm-without-having-a-web-server)  
[Directly connect to PHP-FPM](https://easyengine.io/tutorials/php/directly-connect-php-fpm/)

## Learn

[PHP: PHP Manual - Manual](https://www.php.net/manual/en/index.php)

```sh
echo '<?php phpinfo(); ?>' > /srv/http/phpinfo.php
http://localhost/phpinfo.php
```

[27 Best Tutorials to Learn PHP in 2021 (Free and Paid Resources)](https://kinsta.com/blog/php-tutorials/)

[PHP Training Courses - Learn the world's most popular web programming language from the PHP Experts.](http://www.zend.com/en/services/training#PHP%20Courses)
[PHP - Getting started with PHP | php Tutorial](https://riptutorial.com/php)

[The Best Way to Learn PHP - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/the-best-way-to-learn-php--net-22287)
[8 Awesome and Free PHP Books - Tutorialzine](https://tutorialzine.com/2018/03/8-awesome-and-free-php-books)

[PHP: The Right Way](https://www.phptherightway.com/)
[PHP & MySQL: Novice to Ninja, 6th Edition - Installation](https://www.sitepoint.com/premium/books/php-mysql-novice-to-ninja-6th-edition/read/1)

## the bad

[Is PHP a badly designed programming language? - Quora](https://www.quora.com/Is-PHP-a-badly-designed-programming-language)
[Why is PHP hated by so many developers? - Quora](https://www.quora.com/Why-is-PHP-hated-by-so-many-developers)
[PHP: a fractal of bad design / fuzzy notepad](http://eev.ee/blog/2012/04/09/php-a-fractal-of-bad-design/)
[PHP Sadness](http://phpsadness.com/)
[The PHP Singularity](http://blog.codinghorror.com/the-php-singularity/)

## Docker

[jniltinho/caddy-php-fpm: Caddy v2 + PHP-FPM 7.2.x + Composer built on Ubuntu](https://github.com/jniltinho/caddy-php-fpm)
[Yavin/docker-alpine-php-fpm: Docker image for php-fpm based on alpine linux that makes it small](https://github.com/Yavin/docker-alpine-php-fpm) 7.2, with extensions

[phpdockerio/php74-fpm](https://hub.docker.com/r/phpdockerio/php74-fpm/)

```sh
mkdir -p ~/php/php-fpm/logs ~/php/php-fpm/conf
docker run -p 9000:9000 --name myphp-fpm \
  -v (pwd):/www \
  -v $HOME/php/php-fpm/conf:/usr/local/etc/php \
  -v $HOME/php/php-fpm/logs:/phplogs \
  phpdockerio/php74-fpm
```

## HHVM/Hack

[HHVM | HHVM](http://hhvm.com/) JIT VM for Hack, PHP 5 and majority of PHP 7.
[The Hack Programming Language | Hack](http://hacklang.org/)

Zend PHP 7.3 outperforms HHVM in PHP

## Variables

[PHP: $\_SERVER - Manual](https://www.php.net/manual/en/reserved.variables.server.php)

[PHP: Variables From External Sources - Manual](https://www.php.net/manual/en/language.variables.external.php)
[PHP: $\_GET - Manual](https://www.php.net/manual/en/reserved.variables.get.php) query param
[PHP: $\_POST - Manual](https://www.php.net/manual/en/reserved.variables.post.php) support array, not dots (`.`)
[PHP: $\_REQUEST - Manual](https://www.php.net/manual/en/reserved.variables.request.php)

[How to receive JSON POST with PHP - GeeksforGeeks](https://www.geeksforgeeks.org/how-to-receive-json-post-with-php/)

```php
// Takes raw data from the request
if ($_REQUEST["CONTENT_TYPE"] === "application/json") {
	$body = file_get_contents('php://input');

	// Converts it into a PHP object
	$data = json_decode($body);
}
```

## stdlib

[PHP: Function Reference - Manual](https://www.php.net/manual/en/funcref.php)

## Packages

### Composer

[Composer](https://getcomposer.org/) 2012, inspired by `npm`, `./vendor/`
[Composer Docs](https://getcomposer.org/doc/)
[Composer (software) - Wikiwand](<https://www.wikiwand.com/en/Composer_(software)>)

[Basic usage - Composer](https://getcomposer.org/doc/01-basic-usage.md)
[jakoch/awesome-composer: A curated awesome list for Composer, Packagist, Satis, Plugins, Scripts, Composer related resources, tutorials.](https://github.com/jakoch/awesome-composer)
[How to Install and Use PHP Composer on Linux Distributions](https://www.ubuntupit.com/how-to-install-and-use-php-composer-on-linux-distributions/)

```sh
composer diagnose
```

[Packagist](https://packagist.org/) repository

`composer.json`

```json
{
  "require": {
    "vendor/package": "1.3.2",
    "vendor/package2": "1.*",
    "vendor/package3": "^2.0.3"
  }
}
```

[PSR-4: Autoloader - PHP-FIG](https://www.php-fig.org/psr/psr-4/)
[Basic usage Autoloading - Composer](https://getcomposer.org/doc/01-basic-usage.md#autoloading)
[Autoloader optimization - Composer](https://getcomposer.org/doc/articles/autoloader-optimization.md)

### PEAR

[PEAR - PHP Extension and Application Repository](https://pear.php.net/) 1999, global `pear/`
[PEAR - Wikiwand](https://www.wikiwand.com/en/PEAR)

### ReactPHP

[ReactPHP: Event-driven, non-blocking I/O with PHP - ReactPHP](https://reactphp.org/)
[reactphp/react: Event-driven, non-blocking I/O with PHP.](https://github.com/reactphp/react)
[Category Archive "ReactPHP Series" — Cees-Jan Kiewiet's blog](https://blog.wyrihaximus.net/categories/reactphp-series/)
[FLOSS Weekly 486 ReactPHP](https://twit.tv/shows/floss-weekly/episodes/486)

### scraping

[PHP: DOMDocument::loadHTML - Manual](https://www.php.net/manual/en/domdocument.loadhtml.php)
[How to Parse HTML using PHP Native Classes](https://codingreflections.com/php-parse-html/)

[PHP Scraper - An opinionated web-scraping library for PHP](https://phpscraper.de/)

[paquettg/php-html-parser: An HTML DOM parser. It allows you to manipulate HTML. Find tags on an HTML page with selectors just like jQuery.](https://github.com/paquettg/php-html-parser)

[PHP Simple HTML DOM Parser](https://simplehtmldom.sourceforge.io/)

### Laravel

[Laravel - The PHP Framework For Web Artisans](https://laravel.com/)
[Laravel - Wikiwand](https://www.wikiwand.com/en/Laravel)

[Laracasts](https://laracasts.com/)
[Installation - Laravel - The PHP Framework For Web Artisans](https://laravel.com/docs/)

[Introduction | Laravel Jetstream](https://jetstream.laravel.com/2.x/introduction.html)

[Livewire | Laravel Livewire](https://laravel-livewire.com/) Meteor-like, send HTML-partials
[Inertia.js - The Modern Monolith](https://inertiajs.com/)
[Lumen - PHP Micro-Framework By Laravel](https://lumen.laravel.com/) Express-like

[Eloquent ORM - Laravel - The PHP Framework For Web Artisans](https://laravel.com/docs/5.0/eloquent)
[Laravel Eloquent Tutorial With Examples – Stackify](https://stackify.com/laravel-eloquent-tutorial/amp/)
[calebporzio/sushi: Eloquent's missing "array" driver.](https://github.com/calebporzio/sushi)
