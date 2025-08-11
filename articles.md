---
layout: default_with_sidebar
title: Articles
permalink: /articles/
---

# All Articles
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      <span style="color:#666; font-size:0.95em;">{{ post.excerpt }}</span>
    </li>
  {% endfor %}
</ul>
