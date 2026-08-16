---
title: "Research Notes"
permalink: /docs/research-notes/
layout: single
breadcrumbs: false
sidebar:
  nav: "main"
---

<style>
.notes-group{margin-top:1.5em}
.notes-group-title{font-size:1.25em;font-weight:700;margin:2em 0 .6em;padding-bottom:.35em;border-bottom:2px solid #52adc8;display:inline-block;color:#494e52}
.notes-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:1.1em;margin-top:.8em}
.notes-card{background:#fafafa;border:1px solid #f2f3f3;border-radius:6px;padding:1.1em 1.2em;transition:all .18s ease;display:flex;flex-direction:column}
.notes-card:hover{transform:translateY(-3px);box-shadow:0 6px 18px rgba(82,173,200,.18);border-color:#52adc8}
.notes-cat{font-size:.68em;text-transform:uppercase;letter-spacing:.07em;color:#3d8ca6;margin-bottom:.4em}
.notes-card-title{margin:0 0 .4em;font-size:1.02em;line-height:1.35}
.notes-card-title a{color:#494e52;text-decoration:none}
.notes-card-title a:hover{color:#3d8ca6}
.notes-meta{font-size:.78em;color:#777a7d;margin-bottom:.6em}
.notes-ex{font-size:.88em;color:#494e52;margin:0 0 .6em;flex:1}
.notes-more{font-size:.8em;font-weight:600;color:#52adc8}
</style>

Short, informal notes on communication, AI and society — distinct from the formal [Publications](/docs/publications/) page. Planned directions:

- **AI and Society** — how generative AI changes communication; how AI changes knowledge production.
- **Media Effects** — why information shapes human decisions; how algorithms influence attention.
- **Higher Education** — AI literacy in universities; the future of digital learning.

{% assign notes = site.docs | where: "note", "yes" | sort: "date" | reverse %}
{% assign groups = notes | group_by: "category" %}
{% for group in groups %}
<section class="notes-group">
  <h2 class="notes-group-title">{{ group.name }}</h2>
  <div class="notes-grid">
  {% for note in group.items %}
    <article class="notes-card">
      <div class="notes-cat">{{ note.category }}</div>
      <h3 class="notes-card-title"><a href="{{ note.url }}">{{ note.title }}</a></h3>
      <div class="notes-meta">{{ note.date | date: "%d %b %Y" }}</div>
      <p class="notes-ex">{{ note.excerpt }}</p>
      <a class="notes-more" href="{{ note.url }}">Read note &rarr;</a>
    </article>
  {% endfor %}
  </div>
</section>
{% endfor %}
