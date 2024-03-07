---
title: "DINOMO: an elastic, scalable, high-performance key-value store for DPM"
collection: publications
permalink: 'vldb/dinomo'
excerpt: 'This paper presents Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, selective replication, and lock-free and log-free indexing to achieve these goals. Dinomo achieves at least 3.8X better throughput than a state-of-the-art DPM key-value store while providing fast reconfiguration.\\

[Paper](https://dl.acm.org/doi/pdf/10.14778/3565838.3565854)
[Slides](https://wuklab.github.io/words/words22-lee-slides.pdf)
[Talk](https://www.youtube.com/watch?v=Q1-nqbrmu0o&ab_channel=WukLab)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:yoFaNvcx5YUJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQBrxM:AFWwaeYAAAAAZekHtxNW12bx341L-MmdskgZspo&scisig=AFWwaeYAAAAAZekHt9zGwIn9fvV_xoXalY9bNkE&scisf=4&ct=citation&cd=-1&hl=en)
'
date: 2022-09-01
venue: 'Proceedings of the VLDB Endowment (pVLDB)'
# paperurl: 'https://www.usenix.org/system/files/atc21-ponnapalli.pdf'
# citation: 'https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en'
# slides: 'https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf'
# talk: 'https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX'
---

We present Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration. We observe that previously proposed key-value stores for DPM had architectural limitations that prevent them from achieving all three goals simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, selective replication, and lock-free and log-free indexing to achieve these goals. Compared to a state-of-the-art DPM key-value store, Dinomo achieves at least 3.8X better throughput at scale on various workloads and higher scalability, while providing fast reconfiguration.

[Publication](https://dl.acm.org/doi/10.14778/3565838.3565854)
[Paper](https://dl.acm.org/doi/pdf/10.14778/3565838.3565854)
[Slides](https://wuklab.github.io/words/words22-lee-slides.pdf)
[Talk](https://www.youtube.com/watch?v=Q1-nqbrmu0o&ab_channel=WukLab)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:yoFaNvcx5YUJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQBrxM:AFWwaeYAAAAAZekHtxNW12bx341L-MmdskgZspo&scisig=AFWwaeYAAAAAZekHt9zGwIn9fvV_xoXalY9bNkE&scisf=4&ct=citation&cd=-1&hl=en)
