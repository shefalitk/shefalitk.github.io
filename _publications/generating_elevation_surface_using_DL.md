---
title: 'Generating Elevation Surface from a single RGB remotely sensed image using Deep Learning'
collection: publications
permalink: /publication/generating_elevation_surface_using_DL
excerpt: 'End-to-end approach to construct a remotely sensed image to elevation surface mapping using Conditional Generative Adversarial Networks'
date: 2020-06-22
venue: 'Remote Sensing'
published: 'true'
paperurl: https://www.mdpi.com/2072-4292/12/12/2002/pdf
citation: 'Panagiotou, E.; Chochlakis, G.; Grammatikopoulos, L.; Charou, E. Generating Elevation Surface from a Single RGB Remotely Sensed Image Using Deep Learning. Remote Sens. 2020, 12, 2002.'
---

_Abstract_: Generating Digital Elevation Models (DEM) from satellite imagery or other data sources constitutes an essential tool for a plethora of applications and disciplines, ranging from 3D flight planning and simulation, autonomous driving and satellite navigation, such as GPS, to modeling water flow, precision farming and forestry. The task of extracting this 3D geometry from a given surface hitherto requires a combination of appropriately collected corresponding samples and/or specialized equipment, as inferring the elevation from single image data is out of reach for contemporary approaches. On the other hand, Artificial Intelligence (AI) and Machine Learning (ML) algorithms have experienced unprecedented growth in recent years as they can extrapolate rules in a data-driven manner and retrieve convoluted, nonlinear one-to-one mappings, such as an approximate mapping from satellite imagery to DEMs. Therefore, we propose an end-to-end Deep Learning (DL) approach to construct this mapping and to generate an absolute or relative point cloud estimation of a DEM given a single RGB satellite (Sentinel-2 imagery in this work) or drone image. The model has been readily extended to incorporate available information from the non-visible electromagnetic spectrum. Unlike existing methods, we only exploit one image for the production of the elevation data, rendering our approach less restrictive and constrained, but suboptimal compared to them at the same time. Moreover, recent advances in software and hardware allow us to make the inference and the generation extremely fast, even on moderate hardware. We deploy Conditional Generative Adversarial networks (CGAN), which are the state-of-the-art approach to image-to-image translation. We expect our work to serve as a springboard for further development in this field and to foster the integration of such methods in the process of generating, updating and analyzing DEMs.

[[website](https://www.mdpi.com/2072-4292/12/12/2002)] [[doi](https://doi.org/10.3390/rs12122002)]

Relevant presentation: [[odp](https://gchochla.github.io/files/rssa2020-presentation.odp)] [[pdf](https://gchochla.github.io/files/rssa2020-presentation.pdf)] (Note: .odp contains GIFs, .pdf contains only the first/last frame of those)
