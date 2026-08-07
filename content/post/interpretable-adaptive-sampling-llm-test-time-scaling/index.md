---
title: "Interpretable Adaptive Sampling for LLM Test-Time Scaling and Test-Time Compute"
date: 2026-08-04
draft: false

summary: "Interpretable adaptive sampling for LLM test-time scaling and test-time compute. A fuzzy controller uses prompt complexity and model confidence to dynamically allocate inference-time compute for efficient LLM reasoning."

authors:
  - admin

tags:
  - LLM Test-Time Scaling
  - Test-Time Scaling
  - Test-Time Compute
  - Test-Time Computing
  - Inference-Time Compute
  - Inference-Time Scaling
  - LLM Reasoning
  - Adaptive Sampling
  - Adaptive Inference
  - Efficient LLM Inference
  - Efficient LLM Reasoning
  - Best-of-N Sampling
  - Self-Consistency
  - Inference-Time Sampling
  - Interpretable AI
  - Fuzzy Controller
  - Model Confidence
  - Prompt Complexity
  - Mathematical Reasoning

categories:
  - Large Language Models
  - Artificial Intelligence
  - LLM Reasoning
  - Test-Time Scaling
  - Research Summary
---

## What Is LLM Test-Time Scaling?

Test-time scaling, also referred to as test-time compute or inference-time scaling, improves large language model reasoning by allocating additional computation during inference.

## Adaptive Sampling for Test-Time Compute

Most fixed best-of-N approaches assign the same sampling budget to every prompt. Our approach dynamically allocates inference-time compute based on prompt complexity and model confidence.

## Interpretable Inference-Time Compute

A lightweight fuzzy controller determines how many candidate responses each query receives. Easier or higher-confidence prompts receive fewer samples, while more difficult or uncertain prompts receive additional test-time compute.

## Efficient LLM Reasoning

Adaptive sampling can reduce unnecessary candidate generation while maintaining competitive reasoning performance across question-answering and mathematical reasoning tasks.

## Comparison with Best-of-N and Self-Consistency

We compare the approach with fixed best-of-N sampling, compute-aware test-time scaling, and self-certainty-based methods.

## Paper

**Interpretable Adaptive Sampling for LLM Test-Time Scaling**

Mobina Kashaniyan and Ali Jannesari

- [arXiv Abstract](https://arxiv.org/abs/2608.03961)
- [PDF](https://arxiv.org/pdf/2608.03961)
- [DOI](https://doi.org/10.48550/arXiv.2608.03961)
