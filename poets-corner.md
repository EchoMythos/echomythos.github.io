---
title: Poets Corner
permalink: /poets-corner/
layout: none
---

{% include header.html %}
{% include banner.html %}

# Poets Corner

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 2em; padding: 2em 0;">
  {% for poet in site.poets %}
    <div style="flex: 0 0 300px; text-align: center;">
      <a href="{{ poet.url | relative_url }}">
        <img src="{{ poet.thumbnail }}" alt="{{ poet.title }} thumbnail" style="width: 100%; height: auto; border-radius: 8px;" />
      </a>
      <h3 style="margin-top: 0.5em;"><a href="{{ poet.url | relative_url }}">{{ poet.title }}</a></h3>
      <p style="color: #666;">{{ poet.excerpt }}</p>
    </div>
  {% endfor %}
</div>
