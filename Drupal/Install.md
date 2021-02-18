---
layout: default
title: Local install
parent: Drupal
nav_order: 1
has_children: false
has_toc: true

---
# Install local machine

## With DDEV

DDEV is a local development tool that requires Docker and make it easy to setup and run the local Drupal site. Assuming you are all setup with Docker and composer on your machine, here's how I set it up.

**Install DDEV on your machine**

```bash
curl -L https://raw.githubusercontent.com/drud/ddev/master/scripts/install_ddev.sh | bash
```
Or with Homebrew:
```bash
brew tap drud/ddev && brew install ddev
```

To check your `ddev` version:
```bash
ddev -v
```

**Setup your Drupal project**
Use `composer` to setup your Drupal project. Say we name this `web-app` (replace with your own project name)

```bash
# Replace web-app!
export SITE_NAME=web-app
composer create-project drupal/recommended-project $SITE_NAME
cd $SITE_NAME
```

And setup your project:

```bash
ddev config --docroot=web --project-name=$SITE_NAME --project-type=drupal8
```

Start the container by running

```bash
ddev start 
```

**Install Drupal**

And start intalling the site with your credentials:

```bash
ddev exec drush site-install --account-name=admin --account-pass=my-password

```