---
layout: default
title: Tree
parent: OSX CLI
nav_order: 2
has_children: false
has_toc: false

---

# Tree

Shows you the file structure with tree lines.

## Install

Install with homebrew:
```bash
brew install tree
```

Install with Macports:
```bash
sudo port install tree
```

If you have Fink:
```bash
fink install tree
```

## Using `tree`

Example below, in `static-sites` folder, run:
```bash
tree
```

Then it will show you the file structure:

```bash
static-sites
├── Gatsby
│   ├── README.md
│   ├── building-site.md
│   ├── install.md
│   └── publish-netlify-cms.md
├── Hugo
│   └── README.md
├── README.md
└── jekyll
    ├── building-contents.md
    ├── configure.md
    ├── custom-domain.md
    ├── front-matter.md
    ├── google-analytics.md
    ├── install.md
    ├── publish-to-netlify.md
    ├── readme.md
    └── theme.md

```