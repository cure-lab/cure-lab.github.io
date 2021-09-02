---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "professor|phd|ra" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'phd' %}
<h3>Phd Students</h3>
 {% elsif role == 'professor' %}
<h3>Professor</h3>
 {% elsif role == 'ra' %}
<h3>Research Staff</h3>
 {% elsif role == 'researchstaff' %}
{% endif %}
</div>
