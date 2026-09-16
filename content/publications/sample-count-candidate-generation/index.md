---
title: "Sample Count Is Not Enough: Candidate-Generation Strategy Shapes the Energy and Performance of LLM Test-Time Scaling"
date: 2026-11-01
publishDate: 2026-09-16
draft: false

authors:
  - "**Mobina Kashaniyan**"
  - Ali Jannesari

publication_types:
  - "1"

publication: "In *Proc. of the 3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP)*, co-located with SC26, Chicago, USA, pages 1–8, November 2026."
conference: "3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP)"
publisher: "IEEE/ACM"
pages: "1–8"
url_pdf: "https://mobinakashaniyan.github.io/papers/sample-count-is-not-enough-candidate-generation-llm-test-time-scaling.pdf"

abstract: >-
  Test-time scaling can improve large language model reasoning by generating and
  combining multiple candidate responses. In sampling-based methods, the inference
  budget is often described by the number of generated candidates, N. However, N
  tells us how many candidates are generated, not how they are executed. The same
  candidate budget can be produced in one batched generation call or split across
  several sequential calls with smaller batch sizes. We first study the effect of
  increasing N on reasoning accuracy using Phi-3-mini and Qwen2.5-1.5B on 500 GSM8K
  prompts. As expected, increasing N from 1 to 8 improves accuracy by 8.4 percentage
  points for Phi-3-mini and 18.4 points for Qwen2.5-1.5B. However, accuracy alone
  does not show the systems cost of using a larger candidate budget. We therefore
  fix N=8 and compare four generation schedules: 1×8, 2×4, 4×2, and 8×1, where a×b
  denotes a generation calls with b candidates per call. We measure latency,
  throughput, GPU-hours, and gross GPU-device energy while keeping the total
  candidate count fixed. On A100 GPUs, eight serial calls use 4.64–4.86× as much
  gross GPU-device energy and have 5.77–6.12× the P95 latency of one batched call
  with eight candidates. The same pattern appears across three independently
  scheduled A100 nodes per model and in short-output SciQ/V100 experiments. These
  results show that candidate count alone is not enough to describe the systems
  cost of multi-candidate test-time scaling. When candidates are independent and
  memory allows it, fewer generation calls with larger batch sizes are more
  efficient. Evaluations should therefore report not only candidate count and
  accuracy, but also generation schedule and GPU-level systems metrics.

summary: "At fixed candidate count N, how candidates are batched into generation calls can change LLM test-time scaling energy and latency by several times on A100 GPUs."

tags:
  - LLM Test-Time Scaling
  - Test-Time Scaling
  - Test-Time Compute
  - Candidate Generation
  - Candidate-Generation Strategy
  - Generation Schedule
  - Batched Inference
  - Multi-Candidate Sampling
  - Self-Consistency
  - Best-of-N
  - LLM Energy Efficiency
  - GPU Energy Measurement
  - GPU Inference
  - High-Performance Computing
  - Sustainable AI
  - Green AI
  - Energy-Efficient AI
  - SC26
  - EESP
  - Large Language Models
  - Inference Performance
  - Throughput
  - Latency
  - A100
  - GSM8K
  - Phi-3-mini
  - Qwen2.5

categories:
  - Conference Paper
  - Workshop Paper
  - Large Language Models
  - High-Performance Computing
  - Energy Efficiency

sitemap:
  priority: 1.0
  changefreq: monthly

links:
  - icon_pack: fas
    icon: file-pdf
    name: PDF
    url: "https://mobinakashaniyan.github.io/papers/sample-count-is-not-enough-candidate-generation-llm-test-time-scaling.pdf"
  - icon_pack: ai
    icon: google-scholar
    name: Google Scholar
    url: "https://scholar.google.com/citations?user=WcGHM0sAAAAJ&hl=en"
  - icon_pack: fas
    icon: newspaper
    name: Research Summary
    url: "https://mobinakashaniyan.github.io/post/sample-count-is-not-enough-candidate-generation-llm-test-time-scaling/"
---

This paper studies **LLM test-time scaling** from a **systems and energy** perspective. It shows that the **candidate count N is not enough** to describe the cost of multi-candidate inference.

In sampling-based test-time scaling, the same budget of **N candidates** can be generated as one large batch or as many small sequential calls. Those schedules have the same candidate count, but they can differ dramatically in **latency, throughput, GPU-hours, utilization, and GPU-device energy**.

We evaluate **Phi-3-mini** and **Qwen2.5-1.5B** on **GSM8K**, then fix **N=8** and compare generation schedules **1×8, 2×4, 4×2, and 8×1**. On **A100 GPUs**, eight serial calls use about **4.64–4.86×** the energy and **5.77–6.12×** the P95 latency of one batched eight-candidate call.

This work was accepted to the **3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP)**, co-located with **SC26** in Chicago, USA.

It is relevant to researchers working on **test-time scaling, test-time compute, candidate generation, batched LLM inference, GPU energy measurement, sustainable AI, green AI, high-performance computing, and efficient large language model systems**.

**Keywords:** LLM test-time scaling, test-time compute, candidate-generation strategy, generation schedule, batched inference, multi-candidate sampling, self-consistency, best-of-N, GPU energy, energy-efficient AI, sustainable AI, SC26, EESP, high-performance computing, A100, GSM8K.

## Venue

Mobina Kashaniyan, Ali Jannesari. *Sample Count Is Not Enough: Candidate-Generation Strategy Shapes the Energy and Performance of LLM Test-Time Scaling.* In Proc. of the 3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP), co-located with SC26, Chicago, USA, pages 1–8, November 2026.

## Citation

Kashaniyan, M., & Jannesari, A. (2026). Sample count is not enough: Candidate-generation strategy shapes the energy and performance of LLM test-time scaling. In *Proceedings of the 3rd IEEE/ACM SC26 Workshop on Energy Efficiency with Sustainable Performance (EESP)* (pp. 1–8). IEEE/ACM.
