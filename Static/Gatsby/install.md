---
layout: about
title: Install Gatsby
parent: Gatsby
grand_parent: Static
nav_order: 1
has_children: true
has_toc: true

---

# Install on your local with NPM

Ensure that the `npm` on your machine is up to date

```bash
npm update graceful-fs@latest                                                                      
   ╭───────────────────────────────────────────────────────────────╮
   │                                                               │
   │      New major version of npm available! 6.14.11 → 7.5.6      │
   │   Changelog: https://github.com/npm/cli/releases/tag/v7.5.6   │
   │               Run npm install -g npm to update!               │
   │                                                               │
   ╰───────────────────────────────────────────────────────────────╯

npm install -g npm

```

Then install the `gatsby-cli`

```bash
npm install -g gatsby-cli

```

Then start installing and developing `gatsby` with starter packages that can be found on [this page](https://www.gatsbyjs.com/starters/?v=2) which is like templates for your website.

For example this one called Gatsby Starter Netlify CMS, start with `gatsby new` followed with the name of your project/folder e.g. `blog` then the Github URL of the source to install:

```bash
gatsby new blog https://github.com/gatsbyjs/gatsby-starter-blog
```
This will clone the repo and install Gatsby packages.
```bash
info
Your new Gatsby site has been successfully bootstrapped. Start developing it by running:

  cd blog # --> get in to the folder you setup above
  gatsby develop  # --> starting the gatsby engine
```

