---
title: 'Leveraging Label Correlations in a Multi-label Setting: A Case Study in Emotion'
collection: publications
permalink: /publication/label-correlations
excerpt: 'We develop two modeling approaches to emotion recognition in order to capture word associations of the emotion words themselves, by either including the emotions in the input, or by leveraging Masked Language Modeling (MLM). Second, we integrate pairwise constraints of emotion representations as regularization terms alongside the classification loss of the models.'
date: 2022-10-28
venue: ''
published: 'review'
paperurl: https://arxiv.org/abs/2210.15842
citation: 'Chochlakis, G., Mahajan, G., Baruah, S., Burghardt, K., Lerman, K. and Narayanan, S., 2022. Leveraging Label Correlations in a Multi-label Setting: A Case Study in Emotion. arXiv preprint arXiv:2210.15842.'
---

<img src="https://gchochla.github.io/images/correlations.png" style="display: block; margin-left: auto; margin-right:auto; width: 90%; height: auto;">
<br>
_Abstract_: Detecting emotions expressed in text has become critical to a range of fields. In this work, we investigate ways to exploit label correlations in multi-label emotion recognition models to improve emotion detection. First, we develop two modeling approaches to the problem in order to capture word associations of the emotion words themselves, by either including the emotions in the input, or by leveraging Masked Language Modeling (MLM). Second, we integrate pairwise constraints of emotion representations as regularization terms alongside the classification loss of the models. We split these terms into two categories, local and global. The former dynamically change based on the gold labels, while the latter remain static during training. We demonstrate state-of-the-art performance across Spanish, English, and Arabic in SemEval 2018 Task 1 E-c using monolingual BERT-based models. On top of better performance, we also demonstrate improved robustness.

[[code](https://github.com/gchochla/Demux-MEmo)]
<br>
<img src="https://gchochla.github.io/images/demux.png" style="display: block; margin-left: auto; margin-right:auto; width: 90%; height: auto;">
<img src="https://gchochla.github.io/images/memo.png" style="display: block; margin-left: auto; margin-right:auto; width: 90%; height: auto;">
<br>


BibTex Citation
-
```
@article{chochlakis2022leveraging,
  title={Leveraging Label Correlations in a Multi-label Setting: A Case Study in Emotion},
  author={Chochlakis, Georgios and Mahajan, Gireesh and Baruah, Sabyasachee and Burghardt, Keith and Lerman, Kristina and Narayanan, Shrikanth},
  journal={arXiv preprint arXiv:2210.15842},
  year={2022}
}
```
