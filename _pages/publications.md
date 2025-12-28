---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

## Conference & Workshops
{% for paper in site.data.conference %}
- **{{ paper.title }}**  
  *{{ paper.authors }}*  
  _{{ paper.conference }}_  
{% endfor %}