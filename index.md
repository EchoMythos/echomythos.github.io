---
layout: base
title: Echo Mythos
---

**Unseen Origins, Infinite Reflections.**  
Echo Mythos shares cinematic music and visual stories that transcend time and voice.

<style>
/* 3-column grid: left sidebar, main, right sidebar */
.em-grid {
  display: grid;
  grid-template-columns: 260px 1fr 260px;
  gap: 2rem;
  align-items: start;
}
.em-left, .em-right { border-left: 1px solid #e5e5e5; padding-left: 1rem; }
.em-left { border-left: none; padding-left: 0; }
.em-main .post-item { margin: 2rem 0; }
.em-main .post-item h2 { margin: 0 0 .5rem; }

/* Stack on mobile */
@media (max-width: 900px){
  .em-grid { grid-template-columns: 1fr; }
  .em-left, .em-right { border-left: none; padding-left: 0; }
}
</style>

<div class="em-grid">
  <!-- LEFT SIDEBAR: Videos -->
  <aside class="em-left">
    <h3>Videos</h3>
    <ul style="margin:0; padding-left:1rem;">
      {% assign vids = site.videos | sort: "date" | reverse %}
      {% for v in vids %}
        <li><a href="{{ v.url | relative_url }}">{{ v.title }}</a></li>
      {% endfor %}
      {% if site.videos == empty %}<li>No videos yet.</li>{% endif %}
    </ul>
  </aside>

  <!-- MAIN: single-column list of articles with Read more -->
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

  <!-- RIGHT SIDEBAR: quick article links -->
  <aside class="em-right">
    <h3>Articles</h3>
    <ul style="margin:0; padding-left:1rem;">
      {% for post in site.posts %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
      {% endfor %}
      {% if site.posts == empty %}<li>No articles yet.</li>{% endif %}
    </ul>
  </aside>
</div>
