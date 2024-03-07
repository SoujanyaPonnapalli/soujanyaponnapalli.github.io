---
title: "Crashmonkey and ACE: Systematically testing file-system crash consistency"
authors: "Jayashree Mohan,  Ashlie Martinez,  Soujanya Ponnapalli,  Pandian Raju,  Vijay Chidambaram"
collection: publications
permalink: 'tocs/crashmonkey'
excerpt: 'This paper presents CrashMonkey and Ace, a set of tools to systematically find crash-consistency bugs in Linux file systems. CrashMonkey is a record-and-replay framework that simulates power-loss crashes while executing a given workload, and checks if the file system recovers to a consistent state after each crash. Ace automatically generates workloads to be run on the target file system. CrashMonkey and Ace are based on a new approach to test file-system crash consistency: bounded black-box crash testing (B3) which alleviates the consequences of having an infinite set of possible workloads to test. CrashMonkey and Ace are able to find 24 out of the 26 crash-consistency bugs reported in the last 5 years. These tools also revealed 10 new crash-consistency bugs in widely used, mature Linux file systems, 7 of which existed in the kernel since 2014. They also found a crash-consistency bug in a verified file system, FSCQ.\\

[Paper](https://dl.acm.org/doi/pdf/10.1145/3320275)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf)
[Talk](https://www.youtube.com/watch?v=BmhKbGoCyqo&ab_channel=Heisenbug)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:h5hldFGUgD4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQCZvs:AFWwaeYAAAAAZekEfvvK92PdaHO3UzJbotUQH_g&scisig=AFWwaeYAAAAAZekEfmbwwnDrihWbkv2b28_cstA&scisf=4&ct=citation&cd=-1&hl=en)
'
date: 2019-04-20
venue: 'ACM Transactions on Storage (TOCS)'
# paperurl: 'https://www.usenix.org/system/files/atc21-ponnapalli.pdf'
# citation: 'https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en'
# slides: 'https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf'
# talk: 'https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX'
---

We present CrashMonkey and Ace, a set of tools to systematically find crash-consistency bugs in Linux file systems. CrashMonkey is a record-and-replay framework which tests a given workload on the target file system by simulating power-loss crashes while the workload is being executed, and checking if the file system recovers to a correct state after each crash. Ace automatically generates all the workloads to be run on the target file system. We build CrashMonkey and Ace based on a new approach to test file-system crash consistency: bounded black-box crash testing (B3). 
B3 tests the file system in a black-box manner using workloads of file-system operations. Since the space of possible workloads is infinite, 
B3 bounds this space based on parameters such as the number of file-system operations or which operations to include, and exhaustively generates workloads within this bounded space. 
B3 builds upon insights derived from our study of crash-consistency bugs reported in Linux file systems in the last 5 years. We observed that most reported bugs can be reproduced using small workloads of three or fewer file-system operations on a newly created file system, and that all reported bugs result from crashes after fsync()-related system calls. CrashMonkey and Ace are able to find 24 out of the 26 crash-consistency bugs reported in the last 5 years. Our tools also revealed 10 new crash-consistency bugs in widely used, mature Linux file systems, 7 of which existed in the kernel since 2014. Additionally, our tools found a crash-consistency bug in a verified file system, FSCQ. The new bugs result in severe consequences like broken rename atomicity, loss of persisted files and directories, and data loss.


[Publication](https://dl.acm.org/doi/fullHtml/10.1145/3320275)
[Paper](https://dl.acm.org/doi/pdf/10.1145/3320275)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/osdi18_slides_mohan.pdf)
[Talk](https://www.youtube.com/watch?v=BmhKbGoCyqo&ab_channel=Heisenbug)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:h5hldFGUgD4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQCZvs:AFWwaeYAAAAAZekEfvvK92PdaHO3UzJbotUQH_g&scisig=AFWwaeYAAAAAZekEfmbwwnDrihWbkv2b28_cstA&scisf=4&ct=citation&cd=-1&hl=en)