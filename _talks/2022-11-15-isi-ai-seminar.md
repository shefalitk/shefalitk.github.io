---
title: "ISI Artificial Intelligence Seminars"
collection: talks
type: "Talk"
permalink: /talks/2024-11-15-isi-ai-seminar
venue: "ISI"
date: 2024-11-15
location: "Information Science Institute, Los Angeles, CA, USA"
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/R76TmU8XMzk?si=fmsVaGyhTrAErXHY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<br>

The Institute Science Institute at the University of Southern California hosts weekly AI seminar, and I had the pleasure to present my research on the 15th of November, 2024. In this talk, I discussed my rcent findings on the "stubborness" of Large Language Models in the presence of evidence conflicting with their prior knowledge.

_Abstract_: In-Context Learning (ICL) has rapidly become the leading approach for performing natural language tasks with Large Language Models (LLMs), due to the ability to leverage background knowledge. ICL’s few-shot adaptability shows promise but relies heavily on retrieving task priors from that background knowledge. This is especially challenging in domains where human judgements vary, causing LLMs to default to priors even when evidence conflicts with them, which can limit performance on complex, subjective tasks like emotion and morality recognition. Augmenting ICL with Chain-of-Thought (CoT) prompting, intended to explicitly include reasoning, does not overcome these limitations, as it instead retrieves reasoning priors that remain fixed despite task-specific prompts. We design experiments to measure the influence of LLM priors on their posteriors and find that the effect intensifies with model size, leading to posterior collapse. Additionally, we explore how aggregating human judgments in subjective tasks introduces artifacts and biases that may confound LLM performance. Our findings suggest a need for caution when deploying larger LLMs for subjective tasks and underscore the value of annotator-level modeling over aggregated datasets in these contexts.