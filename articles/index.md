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
	<li style="height: 250px; border-radius: 15px;">
    <a href="{{ site.url }}{{ post.url }}">
      <div style="background-image: url('{{ site.url }}/images/{{ post.image.feature }}'); width: 100%; height: 100%;  border-radius: 15px;background-size: cover;" >
        <div style=" background: rgba(0, 0, 0, 0.6); height: 100%; border-radius: 15px;">
          <div style=" width: 80%; height: 100%; margin: 0 auto; padding: 10% 5%;">
            <span class="entry-date" style="color: #fff;"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date |   date: "%B %d, %Y" }}</time>
            </span>
            <article style="height: 100%;">
              <div style="font-size: 30px; font-weight: bold; text-align: center; color: #fff; text-shadow: 2px;"> {{ post.title }} {% if post.excerpt %} <span class="excerpt" style="font-size: 16px; font-weight: normal;  color: #fff;margin: 5px 0px; width: 100%;">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}
              </div>
            </article>
          </div>
        </div>
      </div>
    </a>
  </li>
  <br>
{% endfor %}
</ul>
