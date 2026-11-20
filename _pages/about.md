---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Ph.D. candidate in Electrical and Computer Engineering at the University of Michigan, co-advised by [Prof. Liyue Shen](https://liyueshen.engin.umich.edu/) and [Prof. Jesse Hamilton](https://medschool.umich.edu/profile/6748/jesse-hamilton). I work on **machine learning, computer vision, and inverse problems**, and on the **ML systems** that take these methods from research code to deployment.

My research develops self-supervised and physics-informed deep learning methods that reconstruct images, videos, and physical parameters from heavily undersampled, noisy measurements, without labeled training data. The main application is quantitative cardiac MRI. My methods have reached a clinical scanner, where one runs inline on an edge GPU. More on the [Research](/research/) page.

**I am seeking a Summer 2027 Research Scientist / ML Engineer internship.** Feel free to reach out at [znanliu@umich.edu](mailto:znanliu@umich.edu).

### Research Interests

- Self-supervised learning and generative priors for inverse problems
- Meta-learning and fast test-time adaptation
- Image and video reconstruction, motion correction
- Efficient GPU inference and on-device deployment

### News

{% for item in site.data.news %}
- **{{ item.date }}** – {% if item.url %}[{{ item.title }}]({{ item.url }}){% else %}{{ item.title }}{% endif %}
{% endfor %}
