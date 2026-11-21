---
layout: single
title: 分类
permalink: /categories/
---

{% include blog-topics.html %}

{% for category in site.categories %}
  {% assign name = category | first %}
  {% unless site.blog_categories contains name %}
    {% assign slug = name | slugify %}
- [{{ name }}]({{ '/categories/' | append: slug | append: '/' | relative_url }})
  {% endunless %}
{% endfor %}
