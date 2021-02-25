---
layout: about
title: Theme
parent: Jekyll
grand_parent: Static
nav_order: 3
has_children: false
has_toc: false

---
# Theme

## Installing Jekyll theme

There are two common ways to install themes in Jekyll:
* Fork the Github repo - this will have to fork on `git clone` the repo and use this theme as starting point of your Jekyll install
* Use Ruby `gem` - you can install this on the existing Jekyll install 
** pick the theme you like and get the gem slug to put on the Gemfile e.g: `gem "minimal-mistakes-jekyll"`
** change the theme name on `Gemfile` and update the theme on `_config.yml` files
** run `bundle`
** check your new theme by running
```bash
bundle exec jekyll serve
```

And you should see the theme has changed. Please be aware that you may have some `Build warnings` because themes have different layouts and may scream that the layout required didn't exist. 


