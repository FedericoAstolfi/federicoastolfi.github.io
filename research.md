---
title: Research
layout: default
permalink: /research/
description: Research lines of Federico Astolfi — quantum optimal control and quantum error correction.
---

<section class="content">
    <p class="eyebrow">Research</p>
    <h1 class="research-title">What I'm working on</h1>
    <p class="research-intro">Two lines of work at the intersection of quantum optimal control and quantum error correction. Each page is a running story — the big picture, the developments, and the papers as they land.</p>

    <div class="research-cards">
    {% for line in site.data.research.lines %}
        <a class="research-card" href="{{ '/research/' | append: line.id | append: '/' | relative_url }}">
            <h3>{{ line.title }}</h3>
            <p class="research-card-tagline">{{ line.tagline }}</p>
            <div class="research-card-papers">
            {% for item in line.papers %}{% if item.status %}
                <div class="paperrow">
                    <span class="paperrow-title">{{ item.title }}</span>
                    {% case item.status %}
                        {% when 'published' %}<span class="badge b-pub">Published</span>
                        {% when 'preprint' %}<span class="badge b-pre">Preprint</span>
                        {% when 'in-preparation' %}<span class="badge b-prep">In preparation</span>
                        {% when 'planned' %}<span class="badge b-plan">Planned</span>
                    {% endcase %}
                </div>
            {% endif %}{% endfor %}
            </div>
            <span class="research-more">Read the story →</span>
        </a>
    {% endfor %}
    </div>
</section>
