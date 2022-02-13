---
layout: default
title: Drush issues
parent: Drupal
grand_parent: PHP Frameworks
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
## Using MAMP
When using MAMP, for some reason it failed to talk to the MySQL database if you leave the setting as default. Running just simply `drush` or `drush --help` is fine but when it's using the database such as `drush cr` or `drush pm **` it will result:

```bash
In Connection.php line 156:
                                                    
  SQLSTATE[HY000] [2002] No such file or directory  
                                                    

cache:rebuild [--cache-clear [CACHE-CLEAR]] [--no-cache-clear] [-h|--help] [-q|--quiet] [-v|vv|vvv|--verbose] [-V|--version] [--ansi] [--no-ansi] [-n|--no-interaction] [-d|--debug] [-y|--yes] [--no] [--remote-host REMOTE-HOST] [--remote-user REMOTE-USER] [-r|--root ROOT] [-l|--uri URI] [--simulate] [--pipe] [-D|--define DEFINE] [--notify [NOTIFY]] [--druplicon] [--xh-link XH-LINK] [--] <command>
```
### Solution:
On ~/settings.php, change the 
```bash
'host' => 'localhost'
```
to
```bash
'host' => '127.0.0.1',
```
And add the unix socket :
```bash
'unix_socket' => '/Applications/MAMP/tmp/mysql/mysql.sock',
```

Happy drushing!