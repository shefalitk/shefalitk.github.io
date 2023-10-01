---
title: 'Using Emotion Embeddings to Transfer Knowledge Between Emotions, Languages, and Annotation Formats'
collection: publications
permalink: /publication/emotion-embeddings
excerpt: 'In this work, we study how we can build a single emotion recognition model that can transition between different configurations, i.e., languages, emotions, and annotation formats, by leveraging multilingual models and Demux.'
date: 2023-06-04
venue: 'ICASSP'
published: 'true'
paperurl: https://arxiv.org/abs/2211.00171
citation: 'Chochlakis, G., Mahajan, G., Baruah, S., Burghardt, K., Lerman, K. and Narayanan, S., 2022. Using Emotion Embeddings to Transfer Knowledge Between Emotions, Languages, and Annotation Formats. arXiv preprint arXiv:2211.00171.'
---

<img src="https://gchochla.github.io/images/demux-cluster.png" style="display: block; margin-left: auto; margin-right:auto; width: 90%; height: auto;">
<br>
_Abstract_: The need for emotional inference from text continues to diversify as more and more disciplines integrate emotions into their theories and applications. These needs include inferring different emotion types, handling multiple languages, and different annotation formats. A shared model between different configurations would enable the sharing of knowledge and a decrease in training costs, and would simplify the process of deploying emotion recognition models in novel environments. In this work, we study how we can build a single model that can transition between these different configurations by leveraging multilingual models and Demux, a transformer-based model whose input includes the emotions of interest, enabling us to dynamically change the emotions predicted by the model. Demux also produces emotion embeddings, and performing operations on them allows us to transition to clusters of emotions by pooling the embeddings of each cluster. We show that Demux can simultaneously transfer knowledge in a zero-shot manner to a new language, to a novel annotation format and to unseen emotions. 

[[code](https://github.com/gchochla/Demux-MEmo)]

BibTex Citation
-
```
@INPROCEEDINGS{chochlakis2023emotion,
  author={Chochlakis, Georgios and Mahajan, Gireesh and Baruah, Sabyasachee and Burghardt, Keith and Lerman, Kristina and Narayanan, Shrikanth},
  booktitle={ICASSP 2023 - 2023 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
  title={Using Emotion Embeddings to Transfer Knowledge between Emotions, Languages, and Annotation Formats}, 
  year={2023},
  volume={},
  number={},
  pages={1-5},
  doi={10.1109/ICASSP49357.2023.10095597}
}
```
