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
scalable, but also reliable, providing strong guarantees, such as performance
isolation and fault tolerance, in practice.<br>
**I am on the job market this year!**

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
I have always been equally passionate about academic and non-academic pursuits,
  and in recognition, I received the best all-rounder gold medal.

My research sits at the intersection of distributed and storage systems. I
rethink how systems *should be* designed to meet the demands of new-age
applications, both the guarantees and performance that applications need and
expect. Take a look at the broad [research themes](#research-themes) I have been
working on!

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
      How do you give one tenant a guarantee when it shares storage, page
      cache and inference capacity with every other tenant? I design isolation
      mechanisms that put a bound on the interference a tenant can suffer,
      and cut the cost of the shared path itself.
    </div>
    {% include theme-papers.html items="Delta Fair Sharing::vldb27/delta-fair-sharing|Token Latency Fairness::arxiv26/token-latency-fairness|Page Cache Fairness::|Metronome::vldb27/metronome" %}
  </div>

  <div class="theme-card">
    <div class="theme-name">Reliability and fault tolerance</div>
    <div class="theme-blurb">
      What should a system promise, and what should it charge for that
      promise? I work on finer-grained fault tolerance and recovery, so that
      the guarantees a system provides match the faults it actually sees.
    </div>
    {% include theme-papers.html items="Real Life Is Uncertain::powder|Powder::|Fugue::|CrashMonkey::osdi18/crashmonkey|Recoverable Processes::" %}
  </div>

  <div class="theme-card">
    <div class="theme-name">Emerging technologies</div>
    <div class="theme-blurb">
      Persistent memory, CXL, disaggregation, holographic media and
      multi-cloud object stores each break an assumption baked into the storage
      stack. What does that stack look like when it is designed around what these
      technologies actually offer?
    </div>
    {% include theme-papers.html items="SkyStore::skystore|SKYE::arxiv26/skye|DINOMO::vldb/dinomo|WineFS::sosp21/winefs|Holographic Storage::tos25/holographic-storage|Lost in Translation::hotnets25/lost-in-translation" %}
  </div>

  <div class="theme-card">
    <div class="theme-name">Systems for AI</div>
    <div class="theme-blurb">
      Agents query, branch and discard data very differently from people.
      What do data systems look like when agents, not humans, are the primary
      client?
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

### Service
-----

<ul class="service-rows">
  <li><span class="service-role">Program Committee</span><span>OSDI'26, NSDI'26, ATC'25, NSDI'25, EuroSys'25</span></li>
  <li><span class="service-role">External Review Committee</span><span>FAST'25, ATC'24, NSDI'19</span></li>
  <li><span class="service-role">Journal Reviewer</span><span>ACM TOCS 2024</span></li>
  <li><span class="service-role">NSF Reviewer</span><span>Proposal review panel, 2026</span></li>
  <li><span class="service-role">Other</span><span>Chair, Graduate Application Assistance Program (GAAP@UT), 2020-21<br>
    Hallway discussion lead, SOSP'21<br>
    Shadow PC, EuroSys'20</span></li>
</ul>

### Mentoring and Leadership
-----

<ul class="service-plain">
  <li>I have mentored PhD, Masters, and undergraduate students.
    <a href="{{ base_path }}/mentoring/">See who I have worked with</a> and what we built together.</li>
  <li>I have mentored women in CS (WiCS) at UT Austin, and was a mentor for young
    researchers at SOSP and OSDI.</li>
  <li>I founded and chaired the Graduate Application Assistance Program (GAAP) at UT Austin.</li>
</ul>

### Get in Touch!
-----

<p class="page-intro">
  I organize the <a href="https://sky.cs.berkeley.edu/" target="_blank" rel="noopener noreferrer">Sky Systems Seminar</a>
  at Berkeley. If you would like to present your recent systems research, or just want to talk
  about any of the above, please reach out:
  {% comment %}
    Spelled out rather than linked, so a scraper cannot lift it. A mailto:
    would put the address back in the markup and undo the point.
  {% endcomment %}
  soujanya at berkeley dot edu &middot;
  <a href="https://www.linkedin.com/in/soujanya-ponnapalli-553275107/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
</p>

<!-- "I am a postdoctoral scholar at the University of California, Berkeley, working in collaboration with Prof. Natacha Crooks and affiliated with the Sky Computing Lab within the EECS Department. Presently, my focus lies on untrusted storage systems and crash- and byzantine-fault tolerant distributed systems.

Prior to joining Berkeley, I completed my PhD in the CS Department at UT Austin, under the guidance of Prof. Vijay Chidambaram, as a member of the Systems and Storage Lab. My doctoral dissertation centered on minimizing I/O bottlenecks within modern systems' infrastructure to achieve heightened throughput and scalability.

Preceding my graduate studies, I obtained my Bachelor's degree with Honors in Computer Science and Engineering from the International Institute of Information Technology, Hyderabad (IIIT-H), where I collaborated with Prof. Suresh Purini. I was honored with the best all-rounder gold medal for academic excellence and my significant contributions to cultural and extracurricular activities at the institute." -->

<!-- This is the front page of a website that is powered by the [academicpages template](https://github.com/academicpages/academicpages.github.io) and hosted on GitHub pages. [GitHub pages](https://pages.github.com) is a free service in which websites are built and hosted from code and data stored in a GitHub repository, automatically updating when a new commit is made to the respository. This template was forked from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) created by Michael Rose, and then extended to support the kinds of content that academics have: publications, talks, teaching, a portfolio, blog posts, and a dynamically-generated CV. You can fork [this repository](https://github.com/academicpages/academicpages.github.io) right now, modify the configuration and markdown files, add your own PDFs and other content, and have your own site for free, with no ads! An older version of this template powers my own personal website at [stuartgeiger.com](http://stuartgeiger.com), which uses [this Github repository](https://github.com/staeiou/staeiou.github.io).

A data-driven personal website
======
Like many other Jekyll-based GitHub Pages templates, academicpages makes you separate the website's content from its form. The content & metadata of your website are in structured markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.

Many of the features of dynamic content management systems (like Wordpress) can be achieved in this fashion, using a fraction of the computational resources and with far less vulnerability to hacking and DDoSing. You can also modify the theme to your heart's content without touching the content of your site. If you get to a point where you've broken something in Jekyll/HTML/CSS beyond repair, your markdown files describing your talks, publications, etc. are safe. You can rollback the changes or even delete the repository and start over -- just be sure to save the markdown files! Finally, you can also write scripts that process the structured data on the site, such as [this one](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) that analyzes metadata in pages about talks to display [a map of every location you've given a talk](https://academicpages.github.io/talkmap.html).

Getting started
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the academicpages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring academicpages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful. -->
