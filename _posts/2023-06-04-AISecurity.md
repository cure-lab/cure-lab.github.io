---
title: AI Safety and Security
header-img: images/projects/aisecurity.png
categories: projectHome
---

<!-- **Exploring the defects of AI systems, particularly generative models used for image generation, holds paramount importance in advancing the field and enhancing model performance. Understanding and addressing these defects not only helps us identify areas for improvement but also provides valuable insights into the limitations and potential biases of the models. By actively investigating and mitigating these issues, we can create more reliable and trustworthy AI systems.**

**Exploring defects provides an opportunity for continuous learning and refinement. By thoroughly analyzing the failure cases and weaknesses of generative models, we can extract valuable knowledge about the underlying factors contributing to these issues. This knowledge can then be leveraged to design novel algorithms, techniques, and architectures to overcome the identified challenges. Through a progressive approach that embraces the knowledge gained from defects, we can iteratively improve the performance of generative models, pushing the boundaries of what is possible in text-to-image generation.** -->

Despite the remarkable advancement of deep learning (DL) techniques in the past decade, certain inherent shortcomings and vulnerabilities persist, undermining the performance of these models in critical situations. First and foremost, DL models are prone to systematic failures when handling subsets of data involving unusual cases, out-of-distribution samples, and complex scenarios. Secondly, they are vulnerable under carefully-crafted malicious inputs, such as adversarial examples, where minuscule perturbations can mislead deep neural networks into making erroneous predictions. These flaws and susceptibilities raise serious concerns regarding the deployment of deep neural networks in domains where safety is paramount, e.g., autonomous driving and medical systems.
<!-- 
**While there has been a vast body of research to defend against AEs or OODs, to the best of our knowledge, they all suffer from some weaknesses, e.g., defending against only a subset of AEs or OODs or causing a relatively high accuracy loss for legitimate inputs. Moreover, most of the existing solutions cannot defend against adaptive attacks, wherein attackers are knowledgeable about the defense mechanisms and craft adversarial examples accordingly.** -->

We introduce a collection of defense frameworks designed to safeguard deep neural networks from the risks outlined previously, applicable across a variety of tasks. Our strategies fundamentally use the outputs from deep neural networks as feedback, and incorporate the principle of semantic input validation with generative models to detect adversarial examples and out-of-distribution samples. In more detail, we conduct this input validation by supplying both the input and the predictions to a generative model, such as a Generative Adversarial Network or Stable Diffusion. This generates a synthetic output, which we then compare to the original input. For legitimate inputs that are correctly inferred, the synthetic output attempts to reconstruct the input. On the contrary, for AEs or OODs, instead of reconstructing the input, the synthetic output would be created to conform to the wrong predictions whenever possible. Consequently, by validating the distance between the input and the synthetic output, we can distinguish AEs or OODs from legitimate inputs.

We also devote ourselves to enhancing model performance by pioneering new test and debugging methods. To start, we delve into test input prioritization, a technique designed to pinpoint "high-quality" test instances from a large volume of unlabeled data. Through this selection, we can uncover more model failures with less labeling effort, thereby streamlining the process of identifying and addressing the model's performance shortfalls. Next, we investigate active learning strategies, which involve choosing a set amount of unlabeled data that, following human annotation and model retraining, could most effectively boost the model's performance. In addition, we engage in failure discovery and reasoning, a process aimed at identifying visual attributes or specific patterns that are comprehensible to humans and that contribute to model failures. Gaining an understanding of these factors is vital for researchers aiming to improve their models.

<hr>

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'AISecurity' %}
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

