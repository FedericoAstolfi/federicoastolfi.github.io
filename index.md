---
title: Home
layout: default
---

<section class="content">
    <h3>Latest news</h3>
    <div class="carousel news-carousel">
        <div class="carousel-track">
        {% for n in site.data.news.items %}
            <div class="carousel-slide" style="background-image:url('{{ n.image | relative_url }}')">
                <div class="carousel-body">
                    <div class="news-meta">
                        {% if n.badge %}<span class="news-badge {{ n.badge_class }}">{{ n.badge }}</span>{% endif %}
                        {% if n.date %}<span class="news-date">{{ n.date }}</span>{% endif %}
                    </div>
                    <h4>{{ n.title }}</h4>
                    {% if n.venue %}<p class="news-venue">{{ n.venue }}</p>{% endif %}
                    {% if n.text %}<p>{{ n.text }}</p>{% endif %}
                    {% if n.link %}<a href="{{ n.link | relative_url }}"{% if n.link contains '//' %} target="_blank"{% endif %}>{{ n.link_label | default: 'Read more' }} →</a>{% endif %}
                </div>
            </div>
        {% endfor %}
        </div>
        <div class="carousel-nav">
            <button class="carousel-btn carousel-prev">&#8249;</button>
            <button class="carousel-btn carousel-next">&#8250;</button>
        </div>
        <div class="carousel-dots">
        {% for n in site.data.news.items %}
            <button class="carousel-dot{% if forloop.first %} active{% endif %}" data-index="{{ forloop.index0 }}"></button>
        {% endfor %}
        </div>
    </div>
</section>
