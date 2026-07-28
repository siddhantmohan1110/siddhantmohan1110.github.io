---
layout: default
title: Siddhant Mohan
---

<link rel="stylesheet" href="assets/custom.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

<p>
AI/ML Engineer with <strong>4 years of applied AI research experience</strong> and an M.S. from NYU (May 2026). Passionate about building efficient, scalable state-of-the-art machine learning and computer vision systems and actively seeking <strong>AI/ML Engineer and Applied Research</strong> opportunities.
</p>

<div class="button-row">
  <a class="btn fa-btn email" href="mailto:siddhantmohan1110@gmail.com">
    <i class="fa-solid fa-envelope"></i> Email
  </a>

  <a class="btn fa-btn github" href="https://github.com/siddhantmohan1110" target="_blank" rel="noopener">
    <i class="fa-brands fa-github"></i> GitHub
  </a>

  <a class="btn fa-btn linkedin" href="https://www.linkedin.com/in/siddhant-mohan-1110/" target="_blank" rel="noopener">
    <i class="fa-brands fa-linkedin"></i> LinkedIn
  </a>

  <a class="btn fa-btn resume" href="Siddhant_Mohan_CV_AI.pdf" target="_blank" rel="noopener">
    <i class="fa-regular fa-file-lines"></i> Resume
  </a>
</div>

---

## 🚀 Key Projects

### Distribution-Aware Companding Quantization (DACQ)

Modern Large Language Models (LLMs) are powerful but expensive to deploy due to their high memory and compute requirements. A common solution is **post-training quantization (PTQ)**, which reduces model precision without retraining. However, most existing methods rely on **uniform quantization**, which assumes weights are evenly distributed — an assumption that does not hold in practice.

In transformer models, weights are **highly non-uniform**, with dense regions near zero and long heavy tails. Uniform quantization therefore wastes precision in sparse regions and introduces unnecessary error in dense regions.

---

#### 💡 Key Idea

DACQ addresses this mismatch by making quantization **distribution-aware**.

Instead of using uniformly spaced quantization levels, DACQ:
- Models the **true statistical distribution of weights** in each layer  
- Applies a **CDF-based companding transform** to map weights into a uniform domain  
- Performs quantization in this transformed space  
- Maps values back to obtain a **non-uniform quantizer tailored to the model**

This allows:
- Higher precision where weights are dense  
- More efficient use of limited bit-width  

---

#### 🧠 Key Insight

Empirical analysis across LLaMA-3-8B and Qwen2.5-7B shows that transformer weights consistently follow a **logistic-like distribution**, rather than Gaussian or Laplace.

This explains why uniform quantization underperforms, and motivates the use of **logistic CDF-based companding** for improved fidelity.

---

#### ⚙️ Method Overview

DACQ combines two complementary components:

**1. Activation-Aware Scaling (AWQ-inspired)**  
Identifies important channels based on activations and rescales them to reduce output error.

**2. Distribution-Aware Companding (DACQ)**  
- Fits a parametric distribution to each layer  
- Uses its CDF to derive **non-uniform quantization levels**  
- Allocates resolution based on weight density  

We also introduce a **hybrid quantization scheme** that balances:
- Distribution-aware precision (for dense regions)  
- Uniform coverage (to preserve critical outliers)  

---

#### 🚀 Results

- Achieves **lower reconstruction error (MSE / MAE)** than strong baselines like AWQ  
- Maintains **competitive accuracy and perplexity** on benchmarks such as MMLU and WikiText-2  
- Provides **~15–20% throughput improvement** over full-precision models while retaining most benefits of 4-bit quantization :contentReference[oaicite:1]{index=1}  

---

#### ⚠️ Key Observation

Improved weight reconstruction does **not always translate to better model performance**.

DACQ reveals an important trade-off:
- Distribution-based methods optimize global error  
- But may compress **rare yet critical outlier weights**, which can affect downstream accuracy  

---

#### 🌍 Impact

DACQ demonstrates that **model-aware, distribution-driven quantization** can significantly improve efficiency while preserving performance, making large-scale LLM deployment more practical.

---

**Stack:** PyTorch • HuggingFace • CUDA • HPC (Slurm) • Statistical Modeling

Paper : https://arxiv.org/abs/2603.00364

GitHub : https://github.com/siddhantmohan1110/dacq


---

### Efficient Data Pipelines for Vision–Language Models
Clustered prompt embeddings for hybrid autoregressive transformers to reuse lower-scale generated images and reduce redundant computation. Improved computational efficiency through embedding clustering and distributed experimentation.

**Stack:** PyTorch • Ray • HPC (Slurm)

---

### Core-Set Selection for Incremental Learning
Analyzed dataset characteristics to construct compact core-sets that preserve downstream model performance during incremental updates, improving memory efficiency without significant accuracy degradation.

**Stack:** PyTorch • Data analysis • Model evaluation

---

## 💼 Work Experience

### Senior Research Engineer — Toshiba Software India (R&D)
*2019 – 2024*

Led applied AI research projects in industrial computer vision and manufacturing systems.

- Developed incremental learning pipelines for object detection systems.
- Built anomaly localization systems evaluated on MVTec-AD.
- Designed domain adaptation solutions for robotic and inspection environments.
- Optimized deep learning pipelines under compute and latency constraints.

---

## 🎓 Education

### New York University (NYU) Tandon School of Engineering
**M.S. Electrical Engineering** — Expected May 2026  
Coursework: Machine Learning, Deep Learning, Computer Vision, NLP, Efficient AI, Probability & Statistics

---

### Indian Institute of Technology (IIT) Tirupati
**B.Tech. Electrical Engineering** — 2020  

---

## 🛠 Technical Skills

**Languages:** Python, C/C++, SQL  
**Frameworks:** PyTorch, TensorFlow, HuggingFace, Ray, MLflow  
**Systems:** CUDA, Distributed Training, Docker, Linux, Slurm  
**Focus Areas:** LLM Optimization, Quantization, Efficient AI Systems, Computer Vision