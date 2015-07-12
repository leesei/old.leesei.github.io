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

[Instant WordPress](http://www.instantwp.com/)  
[Command line interface for WordPress | WP-CLI](http://wp-cli.org/)  

### Sites

[Digging Into WordPress | Take your WordPress skills to the next level.](https://digwp.com/)
[WordPress Arena](http://wparena.com/)
[WordPress News, Hacks, Tips, Tutorials, Plugins and Themes - WP Engineer](http://wpengineer.com/)
[WordPress Hacks - WP Engineer](http://wpengineer.com/category/wordpress-hacks/)
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

## Security

[Security Measures to keep WordPress powered Websites more Secure | WordPress Arena](http://wparena.com/how-to/security-measures-to-keep-wordpress-powered-websites-more-secure/)

[Important Security Fix for WordPress | Perishable Press](https://perishablepress.com/important-security-fix-for-wordpress/)

[Changing File Permissions « WordPress Codex](https://codex.wordpress.org/Changing_File_Permissions)

[How To Change Wordpress Default 'Admin" Username](http://www.shoutmeloud.com/how-to-change-wordpress-default-username-security.html)

[How to prevent access to WordPress Administration Menu items | WordPress Arena](http://wparena.com/how-to/how-to-prevent-access-to-wordpress-administration-menu-items/)

[Making your WordPress site More Secure by Adding HTTPS and SSL | WordPress Arena](http://wparena.com/how-to/making-your-wordpress-site-more-secure-by-adding-https-and-ssl/)  
[How To Use SSL & HTTPS With WordPress | Elegant Themes Blog](http://www.elegantthemes.com/blog/tips-tricks/how-to-use-ssl-https-with-wordpress)  
[Options for SSL in WordPress - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/options-for-ssl-in-wordpress--cms-21995)  
[SSL and Cookies in WordPress 2.6 | Ryan Boren](http://ryan.boren.me/2008/07/14/ssl-and-cookies-in-wordpress-26/)  

[Secure WordPress with IP restricted access](https://www.sitestillup.com/how-to-lock-down-wordpress-admin-section-by-ip.html)  
[How to Restrict IP Addresses to Login on WordPress Dashboard](http://www.wpoptimus.com/912/ban-ip-addresses-login-wordpress-dashboard/)  
[How to Limit Access by IP to Your wp-login.php file in WordPress](http://www.wpbeginner.com/wp-tutorials/how-to-limit-access-by-ip-to-your-wp-login-php-file-in-wordpress/)  

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

[WordPress › WordPress Plugins](https://wordpress.org/plugins/)

[Plugins « WordPress Codex](http://codex.wordpress.org/Plugins)  
[Writing a Plugin « WordPress Codex](http://codex.wordpress.org/Writing_a_Plugin)  
[How To Improve WordPress Plugins - WP Engineer](http://wpengineer.com/353/how-to-improve-wordpress-plugins/#more-353)  

[The WordPress Plugin Boilerplate | A Foundation For Building High-Quality WordPress Plugins](http://wppb.io/)  
[Developing Plugins With WordPress Boilerplates: Building a Plugin - Tuts+ Code Article](http://code.tutsplus.com/articles/developing-plugins-with-wordpress-boilerplates-building-a-plugin--wp-29300)  

[Aesop Story Engine](http://aesopstoryengine.com/)  
[Helpful Wordpress Plugins | Linux.org](http://www.linux.org/threads/helpful-wordpress-plugins.7765/)  

## Themes

[Theme Development « WordPress Codex](https://codex.wordpress.org/Theme_Development)  
[WordPress › Getting Started | Theme Developer Handbook | WordPress Developer Resources](https://developer.wordpress.org/themes/getting-started/)  

[Theme Customization API « WordPress Codex](http://codex.wordpress.org/Theme_Customization_API)  
[Stepping into Templates « WordPress Codex](https://codex.wordpress.org/Stepping_Into_Templates)  
[Template Tags « WordPress Codex](https://codex.wordpress.org/Template_Tags)  
[Theme Features « WordPress Codex](https://codex.wordpress.org/Theme_Features)  

[The Tuts+ Guide to Template Tags - Tuts+ Code Tutorials](http://code.tutsplus.com/series/the-tuts-guide-to-template-tags--cms-805)  
[A Walkthrough on Conditional Tags in WordPress - Tuts+ Code Tutorials](http://code.tutsplus.com/series/a-walkthrough-on-conditional-tags-in-wordpress--cms-804)  

[Writing Maintainable WordPress Themes | Tom McFarlin](http://tommcfarlin.com/maintainable-wordpress-themes/)  
[Separation of Concerns with WordPress Templates | Tom McFarlin](https://tommcfarlin.com/separation-of-concerns-with-wordpress-templates/)  
[A Rule of Thumb for WordPress Partials | Tom McFarlin](https://tommcfarlin.com/wordpress-partials/)  
[Adding Scripts and Styles to WordPress the Right Way With Enqueueing - WPMU DEV](http://premium.wpmudev.org/blog/adding-scripts-and-styles-wordpress-enqueueing/)  

[10 Checks to the Perfect WordPress theme - WP Engineer](http://wpengineer.com/236/perfect-wordpress-theme/)
[Widgetizing Themes — Automattic](http://automattic.com/code/widgets/themes/)
[Widgetizing Themes « WordPress Codex](http://codex.wordpress.org/Widgetizing_Themes)

### Customizing Theme

[» The WordPress Theme Customizer: a Comprehensive Developer’s Guide](http://themefoundation.com/wordpress-theme-customizer/)

[Deactivate WordPress Default Widgets - WP Engineer](http://wpengineer.com/1650/deactivate-wordpress-default-widgets/)

[paulund/wordpress-theme-customizer-custom-controls](https://github.com/paulund/Wordpress-Theme-Customizer-Custom-Controls)

[WordPress › Customizer Framework « WordPress Plugins](https://wordpress.org/plugins/customizer-framework/)  
[WordPress › Custom Sidebars « WordPress Plugins](https://wordpress.org/plugins/custom-sidebars/)  
[WordPress › Stag Custom Sidebars « WordPress Plugins](https://wordpress.org/plugins/stag-custom-sidebars/)  
[WordPress › Easy Custom Sidebars « WordPress Plugins](https://wordpress.org/plugins/easy-custom-sidebars/)  

Customizer: Theme as documentation  
[bueltge/Documentation](https://github.com/bueltge/Documentation)  
[The Customizer on Vimeo](https://vimeo.com/51533540)  
[WordPress Theme Customizer Custom Controls - WP Engineer](http://wpengineer.com/2527/wordpress-theme-customizer-custom-controls/#more-2527)  

[Easily Adaptable WordPress Loop Templates: Basic Loops, Mullet Loops, and More.. | Perishable Press](https://perishablepress.com/easily-adaptable-wordpress-loop-templates/)

Also see [Widgets](#widgets)

### Query

[Writing Clean, Maintainable Custom WordPress Queries | Tom McFarlin](https://tommcfarlin.com/custom-wordpress-queries/)  
[How To Setup Custom Queries For WP_Query Pagination | Tom McFarlin](https://tommcfarlin.com/wp_query-pagination/)  
[Separation of Concerns: Queries and Helper Functions | Tom McFarlin](https://tommcfarlin.com/separation-of-concerns-with-queries-and-helper-functions/)  

[Mastering WP_Query - Tuts+ Code Tutorials](http://code.tutsplus.com/series/mastering-wp_query--cms-818)

### Settings

[Sanitization with the WordPress Settings API | Tom McFarlin](https://tommcfarlin.com/tag/sanitization-with-the-wordpress-settings-api/)

### ThemeShaper

[The ThemeShaper WordPress Theme Tutorial: 2nd Edition | ThemeShaper](http://themeshaper.com/2012/10/22/the-themeshaper-wordpress-theme-tutorial-2nd-edition/)  
[What Do You Really Need in a WordPress Starter Theme? | ThemeShaper](http://themeshaper.com/2012/01/17/what-do-you-really-need-in-a-wordpress-starter-theme/)  
[Underscores.me — The Best Way To Get Started With The _s Theme | ThemeShaper](http://themeshaper.com/2012/08/15/underscores-me-the-best-way-to-get-started-with-the-_s-theme/)  
[Automattic/_s](https://github.com/automattic/_s)  

### Child Themes

You can easily inherit from an existing theme and override the functions.  
But the theme may not be child friendly (using `get_template_directory()` instead of `get_stylesheet_directory()`, not using templates). And my experience is that overriding files may cause the child theme to breakdown altogether.  
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

[The Complete Guide To The WordPress Settings API - Tuts+ Code Tutorials](http://code.tutsplus.com/series/the-complete-guide-to-the-wordpress-settings-api--cms-624)  
[Making the Perfect WordPress Theme - Tuts+ Code Tutorials](http://code.tutsplus.com/series/making-the-perfect-wordpress-theme--wp-33987)  
[A Walkthrough on Conditional Tags in WordPress - Tuts+ Code Tutorials](http://code.tutsplus.com/series/a-walkthrough-on-conditional-tags-in-wordpress--cms-804)  
[Quick Tips to Boost Your WordPress Website's Speed - Tuts+ Code Tutorials](http://code.tutsplus.com/series/quick-tips-to-boost-your-wordpress-websites-speed--cms-800)  
[WordPress - Tuts+ Code Category](http://code.tutsplus.com/categories/wordpress)  

[A Beginner’s Guide to Using WordPress - Tuts+ Course](http://webdesign.tutsplus.com/courses/a-beginners-guide-to-using-wordpress)  
[The Beginner's Guide to Selecting a WordPress Theme - Tuts+ Code Article](http://code.tutsplus.com/articles/the-beginners-guide-to-selecting-a-wordpress-theme--wp-35032)  

[Trim the Bloat: Keeping WordPress Healthy - Tuts+ Code Tutorials](http://code.tutsplus.com/series/trim-the-bloat-keeping-wordpress-healthy--cms-758)

[Understanding and Working with Content Types in WordPress - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/understanding-and-working-with-content-types-in-wordpress--cms-20937)  
[Understanding and Working with Data in WordPress - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/an-introduction-to-understanding-and-working-with-data-in-wordpress--cms-20567)  
[Understanding and Working with Posts in WordPress - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/understanding-and-working-with-posts-in-wordpress--cms-21032)  
[Understanding and Working with Relationships Between Data in WordPress - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/understanding-and-working-with-relationships-between-data-in-wordpress--cms-20632)  
[Understanding and Working with User Data in WordPress - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/understanding-and-working-with-user-data-in-wordpress--cms-20940)  
