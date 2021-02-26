---
layout: default
title: Building contents
parent: Jekyll
grand_parent: Static
nav_order: 5
has_child: false
has_toc: false

---

# Building contents

{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Create page

We can add post manually by adding new .MD file with the name of the post but there's a quick way using `jekyll-compose` plugin.

**Install `jekyll-compose` plugin**

Add the following line inside the `Gemfile`

```Gemfile
gem 'jekyll-compose', group:[:jekyll_plugins]
```
Then in terminal run `bundle` and this will install this plugin. Then add a post:

```bash
bundle exec jekyll page "The title of your page"
```

this will create `the-title-of-your-page.md` file, then you can edit it and adjust the `Front matter` part.

## Create posts

We can also create post for blogging if your template has the post layout:

```bash
bundle exec jekyll post "Woohoo post"
```

This will create the `2020-02-20-woohoo-post.md` and to check the page, run the serve and URL structure will be `/2020/02/20/woohoo-post.html`.

You can define the URL structure with categories on the `front matter` and matched with the layout file.
