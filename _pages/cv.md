---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
{% assign cv = site.data.cv_sections %}

<a href="{{ base_path }}/files/cv.pdf" class="btn btn--primary">Download CV as PDF</a>


## Contact Information

Email  
:   [`{{ cv.basics.email }}`](mailto:{{ cv.basics.email }})

Web  
:   <{{ cv.basics.website }}>

GitHub  
:   <{{ cv.basics.github }}>

Location  
:   {{ cv.basics.location }}


## Education

<ul>
{%- for e in cv.education %}
  <li>
    <strong>{{ e.institution }}</strong>, {{ e.location }}<br />
    {{ e.degree }}, {{ e.dates }}.
    {%- for d in e.detail %}<br />{{ d }}.{% endfor %}
  </li>
{%- endfor %}
</ul>


## Research Experience

<ul>
{%- for r in cv.research_experience %}
  <li>
    <strong>{{ r.role }}</strong>, {{ r.institution }}<br />
    {{ r.dates }}.
    {%- if r.supervisor %}<br />Supervisor: {{ r.supervisor }}.{% endif %}<br />
    {{ r.topics }}.
  </li>
{%- endfor %}
</ul>


## Working Papers

<ul>{% for post in site.papers reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>


## Conference Presentations and Talks

<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>

## Teaching Experience

<ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>


## Fellowships and Grants

<ul>
{%- for f in cv.fellowships %}
  <li>{{ f }}.</li>
{%- endfor %}
</ul>


## Workshops and Seminars

<ul>
{%- for w in cv.workshops %}
  <li><strong>{{ w.name }}</strong>{% if w.venue %}, {{ w.venue }}{% endif %} — {{ w.role }}, {{ w.dates }}.</li>
{%- endfor %}
</ul>


## Skills

<ul>
{%- for s in cv.skills %}
  <li><strong>{{ s.label }}</strong>: {{ s.items }}</li>
{%- endfor %}
</ul>


## Service

<ul>
{%- for s in cv.service %}
  <li>{{ s }}.</li>
{%- endfor %}
</ul>


## References

{{ cv.references }}
