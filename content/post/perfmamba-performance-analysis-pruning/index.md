---
title: "PerfMamba: Performance Analysis and Pruning of Selective State Space Models"
date: 2026-07-02
draft: false
summary: "Research summary of PerfMamba, a Springer conference paper on performance analysis, runtime profiling, scaling behavior, and pruning of Mamba-1 and Mamba-2 selective state space models."
authors:
  - admin
tags:
  - PerfMamba
  - Mamba
  - Mamba-1
  - Mamba-2
  - Selective State Space Models
  - State Space Models
  - SSM
  - Sequence Modeling
  - Transformer Alternatives
  - Performance Analysis
  - Runtime Profiling
  - Benchmarking
  - Model Pruning
  - State Pruning
  - Model Compression
  - Efficient AI
  - High-Performance Computing
  - Hardware-Aware Optimization
  - Large Language Models
  - AI Systems
categories:
  - Research Summary
  - Efficient AI
  - High-Performance Computing
  - Machine Learning Systems
---

Modern sequence models are becoming increasingly powerful, but their computational cost, memory behavior, and deployment efficiency remain important challenges. This is especially relevant for emerging architectures such as **Mamba** and **selective state space models**, which have been proposed as efficient alternatives to Transformer-based sequence models.

Our paper, **“PerfMamba: Performance Analysis and Pruning of Selective State Space Models,”** presents an empirical study of **Mamba-1 and Mamba-2**. The work analyzes runtime behavior, resource utilization, computation patterns, memory access, I/O characteristics, and scaling properties across sequence lengths from **64 to 16,384 tokens**.

The study shows how different components of selective state space models contribute to performance and efficiency. In particular, the paper examines the SSM component, which plays a central role in Mamba-style architectures, and identifies opportunities for optimization through pruning.

Based on the profiling results, **PerfMamba** explores pruning low-activity states in the SSM component to improve throughput and reduce memory usage while maintaining model accuracy under moderate pruning.

This work contributes to research on **Mamba, selective state space models, performance analysis, runtime profiling, model pruning, model compression, efficient AI, high-performance computing, and hardware-aware optimization**.

Researchers working on **large language models, sequence modeling, AI systems, neural network acceleration, scalable machine learning, and efficient deep learning** may find this work useful.

## Paper

**PerfMamba: Performance Analysis and Pruning of Selective State Space Models**  
Abdullah Al Asif, Mobina Kashaniyan, Sixing Yu, Juan Pablo Muñoz, Ali Jannesari  

Published in: **International Symposium on Benchmarking, Measuring and Optimization**  
Publisher: **Springer, Singapore**  
Year: **2026**  
Pages: **27–44**

Paper page: https://mobinakashaniyan.github.io/publications/perfmamba/

PDF: https://mobinakashaniyan.github.io/publications/perfmamba/PerfMamba%20Performance%20Analysis%20and%20Pruning%20of%20selective%20state%20space%20models.pdf

## Keywords

PerfMamba, Mamba, Mamba-1, Mamba-2, selective state space models, state space models, SSM, sequence modeling, Transformer alternatives, performance analysis, runtime profiling, benchmarking, resource utilization, memory access patterns, I/O characteristics, scaling analysis, model pruning, state pruning, model compression, efficient AI, high-performance computing, hardware-aware optimization, large language models, AI systems, neural network acceleration.

## Citation

Al Asif, A., Kashaniyan, M., Yu, S., Muñoz, J. P., & Jannesari, A. (2026). *PerfMamba: Performance analysis and pruning of selective state space models*. In **International Symposium on Benchmarking, Measuring and Optimization** (pp. 27–44). Springer, Singapore.
