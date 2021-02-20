---
layout: default
title: WP CLI
parent: Wordpress
grand_parent: CMS
nav_order: 2
has_children: false
has_toc: true

---

# WP-CLI - Wordpress Command Line Interface

With WP-CLI you can manage and update core, plugins, users, themes and many more without using browsers.

**Requirements**
* UNIX-like environment
* PHP 5.6 or later
* WP core version 3.7 or later

## Installation 

Donload the `wp-cli.phar` file:
```bash
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
```
Check if it's working:

```bash
php wp-cli.phar --info
```

To be able to use the command: `wp`, make this file executable:
```bash
chmod +x wp-cli.phar
```

Move it in your working file somewhere:
```bash
sudo mv wp-cli.phar /usr/local/bin/wp
```

Check if it works:

```bash
wp --info
```

Or check your WP version
```bash
wp core version
```

**Note**

If you are working on a shared hosting where you don't have the `sudo` access to the root and they don't install WP-CLI, you still can use this but not with `wp` alias. Use the following for this example `wp core version` :
```bash
php wp-cli.phar core version
```