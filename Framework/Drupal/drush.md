---
layout: default
title: Drush
parent: Drupal
grand_parent: Framework
nav_order: 5
has_children: false
has_toc: true

---

# Drush

## Install Drush on root

```bash
curl -sS https://getcomposer.org/installer | php
```
```bash
$mv composer.phar /usr/local/bin/composer
```
```bash
$ln -s /usr/local/bin/composer /usr/bin/composer
```
```bash
$git clone https://github.com/drush-ops/drush.git /usr/local/src/drush
```
```bash
$cd /usr/local/src/drush git checkout master (for the latest one or whatever version you want)
```
```bash
$ln -s /usr/local/src/drush/drush /usr/bin/drush
```
```bash
$composer install #if this results in error, run composer update to add the dependencies
```

```bash
$drush --version 
```

