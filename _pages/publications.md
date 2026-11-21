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
  _{{ paper.venue }}_{% if paper.url %} [[{{ paper.link_label }}]]({{ paper.url }}){% endif %}  
{% endfor %}

## Conference Papers
{% for paper in site.data.conference_papers %}
- **{{ paper.title }}**  
  {{ paper.authors }}  
  _{{ paper.venue }}_{% if paper.url %} [[{{ paper.link_label }}]]({{ paper.url }}){% endif %}  
{% endfor %}

## Conference Abstracts
I have co-authored 22 ISMRM/SCMR abstracts (9 as first author), with 5 oral presentations. Selected abstracts are listed below.

### First-author
{% for paper in site.data.conference %}{% if paper.first_author %}
- **{{ paper.title }}**  
  {{ paper.authors }}  
  _{{ paper.conference }}_{% if paper.url %} [[Abstract]]({{ paper.url }}){% endif %}  
{% endif %}{% endfor %}

### Co-author
{% for paper in site.data.conference %}{% unless paper.first_author %}
- **{{ paper.title }}**  
  {{ paper.authors }}  
  _{{ paper.conference }}_{% if paper.url %} [[Abstract]]({{ paper.url }}){% endif %}  
{% endunless %}{% endfor %}
