title: WordPress (dev)
categories:
  - app
toc: true
date: 2015-06-21 17:31:05
tags:
- wordpress
- cms
---

[WordPress › Make WordPress](https://make.wordpress.org/)
[WordPress › Handbook « Make WordPress Core](https://make.wordpress.org/core/handbook/)

## Resources

[WordPress Development Stack Exchange](http://wordpress.stackexchange.com/)
[Instant WordPress](http://www.instantwp.com/)  
[Command line interface for WordPress | WP-CLI](http://wp-cli.org/)  
[Toolbox of the Smart WordPress Developer: WP-CLI - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/toolbox-of-the-smart-wordpress-developer-wp-cli--cms-24098)

### WP API

[Category:API « WordPress Codex](https://codex.wordpress.org/Category:API)

[Plugin API « WordPress Codex](https://codex.wordpress.org/Plugin_API)
[Widgets API « WordPress Codex](https://codex.wordpress.org/Widgets_API)
[Shortcode API « WordPress Codex](https://codex.wordpress.org/Shortcode_API)
[Settings API « WordPress Codex](https://codex.wordpress.org/Settings_API)
[Options API « WordPress Codex](https://codex.wordpress.org/Options_API)
[Dashboard Widgets API « WordPress Codex](https://codex.wordpress.org/Dashboard_Widgets_API)
[Rewrite API « WordPress Codex](https://codex.wordpress.org/Rewrite_API)

### Sites

[Digging Into WordPress | Take your WordPress skills to the next level.](https://digwp.com/)
[WordPress Arena](http://wparena.com/)
[WordPress News, Hacks, Tips, Tutorials, Plugins and Themes - WP Engineer](http://wpengineer.com/)
[WordPress Hacks - WP Engineer](http://wpengineer.com/category/wordpress-hacks/)
[WP Smith - My Journey with WordPress & Genesis](http://wpsmith.net/)
[Home - Pippins Plugins](https://pippinsplugins.com/)

### Books 

[WPDK](http://gfazioli.gitbooks.io/wpdk/content/)
[WordPress The Right Way](http://www.wptherightway.org/en/index.html)
[雅戈的WordPress教程](http://yager.gitbooks.io/yager-wordpress/content/)

### Tips

[Stupid WordPress Tricks | Perishable Press](https://perishablepress.com/stupid-wordpress-tricks/)
[WordPress constants overview - WP Engineer](http://wpengineer.com/2382/wordpress-constants-overview/)
[14 Most Common WordPress Errors and How to Fix Them](http://www.wpbeginner.com/beginners-guide/14-most-common-wordpress-errors-and-how-to-fix-them/)
[Some of the most common Mistakes in Blogging | WordPress Arena](http://wparena.com/how-to/some-of-the-most-common-mistakes-in-blogging/)
[Excluding your plugin or theme from update checks | Mark on WordPress](https://markjaquith.wordpress.com/2009/12/14/excluding-your-plugin-or-theme-from-update-checks/)
[What’s the difference between __(), _e(), _x(), and _ex()? - WP Engineer](http://wpengineer.com/2237/whats-the-difference-between-__-_e-_x-and-_ex/)

[WordPress Tutorials - WP Engineer](http://wpengineer.com/category/wordpress-tutorials/)

## `wp-config.php`

[Editing wp-config.php « WordPress Codex](https://codex.wordpress.org/Editing_wp-config.php)

```php
# show error on screen
define('WP_DEBUG', true)

# disable revision
define('WP_POST_REVISIONS', false)

# for debugging theme
define('SAVEQURIES', true)
# in theme
if (current_user_can('manage_options')) {
    global $wpdb;
    print_r($wpdb->quries);
}

# force SSL
define('FORCE_SSL_LOGIN', true)
define('FORCE_SSL_ADMIN', true)
```

## Security

[Security Measures to keep WordPress powered Websites more Secure | WordPress Arena](http://wparena.com/how-to/security-measures-to-keep-wordpress-powered-websites-more-secure/)

[22 Must Follow WordPress Security Tips - Bloggersignal](https://www.bloggersignal.com/wordpress-security-tips/)

[Important Security Fix for WordPress | Perishable Press](https://perishablepress.com/important-security-fix-for-wordpress/)

[Changing File Permissions « WordPress Codex](https://codex.wordpress.org/Changing_File_Permissions)

[How To Change Wordpress Default 'Admin" Username](http://www.shoutmeloud.com/how-to-change-wordpress-default-username-security.html)

[How to prevent access to WordPress Administration Menu items | WordPress Arena](http://wparena.com/how-to/how-to-prevent-access-to-wordpress-administration-menu-items/)

[Making your WordPress site More Secure by Adding HTTPS and SSL | WordPress Arena](http://wparena.com/how-to/making-your-wordpress-site-more-secure-by-adding-https-and-ssl/)  
[How To Use SSL & HTTPS With WordPress | Elegant Themes Blog](http://www.elegantthemes.com/blog/tips-tricks/how-to-use-ssl-https-with-wordpress)  
[Options for SSL in WordPress - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/options-for-ssl-in-wordpress--cms-21995)  
[SSL and Cookies in WordPress 2.6 | Ryan Boren](http://ryan.boren.me/2008/07/14/ssl-and-cookies-in-wordpress-26/)  

### Restricted Login Access

[Secure WordPress with IP restricted access](https://www.sitestillup.com/how-to-lock-down-wordpress-admin-section-by-ip.html)  
[How to Restrict IP Addresses to Login on WordPress Dashboard](http://www.wpoptimus.com/912/ban-ip-addresses-login-wordpress-dashboard/)  
[How to Limit Access by IP to Your wp-login.php file in WordPress](http://www.wpbeginner.com/wp-tutorials/how-to-limit-access-by-ip-to-your-wp-login-php-file-in-wordpress/)  

In `.htaccess` file of the WordPress directory:
```
# Limit access by IP address
<Files wp-login.php>
        order deny,allow
        Deny from all
 
# whitelist IP address one
allow from xx.xxx.xx.xxx
 
# whitelist IP Address two
allow from xx.xxx.xx.xxx
</Files>
```

## Insert Sample Data

[Function Reference « WordPress Codex](https://codex.wordpress.org/Function_Reference)  
[Function Reference/wp insert category « WordPress Codex](https://codex.wordpress.org/Function_Reference/wp_insert_category)  
[Function Reference/wp insert term « WordPress Codex](https://codex.wordpress.org/Function_Reference/wp_insert_term)  
[Function Reference/wp insert post « WordPress Codex](https://codex.wordpress.org/Function_Reference/wp_insert_post)  
[Function Reference/wp trash post « WordPress Codex](https://codex.wordpress.org/Function_Reference/wp_trash_post)  

`themes/exclusive/admin/install_sampl_date.php`

```php
//Check if category already exists
$cat_ID = get_cat_ID( $category );

//If it doesn't exist create new category
if($cat_ID == 0) {
    $my_cat = array(
        'cat_name' => 'My Category', 
        'category_description' => 'A Cool Category', 
        'category_nicename' => 'category-slug', 
        'category_parent' => '',
        'taxonomy' => 'category'
    );

    $my_cat_id = wp_insert_category($my_cat);
}

// this is practically what wp_insert_category() does underneath
if(!term_exists('sample-category')) {
    wp_insert_term(
        'Sample Category',
        'category',
        array(
          'description' => 'This is an sample category.',
          'slug'        => 'sample-category'
        )
    );
}
```

## Plugins

[Plugins « WordPress Codex](http://codex.wordpress.org/Plugins)  

[WordPress › WordPress Plugins](https://wordpress.org/plugins/)  
[Writing a Plugin « WordPress Codex](http://codex.wordpress.org/Writing_a_Plugin)  
[Plugin API « WordPress Codex](http://codex.wordpress.org/Plugin_API)  
[How To Improve WordPress Plugins - WP Engineer](http://wpengineer.com/353/how-to-improve-wordpress-plugins/#more-353)  

[The WordPress Plugin Boilerplate | A Foundation For Building High-Quality WordPress Plugins](http://wppb.io/)  
[Developing Plugins With WordPress Boilerplates: Why Boilerplates Matter - Tuts+ Code Article](http://code.tutsplus.com/articles/developing-plugins-with-wordpress-boilerplates-why-boilerplates-matter--wp-29298)
[Developing Plugins With WordPress Boilerplates: Building a Plugin - Tuts+ Code Article](http://code.tutsplus.com/articles/developing-plugins-with-wordpress-boilerplates-building-a-plugin--wp-29300)  

[Aesop Story Engine](http://aesopstoryengine.com/)  
[Helpful Wordpress Plugins | Linux.org](http://www.linux.org/threads/helpful-wordpress-plugins.7765/)  
[Top 20 Useful WordPress ShortCode Plugins | Web Development Tutorials and Resources @ ScratchingInfo](http://www.scratchinginfo.net/useful-wordpress-shortcode-plugins/)  

## Themes

[Theme Development « WordPress Codex](https://codex.wordpress.org/Theme_Development)  
[WordPress › Getting Started | Theme Developer Handbook | WordPress Developer Resources](https://developer.wordpress.org/themes/getting-started/)  

[Theme Customization API « WordPress Codex](http://codex.wordpress.org/Theme_Customization_API)  
[Stepping into Templates « WordPress Codex](https://codex.wordpress.org/Stepping_Into_Templates)  
[Template Tags « WordPress Codex](https://codex.wordpress.org/Template_Tags)  
[Theme Features « WordPress Codex](https://codex.wordpress.org/Theme_Features)

[Writing Maintainable WordPress Themes - Tuts+ Code Tutorials](http://code.tutsplus.com/series/writing-maintainable-wordpress-themes--cms-659)

[Writing Maintainable WordPress Themes | Tom McFarlin](http://tommcfarlin.com/maintainable-wordpress-themes/)  
[Separation of Concerns with WordPress Templates | Tom McFarlin](https://tommcfarlin.com/separation-of-concerns-with-wordpress-templates/)  
[A Rule of Thumb for WordPress Partials | Tom McFarlin](https://tommcfarlin.com/wordpress-partials/)  
[Adding Scripts and Styles to WordPress the Right Way With Enqueueing - WPMU DEV](http://premium.wpmudev.org/blog/adding-scripts-and-styles-wordpress-enqueueing/)  

[10 Checks to the Perfect WordPress theme - WP Engineer](http://wpengineer.com/236/perfect-wordpress-theme/)

[Widgetizing Themes — Automattic](http://automattic.com/code/widgets/themes/)
[Widgetizing Themes « WordPress Codex](http://codex.wordpress.org/Widgetizing_Themes)

[Easily Adaptable WordPress Loop Templates: Basic Loops, Mullet Loops, and More.. | Perishable Press](https://perishablepress.com/easily-adaptable-wordpress-loop-templates/)

Also see [Widgets](#widgets)  

### Customizing Theme

[Deactivate WordPress Default Widgets - WP Engineer](http://wpengineer.com/1650/deactivate-wordpress-default-widgets/)

[WordPress › Customizer Framework « WordPress Plugins](https://wordpress.org/plugins/customizer-framework/)  
[WordPress › Custom Sidebars « WordPress Plugins](https://wordpress.org/plugins/custom-sidebars/)  
[WordPress › Stag Custom Sidebars « WordPress Plugins](https://wordpress.org/plugins/stag-custom-sidebars/)  
[WordPress › Easy Custom Sidebars « WordPress Plugins](https://wordpress.org/plugins/easy-custom-sidebars/)  

### Adding Sidebar

[Function Reference/register sidebars « WordPress Codex](https://codex.wordpress.org/Function_Reference/register_sidebars)
[Function Reference/dynamic sidebar « WordPress Codex](https://codex.wordpress.org/Function_Reference/dynamic_sidebar)

Define sidebar in `functions.php`:
```php
register_sidebar(array(
    'name' => __('MySidebar', 'theme'),
    'id' => 'my-sidebar',
    'description' => __('this is a custom sidebar', 'theme'),
    'before_widget' => '<div class="sidebar-box">',
    'after_widget' => '</div>',
    'before_title' => '<span class="sidebar-title">',
    'after_title' => '</span><div class="dots"></div>'
))
```

Add to the desired location in the theme:
```html
<div id="sidebar">
    <?php if ( !dynamic_sidebar("my-sidebar") ) : ?>
    <div class="sidebar-box">
        <span class="sidebar-title">MySidebar</span>
        <p>Add Widgets to the sidebar 'MySidebar'</p>
    </div>
    <?php endif; ?>
</div><!-- sidebar -->
```

Different sidebar depending on page, usually in `sidebar.php`:
```html
<?php
<div id="sidebar">
    if ( is_front_page() ) {
        if ( !dynamic_sidebar("front-page-sidebar") ) : ?>
            <li>front-page-sidebar is empty</li>
        <?php endif;
    }
    elseif ( is_category('news') || in_category('news') ) {
        if ( !dynamic_sidebar("news-sidebar") ) : ?>
            <li>news-sidebar is empty</li>
        <?php endif;
    }
    elseif ( is_single() ) {  // is_singular() for both Posts/Pages
        if ( !dynamic_sidebar("post-sidebar") ) : ?>
            <li>post-sidebar is empty</li>
        <?php endif;
    }
    elseif ( is_page() ) {
        if ( !dynamic_sidebar("page-sidebar") ) : ?>
            <li>page-sidebar is empty</li>
        <?php endif;
    }
?>
```

### Adding Nav Menu

[Function Reference/register nav menus « WordPress Codex](https://codex.wordpress.org/Function_Reference/register_nav_menus)
[Function Reference/wp nav menu « WordPress Codex](https://codex.wordpress.org/Function_Reference/wp_nav_menu)

Define nav_menu in `functions.php`:
```php
register_nav_menus( array(
    'top-navigation' => __('Top Navigation', 'theme')
) );
```

Add to the desired location in the theme:
```html
<div id="header-bottom">
    <?php wp_nav_menu('top-navigation') ?>
</div>
```

### Customizer

[» The WordPress Theme Customizer: a Comprehensive Developer’s Guide](http://themefoundation.com/wordpress-theme-customizer/)
[A Guide to the WordPress Theme Customizer - Tuts+ Code Tutorials](http://code.tutsplus.com/series/a-guide-to-the-wordpress-theme-customizer--wp-33722)
[Digging Into the Theme Customizer - Tuts+ Code Tutorials](http://code.tutsplus.com/series/digging-into-the-theme-customizer--wp-33847)

[paulund/wordpress-theme-customizer-custom-controls](https://github.com/paulund/Wordpress-Theme-Customizer-Custom-Controls)

Customizer: Theme as documentation  
[bueltge/Documentation](https://github.com/bueltge/Documentation)  
[The Customizer on Vimeo](https://vimeo.com/51533540)  
[WordPress Theme Customizer Custom Controls - WP Engineer](http://wpengineer.com/2527/wordpress-theme-customizer-custom-controls/#more-2527)  

### Framework

[Thematic, A WordPress Theme Framework | ThemeShaper](http://themeshaper.com/thematic/)  
[Hybrid Core WordPress theme framework](http://themehybrid.com/hybrid-core)  
[Whiteboard Framework for WordPress](http://whiteboardframework.com/)  
[Roots | Modern WordPress Development](https://roots.io/)
[Wonderflux - WordPress free, open source theme framework](http://wonderflux.com/)

[How Theme Frameworks Actually Work - Tuts+ Code Tutorials](http://code.tutsplus.com/series/how-theme-frameworks-actually-work--cms-713)  

[Theme Hybrid: A WordPress theme club](http://themehybrid.com/)  
[Bones - The HTML5 Wordpress Starter Theme](http://themble.com/bones/)  
[Responsive WordPress Theme WP-Forge](http://themeawesome.com/responsive-wordpress-theme/)

### ThemeShaper

[The ThemeShaper WordPress Theme Tutorial: 2nd Edition | ThemeShaper](http://themeshaper.com/2012/10/22/the-themeshaper-wordpress-theme-tutorial-2nd-edition/)  
[What Do You Really Need in a WordPress Starter Theme? | ThemeShaper](http://themeshaper.com/2012/01/17/what-do-you-really-need-in-a-wordpress-starter-theme/)  
[Underscores.me — The Best Way To Get Started With The _s Theme | ThemeShaper](http://themeshaper.com/2012/08/15/underscores-me-the-best-way-to-get-started-with-the-_s-theme/)  
[Thematic, A WordPress Theme Framework | ThemeShaper](http://themeshaper.com/thematic/)  
[Automattic/_s](https://github.com/automattic/_s)  

### The Loop

The Loop selects content from MySQL database (typically with query based on URL). It is the link between the theme and the contents in database. WordPress is using the Loop anywhere content is displayed.

Simplest Loop:

```php
// these functions uses global variable `WP_Query $wp_query`
if ( have_posts() ) :
    while ( have_posts() ) :
        the_post();
        // content is available
    endwhile;
endif;
```

[Writing Clean, Maintainable Custom WordPress Queries | Tom McFarlin](https://tommcfarlin.com/custom-wordpress-queries/)  
[How To Setup Custom Queries For WP_Query Pagination | Tom McFarlin](https://tommcfarlin.com/wp_query-pagination/)  
[Separation of Concerns: Queries and Helper Functions | Tom McFarlin](https://tommcfarlin.com/separation-of-concerns-with-queries-and-helper-functions/)  

[wp query - When should you use WP_Query vs query_posts() vs get_posts()? - WordPress Development Stack Exchange](http://wordpress.stackexchange.com/questions/1753/when-should-you-use-wp-query-vs-query-posts-vs-get-posts)

[Mastering WP_Query - Tuts+ Code Tutorials](http://code.tutsplus.com/series/mastering-wp_query--cms-818)

### Settings

[Settings API « WordPress Codex](https://codex.wordpress.org/Settings_API)
[Sanitization with the WordPress Settings API | Tom McFarlin](https://tommcfarlin.com/tag/sanitization-with-the-wordpress-settings-api/)
[The Complete Guide To The WordPress Settings API - Tuts+ Code Tutorials](http://code.tutsplus.com/series/the-complete-guide-to-the-wordpress-settings-api--cms-624)

### Child Themes

You can easily inherit from an existing theme and override the functions.  
But the theme may not be child friendly (e.g.: using `get_template_directory()` instead of `get_stylesheet_directory()`, not using `get_template_part()`). And my experience is that overriding files may cause the child theme to breakdown altogether.  
I now prefer make a copy of the desired theme, change the code directly and track the modification via git.  

[Child Themes « WordPress Codex](https://codex.wordpress.org/Child_Themes)  
[How To Modify WordPress Themes The Smart Way | ThemeShaper](http://themeshaper.com/modify-wordpress-themes/)  
[How to Create a WordPress Child Theme - WPMU DEV](http://premium.wpmudev.org/blog/how-to-create-wordpress-child-theme/)  

[What is a WordPress Child Theme? Pros, Cons, and More](http://www.wpbeginner.com/beginners-guide/wordpress-child-theme-pros-cons/)  
[WordPress › Support » Overriding parent theme sub-files with a child theme. HOW?](https://wordpress.org/support/topic/overriding-parent-theme-sub-files-with-a-child-theme-how)  
[WordPress › Support » Child Themes and PHP pages](https://wordpress.org/support/topic/child-themes-and-php-pages)  

## Widgets

[WordPress Widgets « WordPress Codex](http://codex.wordpress.org/WordPress_Widgets)

[Build A WordPress 2.8 Widget With The New Widget API - WP Engineer](http://wpengineer.com/1023/wordpress-built-a-widget/)

## Tuts+

[WordPress - Tuts+ Code Category](http://code.tutsplus.com/categories/wordpress)  
[Tools of the Smart WordPress Developer - Tuts+ Code Tutorials](http://code.tutsplus.com/series/tools-of-the-smart-wordpress-developer--cms-838)

[The Complete Guide To The WordPress Settings API - Tuts+ Code Tutorials](http://code.tutsplus.com/series/the-complete-guide-to-the-wordpress-settings-api--cms-624)  
[Making the Perfect WordPress Theme - Tuts+ Code Tutorials](http://code.tutsplus.com/series/making-the-perfect-wordpress-theme--wp-33987)  
[Quick Tips to Boost Your WordPress Website's Speed - Tuts+ Code Tutorials](http://code.tutsplus.com/series/quick-tips-to-boost-your-wordpress-websites-speed--cms-800)  
[The Tuts+ Guide to Template Tags - Tuts+ Code Tutorials](http://code.tutsplus.com/series/the-tuts-guide-to-template-tags--cms-805)  
[A Walkthrough on Conditional Tags in WordPress - Tuts+ Code Tutorials](http://code.tutsplus.com/series/a-walkthrough-on-conditional-tags-in-wordpress--cms-804)  
[A Beginner’s Guide to Using WordPress - Tuts+ Course](http://webdesign.tutsplus.com/courses/a-beginners-guide-to-using-wordpress)  
[The Beginner’s Guide to WordPress Taxonomies - Tuts+ Code Tutorials](http://code.tutsplus.com/series/the-beginners-guide-to-wordpress-taxonomies--cms-706)  
[The Beginner's Guide to Selecting a WordPress Theme - Tuts+ Code Article](http://code.tutsplus.com/articles/the-beginners-guide-to-selecting-a-wordpress-theme--wp-35032)  
[Trim the Bloat: Keeping WordPress Healthy - Tuts+ Code Tutorials](http://code.tutsplus.com/series/trim-the-bloat-keeping-wordpress-healthy--cms-758)  
[Fifty Actions of WordPress - Tuts+ Code Tutorials](http://code.tutsplus.com/series/fifty-actions-of-wordpress--cms-708)
[Understanding and Working with Data in WordPress - Tuts+ Code Tutorials](http://code.tutsplus.com/series/understanding-and-working-with-data-in-wordpress--cms-670)  

[Create a Mobile Application Using WordPress, Ionic, and AngularJS - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/create-a-mobile-application-using-wordpress-ionic-and-angularjs--cms-24170)
