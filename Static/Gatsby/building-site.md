---
layout: about
title: Building the site
parent: Gatsby
grand_parent: Static
nav_order: 2
has_children: true
has_toc: true

---

# Running in local machine

If you happen to work on a new computer and just `git clone` the Gatsby repository from Github, i wont be straight away worked. You might have to do the following:

**Update NPM**
```bash
 ERROR 

   ╭───────────────────────────────────────╮
   │                                       │
   │   Update available 2.19.1 → 2.19.2    │
   │   Run npm i -g gatsby-cli to update   │
   │                                       │
   ╰───────────────────────────────────────╯
```
And run `npm install` there might be some issues during this update with `vulnerabilities` in the packates, so we need to run `npm audit fix`.

After this, you should be good running `gatsby develop`
