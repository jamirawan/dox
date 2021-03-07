---
layout: default
title: Child theme
parent: Wordpress
grand_parent: CMS
nav_order: 4
has_children: false
has_toc: true

---

# Child theme

Child theme is pretty much using an available theme on the market, whether it's free or not but renaming it yourself and change the styling to your need. Most of the file are still dependent on the parent theme. 
The core requirement for child theme is `function.php` and `style.css`. And `screenshot.png` if you wish. 
This is recommended if you would like to change some styling on the theme you purchase or download so that when the parent is updated, the styling you changed are still there.

## The `function.php` file for child theme:

```php
<?php
add_action( 'wp_enqueue_scripts', 'my_theme_enqueue_styles' );
function my_theme_enqueue_styles() {

    $parent_style = 'parent-style'; // This is 'parent-theme-style' for the Nasi Goreng theme.

    wp_enqueue_style( $parent_style, get_template_directory_uri() . '/style.css' );
    wp_enqueue_style( 'child-style',
        get_stylesheet_directory_uri() . '/style.css',
        array( $parent_style ),
        wp_get_theme()->get('Version')
    );
}
?>
```

## The `style.css` file

Here's the `style.css` that you can modify or add styling for your child theme

```css
/*
 Theme Name:   Nasi Goreng
 Theme URI:    http://irawan.id.au
 Description:  Nasi Goreng theme
 Author:       Nasi Goreng theme
 Author URI:   http://irawan.id.au
 Template:     parent-theme
 Version:      1.0.0
 License:      GNU General Public License v2 or later
 License URI:  http://www.gnu.org/licenses/gpl-2.0.html
 Tags:         light, dark, two-columns, right-sidebar, responsive-layout, accessibility-ready
 Text Domain:  topend
*/

/* add your custom style below */

@media screen and (max-width: 580px){
        #site-branding{
                margin: 0 60px 0 60px;
                width: calc(55% - 120px);
        }
        p {
                font-size:1.3rem !important;
                font-weight:500;
        }
        .top-tel .mobile-clear {
            padding-bottom:20px;
        }
}
@media screen and (max-width: 480px){
        #site-branding{
                margin: 0 60px 0 60px;
                width: calc(55% - 120px);
        }
        p {
                font-size:1.3rem !important;
                font-weight:500;
        }
        .top-tel .mobile-clear {
            padding-bottom:20px;
        }
}

.top-cart .item-count {
    background: #e9fd06;
}
```


## Using `wp scaffold -` to start child theme

Running the following `wp cli` will start and create `function.php` and `style.css` to your child theme. E.g child theme name `nasigoreng` with parent `twentytwentyone`

```bash
wp scaffold child-theme nasigoreng --parent_theme=twentytwentyone
```
Then activate the theme:
```bash
wp theme activate nasigoreng
```