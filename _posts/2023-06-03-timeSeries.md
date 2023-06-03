---
title: Time Series Analysis
header-img: images/projects/timeSeries.png
categories: projectHome
---

**Time series analysis is a crucial field in data analysis and forecasting, widely used in various domains such as finance, weather forecasting, and industrial process control. Traditionally, researchers have treated time series as sequential data and applied transformer models to address these problems. However, we believe that transformers are not suitable for time series tasks due to several reasons.**

**Firstly, the attention mechanism in transformers only captures the correlation between tokens, lacking the ability to extract the temporal relationships present in time series data. Secondly, transformers rely on positional embeddings to represent relative position information, which cannot effectively capture the temporal nature of the data. Lastly, tokenizing time series data is often meaningless since it typically contains multiple data points from different channels on a single timestamp.**

**In response to these limitations, our project aims to challenge the prevailing notion of using transformer-based models for time series analysis. We have developed a groundbreaking model called DLinear, which employs a simple linear combination in the temporal domain. Surprisingly, DLinear consistently outperforms other transformer-based methods in time series forecasting tasks.**

**Furthermore, we have shifted our focus to the frequency domain, considering time series as samples of signals from real-world physical systems. To enhance the performance of time series forecasting models, we have devised FrAug, a frequency domain augmentation method tailored specifically for this task. FrAug effectively boosts the predictive capabilities of time series forecasting models.**

**Moving forward, our research team plans to delve deeper into multiple time series analysis problems, including probabilistic forecasting and forecasting as a generative task. We are also enthusiastic about exploring the application of our findings in various domains, enabling advancements in fields such as finance, climate science, and health care.**

<hr>

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'timeSeries' %}
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
