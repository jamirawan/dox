---
layout: default
title: Drush issues
parent: Drush
grand_parent: Drupal
nav_order: 8
has_children: false
has_toc: true

---

## Using PHP 8.X

I just updated my local PHP version into 8 and it seems that the PHP8/PHAR updater is abondened. 
Here's what happened when I run `drush status`

```bash
Box Requirements Checker
========================

> Using PHP 8.0.6
> PHP is using the following php.ini file:
  /usr/local/etc/php/8.0/php.ini

> Checking Box requirements:
  ..E.........


 [ERROR] Your system is not ready to run the application.


Fix the following mandatory requirements:
=========================================

 * The package "padraic/humbug_get_contents" requires the version "^5.3 || ^7.0
   || ^7.1 || ^7.2" or greater.

```
This issue was resolved by downloading the latest Drush launcher:
```bash
wget -O /usr/local/bin/drush https://github.com/drush-ops/drush-launcher/releases/latest/download/drush.phar \
    && chmod +x /usr/local/bin/drush

```
Happy drushing!