---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

## Minimizing I/O Bottlnecks to Achieve Scalable and High-Throughput Systems
PhD Dissertation, University of Texas at Austin, 2023 <br>
**Soujanya Ponnapalli**, Vijay Chidambaram <br>
[Paper](https://people.eecs.berkeley.edu/~soujanya/dissertation.pdf)
[Slides](https://wuklab.github.io/words/words22-lee-slides.pdf)
<br>
> *This dissertation studies the performance limitations of three distinct systems: monolithic key-value stores, distributed transactional stores, and public blockchains. First, it attributes their low throughput and poor scalability to I/O-bottlenecks that are inherent to the systems’ design and architecture. Next, it addresses the question: How do we architect systems to minimize I/O-bottlenecks and simultaneously achieve high throughput and scalability? It proposes a fundamental redesign of systems by carefully crafting the roles and responsibilities of each system component to improve the utilization of underlying resources.*


## DINOMO: an elastic, scalable, high-performance kv-store for Disaggregated PM 
Proceedings of the VLDB Endowment (pVLDB), 2022 <br>
Sekwon Lee, **Soujanya Ponnapalli**, Sharad Singhal, Marcos Aguilera, Kimberly Keeton, Vijay Chidambaram <br>
[Paper](https://dl.acm.org/doi/pdf/10.14778/3565838.3565854)
[Slides](https://wuklab.github.io/words/words22-lee-slides.pdf)
[Talk](https://www.youtube.com/watch?v=Q1-nqbrmu0o&ab_channel=WukLab)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:yoFaNvcx5YUJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQBrxM:AFWwaeYAAAAAZekHtxNW12bx341L-MmdskgZspo&scisig=AFWwaeYAAAAAZekHt9zGwIn9fvV_xoXalY9bNkE&scisf=4&ct=citation&cd=-1&hl=en) <br>
> *We present Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration. We observe that previously proposed key-value stores for DPM had architectural limitations that prevent them from achieving all three goals simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, selective replication, and lock-free and log-free indexing to achieve these goals. Compared to a state-of-the-art DPM key-value store, Dinomo achieves at least 3.8X better throughput at scale on various workloads and higher scalability, while providing fast reconfiguration.*


## WineFS: a hugepage-aware file system for persistent memory that ages gracefully 
ACM SIGOPS 28th Symposium on Operating Systems Principles, 2021 <br>
Rohan Kadekodi, Saurabh Kadekodi, **Soujanya Ponnapalli**, Harshad Shirwadkar, Gregory Ganger, Aasheesh Kolli, Vijay Chidambaram <br>
[Paper](https://dl.acm.org/doi/pdf/10.1145/3477132.3483567)
[Slides](https://www.cs.utexas.edu/~vijay/papers/winefs-sosp21-slides.pdf)
[Talk](https://www.youtube.com/watch?v=16Ami3IsYI8&ab_channel=ACMSIGOPS)
[Citation](https://www.cs.utexas.edu/~vijay/bibtex/winefs-sosp21.bib) <br>
> *Modern persistent-memory (PM) file systems perform well in benchmark settings, when the file system is freshly created and empty. But after being aged by usage, as will be the normal mode in practice, their memory-mapped performance degrades significantly. This paper shows that the cause is their inability to use 2MB hugepages to map files when aged, having to use 4KB pages instead and suffering many extra page faults and TLB misses as a result.*
> *We introduce WineFS, a novel hugepage-aware PM file system that largely eliminates this effect. WineFS combines a new alignment-aware allocator with fragmentation-avoiding approaches to consistency and concurrency to preserve the ability to use hugepages. Experiments show that WineFS resists the effects of aging and outperforms state-of-the-art PM file systems in both aged and un-aged settings. For example, in an aged setup, the LMDB memory-mapped database obtains 2x higher write throughput on WineFS compared to NOVA, and 70% higher throughput compared to ext4-DAX. When reading a memory-mapped persistent radix tree, WineFS results in 56% lower median latency than NOVA.*



## RainBlock: Faster Transaction Processing for Public Blockchains 
USENIX Annual Technical Conference (ATC), 2021<br>
**Soujanya Ponnapalli**,  Aashaka Shah,  Souvik Banerjee,  Amy Tai,  Malkhi Dahlia,  Vijay Chidambaram,  Michael Wei <br>
[Paper](https://www.usenix.org/system/files/atc21-ponnapalli.pdf)
[Slides](https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf)
[Talk](https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en)
<br>
> *We present RAINBLOCK, a public blockchain that achieves high transaction throughput. The chief insight behind RAINBLOCK is that the number of transactions in each block is limited by I/O bottlenecks. By removing these I/O bottlenecks, RAINBLOCK allows miners to process more transactions in the same amount of time. The paper makes two novel contributions: the RAINBLOCK architecture that removes I/O from the critical path of processing transactions, and the distributed, multi-versioned DSM-TREE data structure that stores the system state efficiently. A single RAINBLOCK miner processes 27.4 K transactions per second (27× higher than an Ethereum miner). In a geo-distributed settings, RAINBLOCK miners process 20K transactions per second.*

## Software-defined data protection: Low overhead policy compliance is within reach 
Proceedings of the VLDB Endowment (pVLDB), 2021 <br>
Zsolt Istvan,  **Soujanya Ponnapalli**,  Vijay Chidambaram <br>
[Paper](https://dl.acm.org/doi/pdf/10.14778/3450980.3450986)
[Slides](https://www.youtube.com/watch?v=beM1qWI7tho&ab_channel=VLDB2021))
[Talk](https://www.youtube.com/watch?v=beM1qWI7tho&ab_channel=VLDB2021)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:lbGn4Hm5ml4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQVdM0:AFWwaeYAAAAAZekTbM27vjR36aCY7495-eseBnM&scisig=AFWwaeYAAAAAZekTbM6Bbho1Vqw_ns0yEUMuCUE&scisf=4&ct=citation&cd=-1&hl=en)
> *This paper presents our novel approach "Software-Defined Data Protection" (SDP). Its simple, yet powerful premise is to decouple often changing policies from request-level enforcement to allow distributed smart storage nodes to implement the latter at line-rate. Existing and future data protection frameworks can be translated to the same hardware interface which allows storage nodes to offload enforcement efficiently both for company-specific rules and regulations, such as GDPR or CCPA*

## Crashmonkey and ACE: Systematically testing file-system crash consistency
ACM Journal on Transactions on Storage (TOCS)), 2019 <br>
Jayashree Mohan,  Ashlie Martinez,  **Soujanya Ponnapalli**,  Pandian Raju,  Vijay Chidambaram <br>
[Paper](https://dl.acm.org/doi/pdf/10.1145/3320275)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf)
[Talk](https://www.youtube.com/watch?v=BmhKbGoCyqo&ab_channel=Heisenbug)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:h5hldFGUgD4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQCZvs:AFWwaeYAAAAAZekEfvvK92PdaHO3UzJbotUQH_g&scisig=AFWwaeYAAAAAZekEfmbwwnDrihWbkv2b28_cstA&scisf=4&ct=citation&cd=-1&hl=en)
<br>
> *We present CrashMonkey and Ace, a set of tools to systematically find crash-consistency bugs in Linux file systems. CrashMonkey is a record-and-replay framework which tests a given workload on the target file system by simulating power-loss crashes while the workload is being executed, and checking if the file system recovers to a correct state after each crash. Ace automatically generates all the workloads to be run on the target file system. We build CrashMonkey and Ace based on a new approach to test file-system crash consistency: bounded black-box crash testing (B3). B3 tests the file system in a black-box manner using workloads of file-system operations. Since the space of possible workloads is infinite, B3 bounds this space based on parameters such as the number of file-system operations or which operations to include, and exhaustively generates workloads within this bounded space. B3 builds upon insights derived from our study of crash-consistency bugs reported in Linux file systems in the last 5 years. We observed that most reported bugs can be reproduced using small workloads of three or fewer file-system operations on a newly created file system, and that all reported bugs result from crashes after fsync()-related system calls. CrashMonkey and Ace are able to find 24 out of the 26 crash-consistency bugs reported in the last 5 years. Our tools also revealed 10 new crash-consistency bugs in widely used, mature Linux file systems, 7 of which existed in the kernel since 2014. Additionally, our tools found a crash-consistency bug in a verified file system, FSCQ. The new bugs result in severe consequences like broken rename atomicity, loss of persisted files and directories, and data loss.*


## Finding Crash-Consistency Bugs with Bounded Black-Box Crash Testing 
13th USENIX Symposium on Operating Systems Design and Implementation (OSDI), 2018 <br>
Jayashree Mohan,  Ashlie Martinez,  **Soujanya Ponnapalli**,  Pandian Raju,  Vijay Chidambaram <br>
[Paper](https://www.usenix.org/system/files/osdi18-mohan.pdf)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf)
[Talk](https://www.usenix.org/conference/osdi18/presentation/mohan)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:EgMj9Ky_CP4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX9HCo:AFWwaeYAAAAAZej7BCopPgegrDeBMBeKibc3tRk&scisig=AFWwaeYAAAAAZej7BADVtcQvouJ14tUjpA6LgKg&scisf=4&ct=citation&cd=-1&hl=en)
<br>
> *We present a new approach to testing file-system crash consistency: bounded black-box crash testing (B3). B3 tests the file system in a black-box manner using workloads of file-system operations. Since the space of possible workloads is infinite, B3 bounds this space based on parameters such as the number of file-system operations or which operations to include, and exhaustively generates workloads within this bounded space. Each workload is tested on the target file system by simulating power-loss crashes while the workload is being executed, and checking if the file system recovers to a correct state after each crash. B3 builds upon insights derived from our study of crash-consistency bugs reported in Linux file systems in the last five years. We observed that most reported bugs can be reproduced using small workloads of three or fewer file-system operations on a newly-created file system, and that all reported bugs result from crashes after fsync () related system calls. We build two tools, CrashMonkey and Ace, to demonstrate the effectiveness of this approach. Our tools are able to find 24 out of the 26 crash-consistency bugs reported in the last five years. Our tools also revealed 10 new crash-consistency bugs in widely-used, mature Linux file systems, seven of which existed in the kernel since 2014. The new bugs result in severe consequences like broken rename atomicity and loss of persisted files.*


## mLSM: Making Authenticated Storage Faster in Ethereum 
USENIX Workshop on Hot Topics in Storage and File Systems, 2018 <br>
Pandian Raju, **Soujanya Ponnapalli**, Evan Kaminsky, Gilad Oved, Zachary Keener, Vijay Chidambaram, Ittai Abraham <br>
[Paper](https://www.usenix.org/system/files/conference/hotstorage18/hotstorage18-paper-raju.pdf)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/hotstorage18_slides_ponnapalli.pdf)
[Talk](https://www.usenix.org/conference/hotstorage18/presentation/raju)
[Citation](https://www.usenix.org/biblio/export/bibtex/216872) <br>
> *Ethereum provides authenticated storage: each read
returns a value and a proof that allows the client to verify
the value returned is correct. We experimentally show
that such authentication leads to high read and write amplification (64× in the worst case). We present a novel
data structure, Merkelized LSM (mLSM), that significantly reduces the read and write amplification while still
allowing client verification of reads. mLSM significantly
increases the performance of the storage subsystem in
Ethereum, thereby increasing the performance of a wide
range of Ethereum applications.*


<!-- | Abstract   | Solution Preview |
| ------------- | ------------- |
| <center><a href="https://www.usenix.org/system/files/conference/hotstorage18/hotstorage18-paper-raju.pdf" target="_blank"><img src="../images/abstract_mlsm.png" style="width: 30vw"></a></center> | <center><a href="https://www.usenix.org/sites/default/files/conference/protected-files/hotstorage18_slides_ponnapalli.pdf" target="_blank"><img src="../images/paper_mlsm.png" style="width: 30vw"></a></center> | -->


<!-- ## mLSM: Making Authenticated Storage Faster in Ethereum 
USENIX Workshop on Hot Topics in Storage and File Systems, 2018 <br>
Pandian Raju, **Soujanya Ponnapalli**, Evan Kaminsky, Gilad Oved, Zachary Keener, Vijay Chidambaram, Ittai Abraham

| Abstract   | Solution Preview |
| ------------- | ------------- |
| <center><a href="https://www.usenix.org/system/files/conference/hotstorage18/hotstorage18-paper-raju.pdf" target="_blank"><img src="../images/abstract_mlsm.png" style="width: 30vw"></a></center> | <center><a href="https://www.usenix.org/sites/default/files/conference/protected-files/hotstorage18_slides_ponnapalli.pdf" target="_blank"><img src="../images/paper_mlsm.png" style="width: 30vw"></a></center> | -->

<!-- {% if author.googlescholar %}
 You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
 {% include archive-single.html %}
{% endfor %} -->
