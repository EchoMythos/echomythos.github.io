---
title: Articles
permalink: /articles/
layout: none
---

{% include header.html %}
{% include banner.html %}

# All Articles

<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 1.5em;">
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      <span style="color:#666; font-size:0.95em;">{{ post.excerpt }}</span>
    </li>
  {% endfor %}
</ul>
