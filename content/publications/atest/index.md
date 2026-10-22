---
title: "ATEST: Adaptive Resource-Aware Test-Time Scaling for LLM Inference"
slug: atest
date: 2026-10-18
publishDate: 2026-10-18
draft: false
featured: true

authors:
  - "**Mobina Kashaniyan**"
  - Ali Jannesari

publication_types:
  - "3"

publication: "*arXiv preprint arXiv:2610.25519*, 2026"
publisher: "arXiv"

doi: "10.48550/arXiv.2610.25519"
arxiv: "2610.25519"
url_pdf: "https://arxiv.org/pdf/2610.25519"

abstract: >-
  Test-time scaling (TTS) improves large language model reasoning by generating
  several samples for a query and voting on the answer. However, a fixed sampling
  budget ignores two facts: different queries need different amounts of reasoning,
  and the cost of one more sample changes with GPU load. In our measurements, the
  same four-sample query uses up to 4.1× more energy when other jobs load the GPU.
  Existing adaptive methods mainly set the budget from answer agreement, question
  structure, or question difficulty. They decide how much reasoning a query needs,
  but not what that reasoning costs on the GPU right now. We present ATEST, a
  runtime framework for resource-aware test-time scaling (RATTS) with two modes.
  Its default mode, ATEST-Online, needs no offline calibration: it starts with one
  sample, checks whether the plurality answer is stable, reads the live GPU state,
  predicts the cost of the next step with an online cost model, and decides whether
  to stop or continue. For stable deployments that can reuse a one-time profile,
  ATEST also offers an offline mode, ATEST-Calibrated, which picks the budget from
  accuracy and cost models built offline. We evaluate ATEST with Phi-3-mini on an
  NVIDIA A100 across four reasoning and question-answering datasets under a
  controlled idle-to-high GPU load schedule, and repeat the study on an NVIDIA L40S
  and with a second model, Qwen2.5-3B. On the A100, ATEST-Online answers every query,
  never exceeds the energy budget, gives the highest or statistically tied accuracy
  on all four datasets, and uses fewer samples as load rises. On GSM8K at high load,
  it keeps 60.0% accuracy, while ATEST-Calibrated drops to 44.0% because it defers
  42.4% of the queries. Including offline calibration, ATEST-Online uses 42× less
  GPU time and 48× less energy than ATEST-Calibrated.

summary: "ATEST (RATTS) adapts LLM test-time scaling to live GPU load. The same four-sample query can cost 4.1× more energy when the GPU is busy. arXiv:2610.25519."

tags:
  - ATEST
  - RATTS
  - Resource-Aware Test-Time Scaling
  - Adaptive Resource-Aware Test-Time Scaling
  - arXiv:2610.25519
  - LLM Test-Time Scaling
  - Test-Time Scaling
  - Test-Time Compute
  - Adaptive Sampling
  - Energy-Aware Inference
  - GPU Load
  - Shared GPU Inference
  - Online Cost Model
  - ATEST-Online
  - ATEST-Calibrated
  - LLM Energy Efficiency
  - Energy-Efficient AI
  - Sustainable AI
  - Green AI
  - High-Performance Computing
  - Large Language Models
  - Phi-3-mini
  - Qwen2.5-3B
  - NVIDIA A100
  - NVIDIA L40S
  - GSM8K
  - Self-Consistency
  - Best-of-N
  - cs.LG
  - cs.AI
  - cs.CL
  - cs.DC
  - cs.PF

categories:
  - Preprint
  - Large Language Models
  - High-Performance Computing
  - Energy Efficiency
  - Test-Time Scaling

sitemap:
  priority: 1.0
  changefreq: weekly

links:
  - icon_pack: fas
    icon: file-pdf
    name: PDF
    url: "https://arxiv.org/pdf/2610.25519"
  - icon_pack: fas
    icon: link
    name: arXiv
    url: "https://arxiv.org/abs/2610.25519"
  - icon_pack: fas
    icon: external-link-alt
    name: DOI
    url: "https://doi.org/10.48550/arXiv.2610.25519"
  - icon_pack: ai
    icon: google-scholar
    name: Google Scholar
    url: "https://scholar.google.com/citations?user=WcGHM0sAAAAJ&hl=en"
  - icon_pack: fas
    icon: newspaper
    name: Research Summary
    url: "https://mobinakashaniyan.github.io/post/atest-adaptive-resource-aware-test-time-scaling/"
  - icon_pack: fas
    icon: file
    name: Local PDF
    url: "https://mobinakashaniyan.github.io/papers/atest-adaptive-resource-aware-test-time-scaling.pdf"
---

**New preprint:** [arXiv:2610.25519](https://arxiv.org/abs/2610.25519) — **ATEST: Adaptive Resource-Aware Test-Time Scaling for LLM Inference** by **Mobina Kashaniyan** and **Ali Jannesari**.

ATEST is a **resource-aware test-time scaling** method, also called **RATTS (Resource-Aware Test-Time Scaling)**. Standard test-time scaling generates a fixed number of samples whether the GPU is idle or busy. ATEST reads the live GPU state and skips extra samples when they are not worth their current energy cost.

On an **NVIDIA A100**, the same four-sample query uses up to **4.1× more energy** when other jobs load the GPU. A GSM8K query that costs **121.7 J** on an idle GPU can cost **455.6 J** on a busy one.

**ATEST-Online**, the default mode, needs no offline calibration. It starts with one sample, checks whether the plurality answer is stable, predicts the energy of the next step, and stops when another sample is not worth the cost. **ATEST-Calibrated** is an offline mode for stable deployments: it profiles a dataset once and picks the whole budget per query.

On GSM8K at high load, ATEST-Online keeps **60.0% accuracy** and answers every query. ATEST-Calibrated drops to **44.0%** because it defers **42.4%** of queries. Including profiling, ATEST-Online uses **42× less GPU time** and **48× less energy** than ATEST-Calibrated. The same pattern holds on an **NVIDIA L40S** and with **Qwen2.5-3B**.

This work follows our earlier result that [candidate count alone is not enough](https://arxiv.org/abs/2609.19499) to describe the systems cost of test-time scaling. ATEST asks the next question: what does one more sample cost on the GPU right now?

**Keywords:** ATEST, RATTS, resource-aware test-time scaling, adaptive test-time scaling, LLM inference, GPU load, energy-aware systems, adaptive sampling, A100, L40S, Phi-3-mini, Qwen2.5-3B, GSM8K, arXiv:2610.25519.

## Links

- [arXiv Abstract](https://arxiv.org/abs/2610.25519)
- [arXiv PDF](https://arxiv.org/pdf/2610.25519)
- [DOI](https://doi.org/10.48550/arXiv.2610.25519)
- [HTML](https://arxiv.org/html/2610.25519)
- [Local mirror PDF](https://mobinakashaniyan.github.io/papers/atest-adaptive-resource-aware-test-time-scaling.pdf)
- [Research Summary](https://mobinakashaniyan.github.io/post/atest-adaptive-resource-aware-test-time-scaling/)

## How to Cite

```bibtex
@misc{kashaniyan2026atest,
  title         = {ATEST: Adaptive Resource-Aware Test-Time Scaling for {LLM} Inference},
  author        = {Kashaniyan, Mobina and Jannesari, Ali},
  year          = {2026},
  eprint        = {2610.25519},
  archivePrefix = {arXiv},
  primaryClass  = {cs.LG},
  doi           = {10.48550/arXiv.2610.25519},
  url           = {https://arxiv.org/abs/2610.25519}
}
```

Kashaniyan, M., & Jannesari, A. (2026). ATEST: Adaptive resource-aware test-time scaling for LLM inference. *arXiv preprint arXiv:2610.25519*. https://doi.org/10.48550/arXiv.2610.25519
