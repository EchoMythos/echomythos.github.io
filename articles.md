---
layout: base
title: Articles
permalink: /articles/
---

<h1>Articles</h1>
<ul>
  {% for post in site.posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
