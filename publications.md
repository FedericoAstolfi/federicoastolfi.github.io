---
title: Publications
layout: default
description: Publications, preprints, and conference talks by Federico Astolfi.
---

# Publications

<ul class="pub-list">
{% for p in site.data.publications.papers %}
    <li class="pub-item">
        <div class="pub-year">{{ p.year }}</div>
        <div class="pub-details">
            <strong>{{ p.title }}</strong><br>
            <span class="pub-authors">{{ p.authors }}</span><br>
            <span class="pub-authors">{{ p.venue }}</span>
            {% if p.abstract %}<p class="pub-abstract">{{ p.abstract }}</p>
            <button class="pub-toggle">▸ Show more</button>{% endif %}
            {% if p.links %}<div class="pub-links">
                {% for l in p.links %}<a href="{{ l.url }}" target="_blank" class="pub-link-btn">{{ l.label }}</a>{% endfor %}
            </div>{% endif %}
        </div>
    </li>
{% endfor %}
</ul>

---

# Thesis

<ul class="pub-list">
{% for p in site.data.publications.thesis %}
    <li class="pub-item">
        <div class="pub-year">{{ p.year }}</div>
        <div class="pub-details">
            <strong>{{ p.title }}</strong><br>
            <span class="pub-authors">{{ p.authors }}</span><br>
            <span class="pub-authors">{{ p.venue }}</span>
            {% if p.abstract %}<p class="pub-abstract">{{ p.abstract }}</p>
            <button class="pub-toggle">▸ Show more</button>{% endif %}
            {% if p.links %}<div class="pub-links">
                {% for l in p.links %}<a href="{{ l.url }}" target="_blank" class="pub-link-btn">{{ l.label }}</a>{% endfor %}
            </div>{% endif %}
        </div>
    </li>
{% endfor %}
</ul>

---

# Talks &amp; Posters

<div class="talks-timeline">
{% for t in site.data.publications.talks %}
    <div class="talk-item">
        <div class="talk-date">{{ t.date }}</div>
        <div class="talk-details">
            <strong>{{ t.title }}</strong><br>
            <span class="talk-conf">{{ t.conf }}</span><br>
            {% if t.meta %}<span class="talk-meta">{{ t.meta }}</span><br>{% endif %}
            <span class="talk-authors">{{ t.authors }}</span>
            {% if t.abstract %}<p class="talk-abstract">{{ t.abstract }}</p>{% endif %}
        </div>
    </div>
{% endfor %}
</div>
