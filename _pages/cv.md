---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<p class="page-intro">
  You can also download my
  <a href="{{ base_path }}/soujanya-resume.pdf" target="_blank" rel="noopener noreferrer">resume</a>
  and <a href="{{ base_path }}/soujanya-cv.pdf" target="_blank" rel="noopener noreferrer">CV</a>
  as PDFs!
</p>

{% comment %}
  Laid out with the same badge-and-card rows as the collaborators and mentoring
  pages, so the whole site shares one type scale. Publications, preprints and
  mentees are generated from _publications and _data/mentees.yml rather than
  retyped, so this page cannot drift from the other two.
{% endcomment %}

<div class="people-section">
  <div class="people-label">Work and education</div>
  <div class="people-names">
    <div class="cv-entry">
      <div class="cv-entry-head"><strong>University of California, Berkeley</strong><span class="cv-years">2023&ndash;ongoing</span></div>
      Postdoc &middot; Sky Computing Lab &middot; EECS Department<br>
      Supervisors: Natacha Crooks and Matei Zaharia
    </div>
    <div class="cv-entry">
      <div class="cv-entry-head"><strong>University of Texas at Austin</strong><span class="cv-years">2017&ndash;23</span></div>
      PhD &middot; Systems and Storage Lab &middot; CS Department<br>
      Advisor: Vijay Chidambaram<br>
      Dissertation: Minimizing I/O Bottlenecks to Achieve Scalable and High-Throughput Systems
    </div>
    <div class="cv-entry">
      <div class="cv-entry-head"><strong>International Institute of Information Technology, Hyderabad</strong><span class="cv-years">2013&ndash;17</span></div>
      Bachelor's with Honors &middot; SERC Lab &middot; CS and Engineering<br>
      Advisor: Suresh Purini
    </div>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Interests</div>
  <div class="people-names">
    Distributed systems &middot; Storage systems &middot; Operating systems &middot; AI systems<br>
    I am a systems researcher. I build systems that are not just fast and scalable but also
    reliable, providing strong guarantees such as performance isolation and fault tolerance
    in practice.
  </div>
</div>

{% assign all_pubs = site.publications | sort: 'order' %}

<div class="people-section">
  <div class="people-label">Publications</div>
  <div class="people-names">
    <ol class="cv-list">
    {% for post in all_pubs %}
      {% unless post.conf == 'arXiv' %}
      <li>
        <span class="cv-title">{{ post.title }}</span>
        <span class="cv-venue">[{{ post.conf }}'{{ post.confyear | append: '' | slice: -2, 2 }}{% if post.conf2 and post.conf2 != '' %}, {{ post.conf2 }}'{{ post.confyear2 | append: '' | slice: -2, 2 }}{% endif %}]</span><br>
        <span class="cv-authors">{{ post.authors | replace: 'Soujanya Ponnapalli', '<strong>Soujanya Ponnapalli</strong>' }}</span>
        {% assign has_status = false %}
        {% if post.status and post.status != '' %}{% assign has_status = true %}{% endif %}
        {% assign has_award = false %}
        {% if post.award and post.award != '' %}{% assign has_award = true %}{% endif %}
        {% if has_status or has_award %}<br>
        <span class="cv-note">{% if has_status %}{{ post.status }}{% endif %}{% if has_status and has_award %} &middot; {% endif %}{% if has_award %}{{ post.award }}{% endif %}</span>
        {% endif %}
      </li>
      {% endunless %}
    {% endfor %}
    </ol>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Preprints</div>
  <div class="people-names">
    <ol class="cv-list">
    {% for post in all_pubs %}
      {% if post.conf == 'arXiv' %}
      <li>
        <span class="cv-title">{{ post.title }}</span>
        <span class="cv-venue">[arXiv'{{ post.confyear | append: '' | slice: -2, 2 }}]</span><br>
        <span class="cv-authors">{{ post.authors | replace: 'Soujanya Ponnapalli', '<strong>Soujanya Ponnapalli</strong>' }}</span>
      </li>
      {% endif %}
    {% endfor %}
    </ol>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Patents</div>
  <div class="people-names">
    <span class="cv-title">Recoverable Processes</span>
    <span class="cv-venue">[US Patent App. 17/981,296]</span><br>
    <span class="cv-authors">Jonathan D. Goldstein, Philip A. Bernstein, <strong>Soujanya Ponnapalli</strong>,
    Jose M. Faleiro, and Peter Charles Shrosbree</span>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Ongoing projects</div>
  <div class="people-names">
    <div class="cv-entry">
      <span class="cv-title">Page Cache Fairness: Performance Isolation for Multiple Tenants in Operating Systems</span><br>
      <span class="cv-authors"><strong>Soujanya Ponnapalli</strong>, Charisse Ivana Yeung, Natacha Crooks, and Matei Zaharia</span>
    </div>
    <div class="cv-entry">
      <span class="cv-title">Powder: Fine-Grained Fault-Tolerance for Distributed Storage Systems</span><br>
      <span class="cv-authors">Reginald Frank, <strong>Soujanya Ponnapalli</strong>, Neil Giridharan, Naama Ben-David, and Natacha Crooks</span>
    </div>
    <div class="cv-entry">
      <span class="cv-title">Fugue: Exploring Durability Trade-Offs in Replicated Storage</span><br>
      <span class="cv-authors">Diogo Antunes, Baltasar Dinis, <strong>Soujanya Ponnapalli</strong>, Vijay Chidambaram, Peter Druschel, and Rodrigo Rodrigues</span>
    </div>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Work experience</div>
  <div class="people-names">
    <ul class="cv-rows">
      <li><span>Microsoft Research, Redmond &middot; Mentor: Jonathan Goldstein</span><span class="cv-years">Summer '22</span></li>
      <li><span>Microsoft Research, Redmond &middot; Mentor: Anirudh Badam</span><span class="cv-years">Summer '20</span></li>
      <li><span>Microsoft Research, Cambridge &middot; Mentors: Dushyanth Narayanan and Antony Rowstron</span><span class="cv-years">Summer '19</span></li>
      <li><span>VMware Research, California &middot; Mentors: Michael Wei and Dahlia Malkhi</span><span class="cv-years">Summer '18</span></li>
    </ul>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Teaching</div>
  <div class="people-names">
    <ul class="cv-rows">
      <li><span>Teaching Assistant, UT Austin &middot; Virtualization with Vijay Chidambaram</span><span class="cv-years">Fall '20, '23</span></li>
      <li><span>Teaching Assistant, IIIT-H &middot; Algorithms and Data Structures with Kishore Kothapalli</span><span class="cv-years">2015&ndash;17</span></li>
      <li><span>Teaching Assistant, IIIT-H &middot; Operating Systems with Suresh Purini</span><span class="cv-years">2015&ndash;17</span></li>
      <li><span>Teaching Assistant, IIIT-H &middot; Electrical Science with Rambabu Kalla</span><span class="cv-years">2015&ndash;17</span></li>
    </ul>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Service</div>
  <div class="people-names">
    <ul class="cv-rows">
      <li><span>NSF proposal reviewer</span><span class="cv-years">2026</span></li>
      <li><span>Program Committee</span><span class="cv-years">OSDI'26, NSDI'26, ATC'25, NSDI'25, EuroSys'25</span></li>
      <li><span>External Program Committee</span><span class="cv-years">FAST'25, ATC'24, NSDI'19</span></li>
      <li><span>Journal reviewer, ACM TOCS</span><span class="cv-years">2024</span></li>
      <li><span>Hallway discussion lead, SOSP</span><span class="cv-years">2021</span></li>
      <li><span>Shadow PC, EuroSys</span><span class="cv-years">2020</span></li>
      <li><span>Chair, Graduate Application Assistance Program (GAAP@UT)</span><span class="cv-years">2020&ndash;21</span></li>
    </ul>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Mentoring</div>
  <div class="people-names">
    {% for block in site.data.mentees %}
      <div class="cv-entry">
        <strong>{{ block.group }} students</strong><br>
        {% for s in block.students %}{{ s.name }}, {{ s.where }}{% unless forloop.last %}<br>{% endunless %}{% endfor %}
      </div>
    {% endfor %}
    <a href="{{ base_path }}/mentoring/">See the projects we worked on together</a>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Leadership</div>
  <div class="people-names">
    <ul class="cv-rows">
      <li><span>Organizer, Sky Systems Seminar, Sky Computing Lab, UC Berkeley</span><span class="cv-years">2024&ndash;25</span></li>
      <li><span>Co-organizer, Databases Seminar, Sky Computing Lab, UC Berkeley</span><span class="cv-years">2024&ndash;25</span></li>
      <li><span>Representative, Graduate Association of Computer Sciences (GRACS@UT)</span><span class="cv-years">2020&ndash;21</span></li>
      <li><span>Mentor, Women in Computer Science (WiCS), UT Austin</span><span class="cv-years">2019&ndash;20</span></li>
      <li><span>Co-organizer, Systems Seminar, Lab for Advanced Systems Research, UT Austin</span><span class="cv-years">2018</span></li>
    </ul>
  </div>
</div>

<div class="people-section">
  <div class="people-label">Awards and grants</div>
  <div class="people-names">
    <ul class="cv-rows">
      <li><span>Summer Research Institute (SuRI) Fellowship, EPFL</span><span class="cv-years">2025</span></li>
      <li><span>Berkeley RDI Frontier Research Funding</span><span class="cv-years">2024</span></li>
      <li><span>The James C. Browne Graduate Fellowship</span><span class="cv-years">2017&ndash;18</span></li>
      <li><span>IIIT-H Best All-Rounder Gold Medalist</span><span class="cv-years">2017</span></li>
      <li><span>Dean's Award for ranking in the top 5% of students, IIIT-H</span><span class="cv-years">2014&ndash;17</span></li>
    </ul>
  </div>
</div>

<div class="people-section">
  <div class="people-label">References</div>
  <div class="people-names">
    Natacha Crooks and Matei Zaharia (UC Berkeley), Vijay Chidambaram (UT Austin),
    Marcos K. Aguilera (NVIDIA), and Tianyin Xu (UIUC)
  </div>
</div>
