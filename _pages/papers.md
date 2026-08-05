---
layout: archive
title: "Working Papers"
permalink: /papers/
author_profile: true
---

{% include base_path %}


{% for paper in site.papers reversed %}
  <section class="paper-listing">
    <h3>{{ paper.title }}</h3>
    <p><strong>{{ paper.status | default: "Working paper" }} ({{ paper.date | date: "%Y" }})</strong></p>
    {% if paper.excerpt %}
      <p>{{ paper.excerpt }}</p>
    {% endif %}
    {% if paper.pdf %}
      <p><a href="{{ paper.pdf }}">Download PDF</a></p>
    {% endif %}
  </section>
  <hr>
{% endfor %}