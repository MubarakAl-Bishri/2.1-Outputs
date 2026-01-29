# All Notes
---
<ul>
  {% for post in site.posts %}
    <li dir="auto">
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
