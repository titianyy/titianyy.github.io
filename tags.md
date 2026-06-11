---
layout: default
title: Tags
permalink: /tags/
---

<div class="tag-list">
{% for tag in site.tags %}
  {% assign tag_name = tag[0] %}
  {% assign post_count = tag[1].size %}
  <a class="tag-pill" href="{{ tag_name | slugify | prepend: '/tags/' | append: '/' | relative_url }}">
    {{ tag_name }} <span class="tag-count">{{ post_count }}</span>
  </a>
{% endfor %}
</div>
