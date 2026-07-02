---
title: "PerfMamba: Performance Analysis and Pruning of Selective State Space Models"
date: 2026-01-01
publishDate: 2026-01-01
draft: false
authors:
  - Abdullah Al Asif
  - "**Mobina Kashaniyan**"
  - Sixing Yu
  - Juan Pablo Muñoz
  - Ali Jannesari
publication_types:
  - "1"
publication: "In *International Symposium on Benchmarking, Measuring and Optimization*, Springer, Singapore, 2026, pp. 27–44."
conference: "International Symposium on Benchmarking, Measuring and Optimization"
publisher: "Springer, Singapore"
pages: "27–44"
url_pdf: "https://mobinakashaniyan.github.io/papers/perfmamba-performance-analysis-pruning-selective-state-space-models.pdf"
abstract: "Recent advances in sequence modeling have introduced selective state space models as promising alternatives to Transformer architectures, offering theoretical computational efficiency and sequence processing advantages. However, a comprehensive understanding of selective state space models in runtime behavior, resource utilization, memory access patterns, I/O characteristics, and scaling behavior remains limited. This paper presents PerfMamba, a performance analysis and pruning study of Mamba-1 and Mamba-2. The work systematically profiles selective state space models across sequence lengths from 64 to 16,384 tokens and analyzes computation patterns, memory behavior, I/O characteristics, and scaling properties. Based on these insights, PerfMamba proposes a pruning technique that selectively removes low-activity states within the SSM component, improving throughput and reducing memory usage while maintaining accuracy within a moderate pruning regime."
summary: "PerfMamba analyzes the runtime behavior, resource utilization, memory access patterns, scaling properties, and pruning opportunities of Mamba-1 and Mamba-2 selective state space models."
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
  - Benchmarking
  - Runtime Profiling
  - Resource Utilization
  - Memory Access Patterns
  - I/O Characteristics
  - Scaling Analysis
  - Model Pruning
  - State Pruning
  - Model Compression
  - Efficient AI
  - High-Performance Computing
  - Hardware-Aware Optimization
  - Large Language Models
  - AI Systems
  - Neural Network Acceleration
categories:
  - Conference Paper
  - Efficient AI
  - High-Performance Computing
sitemap:
  priority: 1.0
  changefreq: monthly
links:
  - icon_pack: fas
    icon: file-pdf
    name: PDF
    url: "https://mobinakashaniyan.github.io/papers/perfmamba-performance-analysis-pruning-selective-state-space-models.pdf"
  - icon_pack: fas
    icon: newspaper
    name: Research Summary
    url: "https://mobinakashaniyan.github.io/post/perfmamba-performance-analysis-pruning/"
---

This paper contributes to research on **PerfMamba, Mamba-1, Mamba-2, selective state space models, performance analysis, model pruning, benchmarking, efficient AI, and high-performance computing** by providing a systematic empirical study of the runtime behavior and optimization opportunities of Mamba-style architectures.

Recent sequence modeling research has introduced **selective state space models** as efficient alternatives to Transformer architectures. However, their real-world performance behavior, memory access patterns, I/O characteristics, resource utilization, and scaling properties require deeper analysis for effective deployment.

**PerfMamba** profiles **Mamba-1 and Mamba-2** across sequence lengths from **64 to 16,384 tokens**. The study analyzes computation patterns, memory behavior, I/O characteristics, and scaling trends to identify the components that dominate runtime and resource usage.

Based on these insights, the paper proposes a pruning technique that removes low-activity states within the SSM component. This supports improved throughput and reduced memory usage while maintaining accuracy under moderate pruning.

This work is relevant to researchers working on **Mamba, selective state space models, state space models, large language models, sequence modeling, model pruning, model compression, runtime profiling, AI systems, neural network acceleration, and hardware-aware optimization**.

**Keywords:** PerfMamba, Mamba, Mamba-1, Mamba-2, selective state space models, state space models, SSM, sequence modeling, Transformer alternatives, performance analysis, benchmarking, runtime profiling, resource utilization, memory access patterns, I/O characteristics, scaling analysis, model pruning, state pruning, model compression, efficient AI, high-performance computing, hardware-aware optimization, large language models, AI systems.

**Citation:**

Al Asif, A., Kashaniyan, M., Yu, S., Muñoz, J. P., & Jannesari, A. (2026). PerfMamba: Performance analysis and pruning of selective state space models. In *International Symposium on Benchmarking, Measuring and Optimization* (pp. 27–44). Springer, Singapore.
