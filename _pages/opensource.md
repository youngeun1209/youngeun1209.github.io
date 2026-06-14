---
layout: page
title: Software & Datasets
permalink: /open-source/
description: Open-source software and publicly released datasets.
nav: true
nav_order: 4
---

## Software

<div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1rem;margin:1.2rem 0 2rem">
{% for p in site.data.projects.software %}
  <div class="card" style="padding:1.1rem;height:100%">
    <h3 style="margin:0 0 .25rem;font-size:1.15rem"><a href="{{ p.url }}" target="_blank">{{ p.name }}</a></h3>
    {% if p.highlight %}<div style="font-size:.78rem;opacity:.7;margin-bottom:.55rem">{{ p.highlight }}</div>{% endif %}
    <p style="margin:0 0 .85rem;font-size:.92rem">{{ p.description }}</p>
    <a href="{{ p.url }}" target="_blank" style="font-size:.9rem"><i class="fa-brands fa-github"></i> GitHub</a>
  </div>
{% endfor %}
</div>

## Datasets

<div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1rem;margin:1.2rem 0">
{% for p in site.data.projects.datasets %}
  <div class="card" style="padding:1.1rem;height:100%">
    <h3 style="margin:0 0 .25rem;font-size:1.15rem"><a href="{{ p.url }}" target="_blank">{{ p.name }}</a></h3>
    {% if p.highlight %}<div style="font-size:.78rem;opacity:.7;margin-bottom:.55rem">{{ p.highlight }}</div>{% endif %}
    <p style="margin:0 0 .85rem;font-size:.92rem">{{ p.description }}</p>
    <a href="{{ p.url }}" target="_blank" style="font-size:.9rem"><i class="fa-solid fa-database"></i> Dataset</a>
    {% if p.paper %}&nbsp;&nbsp;<a href="{{ p.paper }}" target="_blank" style="font-size:.9rem"><i class="fa-solid fa-file-lines"></i> Paper</a>{% endif %}
  </div>
{% endfor %}
</div>
