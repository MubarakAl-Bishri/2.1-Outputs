# All Notes 
<ul> 
	{% for post in site.pages %} 
		{% if post.title and post.url != "/" %} 
			<li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li> 
		{% endif %}
	{% endfor %} 
</ul>


