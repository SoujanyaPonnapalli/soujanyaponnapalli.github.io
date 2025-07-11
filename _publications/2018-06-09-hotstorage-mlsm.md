---
title: "mLSM: Making Authenticated Storage Faster in Ethereum"
authors: "Pandian Raju, Soujanya Ponnapalli, Evan Kaminsky, Gilad Oved, Zachary Keener, Vijay Chidambaram, Ittai Abraham"
collection: publications
permalink: 'hotstorage18/mlsm'
excerpt: 'This paper presents a novel data-authenticating structure, Merkelized LSM (mLSM). In authenticated storage each read returns a value and a proof that allows the client to verify the value returned is correct. Such authentication leads to high read and write amplification (64x in the worst case). mLSM ...'
date: 2018-06-09
venue: 'USENIX Workshop on Hot Topics in Storage and File Systems (HotStorage)'
paperurl: 'https://www.usenix.org/system/files/conference/hotstorage18/hotstorage18-paper-raju.pdf'
slidesurl: 'https://www.usenix.org/sites/default/files/conference/protected-files/hotstorage18_slides_ponnapalli.pdf'
talkurl: 'https://www.usenix.org/conference/hotstorage18/presentation/raju'
citationurl: 'https://scholar.googleusercontent.com/scholar.bib?q=info:imkOnqoy8c8J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX5VNo:AFWwaeYAAAAAZej_TNr8EVdJRBZbqiJQKf0sJOc&scisig=AFWwaeYAAAAAZej_TLSE2o3WdncyXYh0r6aqwoE&scisf=4&ct=citation&cd=-1&hl=en'
---

Ethereum provides authenticated storage: each read returns a value and a proof that allows the client to verify the value returned is correct. We experimentally show that such authentication leads to high read and write amplification (64x in the worst case). We present a novel data structure, Merkelized LSM (mLSM), that significantly reduces the read and write amplification while still allowing client verification of reads. mLSM significantly increases the performance of the storage subsystem in Ethereum, thereby increasing the performance of a wide range of Ethereum applications.


[Publication](https://www.usenix.org/conference/hotstorage18/presentation/raju)
[Paper](https://www.usenix.org/system/files/conference/hotstorage18/hotstorage18-paper-raju.pdf)
[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/hotstorage18_slides_ponnapalli.pdf)
[Talk](https://www.usenix.org/conference/hotstorage18/presentation/raju)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:imkOnqoy8c8J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX5VNo:AFWwaeYAAAAAZej_TNr8EVdJRBZbqiJQKf0sJOc&scisig=AFWwaeYAAAAAZej_TLSE2o3WdncyXYh0r6aqwoE&scisf=4&ct=citation&cd=-1&hl=en)
