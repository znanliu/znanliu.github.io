---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

Full list on [Google Scholar]({{ site.author.googlescholar }}).

## Journal Papers
{% for paper in site.data.journal %}
- **{{ paper.title }}**  
  {{ paper.authors }}  
  _{{ paper.venue }}_  
{% endfor %}

## Machine Learning Conference Papers
{% for paper in site.data.ml_conference %}
- **{{ paper.title }}**  
  {{ paper.authors }}  
  _{{ paper.venue }}_  
{% endfor %}

## Selected Conference Abstracts
I have co-authored 22 ISMRM/SCMR abstracts (9 as first author), with 5 oral presentations. First-author abstracts:

{% for paper in site.data.conference %}
- **{{ paper.title }}**  
  {{ paper.authors }}  
  _{{ paper.conference }}_  
{% endfor %}
