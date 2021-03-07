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

## Using `wp scaffold -` to start child theme

Running the following `wp cli` will start and create `function.php` and `style.css` to your child theme. E.g child theme name `nasigoreng` with parent `twentytwentyone`

```bash
wp scaffold child-theme nasigoreng --parent_theme=twentytwentyone
```
Then activate the theme:
```bash
wp theme activate nasigoreng
```