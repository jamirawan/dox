---
layout: default
title: Custom domain
parent: Jekyll
grand_parent: Static
nav_order: 9
has_child: false
has_toc: false

---

# Publishing on your own domain

You can publish your Jekyll site that you build in Github page to your own domain name. Here's the two steps:
1. On your domain side Zone Editor, add A records pointing to Github
2. On the Github side - add CNAME file and adjust the settings

## On the domain side
Login to your Domain CPanel or client console and navigate to the Zone editors and add 4 A records with the following IPs:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```
[See Github page for more details](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)

Check it in your terminal with `dig`

```bash
dig YOURDOMAIN.COM.AU +noall +answer
YOURDOMAIN.COM.AU.		4122	IN	A	185.199.108.153
YOURDOMAIN.COM.AU.  	4122	IN	A	185.199.111.153
YOURDOMAIN.COM.AU.		4122	IN	A	185.199.109.153
YOURDOMAIN.COM.AU.		4122	IN	A	103.208.219.11
YOURDOMAIN.COM.AU.		4122	IN	A	185.199.110.153
```

It may take a moment to settle these up.

