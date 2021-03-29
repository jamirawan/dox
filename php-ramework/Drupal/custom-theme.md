---
layout: default
title: Custom theme
parent: Drupal
grand_parent: PHP Frameworks
nav_order: 4
has_children: false
has_toc: true

---

# Drupal Custom Theme

## Info

Your theme name info.yml file will define the custom theme. This file should be located in your custom theme name folder. If your theme name is `nasigoreng` this hould be in `/themes/custom/nasigoreng/nasigoreng.info.yml`

Example of a `.info.yml file`

```yml
name: Nasi Goreng
type: theme
description: Spicy Nasi Goreng Theme 
core_version_requirement: ^8 || ^9
base theme: classy
screenshot: nasigoreng.png

libraries:
  - irawan_garden/ig-css
  - irawan_garden/quicksand
  - irawan_garden/normalize

regions:
  header: Header
  highlighted: Highlighted
  help: Help
  content: Content
  sidebar_first: Left sidebar
  sidebar_second: Right sidebar
  front: Front page blocks
  footer: Footer
  page_top: Page top
  page_bottom: Page bottom

```
Following are the key value that are compulsory for the `theme.info.yml`
Required:
    * name (required)
    * type (required)
    * core (required, optional if you include core_version_requirement)
    * base theme (required in Drupal 9, optional for Drupal 8)

Optional    
    * php (optional)
    * version (optional)
    * libraries (optional)
    * libraries-override (optional)
    * libraries-extend (optional)
    * hidden (optional)
    * engine (optional)
    * logo (optional)
    * screenshot (optional)
    * regions (optional)
    * regions_hidden (optional)
    * features (optional)
    * ckeditor_stylesheets (optional)
