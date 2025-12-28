---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---


## Conference & Workshops

{% for paper in site.data.conference %}
- **{{ paper.title }}**  
  *{{ paper.authors }}*  
  _{{ paper.conference }}_  
{% endfor %}