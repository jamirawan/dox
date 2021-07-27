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
Following are some random use of `drush` I picked up, for complete list check out their website.

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
*Start searching with some genral SQL queries*

### to list all table:

```bash
show tables;
```
Note that this will be a very big list if you have a big website

### to search table with some terms use `like '%[term]%';`
```bash
show tables like '%path%';
```
If you are looking for any tables that contains `url` term on them. Dont miss the semicolon (;)
The result should be a list tables with url on them
```
+--------------------------------------------+
| Tables_in_wi_cdu_sandbox (%path%)          |
+--------------------------------------------+
| path_table_set                             |
| irawan_path__background_colour             |
| irawan__table_with_path                    |
| path_alias                                 |
| path_alias_revision                        |
+--------------------------------------------+
5 rows in set (0.00 sec)

```

### to see the list a specific table
Listing all of `path_alias` or URL on the website

```bash
select*from path_alias
```

Then you will have the list of all of the URLs on your website. You can narrow it down by selecting the type with `CONCAT`
Listing all URL with content types:
```bash
select nid, type, alias from node_field_data nfd inner join path_alias ua on CONCAT('/node/', nid) = path;

```

Result:
```bash
+-------+--------------------+---------------------------------------+
| nid   | type               | alias                                 |
+-------+--------------------+---------------------------------------+
|   391 | basic              | /home                                 |
|   443 | basic              | /about                                |
|   444 | basic              | /contact                              |
|   445 | blog               | /the-healthy-nasi-goreng              |
|   447 | blog               | /my-experience-eating-nasi-goreng     | 
|   391 | blog               | /nasi-goreng-is-great                 |
|   443 | blog               | /about-nasi-goreng                    |
|   444 | blog               | /where-can-i-buy-nasi-goreng          |
|   445 | blog               | /the-healthy-nasi-goreng              |
|   447 | blog               | /my-experience-eating-nasi-goreng     |   
+-------+--------------------+---------------------------------------+
```
To see the list of one particular `type`, e.g. `blog` run the following (assuming you are still in `sqlc` session:
```bash
select nid, type, alias from node_field_data nfd inner join path_alias ua on CONCAT('/node/', nid) = path and type = 'blog';

```
Result:
```bash
+-------+--------------------+---------------------------------------+
| nid   | type               | alias                                 |
+-------+--------------------+---------------------------------------+
|   445 | blog               | /the-healthy-nasi-goreng              |
|   447 | blog               | /my-experience-eating-nasi-goreng     | 
|   391 | blog               | /nasi-goreng-is-great                 |
|   443 | blog               | /about-nasi-goreng                    |
|   444 | blog               | /where-can-i-buy-nasi-goreng          |
|   445 | blog               | /the-healthy-nasi-goreng              |
|   447 | blog               | /my-experience-eating-nasi-goreng     |   
+-------+--------------------+---------------------------------------+
```