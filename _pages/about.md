---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Ph.D. candidate in Electrical and Computer Engineering at the University of Michigan, co-advised by [Prof. Liyue Shen](https://liyueshen.engin.umich.edu/) and [Prof. Jesse Hamilton](https://medschool.umich.edu/profile/6748/jesse-hamilton). I work on **machine learning, computer vision, and inverse problems**, and on the **ML systems** that take these methods from research code to deployment.

My research develops self-supervised and physics-informed deep learning methods that reconstruct images, videos, and physical parameters from heavily undersampled, noisy measurements, without labeled training data. I combine generative priors, meta-learning for fast test-time adaptation, and GPU-level performance engineering, and I validate the methods on real-world data, including inline deployment on a clinical MRI scanner. The main application of my work is quantitative cardiac MRI (MR Fingerprinting).

**I am seeking a Summer 2027 Research Scientist / ML Engineer internship.** Feel free to reach out at [znanliu@umich.edu](mailto:znanliu@umich.edu).

### Research Highlights

- **Meta-learned self-supervised inverse-problem solver, from research to on-device deployment.** A PyTorch framework that jointly learns the reconstruction network, the forward-model parameters, and physical-parameter estimates from unlabeled data. REPTILE meta-learning across 40 datasets and profiling-driven GPU optimization (mixed precision, CUDA Graphs, Toeplitz operators) cut per-sample time by **60×** (42 min → ~40 s) on static data and **35×** (2 h → ~3.4 min) on time-series data with no loss in accuracy. I deployed it **inline on a clinical MRI scanner** as a streaming server inside the vendor's sandboxed, network-isolated runtime, running on an 8 GB edge GPU.
- **Self-supervised spatiotemporal reconstruction with learned motion correction.** A physics-informed generative model that recovers a 24-frame sequence and multiple physical parameters from 4× undersampled Fourier-domain data, plus a GPU non-rigid alignment module that **halved estimate variability** across 20 subjects. Acquisition time drops **4×** (~11 s → 2.8 s), validated against calibrated ground truth (R² > 0.99).

### News

{% for item in site.data.news %}
- **{{ item.date }}** – {% if item.url %}[{{ item.title }}]({{ item.url }}){% else %}{{ item.title }}{% endif %}
{% endfor %}

### Education

- **Ph.D. in Electrical and Computer Engineering**, University of Michigan, Ann Arbor, 2024 – present (expected May 2028)
- **M.S. in Electrical and Computer Engineering**, University of Michigan, Ann Arbor, 2022 – 2024
- **B.Eng. in Electronics and Information Technology**, Beijing Forestry University, 2018 – 2022

### Experience

- **Software Engineering Intern**, Tencent (Video Group), Beijing, Jan. – Apr. 2022. Built and maintained Go backend services for a large-scale video-streaming platform.

### Awards

- ISMRM Summa Cum Laude Merit Award, 2024
- National Scholarship, Beijing Forestry University, 2020
