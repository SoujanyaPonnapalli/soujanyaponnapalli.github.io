---
title: 'WineFS: Hugepage-Aware File System for PM that Ages Gracefully'
authors: 'Rohan Kadekodi, Saurabh Kadekodi, Soujanya Ponnapalli, Harshad Shirwadkar, Gregory R. Ganger, Aasheesh Kolli, and Vijay Chidambaram'
collection: publications
permalink: 'sosp21/winefs'
date: 2021-10-26
venue: 'SOSP 2021'
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: ''
paperurl: 'https://dl.acm.org/doi/10.1145/3477132.3483567'
slidesurl: 'https://www.cs.utexas.edu/~vijay/papers/winefs-sosp21-slides.pdf'
talkurl: 'https://www.youtube.com/watch?v=16Ami3IsYI8&ab_channel=ACMSIGOPS'
citationurl: '/files/bib/winefs-sosp21.bib'
excerpt: 'Modern persistent-memory (PM) file systems degrade in performance with usage due to their inability to use hugepages. This paper introduces WineFS, a novel hugepage-aware PM file system that eliminates this effect. WineFS combines a new alignment-aware allocator with fragmentation-avoiding approaches to consistency and concurrency to preserve hugepages. Experiments show that WineFS...'
---

**Abstract**

Modern persistent-memory (PM) file systems degrade in performance with usage due to their inability to use hugepages. This paper introduces WineFS, a novel hugepage-aware PM file system that largely eliminates this effect. WineFS combines a new alignment-aware allocator with fragmentation-avoiding approaches to consistency and concurrency to preserve the ability to use hugepages. Experiments show that WineFS resists the effects of aging and outperforms state-of-the-art PM file systems in both aged and un-aged settings.
