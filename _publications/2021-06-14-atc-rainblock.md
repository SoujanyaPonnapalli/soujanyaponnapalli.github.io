---
title: 'RainBlock: Faster Transaction Processing in Public Blockchains'
authors: 'Soujanya Ponnapalli, Aashaka Shah, Souvik Banerjee, Dahlia Malkhi, Amy Tai, Vijay Chidambaram, and Michael Wei'
collection: publications
permalink: 'atc21/rainblock'
date: 2021-06-14
venue: 'USENIX ATC 2021'
order: 10
conf: 'ATC'
confyear: 2021
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: ''
paperurl: 'https://www.usenix.org/conference/atc21/presentation/ponnapalli'
slidesurl: 'https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf'
talkurl: 'https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX'
citationurl: '/files/bib/rainblock-atc21.bib'
excerpt: 'This paper presents RAINBLOCK, a public blockchain that achieves high transaction throughput. The number of transactions in each block is limited by I/O bottlenecks. By removing these I/O bottlenecks, RAINBLOCK allows miners to process more transactions in the same amount of time. The RAINBLOCK architecture removes I/O from the critical path, and the distributed, sharded Merkle tree, the DSM-TREE data structure...'
---

**Abstract**

This paper presents RAINBLOCK, a public blockchain that achieves high transaction throughput. The chief insight behind RAINBLOCK is that the number of transactions in each block is limited by I/O bottlenecks. By removing these I/O bottlenecks, RAINBLOCK allows miners to process more transactions in the same amount of time. The paper makes two novel contributions: the RAINBLOCK architecture that removes I/O from the critical path of processing transactions, and the distributed, multi-versioned DSM-TREE data structure that stores the system state efficiently. A single RAINBLOCK miner processes 27.4 K transactions per second (27× higher than an Ethereum miner). In a geo-distributed settings, RAINBLOCK miners process 20K transactions per second.
