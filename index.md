---
layout: default
title: Siddhant Mohan
---

<link rel="stylesheet" href="assets/custom.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

<p>
Applied AI/ML Research Engineer with <strong>4 years of work experience</strong> and an M.S. from NYU (graduated May 2026). Passionate about building efficient, state-of-the-art machine learning and computer vision systems. Actively seeking <strong>AI/ML Engineer and Research Scientist</strong> roles.

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

  <a class="btn fa-btn resume" href="Siddhant_Mohan_Resume.pdf" target="_blank" rel="noopener">
    <i class="fa-regular fa-file-lines"></i> Resume
  </a>
</div>

---

## Academic Projects

My graduate projects at NYU showcasing expertise in efficient AI and modern machine learning systems, including vision-language models, large language models, retrieval-augmented generation (RAG) and diffusion models.

### <span class="featured-project-title">Distribution-Aware Companding Quantization (DACQ)</span> <span class="project-title-links">[Paper](https://arxiv.org/abs/2603.00364) · [GitHub](https://github.com/siddhantmohan1110/dacq)</span>

DACQ is a post-training quantization method for large language models that uses distribution-aware companding to better preserve model weights under low-bit precision. It aims to improve upon Activation Aware Quantization (AWQ) by using non-uniform quantization bins based on the distribution instead of uniform quantization bins. The project studies the trade-off between weight reconstruction error, benchmark performance, and deployment efficiency across LLMs like Llama3-8B and Qwen2.5-7B, using benchmark datasets such as MMLU and WikiText-2. It **reduces weight reconstruction error (MSE/MAE) by 20%** compared to AWQ, while maintaining competitive accuracy and perplexity.

**Stack:** PyTorch • HuggingFace • CUDA • HPC (Slurm) • Statistical Modeling  

**Models:** Llama3-8B • Qwen2.5-7B

**Datasets:** MMLU • WikiText-2

**Keywords:** LLM Optimization • Post-Training Quantization • Companding • Efficient AI • Model Compression


<img src="assets/images/NLP_Poster_updated.png" alt="DACQ research poster" class="project-poster">


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
