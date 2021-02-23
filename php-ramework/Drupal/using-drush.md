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
