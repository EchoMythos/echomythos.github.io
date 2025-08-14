---
title: Articles
permalink: /articles/
---


{% include banner.html %}

# All Articles
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      <span style="color:#666; font-size:0.95em;">{{ post.excerpt }}</span>
    </li>
  {% endfor %}
</ul>
