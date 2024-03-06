---
title: "RainBlock: Faster Transaction Processing for Public Blockchains"
collection: publications
permalink: /publication/2021-atc-rainblock
excerpt: 'This paper presents RAINBLOCK, a public blockchain that achieves high transaction throughput without modifying the proof-of-work consensus. The chief insight behind RAINBLOCK is that while consensus controls the rate at which new blocks are added to the blockchain, the number of transactions in each block is limited by I/O bottlenecks. By removing the I/O bottlenecks in transaction processing, RAINBLOCK allows miners to process more transactions in the same amount of time. RAINBLOCK makes two novel contributions: the RAINBLOCK architecture that removes I/O from the critical path of processing transactions (txs), and the distributed, multi-versioned DSM-TREE data structure that stores the system state efficiently. A single RAINBLOCK miner processes 27.4 K txs per second (27× higher than a single Ethereum miner) and in a geo-distributed setting with four regions spread across three continents, RAINBLOCK miners process 20K txs per second.'
date: 2009-10-01
venue: 'Annual Technical Conference (ATC) 2021'
paperurl: 'https://www.usenix.org/conference/atc21/presentation/ponnapalli'
citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---


This paper presents RAINBLOCK, a public blockchain that achieves high transaction throughput without modifying the proof-of-work consensus. The chief insight behind RAINBLOCK is that while consensus controls the rate at which new blocks are added to the blockchain, the number of transactions in each block is limited by I/O bottlenecks. By removing the I/O bottlenecks in transaction processing, RAINBLOCK allows miners to process more transactions in the same amount of time. RAINBLOCK makes two novel contributions: the RAINBLOCK architecture that removes I/O from the critical path of processing transactions (txs), and the distributed, multi-versioned DSM-TREE data structure that stores the system state efficiently. A single RAINBLOCK miner processes 27.4 K txs per second (27× higher than a single Ethereum miner) and in a geo-distributed setting with four regions spread across three continents, RAINBLOCK miners process 20K txs per second.

[Download paper here](https://www.usenix.org/system/files/atc21-ponnapalli.pdf)
[Download slides here](https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf)
[Link to the talk here](https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX)

[Cite](https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en)