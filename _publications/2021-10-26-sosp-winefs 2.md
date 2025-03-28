---
title: "WineFS: a hugepage-aware file system for persistent memory that ages gracefully"
authors: "Rohan Kadekodi,  Saurabh Kadekodi,  Soujanya Ponnapalli,  Harshad Shirwadkar,  Gregory Ganger,  Aasheesh Kolli,  Vijay Chidambaram"
collection: publications
permalink: 'sosp21/winefs'
excerpt: 'Modern persistent-memory (PM) file systems degrade in performance with usage due to their inability to use hugepages. This paper introduces WineFS, a novel hugepage-aware PM file system that largely eliminates this effect.
WineFS combines a new alignment-aware allocator with fragmentation-avoiding approaches to consistency and concurrency to preserve the ability to use hugepages.
Experiments show that WineFS resists the effects of aging and outperforms state-of-the-art PM file systems in both aged and un-aged settings.\\

[Paper](https://dl.acm.org/doi/pdf/10.1145/3477132.3483567)
[Slides](https://www.cs.utexas.edu/~vijay/papers/winefs-sosp21-slides.pdf)
[Talk](https://www.youtube.com/watch?v=16Ami3IsYI8&ab_channel=ACMSIGOPS)
[Citation](https://www.cs.utexas.edu/~vijay/bibtex/winefs-sosp21.bib)
'
date: 2021-10-26
venue: '13th USENIX Symposium on Operating Systems Design and Implementation (OSDI)'
# paperurl: 'https://www.usenix.org/system/files/atc21-ponnapalli.pdf'
# citation: 'https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en'
# slides: 'https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf'
# talk: 'https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX'
---

Modern persistent-memory (PM) file systems perform well in benchmark settings, when the file system is freshly created and empty.
But after being aged by usage, as will be the normal mode in practice, their memory-mapped performance degrades significantly.
This paper shows that the cause is their inability to use 2MB hugepages to map files when aged,
having to use 4KB pages instead and suffering many extra page faults and TLB misses as a result.

We introduce WineFS, a novel hugepage-aware PM file system that largely eliminates this effect.
WineFS combines a new alignment-aware allocator with fragmentation-avoiding approaches to consistency and concurrency to preserve the ability to use hugepages. 
Experiments show that WineFS resists the effects of aging and outperforms state-of-the-art PM file systems in both aged and un-aged settings.
For example, in an aged setup, the LMDB memory-mapped database obtains 2× higher write throughput on WineFS compared to NOVA, and 70% higher throughput compared to ext4-DAX.
When reading a memory-mapped persistent radix tree, WineFS results in 56% lower median latency than NOVA.

[Publication](https://dl.acm.org/doi/10.1145/3477132.3483567)
[Paper](https://dl.acm.org/doi/pdf/10.1145/3477132.3483567)
[Slides](https://www.cs.utexas.edu/~vijay/papers/winefs-sosp21-slides.pdf)
[Talk](https://www.youtube.com/watch?v=16Ami3IsYI8&ab_channel=ACMSIGOPS)
[Citation](https://www.cs.utexas.edu/~vijay/bibtex/winefs-sosp21.bib)
