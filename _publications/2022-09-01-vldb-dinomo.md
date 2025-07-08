---
title: "DINOMO: an elastic, scalable, high-performance key-value store for DPM"
authors: "Sekwon Lee,  Soujanya Ponnapalli,  Sharad Singhal,  Marcos Aguilera,  Kimberly Keeton,  Vijay Chidambaram"
collection: publications
permalink: 'vldb/dinomo'
excerpt: 'This paper presents Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, and selective replication...'
date: 2022-09-01
venue: 'Proceedings of the VLDB Endowment (pVLDB)'
paperurl: 'https://dl.acm.org/doi/pdf/10.14778/3565838.3565854'
slidesurl: 'https://wuklab.github.io/words/words22-lee-slides.pdf'
talkurl: 'https://www.youtube.com/watch?v=Q1-nqbrmu0o&ab_channel=WukLab'
citationurl: 'https://scholar.googleusercontent.com/scholar.bib?q=info:yoFaNvcx5YUJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQBrxM:AFWwaeYAAAAAZekHtxNW12bx341L-MmdskgZspo&scisig=AFWwaeYAAAAAZekHt9zGwIn9fvV_xoXalY9bNkE&scisf=4&ct=citation&cd=-1&hl=en'
---

**Abstract**

This paper presents Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, selective replication, and lock-free and log-free indexing to achieve these goals. Dinomo achieves at least 3.8X better throughput than a state-of-the-art DPM key-value store while providing fast reconfiguration.

