---
layout: post
current: blog
permalink: blog.html
---


{% for post in site.categories.2015  %}
<h1>{{ post.title }}</h1>
<h4>{{post.date | date: '%B %d, %Y'}}</h4>
{% assign page.title = post.title %}
{{ post.content }}
<hr>
{% endfor %}
