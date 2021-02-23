---
layout: default
title: Setup Google Analytics
parent: Jekyll
grand_parent: Static
nav_order: 2
has_children: false
has_toc: true

---

# Settup Google Analytics tracking on Jekyll page

Depending on the theme you are using, it can be varies. Basically you need to add the GA tracking ID into the `_config.yml` then added into the `<head></head>` somewhere in the html file. 

This particular theme I use just needed to add:
```yml
ga_tracking: G-******
ga_tracking_anonymize_ip: true # Use GDPR compliant Google Analytics settings (true by default)
```
In the `includes/head.html` there's this line to match the `_config.yml` file.

**Other theme might be using different method**

On the `_config.yml` file add:

```yml
# Google services
google_analytics: G-******
```

then add this in the /includes/head.html 
````md
``
<!-- Your head content -->

{% if jekyll.environment == 'production' %}
{% include analytics.html %}
{% endif %}
``
````
