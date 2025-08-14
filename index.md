---
layout: base
title: Echo Mythos - Home
---

<div class="tagline">
  <em>Unseen Origins, Infinite Reflections.</em><br>
  Echo Mythos shares cinematic music and visual stories that transcend time and voice.
</div>

<div class="page-wrap">
  <div class="em-grid">
    <!-- LEFT SIDEBAR: Videos -->
    <aside class="em-left">
      <h3>Videos</h3>
      <ul style="margin:0; padding-left:1rem;">
        {% assign vids = site.videos | sort: "date" | reverse %}
        {% for v in vids %}
          <li><a href="{{ v.url | relative_url }}">{{ v.title }}</a></li>
        {% endfor %}
        {% if site.videos == empty %}
          <li>No videos yet.</li>
        {% endif %}
      </ul>
    </aside>

    <!-- MAIN CONTENT: Latest Articles -->
    <main class="em-main">
      <h2>Latest Articles</h2>
      {% for post in site.posts %}
        <article class="post-item">
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <div>{{ post.excerpt }}</div>
          <p><a href="{{ post.url | relative_url }}">Read more →</a></p>
        </article>
      {% endfor %}
      {% if site.posts == empty %}
        <p>No articles yet — add one in <code>_posts/</code>.</p>
      {% endif %}
    </main>

    <!-- RIGHT SIDEBAR: Quick article links -->
    <aside class="em-right">
      <h3>Articles</h3>
      <ul style="margin:0; padding-left:1rem;">
        {% for post in site.posts %}
          <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
        {% endfor %}
        {% if site.posts == empty %}
          <li>No articles yet.</li>
        {% endif %}
      </ul>
    </aside>
  </div>
</div>

