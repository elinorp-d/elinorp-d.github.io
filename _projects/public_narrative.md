---
layout: page
title: LLMs for Public Narrative
subtitle: We propose a novel computational framework for computational analysis of Public Narratives and demonstrate the potential of LLM-assisted annotation for scalable narrative analysis.
img: assets/img/pn_diagram.png
importance: 2

styles: >
    fivehundred {
        max-height:500;
        width: auto;
    }
---

This project has been a collaboration with [Danny Kessler](https://www.ccc.mit.edu/person/daniel-kessler/), [Maggie Hughes](https://m-a-hues.me/), [Emily S. Lin](https://www.hks.harvard.edu/about/emily-lin-0), and [Marshall Ganz](https://www.hks.harvard.edu/faculty/marshall-ganz). It was accepted to the [7th Workshop on Narrative Understanding](https://sites.google.com/cs.stonybrook.edu/wnu2025/accepted-papers?authuser=0) at NAACL 2025 and currently under review at EMNLP 2025. I am very grateful for our talented UROP, [Hannah Chiou](https://www.linkedin.com/in/hannah-chiou/), who also helped on the second submission of this paper.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/pn_poster.png" class="img-fluid rounded z-depth-1 fivehundred" %}
    </div>
</div>
<div class="caption">
    Presenting the poster at NAACL 2025!
</div>


## Abstract
Public Narratives (PNs) are key tools for leadership development and civic mobilization, yet their systematic analysis remains challenging due to their subjective interpretation and the high cost of expert annotation. In this work, we propose a novel computational framework that leverages large language models (LLMs) to automate the qualitative annotation of public narratives. Using a codebook we co-developed with subject-matter experts, we evaluate LLM performance against that of expert annotators. Our work reveals that LLMs can achieve near-human-expert performance, achieving an average F1 score of 0.80 across 8 narratives and 14 codes. We then extend our analysis to empirically explore how PN framework elements manifest across a larger dataset of 22 stories. Lastly, we extrapolate our analysis to a set of political speeches, establishing a novel lens in which to analyze political rhetoric in civic spaces. This study demonstrates the potential of LLM-assisted annotation for scalable narrative analysis and highlights key limitations and directions for future research in computational civic storytelling.