<!-- # All Notes -->
<ul>
  {% for post in site.pages %}
    {% if post.title and post.url != "/" and post.layout != nil %}
      <li dir="auto">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
</ul>