---
title: "Sample Count Is Not Enough (arXiv:2609.19499): Why Candidate-Generation Strategy Matters for LLM Test-Time Scaling Energy and Performance"
date: 2026-09-16
lastmod: 2026-09-17
draft: false

summary: "arXiv:2609.19499 — Candidate count N alone does not define the systems cost of LLM test-time scaling. At fixed N=8, generation schedules like 1×8 vs 8×1 can change A100 energy by about 4.6–4.9× and P95 latency by about 5.8–6.1×."

authors:
  - admin

tags:
  - arXiv:2609.19499
  - Sample Count Is Not Enough
  - LLM Test-Time Scaling
  - Test-Time Scaling
  - Test-Time Compute
  - Test-Time Computing
  - Inference-Time Compute
  - Inference-Time Scaling
  - Candidate Generation
  - Candidate-Generation Strategy
  - Generation Schedule
  - Batched Decoding
  - Batched Inference
  - Multi-Candidate Sampling
  - Self-Consistency
  - Best-of-N Sampling
  - LLM Energy Efficiency
  - Energy-Efficient AI
  - Sustainable AI
  - Green AI
  - GPU Energy Measurement
  - GPU Inference Performance
  - High-Performance Computing
  - SC26
  - EESP Workshop
  - A100 GPU
  - V100 GPU
  - GSM8K
  - SciQ
  - Phi-3-mini
  - Qwen2.5
  - LLM Latency
  - LLM Throughput
  - cs.LG
  - cs.DC
  - cs.PF

categories:
  - Large Language Models
  - High-Performance Computing
  - Energy Efficiency
  - Test-Time Scaling
  - Research Summary
---

## New Paper on arXiv: 2609.19499

Our paper is now live on arXiv:

**[Sample Count Is Not Enough: Candidate-Generation Strategy Shapes the Energy and Performance of LLM Test-Time Scaling](https://arxiv.org/abs/2609.19499)**

- Authors: **Mobina Kashaniyan**, **Ali Jannesari**
- arXiv: [2609.19499](https://arxiv.org/abs/2609.19499)
- DOI: [10.48550/arXiv.2609.19499](https://doi.org/10.48550/arXiv.2609.19499)
- PDF: [arxiv.org/pdf/2609.19499](https://arxiv.org/pdf/2609.19499)
- Venue: 3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (**EESP**), co-located with **SC26**, Chicago, USA, November 2026

## What Is LLM Test-Time Scaling?

**LLM test-time scaling**, also called **test-time compute** or **inference-time scaling**, improves large language model reasoning by spending more compute at inference time. A common approach is to generate multiple candidate answers and then aggregate them, for example with **self-consistency** or **best-of-N** selection.

## Why Candidate Count Alone Is Not Enough

In sampling-based methods, the inference budget is often summarized by the candidate count **N**. That number says how many candidates are generated, but not how they are executed on the GPU.

The same **N** can be produced as:

- one batched generation call with all candidates together, or
- several sequential generation calls with smaller batch sizes

Those schedules have the same candidate count, but they can have very different **latency, throughput, GPU-hours, utilization, and energy**.

## Candidate-Generation Strategy and Generation Schedules

In [arXiv:2609.19499](https://arxiv.org/abs/2609.19499), we formalize the **candidate-generation schedule** and compare four fixed-budget schedules at **N=8**:

- **1×8**: one call with eight candidates
- **2×4**: two calls with four candidates each
- **4×2**: four calls with two candidates each
- **8×1**: eight serial calls with one candidate each

## Energy and Performance Results on A100 GPUs

We evaluate **Phi-3-mini** and **Qwen2.5-1.5B** on **GSM8K**. Increasing **N** from 1 to 8 improves accuracy, as expected. But at fixed **N=8**, systems cost depends strongly on the schedule.

On **A100 GPUs**, eight serial calls use about **4.64–4.86×** as much gross GPU-device energy and have about **5.77–6.12×** the P95 latency of one batched eight-candidate call. Similar patterns appear across independently scheduled A100 nodes and in short-output SciQ/V100 experiments.

## Practical Takeaway for Efficient LLM Inference

When candidates are independent and memory allows it, **fewer generation calls with larger batch sizes** are more efficient. Evaluations of multi-candidate test-time scaling should report not only candidate count and accuracy, but also:

- generation schedule
- calls per query
- candidates per call
- GPU-level systems metrics such as latency, throughput, and energy

# Our Paper

In our paper, **“Sample Count Is Not Enough: Candidate-Generation Strategy Shapes the Energy and Performance of LLM Test-Time Scaling” ([arXiv:2609.19499](https://arxiv.org/abs/2609.19499))**, we show that the systems cost of multi-candidate LLM inference depends on how candidates are grouped into generation calls, not only on how many candidates are generated.

This work was accepted to the **3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP)**, co-located with **SC26** in Chicago, USA (pages 1–8, November 2026).

Authors: **Mobina Kashaniyan** and **Ali Jannesari**, Iowa State University.

## Abstract

Test-time scaling can improve large language model reasoning by generating and combining multiple candidate responses. In sampling-based methods, the inference budget is often described by the number of generated candidates, N. However, N tells us how many candidates are generated, not how they are executed. The same candidate budget can be produced in one batched generation call or split across several sequential calls with smaller batch sizes.

We first study the effect of increasing N on reasoning accuracy using Phi-3-mini and Qwen2.5-1.5B on 500 GSM8K prompts. As expected, increasing N from 1 to 8 improves accuracy by 8.4 percentage points for Phi-3-mini and 18.4 points for Qwen2.5-1.5B. However, accuracy alone does not show the systems cost of using a larger candidate budget.

We therefore fix N=8 and compare four generation schedules: 1×8, 2×4, 4×2, and 8×1, where a×b denotes a generation calls with b candidates per call. We measure latency, throughput, GPU-hours, and gross GPU-device energy while keeping the total candidate count fixed. On A100 GPUs, eight serial calls use 4.64–4.86× as much gross GPU-device energy and have 5.77–6.12× the P95 latency of one batched call with eight candidates.

The same pattern appears across three independently scheduled A100 nodes per model and in short-output SciQ/V100 experiments. These results show that candidate count alone is not enough to describe the systems cost of multi-candidate test-time scaling. When candidates are independent and memory allows it, fewer generation calls with larger batch sizes are more efficient. Evaluations should therefore report not only candidate count and accuracy, but also generation schedule and GPU-level systems metrics.

## Paper Links

**Sample Count Is Not Enough: Candidate-Generation Strategy Shapes the Energy and Performance of LLM Test-Time Scaling**

Mobina Kashaniyan and Ali Jannesari

- [arXiv Abstract](https://arxiv.org/abs/2609.19499)
- [arXiv PDF](https://arxiv.org/pdf/2609.19499)
- [DOI](https://doi.org/10.48550/arXiv.2609.19499)
- [HTML](https://arxiv.org/html/2609.19499)
- [Publication Page](https://mobinakashaniyan.github.io/publication/sample-count-candidate-generation/)
- Venue: 3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP), co-located with SC26, Chicago, USA, November 2026

## Cite This Paper

```bibtex
@inproceedings{kashaniyan2026sample,
  title     = {Sample Count Is Not Enough: Candidate-Generation Strategy Shapes the Energy and Performance of {LLM} Test-Time Scaling},
  author    = {Kashaniyan, Mobina and Jannesari, Ali},
  booktitle = {Proceedings of the 3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP)},
  pages     = {1--8},
  year      = {2026},
  note      = {arXiv:2609.19499},
  doi       = {10.48550/arXiv.2609.19499},
  url       = {https://arxiv.org/abs/2609.19499}
}
```

Kashaniyan, M., & Jannesari, A. (2026). Sample count is not enough: Candidate-generation strategy shapes the energy and performance of LLM test-time scaling. *arXiv preprint arXiv:2609.19499*. https://doi.org/10.48550/arXiv.2609.19499

## LLM Test-Time Scaling Energy and Performance

## Candidate-Generation Strategy for Multi-Candidate Inference

## Batched vs Serial Generation Schedules for Test-Time Compute

## Sustainable and Energy-Efficient LLM Inference on GPUs

## arXiv 2609.19499 LLM Energy Efficiency SC26 EESP
