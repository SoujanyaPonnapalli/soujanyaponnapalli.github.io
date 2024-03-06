---
title: "RainBlock: Faster Transaction Processing for Public Blockchains"
collection: publications
permalink: 'atc21/rainblock'
excerpt: 'This paper presents RAINBLOCK, a public blockchain that achieves high transaction throughput. The chief insight behind RAINBLOCK is that the number of transactions in each block is limited by I/O bottlenecks. By removing these I/O bottlenecks, RAINBLOCK allows miners to process more transactions in the same amount of time. The paper makes two novel contributions: the RAINBLOCK architecture that removes I/O from the critical path of processing transactions, and the distributed, multi-versioned DSM-TREE data structure that stores the system state efficiently. A single RAINBLOCK miner processes 27.4 K transactions per second (27× higher than an Ethereum miner). In a geo-distributed settings, RAINBLOCK miners process 20K transactions per second.\\

[Paper](https://www.usenix.org/system/files/atc21-ponnapalli.pdf)
[Slides](https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf)
[Talk](https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en)
'
date: 2021-06-14
venue: 'Annual Technical Conference (ATC)'
# paperurl: 'https://www.usenix.org/system/files/atc21-ponnapalli.pdf'
# citation: 'https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en'
# slides: 'https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf'
# talk: 'https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX'
---

This paper presents RAINBLOCK, a public blockchain that achieves high transaction throughput without modifying the proof-of-work consensus. The chief insight behind RAINBLOCK is that while consensus controls the rate at which new blocks are added to the blockchain, the number of transactions in each block is limited by I/O bottlenecks. By removing these I/O bottlenecks in transaction processing, RAINBLOCK allows miners to process more transactions in the same amount of time. RAINBLOCK makes two novel contributions: the RAINBLOCK architecture that removes I/O from the critical path of processing transactions, and the distributed, multi-versioned DSM-TREE data structure that stores the system state efficiently. A single RAINBLOCK miner processes 27.4 K transactions per second (27× higher than a single Ethereum miner). In a geo-distributed setting with four regions spread across three continents, RAINBLOCK miners process 20K transactions per second.

[Publication](https:/www.usenix.org/conference/atc21/presentation/ponnapalli)
[Paper](https://www.usenix.org/system/files/atc21-ponnapalli.pdf)
[Slides](https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf)
[Talk](https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en)