---
title: "Interpretable Adaptive Sampling for LLM Test-Time Scaling"
date: 2026-08-04
publishDate: 2026-08-04

authors:
  - "**Mobina Kashaniyan**"
  - "Ali Jannesari"

publication_types:
  - "3"

publication: "*arXiv preprint arXiv:2608.03961*, 2026"
publisher: "arXiv"

doi: "10.48550/arXiv.2608.03961"
url_pdf: "https://arxiv.org/pdf/2608.03961"

abstract: "Test-time scaling improves large language model reasoning by generating multiple candidate answers, but fixed sampling budgets spend equal compute on easy and difficult prompts. We introduce an interpretable adaptive sampling method based on a lightweight fuzzy controller that uses prompt complexity and model confidence to determine a per-query sampling budget. The method reduces unnecessary inference-time computation while maintaining competitive performance across question-answering and mathematical reasoning tasks."

summary: "An interpretable and compute-efficient approach to LLM test-time scaling that adaptively allocates sampling budgets using prompt complexity, model confidence, and fuzzy control."

tags:
  - LLM Test-Time Scaling
  - Adaptive Sampling
  - Inference-Time Compute
  - Efficient LLM Inference
  - Test-Time Reasoning
  - Large Language Models
  - Interpretable AI
  - Fuzzy Logic
  - Compute-Efficient AI
  - Best-of-N Sampling
  - Self-Consistency
  - Mathematical Reasoning
  - Question Answering
  - Adaptive Computation

categories:
  - Preprint

sitemap:
  priority: 1.0
  changefreq: monthly

links:
  - icon_pack: fas
    icon: file-pdf
    name: PDF
    url: https://arxiv.org/pdf/2608.03961
  - icon_pack: fas
    icon: link
    name: arXiv
    url: https://arxiv.org/abs/2608.03961
  - icon_pack: ai
    icon: google-scholar
    name: Google Scholar
    url: https://scholar.google.com/citations?user=WcGHM0sAAAAJ&hl=en
---

This paper introduces an interpretable adaptive sampling framework for large language model test-time scaling. Instead of assigning the same number of candidate generations to every prompt, the method uses estimated prompt complexity and model confidence to dynamically allocate inference-time compute.

A lightweight fuzzy controller assigns fewer samples to easier or higher-confidence prompts and more samples to difficult or uncertain prompts. This makes the sampling decision transparent while reducing unnecessary computation.

The work is relevant to researchers studying LLM reasoning, test-time compute, inference efficiency, adaptive computation, self-consistency, best-of-N sampling, and interpretable artificial intelligence.

**Citation**

Kashaniyan, M., & Jannesari, A. (2026). Interpretable adaptive sampling for LLM test-time scaling. arXiv preprint arXiv:2608.03961. https://doi.org/10.48550/arXiv.2608.03961
