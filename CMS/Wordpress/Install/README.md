---
layout: default
title: Install Wordpress
parent: Wordpress
grand_parent: CMS
nav_order: 1
has_children: false
has_toc: true

---
# Install locally with DDEV

For this, you will only need
* Git
* Docker
* Terminal or some sort
* Code editor

**Install DDEV with brew if you haven't already**

```md
brew tap drud/ddev && brew install ddev 
```

## Setup project

```bash
# Create a working folder e.g my-wp-site
mkdir my-wp-site

# Go to new directory
cd my-wp-site

# Configuring the site
ddev config --project-type=wordpress --docroot=web --create-docroot

#Launch the little one
ddev start
ddev composer create roots/bedrock
```