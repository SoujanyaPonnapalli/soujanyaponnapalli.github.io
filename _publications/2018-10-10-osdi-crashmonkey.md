---
title: 'Finding Crash-Consistency Bugs with Bounded Black-Box Crash Testing'
authors: 'Jayashree Mohan, Ashlie Martinez, Soujanya Ponnapalli, Pandian Raju, and Vijay Chidambaram'
collection: publications
permalink: 'osdi18/crashmonkey'
date: 2018-10-10
venue: 'USENIX OSDI 2018'
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: ''
paperurl: 'https://www.usenix.org/conference/osdi18/presentation/mohan'
slidesurl: 'https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf'
talkurl: ''
citationurl: '/files/bib/crashmonkey-osdi18.bib'
excerpt: 'This paper presents the bounded black-box crash testing (B3), a new approach to test file-system crash consistency. B3 tests the file system in a black-box manner using workloads with file-system operations. Since the space of possible workloads is infinite, B3 bounds this space based on the insights from studying recent crash-consistency bugs reported in Linux file systems. We build CrashMonkey and Ace, to demonstrate the effectiveness of B3 approach. These tools find 24 out of the 26 recent crash-consistency bugs...'
---

We present a new approach to testing file-system crash consistency: bounded black-box crash testing (B3). B3 tests the file system in a black-box manner using workloads of file-system operations. Since the space of possible workloads is infinite, B3 bounds this space based on parameters such as the number of file-system operations or which operations to include, and exhaustively generates workloads within this bounded space. Each workload is tested on the target file system by simulating power-loss crashes while the workload is being executed, and checking if the file system recovers to a correct state after each crash. B3 builds upon insights derived from our study of crash-consistency bugs reported in Linux file systems in the last five years. We observed that most reported bugs can be reproduced using small workloads of three or fewer file-system operations on a newly-created file system, and that all reported bugs result from crashes after fsync () related system calls. We build two tools, CrashMonkey and Ace, to demonstrate the effectiveness of this approach. Our tools are able to find 24 out of the 26 crash-consistency bugs reported in the last five years. Our tools also revealed 10 new crash-consistency bugs in widely-used, mature Linux file systems, seven of which existed in the kernel since 2014. The new bugs result in severe consequences like broken rename atomicity and loss of persisted files.

[Publication](https://www.usenix.org/conference/osdi18/presentation/mohan)
[Paper](https://www.usenix.org/system/files/osdi18-mohan.pdf)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf)
[Talk](https://www.usenix.org/conference/osdi18/presentation/mohan)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:EgMj9Ky_CP4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX9HCo:AFWwaeYAAAAAZej7BCopPgegrDeBMBeKibc3tRk&scisig=AFWwaeYAAAAAZej7BADVtcQvouJ14tUjpA6LgKg&scisf=4&ct=citation&cd=-1&hl=en)
