---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<p class="page-intro">
  18 papers on storage and distributed systems, at VLDB, SIGMOD, SOSP, OSDI, and
  ATC among others, including a Best of VLDB'25 nomination. Each entry below
  states the key insight behind the work in two or three lines.
</p>

{% comment %} Ordered to match the CV, via the `order` field in each entry. {% endcomment %}
{% assign pubs = site.publications | sort: 'order' %}
{% for post in pubs %}
  {% include publication-list-item.html %}
{% endfor %} 