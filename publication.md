---
title: Publication
permalink: /publication/
---

{% assign publication = site.publication %}

{% for pub in publication %}
<li>{{ pub.title}}
{% endfor %}