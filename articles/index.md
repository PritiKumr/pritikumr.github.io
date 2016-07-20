---
layout: page
title: Articles
excerpt: "An archive of articles sorted by date."
search_omit: false
image:
  feature: cover-photo.jpg
---

<ul class="post-list">
{% for post in site.categories.articles %} 
	<li style="height: 40%; border: 2px solid black; border-radius: 30px;">
  	<div class="row">
      <div style="margin: 1% 5%;">
        <a href="{{ site.url }}{{ post.url }}">
         <img src="{{ site.url }}/images/{{ post.image.feature }}" alt="{{ post.title }}">
        </a>
      </div>
      <div style="margin: 1% 10%;">
        <article>
          <a href="{{ site.url }}{{ post.url }}" style="font-size: 20px; font-weight: bold;"> {{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt" style="font-size: 14px; font-weight: normal; margin: 5px 0px; width: 100%;">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}
          </a>
        </article>
      </div>
    </div>
  </li>
  <br>
{% endfor %}
</ul>
