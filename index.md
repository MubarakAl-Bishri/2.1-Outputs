---
layout: default
title: All Notes
---

<!-- # All Notes -->

<ul>
  {% assign _seen_urls = "" %}
  {% if site.notes and site.notes.size > 0 %}
    {% assign list = site.notes | sort: 'title' %}
    {% for note in list %}
      {% if note.title and note.published != false %}
        {% assign note_url = note.url | relative_url %}
        {% unless _seen_urls contains note_url %}
          <li dir="auto">
            <a href="{{ note_url }}">{{ note.title }}</a>
          </li>
          {% assign _seen_urls = _seen_urls | append: note_url | append: "," %}
        {% endunless %}
      {% endif %}
    {% endfor %}
  {% else %}
    {% for page in site.pages %}
      {% if page.title and page.url != "/" and page.layout != nil and page.published != false and page.path != "README.md" %}
        {% assign page_url = page.url | relative_url %}
        {% unless _seen_urls contains page_url %}
          <li dir="auto">
            <a href="{{ page_url }}">{{ page.title }}</a>
          </li>
          {% assign _seen_urls = _seen_urls | append: page_url | append: "," %}
        {% endunless %}
      {% endif %}
    {% endfor %}
  {% endif %}
</ul>
