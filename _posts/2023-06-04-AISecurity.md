---
title: AI Safety and Security
header-img: images/projects/aisecurity.png
categories: projectHome
---

<!-- **Exploring the defects of AI systems, particularly generative models used for image generation, holds paramount importance in advancing the field and enhancing model performance. Understanding and addressing these defects not only helps us identify areas for improvement but also provides valuable insights into the limitations and potential biases of the models. By actively investigating and mitigating these issues, we can create more reliable and trustworthy AI systems.**

**Exploring defects provides an opportunity for continuous learning and refinement. By thoroughly analyzing the failure cases and weaknesses of generative models, we can extract valuable knowledge about the underlying factors contributing to these issues. This knowledge can then be leveraged to design novel algorithms, techniques, and architectures to overcome the identified challenges. Through a progressive approach that embraces the knowledge gained from defects, we can iteratively improve the performance of generative models, pushing the boundaries of what is possible in text-to-image generation.** -->

**Recent advancements in machine learning models have led to significant progress in computer vision tasks. However, these models still exhibit certain limitations and vulnerabilities that hinder their performance in critical scenarios. Specifically, they are (1) susceptible to systematic failures on subsets of data that involve rare cases, out-of-distribution samples (OODs), and hard cases with specific patterns. (2) Moreover, they are vulnerable to anomalous inputs, such as adversarial examples (AEs), where imperceptible perturbations can deceive deep neural networks (DNNs) into making incorrect predictions. These limitations and vulnerabilities pose a substantial threat to the applications of DNNs in safety-critical domains, such as autonomous driving, where unreliable predictions can lead to catastrophic accidents.**
<!-- 
**While there has been a vast body of research to defend against AEs or OODs, to the best of our knowledge, they all suffer from some weaknesses, e.g., defending against only a subset of AEs or OODs or causing a relatively high accuracy loss for legitimate inputs. Moreover, most of the existing solutions cannot defend against adaptive attacks, wherein attackers are knowledgeable about the defense mechanisms and craft adversarial examples accordingly.** -->

**We present a series of defense frameworks to protect DNNs against the aforementioned threats across various tasks. At a high level, our approaches take the outputs from DNNs as feedback and the employ the concept of semantic input validation with generative models to identify AEs and OODs.  More concretely, we perform the input validation by feeding both the input and the predictions  to a generative model like GAN or Stable Diffusion, to obtain a synthetic output and then comparing it to the original input. For legitimate inputs that are correctly inferred, the synthetic output attempts to reconstruct the input. On the contrary, for AEs or OODs, instead of reconstructing the input, the synthetic output would be created to conform to the wrong predictions whenever possible. Consequently, by validating the distance between the input and the synthetic output, we can distinguish AEs or OODs from legitimate inputs.**

**In addition to only detecting OODs and AEs, we are also committed to utilizing these samples to enhance our models. Firstly, we investigate test input prioritization, which aims to identify "high-quality" test instances from a vast amount of unlabeled data. By selecting these instances, we can reveal more model failures with less labeling effort, thereby improving the efficiency of identifying and mitigating limitations in the model's performance. Secondly, we explore active learning techniques, which involve selecting a budget of unlabeled data that can best enhance the model's performance after human annotation and model retraining. Thirdly, we also delve into failure discovery and reasoning, which aims to identify human-understandable visual attributes or specific patterns that contribute to model failures. Understanding these factors is crucial for researchers to enhance their models. Lastly, we develop several defense frameworks that safeguard DNNs against adversarial examples or out-of-distribution samples, thereby bolstering the resilience of the models in the face of potential attacks.**

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

