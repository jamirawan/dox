---
layout: about
title: DDEV
nav_order: 5
has_children: true
has_toc: true

---

# DDEV

[DDEV](https://github.com/drud/ddev) is a container based local and live development. It's making PHP development in Docker simple. We can use DDEV to install Drupal, Wordpress and Typo3.

## Install (MacOX/Linux)

Use Homebrew to install or upgrade the DDEV
```bash
brew tap drud/ddev && brew install ddev
```

To upgrade:
```bash
ddev poweroff && brew upgrade ddev
```

For more detail about installation on other OS visit the [Doc site](https://ddev.readthedocs.io/en/latest/#installation)