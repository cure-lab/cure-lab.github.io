---
title: HybridRepair：Towards Annotation-Efficient Repair for Deep Learning Models
header-img: images/projects/HybridRepair-framework.png
categories: AISecurity
---

A well-trained deep learning (DL) model often cannot achieve the expected performance after deployment due to the mismatch between the distributions of the training data and the field data in the operational environment. Therefore, repairing DL models is critical, especially when deployed on increasingly larger tasks with shifted distributions.Generally speaking, it is easy to obtain a large amount of field data. Existing solutions develop various techniques to select a subset for annotation and then fine-tune the model for repair. While effective, achieving a higher repair rate is inevitably associated with more expensive labelling costs. 

To mitigate this problem, we propose a novel annotation-efficient repair solution for DL models, namely HybridRepair, wherein we take a holistic approach that coordinates the use of a small amount of annotated data and a large amount of unlabeled data for repair. Our key insight is that accurate yet sufficient training data is needed to repair the corresponding failure region in the data distribution. Under a given labelling budget, we selectively annotate some data in failure regions and propagate their labels to the neighbouring data on one hand. On the other hand, we take advantage of the semi-supervised learning (SSL) techniques to further boost the training data density. How- ever, different from existing SSL solutions that try to use all the unlabeled data, we only use a selected part of them considering the impact of distribution shift on SSL solutions. Experimental results show that HybridRepair outperforms both state-of-the-art DL model repair solutions and semi-supervised techniques for model improvements, especially when there is a distribution shift be- tween the training data and the field data


<hr>

##### 1. The Overview of Hybrid Repair
<img width="100%" src="{{site.baseurl}}/images/projects/HybridRepair-framework.png" data-action="zoom">

<hr>

##### 2. Sample selection and labeling algorithm
<img width="100%" src="{{site.baseurl}}/images/projects/HybridRepair-algorithm.png" data-action="zoom">

<hr>

##### 3. Comparison with baselines w.r.t the model accuracy after repair (%).
<img width="100%" src="{{site.baseurl}}/images/projects/HybridRepair-result1.png" data-action="zoom">

<hr>

```
@inproceedings{li2022hybridrepair,
  title={HybridRepair: towards annotation-efficient repair for deep learning models},
  author={Li, Yu and Chen, Muxi and Xu, Qiang},
  booktitle={Proceedings of the 31st ACM SIGSOFT International Symposium on Software Testing and Analysis},
  pages={227--238},
  year={2022}
}
```
