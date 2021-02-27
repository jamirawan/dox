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
| nasigoreng      | active   | none   | 1.1     |
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

**Running in DDEV environment**

If you are running the WP install in DDEV environment, add `ddev` before `wp`

```bash
ddev wp theme activate twentytwenty
```

Or else if will return error connecting database:
```bash
Error: Error establishing a database connection.
```

## `wp scaffold`

`wp scaffold` will help us create some codes for creating:
* child theme
* post types
* custom plugins starter
* taxonomy
* created theme based on [Underscores](https://underscores.me/)

To use the `wp scaffold` just add the subcommands and the name. Example below is creating child theme from `twentytwenty`:

```bash
wp scaffold child-theme nasi-goreng --parent_theme=twentytwenty
```

To create a custom theme starter based on `_s` Undrescore, theme name `nasi-goreng`:
```bash
wp scaffold _s my-theme --theme_name="Nasi Goreng" --author="Emperor Nasi Goreng"
```

If the command above didn't work and give you this message ;
```bash
Error: Could not decompress your theme files ('/tmp/underscores-aede5jGF.tmp') at '/path-to-your-folder/wp/wp-content/themes': Incompatible Archive.
```

just go to the [Underscores website](https://underscores.me/) and generate it from the form, then download and install like a usual WP theme install.


## `wp search-replace` 

This will search through the database rows of tables and replace the first string with second one. This command uses tables that are registerd in `$wpdb` 

Example, I want to replace all `nasi` terms and replace them with `goreng`:
```bash
wp search-replace nasi goreng
```

Recommended to use `--dry run` to be sure of what you are doing, just to show you the changes that will be made before confirming the action.

And it will show you the number of changes made:
```bash
+------------------+-----------------------+--------------+------+
| Table            | Column                | Replacements | Type |
+------------------+-----------------------+--------------+------+
| woop_commentmeta   | meta_key              | 0            | SQL  |
| woop_commentmeta   | meta_value            | 0            | SQL  |
| woop_comments      | comment_author        | 0            | SQL  |
| woop_comments      | comment_author_email  | 0            | SQL  |
| woop_comments      | comment_author_url    | 0            | SQL  |
| woop_comments      | comment_author_IP     | 0            | SQL  |
| woop_comments      | comment_content       | 0            | SQL  |
| woop_comments      | comment_approved      | 0            | SQL  |
| woop_comments      | comment_agent         | 0            | SQL  |
| woop_comments      | comment_type          | 0            | SQL  |
| woop_links         | link_url              | 0            | SQL  |
| woop_links         | link_name             | 0            | SQL  |
| woop_links         | link_image            | 0            | SQL  |
| woop_links         | link_target           | 0            | SQL  |
| woop_links         | link_description      | 0            | SQL  |
| woop_links         | link_visible          | 0            | SQL  |
| woop_links         | link_rel              | 0            | SQL  |
| woop_links         | link_notes            | 0            | SQL  |
| woop_links         | link_rss              | 0            | SQL  |
| woop_options       | option_name           | 0            | SQL  |
| woop_options       | option_value          | 8            | PHP  |
| woop_options       | autoload              | 0            | SQL  |
| woop_postmeta      | meta_key              | 0            | SQL  |
| woop_postmeta      | meta_value            | 0            | SQL  |
| woop_posts         | post_content          | 2            | SQL  |
| woop_posts         | post_title            | 0            | SQL  |
| woop_posts         | post_excerpt          | 0            | SQL  |
| woop_posts         | post_status           | 0            | SQL  |
| woop_posts         | comment_status        | 0            | SQL  |
| woop_posts         | ping_status           | 0            | SQL  |
| woop_posts         | post_password         | 0            | SQL  |
| woop_posts         | post_name             | 0            | SQL  |
| woop_posts         | to_ping               | 0            | SQL  |
| woop_posts         | pinged                | 0            | SQL  |
| woop_posts         | post_content_filtered | 0            | SQL  |
| woop_posts         | guid                  | 4            | SQL  |
| woop_posts         | post_type             | 0            | SQL  |
| woop_posts         | post_mime_type        | 0            | SQL  |
| woop_term_taxonomy | taxonomy              | 0            | SQL  |
| woop_term_taxonomy | description           | 0            | SQL  |
| woop_termmeta      | meta_key              | 0            | SQL  |
| woop_termmeta      | meta_value            | 0            | SQL  |
| woop_terms         | name                  | 0            | SQL  |
| woop_terms         | slug                  | 0            | SQL  |
| woop_usermeta      | meta_key              | 0            | SQL  |
| woop_usermeta      | meta_value            | 0            | PHP  |
| woop_users         | user_login            | 0            | SQL  |
| woop_users         | user_nicename         | 0            | SQL  |
| woop_users         | user_email            | 0            | SQL  |
| woop_users         | user_url              | 1            | SQL  |
| woop_users         | user_activation_key   | 0            | SQL  |
| woop_users         | display_name          | 0            | SQL  |
+------------------+-----------------------+--------------+------+
Success: Made 15 replacements.
```

