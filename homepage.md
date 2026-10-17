# Yusong Zhu

Hi, welcome to my corner of the Internet!

I am a **Ph.D. student in Computer Science at UT Austin**, advised by **[Kevin Tian](https://kjtian.github.io/)** and **[Eric Price](https://www.cs.utexas.edu/~ecprice/)**. Before joining UT Austin, I received my bachelor's degree in Software Engineering from Tsinghua University.

My research focuses on the **theoretical foundations of generative models**. I am also broadly interested in high-dimensional statistics, learning theory, and trustworthy machine learning.

Recently, I have been particularly interested in the question: **How can we effectively and reliably evaluate and audit the behavior of modern generative models?** As these models tackle increasingly complex and challenging tasks, much of the research focuses on expanding and improving their capabilities. This progress calls for principled evaluation and auditing methods that help us understand what these models can do, where they fail, and whether their behavior meets our expectations.

For example, my recent work explores the following questions:

1. **When a metric relies on distributional assumptions, are standard estimators accurate under those assumptions, and can we do better?**

   For the widely used Fréchet Inception Distance (FID), the standard empirical estimator can exhibit substantial systematic bias even when the underlying Gaussian assumptions hold. Reproducible scores can therefore remain far from the population quantity the metric is intended to measure. In our work, we give a sharp theoretical characterization of this estimation problem and develop a computationally efficient estimator with optimal sample complexity under a Gaussian model. We also demonstrate improved estimation accuracy on ImageNet. [Paper](https://arxiv.org/abs/2610.07114)

2. **Can we use the structure of modern generative models to measure distributional differences efficiently, without imposing parametric assumptions on their output distributions?**

   In our work on autoregressive models, we use their sequential prediction and sampling structure to develop efficient estimators of total variation distance with provable guarantees. We apply these methods to quantify differences between the output distributions of different LLM deployments, including vLLM and SGLang serving identical model weights. This provides a direct way to assess how deployment choices affect model behavior. [Paper](https://arxiv.org/abs/2607.19510)

Email: [zhuys@utexas.edu](mailto:zhuys@utexas.edu)

Google Scholar: [Yusong Zhu](https://scholar.google.com/citations?user=abdQY_YAAAAJ&hl=en)

---

# Research Interests

- Theoretical foundations of generative models
- Sampling algorithms with provable guarantees
- Evaluation and auditing of large language models and diffusion models
- High-dimensional statistics

---

# Publications

*Authors are listed in alphabetical order unless otherwise noted.*

## Sample-Optimal Estimation of the Fréchet Inception Distance
**Preprint, 2026**

[Paper](https://arxiv.org/abs/2610.07114) · [arXiv](https://arxiv.org/abs/2610.07114) · [Code](https://github.com/zys996/sample-optimal-fid-estimation)

**Authors:** Ziyun Chen, Jerry Li, Kevin Tian, Yusong Zhu

---

## High-Magnetization Sampling at Low Temperatures: Ising Models and Bayesian Sparse Linear Regression
**Preprint, 2026**

[Paper](https://arxiv.org/abs/2609.08873v1) · [arXiv](https://arxiv.org/abs/2609.08873)

**Authors:** Syamantak Kumar, Purnamrita Sarkar, Kevin Tian, Yusong Zhu

---

## The Tractability Landscape of Sampling with Inexact Scores
**Preprint, 2026**

[Paper](https://arxiv.org/abs/2607.19004) · [arXiv](https://arxiv.org/abs/2607.19004)

**Authors:** Anming Gu, Kevin Tian, Hubert Yang, Yusong Zhu

---

## Revisiting the Provable-Auditable Privacy Gap of DP-SGD
**Advances in Neural Information Processing Systems (NeurIPS), 2026**

[Paper](https://arxiv.org/abs/2608.28934) · [arXiv](https://arxiv.org/abs/2608.28934) · [Code](https://github.com/pineappleEnthusiast/empirical-privacy-defense)

**Authors:** Saloni Modi<sup>*</sup>, Srivi Balaji, Yusong Zhu, Gautam Kamath, Kevin Tian

<sup>*</sup> First author; authors are not listed alphabetically.

---

## Total Variation Distance Estimation in Autoregressive Models
**Advances in Neural Information Processing Systems (NeurIPS), 2026. Preliminary version presented at the ICML 2026 Hypothesis Testing Workshop.**

[Paper](https://arxiv.org/abs/2607.19510) · [arXiv](https://arxiv.org/abs/2607.19510) · [Code](https://github.com/XunZhiyang/llm-tv-estimation)

**Authors:** Eric Price, Kevin Tian, Zhiyang Xun, Yusong Zhu

---

## Separating Oblivious and Adaptive Models of Variable Selection
**Conference on Learning Theory (COLT), 2026**

[Paper](https://proceedings.mlr.press/v336/chen26b.html) · [arXiv](https://arxiv.org/abs/2602.16568)

**Authors:** Ziyun Chen, Jerry Li, Kevin Tian, Yusong Zhu

---

## Spike-and-Slab Posterior Sampling in High Dimensions
**Conference on Learning Theory (COLT), 2025**

[Paper](https://proceedings.mlr.press/v291/kumar25a.html) · [arXiv](https://arxiv.org/abs/2503.02798)

**Authors:** Syamantak Kumar, Purnamrita Sarkar, Kevin Tian, Yusong Zhu

---

## Fast Conditional Mixing of MCMC Algorithms for Non-log-concave Distributions
**Advances in Neural Information Processing Systems (NeurIPS), 2023**

[Paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/2b00b3331bd0f5fbfdd966ac06338f6d-Abstract-Conference.html) · [arXiv](https://arxiv.org/abs/2306.10506)

**Authors:** Xiang Cheng, Bohan Wang, Jingzhao Zhang, Yusong Zhu

---

# News

- **Summer 2026** – Visiting [Jerry Li](https://jerryzli.github.io/) at the University of Washington.
- **July 2026** – One paper presented at the ICML 2026 Hypothesis Testing Workshop.
- **June 2026** – One paper presented at COLT 2026.

---

# Education

## The University of Texas at Austin
**Ph.D. student in Computer Science, September 2024–Present**

Advisors: Kevin Tian and Eric Price

## Tsinghua University, School of Software
**B.S. in Software Engineering, September 2020–June 2024**

## Tsinghua University, Department of Statistics
**Minor in Statistics, September 2020–June 2024**

---

# Teaching

- **Teaching Assistant**, CS 395T: Continuous Algorithms, The University of Texas at Austin, Spring 2026
- **Volunteer Mathematics and Programming Tutor**, Tsinghua University, 2020–2022

---

# Professional Service

- **Conference Reviewer:** ICML 2026 (**Gold Reviewer**), FOCS 2026, and NeurIPS 2026.
