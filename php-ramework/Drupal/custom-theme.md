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
## Steps to create custom theme (e.g. Bootstrap SASS)
1. Install the contributed theme as parent
```bash
composer require drupal/bootstrap_barrio #as the parent
```
this will install the theme under `*/themes/contrib/`
2. Install the starter kit 
```bash
composer require drupal/bootstrap_sass^[version] #installing the starter kit
```
3. Navigate to the folder /themes/contrib/bootstrap_sass and run the  `npm install` and `gulp`
```bash
npm install --global gulp-cli #installing gulp-cli with NPM (ensure that you have installed the latest NPM)
npm install #installing all the dependencies in the folder's package
gulp 
```
It'll show you the progress:
```bash
─ user@macpro ~/dev/drupal-project/app/themes/contrib/bootstrap_sass
╰─ gulp                                                                              ✔  6920  13:49:58 
[13:50:07] Using gulpfile ~/dev/drupal-project/app/themes/contrib/bootstrap_sass/gulpfile.js
[13:50:07] Starting 'default'...
[13:50:07] Starting 'styles'...
[13:50:10] Finished 'styles' after 3.48 s
[13:50:10] Starting 'js'...
[13:50:10] Starting 'serve'...
[Browsersync] Proxying: https://0.0.0.0
[Browsersync] Access URLs:
 -------------------------------------
       Local: https://localhost:3000
    External: https://172.20.10.3:3000
 -------------------------------------
          UI: http://localhost:3001
 UI External: http://localhost:3001
 -------------------------------------
[Browsersync] 3 files changed (bootstrap.min.js, popper.min.js, barrio.js)
[13:50:10] Finished 'js' after 140 ms
[Browsersync] Reloading Browsers... (buffered 3 events)
[13:51:28] Starting 'styles'...
[Browsersync] Reloading Browsers...
[Browsersync] 2 files changed (bootstrap.min.css, style.min.css)
[13:51:32] Finished 'styles' after 3.89 s
[13:56:32] Starting 'styles'...
```
4. Duplicate the starter kit folder 
Once it's all running with SASS, create a custom theme with your own style undr `*\themes\custom\nasigoreng` by copy pasting the starter kit folder above.
Ensure to change the required filenmes and variables.
5. Customise the themplate pages in TWIG under `/themes/custom/nasigoreng/template/` folder
