---
title: "ATEST / RATTS: Adaptive Resource-Aware Test-Time Scaling for LLM Inference (arXiv:2610.25519)"
date: 2026-10-18
draft: false

summary: "ATEST (RATTS) is adaptive resource-aware test-time scaling for LLM inference. The same four-sample query can use 4.1× more energy when the GPU is busy. ATEST-Online answers every query within budget. arXiv:2610.25519."

authors:
  - admin

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
  - Energy-Aware LLM Inference
  - GPU Load Aware Inference
  - Shared GPU
  - Online Cost Learning
  - ATEST-Online
  - ATEST-Calibrated
  - Self-Consistency
  - Best-of-N Sampling
  - LLM Energy Efficiency
  - Sustainable AI
  - Green AI
  - High-Performance Computing
  - Phi-3-mini
  - Qwen2.5-3B
  - NVIDIA A100
  - NVIDIA L40S
  - GSM8K

categories:
  - Large Language Models
  - High-Performance Computing
  - Energy Efficiency
  - Test-Time Scaling
  - Research Summary
---

## New Paper: ATEST (arXiv:2610.25519)

**[ATEST: Adaptive Resource-Aware Test-Time Scaling for LLM Inference](https://arxiv.org/abs/2610.25519)** is now on arXiv.

We also call this idea **RATTS: Resource-Aware Test-Time Scaling for LLM Inference**.

- Authors: **Mobina Kashaniyan**, **Ali Jannesari** (Iowa State University)
- arXiv: [2610.25519](https://arxiv.org/abs/2610.25519)
- DOI: [10.48550/arXiv.2610.25519](https://doi.org/10.48550/arXiv.2610.25519)
- PDF: [arxiv.org/pdf/2610.25519](https://arxiv.org/pdf/2610.25519)

## Why Fixed Test-Time Scaling Wastes Energy

**Test-time scaling** improves LLM answers by generating several samples and voting. Most adaptive methods decide how many samples a question needs from difficulty or answer agreement. They treat the cost of one sample as a fixed number.

On a shared GPU, that cost is not fixed. In our measurements, the **same four-sample query uses up to 4.1× more energy** when other jobs load the GPU. A GSM8K query can cost **121.7 J** on an idle A100 and **455.6 J** on a busy one.

## What ATEST Does

ATEST answers two questions at once:

1. Is one more sample useful for this query?
2. What does that sample cost on the GPU right now?

**ATEST-Online** (default) needs no offline calibration. It starts with one sample, checks whether the plurality answer is stable, reads the live GPU state, learns step energy online, and stops when the next sample is not worth its cost.

**ATEST-Calibrated** profiles a dataset once and picks the full budget per query. That mode is useful when GPU load is stable and low tail latency matters. It does not follow the load when the GPU becomes busy.

## Results

On an **NVIDIA A100** with **Phi-3-mini**, ATEST-Online answers every query, stays inside the energy budget, and matches or leads accuracy on all four datasets while using fewer samples as load rises. The same pattern holds on an **NVIDIA L40S** and with **Qwen2.5-3B**.

On **GSM8K at high load**:

- ATEST-Online: **60.0%** accuracy, no deferred queries
- ATEST-Calibrated: **44.0%** accuracy, because it defers **42.4%** of queries

Including offline profiling, ATEST-Online uses **42× less GPU time** and **48× less energy** than ATEST-Calibrated.

## How to Cite ATEST

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

## Paper Links

- [arXiv](https://arxiv.org/abs/2610.25519)
- [PDF](https://arxiv.org/pdf/2610.25519)
- [DOI](https://doi.org/10.48550/arXiv.2610.25519)
- [Publication page](https://mobinakashaniyan.github.io/publication/atest/)
- Related: [Sample Count Is Not Enough (arXiv:2609.19499)](https://arxiv.org/abs/2609.19499)

## Resource-Aware Test-Time Scaling for Shared GPUs

## Adaptive Sampling under Live GPU Load

## Energy-Aware LLM Inference with ATEST and RATTS
