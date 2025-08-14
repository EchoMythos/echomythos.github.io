---
title: Videos
permalink: /videos/
---

{% include header.html %}
{% include banner.html %}

# All Videos

<ul>
  {% for video in site.videos %}
    <li style="margin-bottom: 1.5em;">
      <a href="{{ video.url }}">{{ video.title }}</a><br>
      <span style="color:#666; font-size:0.95em;">{{ video.excerpt }}</span>
    </li>
  {% endfor %}
</ul>
