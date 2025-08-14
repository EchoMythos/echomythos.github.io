---
layout: base
title: Echo Mythos
---

<div class="tagline">
  <em>Unseen Origins, Infinite Reflections.</em><br>
  Echo Mythos shares cinematic music and visual stories that transcend time and voice.
</div>

<style>
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
</style>



    <!-- MAIN: Articles -->
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
      <ul>
        {% for post in site.posts %}
          <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
        {% endfor %}
        {% if site.posts == empty %}<li>No articles yet.</li>{% endif %}
      </ul>
    </aside>
  </div>
</div>
