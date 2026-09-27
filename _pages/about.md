---
permalink: /
title: "Soujanya Ponnapalli"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div class="page-lead" markdown="1">

I am a systems researcher. I love building systems that are not just fast and
scalable, but also **reliable**, providing strong guarantees, such as performance
isolation and fault tolerance, in practice.<br>
<strong class="job-market">I am on the job market this year!</strong>

I am a postdoctoral scholar at the [University of California, Berkeley](https://www.berkeley.edu/),
  working with [Natacha Crooks](https://nacrooks.github.io/) and
  [Matei Zaharia](https://people.eecs.berkeley.edu/~matei/) at the
  [Sky Computing Lab](https://sky.cs.berkeley.edu/).
Before that, I completed my PhD at [UT Austin](https://www.utexas.edu/) with
  [Vijay Chidambaram](https://www.cs.utexas.edu/~vijay/), in the
  [Systems and Storage Lab](https://utsaslab.cs.utexas.edu/) and the
  [Lab for Advanced Systems Research](https://www.cs.utexas.edu/lasr/).
My dissertation aimed at
  [minimizing I/O bottlenecks to achieve scalable, high-throughput systems](https://people.eecs.berkeley.edu/~soujanya/dissertation.pdf).
Prior to that, I earned my Bachelor's with Honors in Computer Science and
  Engineering from [IIIT Hyderabad](https://iiit.ac.in/), where I worked with
  [Suresh Purini](https://www.iiit.ac.in/people/faculty/psuresh/).
I have always been equally passionate about [academic]({{ base_path }}/publications/)
  and [non-academic]({{ base_path }}/parallel-life/) pursuits, and in recognition,
  I received the best all-rounder gold medal.

My research sits at the intersection of distributed and storage systems. I
enjoy rethinking how systems should be designed to meet both the guarantees and
performance that applications need and expect. Take a look at the broad
[research themes](#research-themes) I have been working on!

</div>

### Selected Publications
-----

{% assign top_venues = "SIGMOD,VLDB,SOSP,OSDI,ATC,HotOS" | split: "," %}
{% assign pubs = site.publications | sort: 'order' %}

{% comment %}
  Same badge-and-card markup the publications page uses, via the .list__item
  wrapper its styles hang off, so the two pages share one badge width, one
  title alignment and one award colour. Compact here: title and award only,
  with the key insight and the paper links left to the full list.
{% endcomment %}
{% for post in pubs %}
  {% comment %}
    Liquid evaluates and/or right to left, so each condition gets its own flag.
    Only accepted work is listed here; the full list carries the rest.
  {% endcomment %}
  {% assign is_top = false %}
  {% if top_venues contains post.conf %}{% assign is_top = true %}{% endif %}
  {% assign is_accepted = true %}
  {% if post.status and post.status != '' %}{% assign is_accepted = false %}{% endif %}
  {% comment %} An entry can opt out of this list with `selected: false`. {% endcomment %}
  {% assign is_selected = true %}
  {% if post.selected == false %}{% assign is_selected = false %}{% endif %}
  {% if is_top and is_accepted and is_selected %}
  {% if post.pdfurl and post.pdfurl != '' %}{% assign paper_url = post.pdfurl %}{% else %}{% assign paper_url = post.paperurl %}{% endif %}
<div class="list__item publication-item">
<div class="publication-row">
  <div class="publication-badges">
    {% comment %}
      Venue and year on one line here, unlike the publications page: these
      cards are a single line of title, so a stacked badge would set the row
      height rather than the content.
    {% endcomment %}
    <div class="publication-badge">
      <span class="publication-badge-conf">{{ post.conf }}'{{ post.confyear | append: '' | slice: -2, 2 }}</span>
    </div>
    {% if post.conf2 and post.conf2 != '' %}
    <div class="publication-badge">
      <span class="publication-badge-conf">{{ post.conf2 }}'{{ post.confyear2 | append: '' | slice: -2, 2 }}</span>
    </div>
    {% endif %}
  </div>
  <div class="publication-body">
    <h2 class="archive__item-title publication-title" itemprop="headline">
      <a href="{{ paper_url }}" target="_blank" rel="noopener noreferrer">{{ post.title }}</a>
    </h2>
    {% if post.award and post.award != '' %}
    <p class="publication-status"><span class="publication-award">{{ post.award }}</span></p>
    {% endif %}
  </div>
</div>
</div>
  {% endif %}
{% endfor %}

<p class="page-intro">
  <a href="{{ base_path }}/publications/">The full publication list</a> with key insights behind each work!
</p>

### Research Themes
{: #research-themes}
-----

<div class="theme-grid">

  <div class="theme-card">
    <div class="theme-name">Performance and multi-tenancy</div>
    <div class="theme-blurb">
      How should multiple tenants share resources? I design resource-sharing
      mechanisms that bound the performance interference a tenant suffers in
      databases, the OS page cache, and LLM inference engines. I also work on
      making systems fast and I/O-efficient.
    </div>
    {% include theme-papers.html items="Delta Fair Sharing::vldb27/delta-fair-sharing|Token Latency Fairness::arxiv26/token-latency-fairness|Page Cache Fairness::|Metronome::vldb27/metronome|RainBlock::atc21/rainblock|mLSM::hotstorage18/mlsm" %}
  </div>

  <div class="theme-card">
    <div class="theme-name">Reliability and fault tolerance</div>
    <div class="theme-blurb">
      What guarantees should a system promise, and what is the cost of such
      abstractions? I work on fine-grained fault modeling for consensus,
      efficient crash recovery in databases, and rollback resistance in trusted
      storage. I also worked on finding where guarantees, such as crash
      consistency, are violated.
    </div>
    {% include theme-papers.html items="Rollbaccine::sigmod26/rollbaccine|Real Life Is Uncertain::powder|Powder::|Fugue::|CrashMonkey::osdi18/crashmonkey|Recoverable Processes::https://patents.google.com/patent/US20240152429A1/en" %}
  </div>

  <div class="theme-card">
    <div class="theme-name">Emerging technologies</div>
    <div class="theme-blurb">
      Persistent memory, CXL, accelerator disaggregation, holographic storage,
      and multi-cloud object stores each break an assumption baked into the storage
      stack. What does that stack look like when it is designed for these
      technologies?
    </div>
    {% include theme-papers.html items="SkyStore::skystore|SKYE::arxiv26/skye|DINOMO::vldb/dinomo|WineFS::sosp21/winefs|Holographic Storage::tos25/holographic-storage|GPU disaggregation::hotnets25/lost-in-translation" %}
  </div>

  <div class="theme-card">
    <div class="theme-name">Systems for AI</div>
    <div class="theme-blurb">
      When should a system be specialized, and for whom? I work on using
      agents to synthesize specialized systems just in time, for a given
      workload and setting. I also work on agent-first design: how these
      systems should change when agents, not humans, are the primary client.
    </div>
    {% include theme-papers.html items="Supporting Our AI Overlords::saa25/agent-first-data-systems|Just-in-Time Systems::mlforsys26/just-in-time-systems" %}
  </div>

</div>

### Selected News
-----

{% comment %}
  Same badge-and-card structure as the selected publications above, so the year
  badges line up with the venue badges and the cards share one left edge.
{% endcomment %}

<div class="list__item publication-item">
<div class="publication-row">
  <div class="publication-badges">
    <div class="publication-badge">
      <span class="publication-badge-conf">2025</span>
    </div>
  </div>
  <div class="publication-body">
    <div class="news-content">
      Invited for a talk at ETH Zurich, 06-18-2025<br>
      Rethinking Fault Tolerance: Abstractions, Guarantees, and Performance!
    </div>
  </div>
</div>
</div>

<div class="list__item publication-item">
<div class="publication-row">
  <div class="publication-badges">
    <div class="publication-badge">
      <span class="publication-badge-conf">2025</span>
    </div>
  </div>
  <div class="publication-body">
    <div class="news-content">
      <a href="https://suri.epfl.ch/#overview" target="_blank" rel="noopener noreferrer">Summer Research Institute 2025</a><br>
      Awarded a fellowship to attend SuRI at EPFL
    </div>
  </div>
</div>
</div>

<div class="list__item publication-item">
<div class="publication-row">
  <div class="publication-badges">
    <div class="publication-badge">
      <span class="publication-badge-conf">2024</span>
    </div>
  </div>
  <div class="publication-body">
    <div class="news-content">
      Received funding from <a href="https://rdi.berkeley.edu/" target="_blank" rel="noopener noreferrer">Berkeley RDI Frontier Research</a><br>
      Proposal: Building Scalable and IO-efficient Authenticated Storage Systems
    </div>
  </div>
</div>
</div>

<div class="list__item publication-item">
<div class="publication-row">
  <div class="publication-badges">
    <div class="publication-badge">
      <span class="publication-badge-conf">2024</span>
    </div>
  </div>
  <div class="publication-body">
    <div class="news-content">
      <a href="https://people.eecs.berkeley.edu/~soujanya/dissertation.pdf" target="_blank" rel="noopener noreferrer">Minimizing I/O Bottlenecks to Achieve Scalable and High-Throughput Systems</a><br>
      Vijay Chidambaram, Emmett Witchel, James Bornholt, Jonathan Goldstein, Natacha Crooks
    </div>
  </div>
</div>
</div>

### Industry Research
-----

{% comment %}
  Same label-and-value rows as Service below. Mentors are named because at
  these labs the mentor is the credential a reader recognises.
{% endcomment %}

<ul class="service-rows">
  <li><span class="service-role">Microsoft Research</span><span>Redmond, 2022 &middot; Jonathan Goldstein<br>
    Redmond, 2020 &middot; Anirudh Badam<br>
    Cambridge, 2019 &middot; Dushyanth Narayanan and Antony Rowstron</span></li>
  <li><span class="service-role">VMware Research</span><span>California, 2018 &middot; Michael Wei and Dahlia Malkhi</span></li>
  <li><span class="service-role">Patent</span><span><a href="https://patents.google.com/patent/US20240152429A1/en" target="_blank" rel="noopener noreferrer">Recoverable Processes</a>, US application 17/981,296<br>
    <a href="{{ base_path }}/posters/cascades.jpg" target="_blank" rel="noopener noreferrer">Poster</a>: Recovery Can Be Simple, Sky Retreat 2024</span></li>
</ul>

### Selected Awards
-----

{% comment %}
  The gold medal stays in the opening paragraph rather than being repeated
  here, so this section carries only what is not already on the page.
{% endcomment %}

{% comment %}
  One line each, with no label column: with three entries the labels carried
  no information the lines do not already give. Each line names the kind of
  award itself, so it still reads on its own.
{% endcomment %}

<ul class="service-plain">
  <li><a href="https://suri.epfl.ch/#overview" target="_blank" rel="noopener noreferrer">Summer Research Institute (SuRI) Fellowship</a>, EPFL, 2025</li>
  <li>James C. Browne Graduate Fellowship, UT Austin, 2017&ndash;18</li>
  <li>Best of VLDB&rsquo;25 nomination, for <a href="https://www.vldb.org/pvldb/vol18/p2084-liu.pdf" target="_blank" rel="noopener noreferrer">SkyStore</a></li>
</ul>

### Service
-----

<ul class="service-rows">
  <li><span class="service-role">Program Committee</span><span>OSDI'26, NSDI'26, ATC'25, NSDI'25, EuroSys'25</span></li>
  <li><span class="service-role">External Review Committee</span><span>FAST'25, ATC'24, NSDI'19</span></li>
  <li><span class="service-role">Journal Reviewer</span><span>ACM TOCS 2024</span></li>
  <li><span class="service-role">NSF Reviewer</span><span>Proposal review panel, 2026</span></li>
  {% comment %} GAAP lives under Mentoring and Leadership, not here. {% endcomment %}
  <li><span class="service-role">Other</span><span>Hallway discussion lead, SOSP'21<br>
    Shadow PC, EuroSys'20</span></li>
</ul>

### Mentoring and Leadership
-----

<ul class="service-plain">
  <li>I have mentored PhD, Masters, and undergraduate students.
    <a href="{{ base_path }}/mentoring/">See who I have worked with</a> and what we built together.</li>
  <li>I have mentored women in CS (WiCS) at UT Austin, and researchers at
    conferences.</li>
  <li>I co-founded and chaired the Graduate Application Assistance Program (GAAP) at UT Austin.</li>
  <li>I co-organize the <a href="https://sky.cs.berkeley.edu/" target="_blank" rel="noopener noreferrer">Sky Systems Seminar</a>
    at Berkeley, and have organized the Databases Seminar there and the Systems
    Seminar at UT Austin's Lab for Advanced Systems Research.</li>
</ul>

### Get in Touch!
-----

<p class="page-intro">
  If you would like to present your systems research at the Sky seminar, or just
  want to talk about any of this, please reach out:
  {% comment %}
    Written out, and clickable through the same js-email reassembly the sidebar
    uses. A literal mailto: here would put the address straight back into the
    markup, which is the first place a scraper looks.
  {% endcomment %}
  <a href="#" class="js-email" data-user="soujanya" data-domain="berkeley.edu">soujanya at berkeley dot edu</a> &middot;
  <a href="https://www.linkedin.com/in/soujanya-ponnapalli-553275107/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
</p>

<!-- "I am a postdoctoral scholar at the University of California, Berkeley, working in collaboration with Prof. Natacha Crooks and affiliated with the Sky Computing Lab within the EECS Department. Presently, my focus lies on untrusted storage systems and crash- and byzantine-fault tolerant distributed systems.

Prior to joining Berkeley, I completed my PhD in the CS Department at UT Austin, under the guidance of Prof. Vijay Chidambaram, as a member of the Systems and Storage Lab. My doctoral dissertation centered on minimizing I/O bottlenecks within modern systems' infrastructure to achieve heightened throughput and scalability.

Preceding my graduate studies, I obtained my Bachelor's degree with Honors in Computer Science and Engineering from the International Institute of Information Technology, Hyderabad (IIIT-H), where I collaborated with Prof. Suresh Purini. I was honored with the best all-rounder gold medal for academic excellence and my significant contributions to cultural and extracurricular activities at the institute." -->
