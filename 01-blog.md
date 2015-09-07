---
layout: post
current: blog
permalink: blog.html
---

{% for post in site.posts  %}
<h1>{{ post.title }}</h1>
<h4>{{post.date | date: '%B %d, %Y'}}</h4>
{% assign page.title = post.title %}
{{ post.content }}
<hr>
{% endfor %}
