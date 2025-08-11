---
layout: default_with_sidebar
title: Videos
permalink: /video/
---

# Videos
<ul>
  {% assign vids = site.videos | sort: "date" | reverse %}
  {% for v in vids %}
    <li><a href="{{ v.url }}">{{ v.title }}</a></li>
  {% endfor %}
</ul>
