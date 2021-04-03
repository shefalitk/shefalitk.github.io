---
title: 'End-to-end Generative Zero-shot Learning via Few-shot Learning'
collection: publications
permalink: /publication/e2e-gen-zsl-via-fsl
excerpt: 'Reducing Zero-shot Learning to Few-shot Learning using the generator of a generative Zero-shot Learning approach for end-to-end learning'
date: 2021-02-08
venue: ''
published: 'false'
paperurl: https://arxiv.org/pdf/2102.04379.pdf
citation: 'Chochlakis G., Georgiou E., Potamianos A. End-to-end Generative Zero-shot Learning via Few-shot Learning. arXiv preprint arXiv:2102.04379, 2021.'
---

<img src="https://gchochla.github.io/images/z2fsl-pipeline-wbg.png" style="display: block; margin-left: auto; margin-right:auto; width: 90%; height: auto;">
<br>
_Abstract_: Contemporary state-of-the-art approaches to Zero-Shot Learning (ZSL) train generative nets to synthesize examples conditioned on the provided metadata. Thereafter, classifiers are trained on these synthetic data in a supervised manner. In this work, we introduce Z2FSL, an end-to-end generative ZSL framework that uses such an approach as a backbone and feeds its synthesized output to a Few-Shot Learning (FSL) algorithm. The two modules are trained jointly. Z2FSL solves the ZSL problem with a FSL algorithm, reducing, in effect, ZSL to FSL. A wide class of algorithms can be integrated within our framework. Our experimental results show consistent improvement over several baselines. The proposed method, evaluated across standard benchmarks, shows state-of-the-art or competitive performance in ZSL and Generalized ZSL tasks.

[[code](https://github.com/gchochla/z2fsl)]

BibTex Citation
-
```
@article{chochlakis2021endtoend,
  title={End-to-end {G}enerative {Z}ero-shot {L}earning via {F}ew-shot {L}earning},
  author={Chochlakis, Georgios and Georgiou, Efthymios and Potamianos, Alexandros},
  journal={arXiv preprint arXiv:2102.04379},
  year={2021}
}
```
