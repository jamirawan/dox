# Welcome! 

1. [Here's my landing page](https://irawan.io)
2. This page is built for some documentation from mostly issues I found during development and document them
3. Will continously updating

## site.pages

<!-- prettier-ignore-start -->

| source          | link                                                           |
| --------------- | -------------------------------------------------------------- |
{% for page in site.pages -%}
| {{ page.path }} | [{{ page.url | relative_url }}]({{ page.url | relative_url }}) |
{% endfor %}

<!-- prettier-ignore-end -->

## Documents











