title: "WordPress"
date: 2015-05-21 18:09:00
categories:
  - app
tags:
- bitnami
- wordpress
- cms
toc: true
---

[WordPress › Blog Tool, Publishing Platform, and CMS](http://wordpress.org/)


<!-- more -->
### Installing with Existing Website

[Integrating WordPress with Your Website « WordPress Codex](https://codex.wordpress.org/Integrating_WordPress_with_Your_Website)
[Giving WordPress Its Own Directory « WordPress Codex](http://codex.wordpress.org/Giving_WordPress_Its_Own_Directory)

## WordPress Configuration

[Editing wp-config.php « WordPress Codex](http://codex.wordpress.org/Editing_wp-config.php)

[聖公會李炳中學 | 升學及就業輔導組](http://careers.liping.edu.hk/)

On a Bitnami WordPress installation, these two URL are available:
- [localhost/phpmyadmin](http://localhost/phpmyadmin)
- [localhost/wordpress](http://localhost/wordpress)

## WordPress Lessons

[Main Page « WordPress Codex](http://codex.wordpress.org/Main_Page)
[WordPress Lessons « WordPress Codex](http://codex.wordpress.org/WordPress_Lessons)
[WordPress Semantics « WordPress Codex](http://codex.wordpress.org/WordPress_Semantics)

Now that WordPress is up and running, visit `http://localhost/wordpress`.
The WordPress admin panel at `http://localhost/wordpress/wp-admin`.


## Themes

[Using Themes « WordPress Codex](http://codex.wordpress.org/Themes)
[WordPress › Featured « Free WordPress Themes](https://wordpress.org/themes/)
[Free WordPress Themes - WPZOOM](http://www.wpzoom.com/free-wordpress-themes/)
[Theme Hybrid: A WordPress theme club](http://themehybrid.com/)
[WordPress Themes | Perishable Press](https://perishablepress.com/perishable-wordpress-themes/)

[The Beginner's Guide to Selecting a WordPress Theme - Tuts+ Code Article](http://code.tutsplus.com/articles/the-beginners-guide-to-selecting-a-wordpress-theme--wp-35032)
[Choosing the Right WordPress Theme - Market Blog](http://marketblog.envato.com/tips/choosing-the-right-wordpress-theme/)

https://wordpress.org/themes/exclusive
https://wordpress.org/themes/expert
https://wordpress.org/themes/sento
https://wordpress.org/themes/minamaze
https://wordpress.org/themes/educate
https://wordpress.org/themes/wordplus/

## Customizing Layout

We can select theme and do standard WordPress customization at `/wordpress/wp-admin/customize.php`. Settings may or may not be reflected depending on the theme being used.

Aside from selecting the theme and Front Page setting, it is recommended to used *Appearence* section in admin page which has access to 
- *Widget* settings (better)
- *Menus* settings
- *Theme Options*

Here's a visualization of a basic *Post/Page Layout*.

|            Header             |
| Nav menu                      |
| ----------------------------- |
|      Post/Page      | Primary |
|      Content        | Widget  |
|                     | Area    |
| ----------------------------- |
| Footer Sidebar                |

Widget Area are also called sidebar. Since it is not limited to reside in the sides of the page, I refrain from using the term altogether. But you have to be aware of it as it is used in many documentations.

## Front Page Layouts

### Expert

[Expert](http://themedemo.web-dorado.com/businesstheme/)
Have *Integration* feature to insert custom code.

[Dorado WordPress Themes Guide Step](https://web-dorado.com/wordpress-themes-guide-step-1.html)

|            Header             |
| Nav menu                      |
| ----------------------------- |
|      Content        | Primary |
|      Posts          | Widget  |
|      (optional)     | Area    |
|                     |         |
| ----------------------------- |
| Footer Sidebar                |

### Exclusive

[Exclusive](http://themedemo.web-dorado.com/exclusive/)

[Dorado WordPress Themes Guide Step](https://web-dorado.com/wordpress-themes-guide-step-1.html)

|            Header             |
| Nav menu                      |
| ----------------------------- |
|            Slider             |
|           Top Posts           | (optional, link to posts of a category)
| ----------------------------- |
|      Featured       | Primary |
|      Post           | Widget  |
|      (optional)     | Area    |
|                     |         |
|                     |         |
|      Content        |         |
|      Posts          |         |
|                     |         |
| ----------------------------- |
| Footer Sidebar                |

### Sento/Minamaze

Post/Page and Archive can have different layouts.
Uses [Redux Framework](http://reduxframework.com/)

| Pre Header menu               |
| Header            Header menu |
| ----------------------------- |
|            Slider             |
|        Message/Button         | (optional)
|        Featured Area          | (optional, link to custom pages)
| ----------------------------- |
|      Post/Page      | Primary |
|      Content        | Widget  |
|                     | Area    |
| ----------------------------- |
| Footer Sidebar                | (optional, multiple columns)

### Educate

You have to create a page with 'front-page template' to see this layout.

| Header            Header menu |
| ----------------------------- |
|            Slider             |
|         About message         | (optional)
|         About Blocks          | (optional)
| ----------------------------- |
|      Posts          | Primary |
|    (Masonry Grid)   | Widget  |
|                     | Area    |
| ----------------------------- |
| Footer Sidebar                | (optional, multiple columns)


### The Navigation Menu

`wordpress/wp-admin/nav-menus.php`

The Primary menu is usually shown above or below the header.
Use the *Menus* settings to create menus and assign them to various locations in the theme. Some themes support multiple menu.

### Static Front Page

We can specify a page as front page. The page will be rendered using *Post/Page Layout*.
However since most themes provides a customizable front page, it is not recommended to use this setting.

### Widgets

`/wordpress/wp-admin/widgets.php`

You can assign Widgets to Widget Areas in the theme.
Some themes support multiple Widget Areas.

### Slider

> TODO: update this when theme is finalized

`/wordpress/wp-admin/themes.php?page=web_dorado_theme&controller=slider_page`

The theme we choose supports slider.
The resolution of the image should be 963x470 (for slider height of 500px). The image will be scaled to fit the slider. It is recommended to add border to resize the image to fit the resolution.
