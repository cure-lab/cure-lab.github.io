---
title: Publication
permalink: /publications/
---

{% assign pubs = site.publications %}

<div>
{% for pub in pubs %}
<li>{{ pub.title}}</li>
{% endfor %}
</div>