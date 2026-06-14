---
layout: page
title: Projects
permalink: /projects/
description: Selected research and AI systems projects. Click a card for details.
nav: true
nav_order: 1
horizontal: false
---

<div class="projects">
  <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3">
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
