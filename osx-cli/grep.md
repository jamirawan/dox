---
layout: default
title: Grep
parent: OSX CLI
nav_order: 1
has_children: false
has_toc: false

---

# grep

`grep` let you search one or more input files for lines containing a match to a specified pattern. By default the outputs the matching lines.

## Search in file

We can use `grep` to search term in file(s)
1. Specify which file you wish to search. Use `grep` followed by the `search term` and file locetion,then it shoud be 	
```bash
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

```bash
   E.g:
$ grep gatsby README.md    

```	





