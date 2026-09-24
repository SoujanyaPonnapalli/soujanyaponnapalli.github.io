---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

{% comment %} Ordered to match the CV, via the `order` field in each entry. {% endcomment %}
{% assign pubs = site.publications | sort: 'order' %}
{% for post in pubs %}
  {% include publication-list-item.html %}
{% endfor %} 