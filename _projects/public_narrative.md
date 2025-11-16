---
layout: page
title: LLMs for Public Narrative
img: assets/img/pn_diagram.png
importance: 2
related_publications: true
---

<div class="row justify-content-center">
    <div class="col-10 col-sm-6">
        {% include figure.liquid path="assets/img/pn_poster.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

This project has been a collaboration with [Hannah Chiou](https://www.linkedin.com/in/hannah-chiou/), [Danny Kessler](https://www.ccc.mit.edu/person/daniel-kessler/), [Maggie Hughes](https://m-a-hues.me/), [Emily S. Lin](https://www.hks.harvard.edu/about/emily-lin-0), and [Marshall Ganz](https://www.hks.harvard.edu/faculty/marshall-ganz). It was accepted to the [7th Workshop on Narrative Understanding](https://sites.google.com/cs.stonybrook.edu/wnu2025/accepted-papers?authuser=0) at NAACL 2025 {% cite publicnarrative_NAACL2025 %}.


<div class="row justify-content-center">
    <div class="col-10 col-sm-8">
        {% include figure.liquid path="assets/img/pn_diagram.png" class="img-fluid rounded z-depth-1" %}
    <div class="caption">
        We compare an LLMs' ability to annotate Public Narratives to human experts following our codebook co-developed with experts. To visualize the annotations, the length of each portion corresponds to the number of sentences coded.
    </div>
    </div>
</div>

## Abstract
Public Narratives (PNs) are key tools for leadership development and civic mobilization, yet their systematic analysis remains challenging due to their subjective interpretation and the high cost of expert annotation. In this work, we propose a novel computational framework that leverages large language models (LLMs) to automate the qualitative annotation of public narratives. Using a codebook we co-developed with subject-matter experts, we evaluate LLM performance against that of expert annotators. Our work reveals that LLMs can achieve near-human-expert performance, achieving an average F1 score of 0.80 across 8 narratives and 14 codes. We then extend our analysis to empirically explore how PN framework elements manifest across a larger dataset of 22 stories. Lastly, we extrapolate our analysis to a set of political speeches, establishing a novel lens in which to analyze political rhetoric in civic spaces. This study demonstrates the potential of LLM-assisted annotation for scalable narrative analysis and highlights key limitations and directions for future research in computational civic storytelling.

## Demo
Check out our interactive data visualization below or [click here](https://maggatronn.github.io/pn_visualization/) to view in a separate tab. Click "Select a story" to begin:
<div class="row justify-content-center">
    <iframe src="https://maggatronn.github.io/pn_visualization/" width="100%" height="1000"></iframe>
</div>