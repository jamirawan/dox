---
layout: default
title: Local install
parent: Drupal
grand_parent: Frameworks
nav_order: 1
has_children: false
has_toc: true

---
# Install local machine

## With DDEV

DDEV is a local development tool that requires Docker and make it easy to setup and run the local Drupal site. Assuming you are all setup with [Docker]({{ site.baseurl }}{% link Docker/README.md %}) and composer on your machine, here's how I set it up.

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

## Setting up with Composer and Drush

```bash
# Create project directory e.g. /web-app
mkdir web-app

# Go to directiry
cd web-app

#Configure the project type and document root
ddev config --project-type=drupal8 --docroot=web --create-docroot

# Start container
ddev start

# Create project
ddev composer create "drupal/recommended-project:^8"

#Install Drush
ddev composer require drush/drush

# Install site
ddev drush site:install -y

# Get the local login URL
ddev drush uli

# Or launch the local site
ddev launch
```

**Other way to setup**
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
With this setup, you dont have to worry about creating database, database user etc it will be setup in Docker containers.
