---
layout: default
title: Git errors and the solutions
parent: Git
has_children: false
nav_order: 3
has_toc: true

---

# Operation must be in a work tree


Error:
```
fatal: this operation must be run in a work tree

```
This error below happend when somehow the git is as a `bare` and no working tree. 


Run this and it will fix the issue

```bash
git config --unset core.bare

```