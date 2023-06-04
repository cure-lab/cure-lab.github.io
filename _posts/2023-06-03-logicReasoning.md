---
title: Logic Reasoning with Circuit Learning
header-img: images/projects/logicReasoning.png
categories: projectHome
---

**Logic reasoning techniques for Boolean satisfiability (SAT) problem solving, satisfiability modulo theories (SMT) problem solving or first-order logic proving have enabled substantial advancements in many practical applications, such as verification, routing and program synthesis. For example, the integration of SAT solvers in electronic design automation (EDA) tools has significantly enhanced the formal verification and testing processes in circuit design.**

**Due to the fact that most logic reasoning problems are NP-hard, it is not possible to find a complete solution in polynomial time. As a result, many logic reasoning engines rely on heuristic search techniques to process problem instances that are presented in a standardized format, such as conjunctive normal form (CNF) in SAT solving. Although this approach has achieved impressive performance on benchmarks, it still faces challenges in solving large-scale industrial problems. One of the critical reasons is the dependence of the standardized format, which lacks topological information and contains redundant structures.**

**To address the above issue, we firstly propose to use circuits as an alternative problem format. Circuits offer several advantages: a) contain rich structural information, b) can be simplified by circuit optimization tools, and c) ease of conversion from both the standardized format and the original problem. Secondly, we plan to develop a circuit learning framework that can capture rich and general circuit representations, which will serve as the backbone of this project. Thirdly, we use the information learned from the circuit to guide the heuristic search process. Since circuits can be mapped into the standardized format, this information can be easily integrated into the existing logic reasoning engines. Finally, we intend to transform the circuits to make them easier to solve and process by the logic reasoning engines as equivalent instances.**

**In summary, our goal is to accelerate logic reasoning using circuit learning, analysis, and transformation. Our proposed approaches can be easily combined with existing logic reasoning engines to improve their efficiency.**


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
