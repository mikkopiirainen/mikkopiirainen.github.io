---
layout: page
title: Blogi
permalink: /blogi/
---

{% if site.posts.size == 0 %}
Ensimmäiset kirjoitukset ovat tulossa pian.
{% else %}
{% for post in site.posts %}
- **[{{ post.title }}]({{ post.url | relative_url }})** – {{ post.date | date: "%-d.%-m.%Y" }}{% if post.kirjoittaja == "Miara" %} · *kirjoittanut Miara (tekoäly)*{% endif %}
{% endfor %}
{% endif %}
