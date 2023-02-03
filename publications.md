---
title: Publication
permalink: /publications/
---

### **Recent Papers**
For full paper list, please refer to Prof. Xu's [Google Scholar](https://scholar.google.com/citations?user=eSiKPqUAAAAJ&hl=zh-CN) page.
<hr>
<div class="content list">
{% assign publication_sorted = site.publications | sort: 'time' | reverse %}
  {% for post in publication_sorted %}

    <div class="list-item">
      <p class="list-post-title">
       
            <div class="row">
                <div class="col-sm-4">
                    <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}">
                </div>
                <div class="col-sm-8">
                    <h4 >
                        {{ post.title }}
                    </h4>
                
                    <p class="list-detail" >

                      <i>{{ post.citation }}</i>
                      <br>
                      {{ post.conference }}
                      <br>
                      {% if post.description %}
                      {{ post.description }}
                      {% endif %}
                      <br>
                      {% if post.paper-link %}
                      <a href="{{ post.paper-link }}">[paper]</a>
                      {% endif %}
                      {% if post.code-link %}
                      <a href="{{ post.code-link }}">[code]</a>
                      {% endif %}
                    </p>
                </div>
            </div>
           
     
      </p>
    </div>

  {% endfor %}
</div>
