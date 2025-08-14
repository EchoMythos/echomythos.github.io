---
title: Articles
permalink: /articles/
layout: none
---

{% include header.html %}
{% include banner.html %}

# All Articles

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2em; padding: 2em 0;">
  {% for post in site.posts %}
    <div style="flex: 0 0 300px; text-align: center;">
      <a href="{{ post.url | relative_url }}">
        <img src="{{ post.thumbnail }}" alt="{{ post.title }} thumbnail" style="width: 100%; height: auto; border-radius: 8px;" />
      </a>
      <h3 style="margin-top: 0.5em;"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p style="color: #666;">{{ post.excerpt }}</p>
    </div>
  {% endfor %}
</div>
