---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<p class="page-intro">
  Here's a full list of my papers on storage and distributed systems, accepted at
  VLDB, SOSP, OSDI, SIGMOD, and ATC among others, including a Best of VLDB'25
  nomination. For the curious, I've outlined the key insight behind each paper in
  a few lines.
</p>

{% comment %} Ordered to match the CV, via the `order` field in each entry. {% endcomment %}
{% assign pubs = site.publications | sort: 'order' %}
{% for post in pubs %}
  {% include publication-list-item.html %}
{% endfor %} 