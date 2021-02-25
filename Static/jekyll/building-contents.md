---
layout: default
title: Building contents
parent: Jekyll
grand_parent: Static
nav_order: 5
has_child: false
has_toc: false

---

# Building contents

## Create post

We can add post manually by adding new .MD file with the name of the post but there's a quick way using `jekyll-compose` plugin.

**Install `jekyll-compose` plugin**
* add the following line inside the `Gemfile`
```Gemfile
gem 'jekyll-compose', group:[:jekyll_plugins]
```
Then in terminal run `bundle` and this will install this plugin. Then add a post:

```bash
bundle exec jekyll post "The title of your post"
```

this will add the .MD file under `/_posts` folder