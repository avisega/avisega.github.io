---
layout: page
title: "projects"
permalink: /projects/
description: Selected collection of key academic projects.
nav: true
nav_order: 3
---

<style>
/* Widen this page (al-folio) */
main, .page, .post, .container {
  max-width: min(1200px, 94vw) !important;  /* was narrower; bump the canvas */
}

/* One-row case-study cards */
.projects-qing { margin-top: .5rem; }
.projects-qing .qing-row{
  display:grid;
  grid-template-columns: minmax(320px, 46%) 1fr; /* bigger image (was 38%) */
  gap: 2rem;                                     /* a bit more breathing room */
  align-items: start;
  margin: 1.25rem 0;
  padding: 1.25rem 1.4rem;
  border-radius: 14px;
  box-shadow: 0 4px 16px rgba(0,0,0,.08);
  background: var(--global-bg-color);
}

/* Image sizing */
.projects-qing .qing-img{ align-self:start; overflow:hidden; }
.projects-qing .qing-img img{
  width: 100%;
  height: auto;            /* keep natural aspect ratio */
  object-fit: cover;
  border-radius: 10px;
  display: block;
}

/* Typography (smaller title, cleaner look) */
.projects-qing .qing-title{
  margin: 0 0 .35rem 0;
  font-weight: 800;
  line-height: 1.12;
  letter-spacing: -0.01em;
  font-size: clamp(1.2rem, 0.85rem + 0.8vw, 1.6rem);
}
.projects-qing .qing-sub{
  margin: .15rem 0 .5rem 0;
  opacity: .9;
  font-style: italic;
  font-size: clamp(1.0rem, .9rem + .3vw, 1.1rem);
}
.projects-qing .qing-meta{
  margin: 0 0 .6rem 0;
  opacity: .75;
  font-size: .95rem;
}
.projects-qing .qing-links a{ text-decoration: underline }

/* Mobile */
@media (max-width: 900px){
  .projects-qing .qing-row{ grid-template-columns: 1fr; gap: 1rem; }
}
</style>

<div class="projects-qing">
{% assign items = site.projects | sort: "importance" | reverse %}
{% for p in items %}
  <section class="qing-row">
    <div class="qing-img">
      {% if p.img %}<img src="{{ p.img }}" alt="{{ p.title }}">{% endif %}
    </div>
    <div class="qing-body">
      <h3 class="qing-title">{{ p.title }}</h3>
      {% if p.subtitle %}<p class="qing-sub">{{ p.subtitle }}</p>{% endif %}
      <p class="qing-meta">
        {% if p.year %}{{ p.year }}{% endif %}
        {% if p.category %}{% if p.year %} · {% endif %}{{ p.category }}{% endif %}
        {% if p.role %} · {{ p.role | join: ", " }}{% endif %}
      </p>

      <!-- substantial project text pulled directly from each _projects/*.md file -->
      <div class="qing-desc">
        {{ p.content | markdownify }}
      </div>

      {% if p.links %}
      <p class="qing-links">
        {% if p.links.paper %}<a href="{{ p.links.paper }}" target="_blank" rel="noopener">Paper</a>{% endif %}
        {% if p.links.code %}{% if p.links.paper %} · {% endif %}<a href="{{ p.links.code }}" target="_blank" rel="noopener">Code</a>{% endif %}
        {% if p.links.demo %}{% if p.links.paper or p.links.code %} · {% endif %}<a href="{{ p.links.demo }}" target="_blank" rel="noopener">Demo</a>{% endif %}
        {% if p.links.talk %}{% if p.links.paper or p.links.code or p.links.demo %} · {% endif %}<a href="{{ p.links.talk }}" target="_blank" rel="noopener">Talk</a>{% endif %}
      </p>
      {% endif %}
    </div>
  </section>
{% endfor %}
</div>
