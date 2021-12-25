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
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
## info.yml file

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
  - nasigoreng/ig-css
  - nasigoreng/quicksand
  - nasigoreng/normalize

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

## Custom theme file structure
```bash
|-core
|  |-modules
|  |-themes
|  |  |-bartik
|  |  |-seven
  ..
|-modules
|-themes
|  |-contrib
|  |  |-zen
|  |  |-basic
|  |  |-bluemarine
|  |-custom
|  |  |-nasigoreng
```
## Folder structure
The folder and file structure of the custom themes
```bash
|-nasigoreng.breakpoints.yml
|-nasigoreng.info.yml
|-nasigoreng.libraries.yml
|-nasigoreng.theme
|-config
| |-install
  | |-nasigoreng.settings.yml
  |-schema
  | |-nasigoreng.schema.yml
|-css
  | |-style.css
|-js
  | |-nasigoreng.js
|-images
  | |-buttons.png
|-logo.svg
|-screenshot.png
|-templates
| |-maintenance-page.html.twig
| |-node.html.twig
```