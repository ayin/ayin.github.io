---
layout: default
title: BrainKO
---

<div class="gallery">
	{% for post in site.posts %}
		<div class="item">
			<a class="item-inner" href="{{ post.url }}">
			{% if post.thumbnail != null %}
 				<div class="item-image"><img src="/thumbnails/{{ post.thumbnail }}"></div>
			{% else %}
				<div class="item-image">
  					<iframe
      					width="100%" 
				      	height="100%" 
      					src="{{ post.homepage }}"
					    frameborder="0" 
					    allowfullscreen>
					</iframe>
				</div>
			{% endif %}
				<div class="item-name">{{ post.title }}</div>
			</a>
		</div>
	{% endfor %}
</div>