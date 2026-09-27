---
title: 'SKYE: Write-Optimized Key-Value Store with Fine-Grained Control over Persistent Memory Accesses'
authors: 'Soujanya Ponnapalli, Sekwon Lee, Rohan Kadekodi, and Vijay Chidambaram'
collection: publications
permalink: 'arxiv26/skye'
date: 2026-04-01
venue: 'arXiv 2026'
order: 18
conf: 'arXiv'
confyear: 2026
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: 'Key-value stores on persistent memory let applications write to the device directly, which keeps latency low but gives up control: throughput collapses once too many threads write concurrently, and the best existing store reaches under half of a single NVDIMM''s write bandwidth. With SKYE, we make access indirect instead, so dedicated threads write on the application''s behalf and the store decides how data is placed across NVDIMMs and NUMA nodes, reaching about 86% of PM write bandwidth.'
paperurl: 'https://arxiv.org/abs/2609.20972'
pdfurl: 'https://arxiv.org/pdf/2609.20972'
slidesurl: ''
talkurl: ''
citationurl: '/files/bib/skye-arxiv26.bib'
---
