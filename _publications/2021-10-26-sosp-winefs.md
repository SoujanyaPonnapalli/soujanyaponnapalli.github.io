---
title: "WineFS: a hugepage-aware file system for persistent memory that ages gracefully"
authors: "Rohan Kadekodi,  Saurabh Kadekodi,  Soujanya Ponnapalli,  Harshad Shirwadkar,  Gregory Ganger,  Aasheesh Kolli,  Vijay Chidambaram"
collection: publications
permalink: 'sosp21/winefs'
excerpt: 'Modern persistent-memory (PM) file systems degrade in performance with usage due to their inability to use hugepages. This paper introduces WineFS, a novel hugepage-aware PM file system that eliminates this effect. WineFS combines a new alignment-aware allocator with fragmentation-avoiding approaches to consistency and concurrency to preserve hugepages. Experiments show that WineFS...'
date: 2021-10-26
venue: 'ACM SIGOPS 28th Symposium on Operating Systems Principles'
paperurl: 'https://dl.acm.org/doi/pdf/10.1145/3477132.3483567'
slidesurl: 'https://www.cs.utexas.edu/~vijay/papers/winefs-sosp21-slides.pdf'
talkurl: 'https://www.youtube.com/watch?v=16Ami3IsYI8&ab_channel=ACMSIGOPS'
citationurl: 'https://www.cs.utexas.edu/~vijay/bibtex/winefs-sosp21.bib'
---

**Abstract**

Modern persistent-memory (PM) file systems degrade in performance with usage due to their inability to use hugepages. This paper introduces WineFS, a novel hugepage-aware PM file system that largely eliminates this effect. WineFS combines a new alignment-aware allocator with fragmentation-avoiding approaches to consistency and concurrency to preserve the ability to use hugepages. Experiments show that WineFS resists the effects of aging and outperforms state-of-the-art PM file systems in both aged and un-aged settings.
