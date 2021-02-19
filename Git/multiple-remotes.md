---
layout: default
title: Multiple remotes
parent: Git
has_children: false
has_toc: true

---

# Working with Git multiple remotes

Working in between two big companies that have their own environments and each using different pipelines put me in to a situation where I have to understand and work with two git remotes, one with Github and the other with Gitlab

So the structure will be like this for example:

```bash
$git remote -v                                                                     
origin	git@github.com:company1/project-name.git (fetch)
origin	git@github.com:company1/project-name.git (push)

upstream	git@gitlab.com:company2/project-name.git (fetch)
upstream	git@gitlab.com:company2/project-name.git (push)
```
Each company will have different environment setup altough this result in one production environment.