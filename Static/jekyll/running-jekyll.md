---
layout: default
title: Building contents
parent: Jekyll
grand_parent: Static
nav_order: 5
has_child: false
has_toc: false

---
# Running Jekyll on local

Ensure that the Ruby version is up to date:
Check available version

```bash
rbenv install -l

```
Now confirm:

```bash
ruby -v

```
Should say: ruby 3.2.2
## Install Bundler & Jekyll (Fresh)
Now that you’re in a clean Ruby environment:

```bash
gem install bundler
gem install jekyll

```
Check:

```bash
bundler -v
jekyll -v
```

Install Project Dependencies from inside your Jekyll project:

```bash

bundle install

```
Then run your site:

```bash
bundle exec jekyll serve
```
Then check on browser : 

````bash
Server address: http://127.0.0.1:4000 #this can be different
```

You can use the `npm start` for the shortcut