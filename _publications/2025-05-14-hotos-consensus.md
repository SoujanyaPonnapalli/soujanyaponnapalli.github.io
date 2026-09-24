---
title: 'Real Life Is Uncertain. Consensus Should Be Too!'
authors: 'Reginald Frank, Octavio Lomeli, Neil Giridharan, Soujanya Ponnapalli, Marcos K. Aguilera, and Natacha Crooks'
collection: publications
permalink: 'powder'
date: 2025-05-14
venue: 'HotOS 2025'
order: 7
conf: 'HotOS'
confyear: 2025
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: ''
paperurl: 'https://doi.org/10.1145/3713082.3730374'
slidesurl: ''
talkurl: ''
citationurl: '/files/bib/consensus-hotos25.bib'
excerpt: 'Modern distributed systems rely on consensus protocols to build a fault-tolerant core upon which they can build applications. Consensus protocols are correct under a specific failure model, where up to $f$ machines can fail. We argue that this $f$-threshold failure model oversimplifies the real world and limits potential opportunities to optimize for cost or performance. We argue instead for a probabilistic failure...'
---

**Abstract**

Modern distributed systems rely on consensus protocols to build a fault-tolerant-core upon which they can build applications. Consensus protocols are correct under a specific failure model, where up to $f$ machines can fail. We argue that this $f$-threshold failure model oversimplifies the real world and limits potential opportunities to optimize for cost or performance. We argue instead for a probabilistic failure model that captures the complex and nuanced nature of faults observed in practice. Probabilistic consensus protocols can explicitly leverage individual machine failure curves and explore side-stepping traditional bottlenecks such as majority quorum intersection, enabling systems that are more reliable, efficient, cost-effective, and sustainable.

[Read the paper (PDF)](https://sigops.org/s/conferences/hotos/2025/papers/hotos25-69.pdf)
