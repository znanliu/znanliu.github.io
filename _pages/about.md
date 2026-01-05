---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a PhD Candidate in ECE department at the University of Michigan, co-advised by [Prof. Liyue Shen](https://liyueshen.engin.umich.edu/) and [Prof. Jesse Hamilton](https://medschool.umich.edu/profile/6748/jesse-hamilton). My research focuses on optimization and machine learning based methods for MR Fingerprinting sequence design and image reconstruction. I am particularly interested in quantitative cardiac MRI and imaging on systems to enable efficient, accelerated, and high-quality image acquisition. My work aims to advance data-driven optimization strategies that improve image fidelity, accelerate scan time, and enhance quantitative reliability. These efforts are closely integrate with clinical collaborations to ensure translational impact and real-world applicability in patient care.

### News

{% for item in site.data.news %}
- **{{ item.date }}** – {% if item.url %}[{{ item.title }}]({{ item.url }}){% else %}{{ item.title }}{% endif %}
{% endfor %}

<! --
<script type="text/javascript" id="mapmyvisitors" src="//mapmyvisitors.com/map.js?d=pguHiRWMKX6zEEkDl1GsuiLK4KV_I_WPdSa-IJjyOm4&cl=ffffff&w=a"></script>
-->
