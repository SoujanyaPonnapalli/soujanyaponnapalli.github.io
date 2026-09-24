---
title: 'DINOMO: An Elastic, Scalable, High-Performance Key-Value Store for Disaggregated Persistent Memory'
authors: 'Sekwon Lee, Soujanya Ponnapalli, Sharad Singhal, Marcos K. Aguilera, Kimberly Keeton, and Vijay Chidambaram'
collection: publications
permalink: 'vldb/dinomo'
date: 2022-09-01
venue: 'VLDB 2022'
order: 9
conf: 'VLDB'
confyear: 2022
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: ''
paperurl: 'https://doi.org/10.14778/3565838.3565854'
slidesurl: 'https://wuklab.github.io/words/words22-lee-slides.pdf'
talkurl: 'https://www.youtube.com/watch?v=Q1-nqbrmu0o&ab_channel=WukLab'
citationurl: '/files/bib/dinomo-vldb22.bib'
excerpt: 'This paper presents Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, and selective replication...'
---

**Abstract**

This paper presents Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, selective replication, and lock-free and log-free indexing to achieve these goals. Dinomo achieves at least 3.8X better throughput than a state-of-the-art DPM key-value store while providing fast reconfiguration.
