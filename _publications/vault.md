---
title: 'VAuLT: Augmenting the Vision-and-Language Transformer for Sentiment Classification on Social Media'
collection: publications
permalink: /publication/vault
excerpt: 'We propose the Vision-and-Augmented-Language Transformer (VAuLT). VAuLT is an extension of the popular Vision-and-Language Transformer (ViLT), with the key insight being to propagate the output representations of a large language model like BERT to the language input of ViLT.'
date: 2022-10-28
venue: ''
published: 'review'
paperurl: https://arxiv.org/abs/2208.09021
citation: 'Chochlakis, G.; Srinivasan, T.; Thomason, J.; and Narayanan, S. 2022. VAuLT: Augmenting the Vision-and-Language Transformer with the Propagation of Deep Language Representations. arXiv preprint arXiv:2208.09021.'
---

<img src="https://gchochla.github.io/images/vault.png" style="display: block; margin-left: auto; margin-right:auto; width: 90%; height: auto;">
<br>
_Abstract_: We propose the Vision-and-Augmented-Language Transformer (VAuLT). VAuLT is an extension of the popular Vision-and-Language Transformer (ViLT), and improves performance on vision-and-language (VL) tasks that involve more complex text inputs than image captions while having minimal impact on training and inference efficiency. ViLT, importantly, enables efficient training and inference in VL tasks, achieved by encoding images using a linear projection of patches instead of an object detector. However, it is pretrained on captioning datasets, where the language input is simple, literal, and descriptive, therefore lacking linguistic diversity. So, when working with multimedia data in the wild, such as multimodal social media data, there is a notable shift from captioning language data, as well as diversity of tasks. We indeed find evidence that the language capacity of ViLT is lacking. The key insight of VAuLT is to propagate the output representations of a large language model (LM) like BERT to the language input of ViLT. We show that joint training of the LM and ViLT in VAuLT can yield relative improvements up to 20% over ViLT on VL tasks involving richer language inputs and affective constructs, such as for Target-Oriented Sentiment Classification in TWITTER-2015 and TWITTER-2017, and Sentiment Classification in MVSA-Single and MVSA-Multiple.

[[code](https://github.com/gchochla/VAuLT)]

BibTex Citation
-
```
@article{chochlakis2022vault,
  author = {Chochlakis, Georgios and Srinivasan, Tejas and Thomason, Jesse and Narayanan, Shrikanth},  
  title = {VAuLT: Augmenting the Vision-and-Language Transformer for Sentiment Classification on Social Media},
  journal={arXiv preprint arXiv:2208.09021},
  year = {2022},
}
```
