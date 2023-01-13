---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' | reverse %}
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
<h3>Principle Investigator</h3>
  </div>
<div class="content list people">
  <div class="list-item-people">
        <p class="list-post-title">
          <a href="{{ site.baseurl }}/qiang_xu.html "><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/qiang_xu1.jpg"></a>
  <a class="name" href="/">Qiang Xu</a>
           </p>
      </div>
</div>
<hr>

  {% continue %}
 {% elsif role == 'ra' %}
<h3>Research Staff</h3>
 {% elsif role == 'researchstaff' %}
<h3>Research Staff</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
 {% elsif role == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif role == 'others' %}
<h3>Honorary Members</h3>
 {% elsif role == 'alumni' %}

{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">

          {% if profile.website %}
             {% assign this_url = profile.website | absolute_url %}
          {% else %}
              {% assign this_url = profile.url | prepend: site.baseurl %}
          {% endif %}
          {% if profile.avatar %}
            <a href="{{ this_url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
             <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ this_url }}">{{ profile.name }}</a>

        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}


{% endif %}
{% endfor %}
