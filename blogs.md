---
layout: page
title: Blogs
permalink: /blogs/
---

I usually write blogs to record my work. The topics include but not limited to the development of research ideas, programming skills in Python, experience in competitions, etc. Here is the full list of my blog posts.

<ul class="listing">
{% for post in site.posts %}
	{% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
		{% if year != y %}
			{% assign year = y %}
			<li class="listing-seperator">{{ y }}</li>
		{% endif %}
		<li class="listing-item">
		<time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
		<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
	</li>
{% endfor %}
</ul>
