---
layout: default
title: Blog
---

# Blog

{% if site.posts.size > 0 %}
  <ul class="post-list">
    {% for post in site.posts %}
      <li class="card">
        <h3>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No posts yet. Check back soon!</p>
{% endif %}

<style>
.post-list {
    list-style: none;
    padding: 0;
}

.post-list li {
    margin-bottom: 2rem;
}

.post-list h3 {
    margin-bottom: 0.5rem;
}

.post-list h3 a {
    color: #667eea;
    text-decoration: none;
}

.post-list h3 a:hover {
    text-decoration: underline;
}

.post-meta {
    color: #666;
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
}
</style>
