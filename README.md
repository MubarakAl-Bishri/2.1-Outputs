%% > Add "layout: default" to the front matter.
- [IQ-EQ-KQ-etc Are All The Same](./IQ-EQ-KQ-etcAllTheSame.md)
- [Life Should Note Be Hard](./LifeShouldNotBeHard.md) %%
# All Notes 
<ul> 
	{% for post in site.pages %} 
		{% if post.title and post.url != "/" %} 
			<li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li> 
		{% endif %}
	{% endfor %} 
</ul>