---
layout: page
permalink: /patents/
title: Patents
description: Granted and pending patents. Edit the list in <code>_data/patents.yml</code>.
nav: true
nav_order: 3
---

{% assign us_granted = site.data.patents.united_states | where: "status", "granted" %}
{% assign us_pending = site.data.patents.united_states | where: "status", "pending" %}
{% assign kr_granted = site.data.patents.korea | where: "status", "granted" %}
{% assign kr_pending = site.data.patents.korea | where: "status", "pending" %}

## United States

{% if us_granted.size > 0 %}
**Granted**
<ul>
{% for p in us_granted %}<li><strong>{{ p.title }}</strong><br>{{ p.number }}{% if p.date %} &middot; {{ p.date }}{% endif %}</li>
{% endfor %}</ul>
{% endif %}

{% if us_pending.size > 0 %}
**Pending / Filed**
<ul>
{% for p in us_pending %}<li><strong>{{ p.title }}</strong><br>{{ p.number }}{% if p.date %} &middot; {{ p.date }}{% endif %}</li>
{% endfor %}</ul>
{% endif %}

## Korea

{% if kr_granted.size > 0 %}
**Granted**
<ul>
{% for p in kr_granted %}<li><strong>{{ p.title }}</strong><br>{{ p.number }}{% if p.date %} &middot; {{ p.date }}{% endif %}</li>
{% endfor %}</ul>
{% endif %}

{% if kr_pending.size > 0 %}
**Pending / Filed**
<ul>
{% for p in kr_pending %}<li><strong>{{ p.title }}</strong><br>{{ p.number }}{% if p.date %} &middot; {{ p.date }}{% endif %}</li>
{% endfor %}</ul>
{% endif %}
