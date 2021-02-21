---
layout: default
title: Running WP CLI
parent: Wordpress
grand_parent: CMS

nav_order: 2
has_children: false
has_toc: true

---

# Running WP CLI

When all setup with the WP CLI, you can use command started with `wp` followed by the subcommands. To see the list of subcommands, just type `wp` or `wp --help` or if you wish to know the list of sub-sub-commands, for example `wp user` run `wp user --help` and it will list the sub sub commands.


For example, if I want to see the list of themes installed on my WP build, I just type the `wp` followed with subcommand `theme` then the task command `list` :

```bash
wp theme list
```

It will give you list of the theme:
```bash
+-----------------+----------+--------+---------+
| name            | status   | update | version |
+-----------------+----------+--------+---------+
| twentyeleven    | inactive | none   | 3.6     |
| twentyfifteen   | inactive | none   | 2.8     |
| twentyfourteen  | inactive | none   | 3.0     |
| twentynineteen  | inactive | none   | 1.9     |
| twentyseventeen | inactive | none   | 2.5     |
| twentysixteen   | inactive | none   | 2.3     |
| twentyten       | inactive | none   | 3.2     |
| twentythirteen  | inactive | none   | 3.2     |
| twentytwelve    | inactive | none   | 3.3     |
| twentytwenty    | inactive | none   | 1.6     |
| twentytwentyone | active   | none   | 1.1     |
+-----------------+----------+--------+---------+
```

To activate or deactivate theme: `wp` followed with sub command `theme` then the task command  `activate` then the object which is the theme name e.g. `twentytwenty`

```bash
 wp theme activate twentytwenty 
```

It will switch the theme from `twentytwentyone` to `twentytwenty`

```bash
Success: Switched to 'Twenty Twenty' theme.
```
