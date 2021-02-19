---
layout: default
title: Drush
parent: Drupal
grand_parent: Frameworks
nav_order: 5
has_children: false
has_toc: true

---

# Drush

## Install Drush on root

Get a `composer` if you haven't already
```bash
curl -sS https://getcomposer.org/installer | php
```
```bash
$mv composer.phar /usr/local/bin/composer
```
```bash
$ln -s /usr/local/bin/composer /usr/bin/composer
```
Download `drush` from git repo
```bash
$git clone https://github.com/drush-ops/drush.git /usr/local/src/drush
```
Get the latest one
```bash
$cd /usr/local/src/drush git checkout master #for the latest one or whatever version you want
```

```bash
$ln -s /usr/local/src/drush/drush /usr/bin/drush
```
```bash
$composer install #if this results in error, run composer update to add the dependencies
```

Check the version

```bash
$drush --version 
```
Have fun with `drush` within the folder where you install Drupal.

