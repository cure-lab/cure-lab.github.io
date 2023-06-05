---
title: Text-to-Image Generation
header-img: images/projects/text2imgGen.png
categories: projectHome
---

Generative AI has emerged as an indispensable facet of modern artificial intelligence, holding the promise of transformative changes across various sectors, from creative arts and entertainment to scientific research and technology development. By generating new content that mimics or complements existing data, generative AI can unlock new realms of possibilities, facilitating the creation of realistic synthetic data, innovative designs, and more.

However, despite its potential, current generative AI models often face significant limitations. For example, the generation process can be unstable or lack control, leading to outputs that do not meet user expectations or requirements. This is particularly evident in the domain of text-to-image generation, where the challenge lies in effectively translating arbitrary textual descriptions into visually appealing and contextually coherent images. Given these limitations, there is a compelling need for continued research to refine and enhance the capabilities of generative AI, with a particular emphasis on creating more efficient, robust, and user-friendly text-to-image generation models.

We plan to tackle this problem in the following aspects. First, we acknowledge the importance of high-quality datasets and hence aim to focus on a data-centric approach, developing methodologies for curating and refining datasets that accurately represent the complexities of real-world scenarios. Second, we intend to develop a novel object-oriented generation methodology. Given a text-image pair, this approach aims to learn not only the entire scene, but also focus on individual objects and object relations. Thus, it dramatically enhances both the effectiveness and efficiency of learning, thereby improving the quality and precision of generated images. Lastly, recognizing that continual learning is key to the evolution of any model, we integrate an error-oriented active learning strategy. This strategy will allow us to continually identify and address the model's weaknesses, further enhancing its performance and adaptability. Through these concerted efforts, we aim to bring significant advancements to the field of text-to-image generation, and later expand to other exciting generative AI field, such as text-to-3D and text-to-video generation.

<hr>

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'text2imageGen' %}
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
