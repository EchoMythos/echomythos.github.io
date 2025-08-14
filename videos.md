---
title: Videos
permalink: /videos/
layout: none
---

{% include header.html %}
{% include banner.html %}

# All Videos

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2em; padding: 2em 0;">
  {% for video in site.videos %}
    <div style="flex: 0 0 300px; text-align: center;">
      <a href="{{ video.url | relative_url }}">
        <img src="{{ video.thumbnail }}" alt="{{ video.title }} thumbnail" style="width: 100%; height: auto; border-radius: 8px;" />
      </a>
      <h3 style="margin-top: 0.5em;"><a href="{{ video.url | relative_url }}">{{ video.title }}</a></h3>
      <p style="color: #666;">{{ video.excerpt }}</p>
    </div>
  {% endfor %}
</div>
