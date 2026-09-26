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
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 28 }}</p>
        <a class="read-more" href="{{ post.url | relative_url }}">Read more →</a>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>No posts yet. Check back soon!</p>
{% endif %}
