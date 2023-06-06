---
title: Logic Reasoning with Circuit Learning
header-img: images/projects/logicReasoning.png
categories: projectHome
---

This project proposes a novel approach to enhance the efficiency of logic reasoning engines, particularly those used for solving the Boolean satisfiability (SAT) problem, satisfiability modulo theories (SMT) problem, or first-order logic proving. These reasoning techniques have had significant impacts on various practical applications like verification, routing, and program synthesis.

The primary challenges these engines face stem from the NP-hard nature of most logic reasoning problems, which makes it impractical to find a complete solution in polynomial time. These engines traditionally rely on heuristic search techniques and process problem instances in a standardized format, such as conjunctive normal form (CNF) in SAT solving. However, this approach has its limitations, particularly when it comes to solving large-scale industrial problems. One critical issue is the dependence on the standardized format, which can lack topological information and contain redundant structures.

To address these challenges, the project proposes several key strategies:

1.**Circuits as Alternative Problem Format**: The project first proposes to use circuits as an alternative problem format. Unlike the standardized formats, circuits contain rich structural information, can be simplified using circuit optimization tools, and can be easily converted from both the standardized format and the original problem.

2.**Circuit Learning Framework**: The project aims to develop a circuit learning framework to capture rich and general circuit representations, serving as the backbone of the project.

3.**Guided Heuristic Search**: The information learned from the circuit will be used to guide the heuristic search process. Given that circuits can be mapped into the standardized format, this information can be easily integrated into existing logic reasoning engines.

4.**Circuit Transformation**: The project also plans to transform the circuits into forms that are easier for the logic reasoning engines to solve and process as equivalent instances.

In summary, the project's goal is to boost logic reasoning efficiency using circuit learning, analysis, and transformation. The proposed approaches are designed to integrate easily with existing heuristic-based engines, enhancing their overall efficiency.


<hr>

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'logicReasoning' %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ post.url | prepend: site.baseurl }}">
            <div class="row">
                <div class="col-sm-4">
                    <img src="/{% if post.header-img %}{{ post.header-img }}{% else %}{{ site.header-img }}{% endif %}">
                </div>
                <div class="col-sm-8">
                    <h3 class="post-title">
                        {{ post.title }}
                    </h3>
<!--                     <p class="list-post-title">
                      posted on {{ post.date | date: "%B %-d, %Y" }}
                    </p> -->
                    <p class="list-detail" >
                      {{ post.content | strip_html | truncatewords:30 }}
                    </p>
                </div>
            </div>
            <hr/>
        </a>
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>
