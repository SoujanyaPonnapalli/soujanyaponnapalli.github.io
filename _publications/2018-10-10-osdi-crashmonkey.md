---
title: "Finding Crash-Consistency Bugs with Bounded Black-Box Crash Testing"
collection: publications
permalink: 'osdi18/crashmonkey'
excerpt: 'This paper presents a new approach to testing file-system crash consistency: bounded black-box crash testing (B3). B3 tests the file system in a black-box manner using workloads with file-system operations. Since the space of possible workloads is infinite, B3 bounds this space based on the insights from studying recent crash-consistency bugs reported in Linux file systems. Most reported bugs can be reproduced using small workloads of three or fewer file-system operations, and all reported bugs result from crashes after fsync () related system calls. We build two tools, CrashMonkey and Ace, to demonstrate the effectiveness of this approach. Our tools find 24 out of the 26 recent crash-consistency bugs and reveal 10 new crash-consistency bugs that result in severe consequences like broken rename atomicity and loss of persisted files.\\

[Paper](https://www.usenix.org/system/files/osdi18-mohan.pdf)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf)
[Talk](https://www.usenix.org/conference/osdi18/presentation/mohan)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:EgMj9Ky_CP4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX9HCo:AFWwaeYAAAAAZej7BCopPgegrDeBMBeKibc3tRk&scisig=AFWwaeYAAAAAZej7BADVtcQvouJ14tUjpA6LgKg&scisf=4&ct=citation&cd=-1&hl=en)
'
date: 2018-10-10
venue: '13th USENIX Symposium on Operating Systems Design and Implementation (OSDI)'
# paperurl: 'https://www.usenix.org/system/files/atc21-ponnapalli.pdf'
# citation: 'https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en'
# slides: 'https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf'
# talk: 'https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX'
---

We present a new approach to testing file-system crash consistency: bounded black-box crash testing (B3). B3 tests the file system in a black-box manner using workloads of file-system operations. Since the space of possible workloads is infinite, B3 bounds this space based on parameters such as the number of file-system operations or which operations to include, and exhaustively generates workloads within this bounded space. Each workload is tested on the target file system by simulating power-loss crashes while the workload is being executed, and checking if the file system recovers to a correct state after each crash. B3 builds upon insights derived from our study of crash-consistency bugs reported in Linux file systems in the last five years. We observed that most reported bugs can be reproduced using small workloads of three or fewer file-system operations on a newly-created file system, and that all reported bugs result from crashes after fsync () related system calls. We build two tools, CrashMonkey and Ace, to demonstrate the effectiveness of this approach. Our tools are able to find 24 out of the 26 crash-consistency bugs reported in the last five years. Our tools also revealed 10 new crash-consistency bugs in widely-used, mature Linux file systems, seven of which existed in the kernel since 2014. The new bugs result in severe consequences like broken rename atomicity and loss of persisted files.

[Publication](https://www.usenix.org/conference/osdi18/presentation/mohan)
[Paper](https://www.usenix.org/system/files/osdi18-mohan.pdf)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf)
[Talk](https://www.usenix.org/conference/osdi18/presentation/mohan)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:EgMj9Ky_CP4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX9HCo:AFWwaeYAAAAAZej7BCopPgegrDeBMBeKibc3tRk&scisig=AFWwaeYAAAAAZej7BADVtcQvouJ14tUjpA6LgKg&scisf=4&ct=citation&cd=-1&hl=en)
