---
layout: page
title: How-Tos
excerpt: "An archive of how-to blog posts sorted by date."
search_omit: true
image:
  feature: front-page.jpg
---

<ul class="post-list">
{% for post in site.categories.blog %} 
  <li style="height: 40%; border: 2px solid black; border-radius: 30px;">
  	<div class="row">
  		<div class="col-sm-6" style="margin: 30px;">
  			<img src="{{ site.url }}/images/{{ post.image.feature }}" alt="{{ post.title }}">
  		</div>
  		<div class="col-sm-6" style="margin: 0 40px;">
		  	<article>
		  		<a href="{{ site.url }}{{ post.url }}"> {{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}
		  		</a>
		  	</article>
	  	</div>
  	</div>
  </li>
  <br>
{% endfor %}
</ul>
