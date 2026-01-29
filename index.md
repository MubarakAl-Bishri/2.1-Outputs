---
layout: default
title: All Notes
---

<!-- # All Notes -->

<ul>
</ul>
  {% if site.notes and site.notes.size > 0 %}
    {% assign list = site.notes | sort: 'title' %}
    {% for note in list %}
      {% if note.title and note.published != false %}
        <li dir="auto">
          <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
        </li>
      {% endif %}
    {% endfor %}
  {% else %}
    <ul>
      {% for page in site.pages %}
        {% if page.title and page.url != "/" and page.layout != nil and page.published != false and page.path != "README.md" %}
          <li dir="auto">
            <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
          </li>
        {% endif %}
      {% endfor %}
    </ul>
  {% endif %}
</ul>
