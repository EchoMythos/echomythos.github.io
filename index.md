---
layout: base
title: Echo Mythos
---

<div class="tagline">
  <em>Unseen Origins, Infinite Reflections.</em><br>
  Echo Mythos shares cinematic music and visual stories that transcend time and voice.
</div>

<style>
/* Tagline styling */
.tagline {
  text-align: center;
  font-size: 1.25rem;
  margin: 1.5rem auto 2.5rem;
  line-height: 1.4;
}
.tagline em {
  font-style: italic;
  font-weight: 500;
}

/* Override wrapper width */
.page-content .wrapper {
  max-width: none;
  padding: 0;
}

/* Main page grid */
.page-wrap {
  padding-left: 2cm;
  padding-right: 2cm;
}
.em-grid {
  display: grid;
  grid-template-columns: 240px minmax(0, 1fr) 240px;
  column-gap: 2cm;
  row-gap: 2rem;
  align-items: start;
}
.em-main {
  min-width: 0;
}
.em-main .post-item {
  margin: 2rem 0;
}
.em-main .post-item h2 {
  margin-bottom: 0.5rem;
}

/* Mobile responsive layout */
@media (max-width: 1100px) {
  .page-wrap {
    padding-left: 1rem;
    padding-right: 1rem;
  }
  .em-grid {
    grid-template-columns: 1fr;
    column-gap: 0;
  }
}

/* Hide site title in footer */
.site-footer .site-title {
  display: none;
}
</style>

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
