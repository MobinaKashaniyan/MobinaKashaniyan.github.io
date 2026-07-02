---
title: "Why Dependency-Aware Auto-Scaling Matters in Serverless Computing"
date: 2026-07-02
draft: false
summary: "A research summary of my SAGE paper on dependency-aware serverless auto-scaling, multi-expert consensus, workload forecasting, and cost-aware resource allocation."
authors:
  - admin
tags:
  - Serverless Computing
  - Auto-Scaling
  - Function-as-a-Service
  - Cloud Resource Management
  - Workload Forecasting
  - Dependency-Aware Scaling
  - Multi-Expert Consensus
  - Ensemble Learning
  - Cold-Start Latency
categories:
  - Research Summary
  - Cloud Computing
  - Artificial Intelligence
---

Serverless computing provides automatic resource management and pay-per-use execution, but efficient auto-scaling remains challenging. Dynamic workloads, cold-start latency, and inter-function dependencies can make scaling decisions unreliable when each function is treated independently.

In my paper, **“An Auto-Scaling Approach for Serverless Environments Based on a Multi-Expert Consensus Mechanism,”** we propose a dependency-aware auto-scaling framework for Function-as-a-Service environments.

The framework models serverless applications as **directed dependency graphs**, identifies high-impact bottleneck functions using **degree centrality**, and applies short-horizon workload forecasting. Instead of relying on one predictor, the system combines multiple lightweight predictive models using a **multi-expert consensus mechanism** inspired by Bayesian model averaging.

This research contributes to **serverless computing, cloud resource management, workload forecasting, dependency-aware scaling, ensemble learning, and cost-aware optimization**.

## Paper

**An Auto-Scaling Approach for Serverless Environments Based on a Multi-Expert Consensus Mechanism**  
Mobina Kashaniyan, Mehrdad Ashtiani, Amirhossein Ghassemi  
Published in *Journal of Ambient Intelligence and Smart Environments*, SAGE Publications.

DOI: https://doi.org/10.1177/18761364261459585

Paper page: https://mobinakashaniyan.github.io/publications/consensus-autoscaling-serverless/

PDF: https://mobinakashaniyan.github.io/publications/consensus-autoscaling-serverless/an-auto-scaling-approach-serverless-environments-multi-expert-consensus.pdf.pdf
