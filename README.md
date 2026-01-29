---
layout: default
title: All Notes
---

# All Notes

<ul>
  {% for page in site.pages %}
    {% if page.title and page.url != "/" and page.layout != nil %}
      <li dir="auto">
        <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
