---
layout: default
title: Using drush
parent: Drupal
grand_parent: PHP Frameworks
nav_order: 6
has_children: false
has_toc: true

---

# Using `drush` command

For a complete use of drush commands run `drush list` or visit documentation page on [Command list](https://www.drush.org/latest/commands/list/)

## Drush list user
Not like WP CLI, Drush doesnt have the command to list all users but there's a way to list based on the role. For example if you wish to list all of the `administrator` users:
```bash
drush uinf --uid=$(drush sqlq "SELECT GROUP_CONCAT(entity_id) FROM user__roles WHERE roles_target_id = 'administrator'")
```
That will give you table of all administrator user role.

To list users from range of ID nubers e.g. 1-200:
```bash
drush user:information --uid="$(echo {1..200},|sed -e 's/ //g')"
```


## Using `drush` within DDEV system

If you are working on local with DDEV, you will have to add `ddev at the front of `drush`:
```bash
ddev drush pm:list
```
Otherwise it will return error connecting database:

```bash
                                                                                                                            
  Command pm:list was not found. Drush was unable to query the database. As a result, many commands are unavailable. Re-run   
  your command with --debug to see relevant log messages.   
  ```

## Using  `drush sql-cli` 

`drush sql-cli` or `drush sqlc` give you a session on the SQL query and search on the tables available.

To use the local `drush` session use the following:
```bash
./bin/drush sql-cli
# instead of just
drush sql-cli
```
This will give you the SQL session:
```bash
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 10380892
Server version: 10.3.27-MariaDB MariaDB Server

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
```
Start searching with some SQL Queries
### to list all table:

```bash
show tables;
```

### to search table with some terms use `like '%[term]%';`
```bash
show table like '%h5p%';
```
If you are looking for any table that contains `h5p` term on them.

### to list a specific table

  