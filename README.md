# All Notes 
<ul> 
	{% for post in site.pages %} 
		{% if post.title and post.url != "/" %} 
			<li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li> 
		{% endif %}
	{% endfor %} 
</ul>


> You can create branches and add things to review them, select what you show and what to not, and more. 
> Costume CSS to matchs Obsidian theme. Like callouts.