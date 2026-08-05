---
title: "Interpretable Adaptive Sampling for LLM Test-Time Scaling"
date: 2026-08-04
publishDate: 2026-08-04
draft: false

authors: ["**Mobina Kashaniyan**", "Ali Jannesari"]

publication_types: ["3"]

publication: "*arXiv preprint arXiv:2608.03961*, 2026"
publisher: "arXiv"

doi: "10.48550/arXiv.2608.03961"
url_pdf: "https://mobinakashaniyan.github.io/publications/interpretable-adaptive-sampling/interpretable-adaptive-sampling-llm-test-time-scaling.pdf"


abstract: >-
  Test-time scaling improves LLM reasoning by generating and aggregating
  multiple candidate answers, yet many pipelines use fixed per-query budgets
  that spend the same compute on easy and difficult prompts. These fixed
  budgets are also difficult to inspect because they do not explain why a
  given prompt receives a particular number of samples. We propose adaptive
  test-time scaling with a lightweight fuzzy controller that maps interpretable
  signals, including estimated prompt complexity and model confidence, to a
  per-query sampling budget. The controller assigns fewer samples to easier or
  more confident prompts and more samples to harder or less certain prompts,
  making inference-time compute inspectable rather than fixed or opaque. We
  evaluate under a fair-alignment protocol with matched decoding settings and
  controlled answer selection, and compare against best-of-N, compute-aware
  scaling, and self-certainty-based baselines on question-answering and
  mathematical reasoning tasks. Across models and datasets, adaptive fuzzy
  control improves over several standard baselines and remains close to a
  selector-matched full-budget control while reducing the average number of
  samples. These findings suggest that interpretable adaptive sampling is a
  practical direction for more efficient test-time reasoning in large
  language models.

summary: "An interpretable adaptive sampling method that dynamically allocates inference-time compute for efficient LLM test-time scaling."

tags: ["LLM Test-Time Scaling", "Adaptive Sampling", "Inference-Time Compute", "Efficient LLM Inference", "Large Language Models", "Test-Time Reasoning", "Interpretable AI", "Fuzzy Logic", "Best-of-N Sampling", "Self-Consistency", "Adaptive Computation"]

categories: ["Preprint", "Artificial Intelligence", "Large Language Models"]

sitemap:
  priority: 1.0
  changefreq: monthly

links:
  - icon_pack: fas
    icon: file-pdf
    name: PDF
    url: "https://arxiv.org/pdf/2608.03961"
  - icon_pack: fas
    icon: link
    name: arXiv
    url: "https://arxiv.org/abs/2608.03961"
  - icon_pack: ai
    icon: google-scholar
    name: Google Scholar
    url: "https://scholar.google.com/citations?user=WcGHM0sAAAAJ&hl=en"
  - icon_pack: fas
    icon: newspaper
    name: Research Summary
    url: "https://mobinakashaniyan.github.io/post/interpretable-adaptive-sampling-llm-test-time-scaling/"
---

This paper introduces an interpretable adaptive sampling framework for large language model test-time scaling.

Most test-time scaling approaches assign the same number of candidate generations to every prompt. However, easy and difficult prompts may require very different amounts of inference-time compute.

Our method uses a lightweight fuzzy controller that combines estimated prompt complexity and model confidence. It assigns fewer samples to easier or higher-confidence prompts and more samples to difficult or uncertain prompts.

The approach is evaluated against fixed best-of-N sampling, compute-aware scaling, and self-certainty-based methods on question-answering and mathematical reasoning tasks. The results demonstrate that adaptive fuzzy control can reduce the average number of generated samples while maintaining competitive reasoning performance.

This work is relevant to LLM test-time scaling, adaptive inference, compute-efficient AI, interpretable sampling, self-consistency, and efficient large language model reasoning.

**Keywords:** LLM test-time scaling, adaptive sampling, inference-time compute, efficient LLM inference, interpretable AI, fuzzy control, best-of-N sampling, self-consistency, adaptive computation, mathematical reasoning.

## Citation

Kashaniyan, M., & Jannesari, A. (2026). Interpretable adaptive sampling for LLM test-time scaling. arXiv preprint arXiv:2608.03961. https://doi.org/10.48550/arXiv.2608.03961
