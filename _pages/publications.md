---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---


## DINOMO: an elastic, scalable, high-performance kv-store for Disaggregated PM 
Proceedings of the VLDB Endowment (pVLDB), 2022 <br>
Sekwon Lee, **Soujanya Ponnapalli**, Sharad Singhal, Marcos Aguilera, Kimberly Keeton, Vijay Chidambaram <br>
[Paper](https://dl.acm.org/doi/pdf/10.14778/3565838.3565854)
[Slides](https://wuklab.github.io/words/words22-lee-slides.pdf)
[Talk](https://www.youtube.com/watch?v=Q1-nqbrmu0o&ab_channel=WukLab)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:yoFaNvcx5YUJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQBrxM:AFWwaeYAAAAAZekHtxNW12bx341L-MmdskgZspo&scisig=AFWwaeYAAAAAZekHt9zGwIn9fvV_xoXalY9bNkE&scisf=4&ct=citation&cd=-1&hl=en) <br>
> *We present Dinomo, a novel key-value store for disaggregated persistent memory (DPM). Dinomo is the first key-value store for DPM that simultaneously achieves high common-case performance, scalability, and lightweight online reconfiguration. We observe that previously proposed key-value stores for DPM had architectural limitations that prevent them from achieving all three goals simultaneously. Dinomo uses a novel combination of techniques such as ownership partitioning, disaggregated adaptive caching, selective replication, and lock-free and log-free indexing to achieve these goals. Compared to a state-of-the-art DPM key-value store, Dinomo achieves at least 3.8X better throughput at scale on various workloads and higher scalability, while providing fast reconfiguration.*


<!-- <p>
 <span style="float: left"><a href="https://www.usenix.org/system/files/conference/hotstorage18/hotstorage18-paper-raju.pdf" target="_blank"><img src="../images/abstract_mlsm.png" style="width:30vw;margin-right=0"></a></span>
 <span style="float: right"><a href="https://www.usenix.org/sites/default/files/conference/protected-files/hotstorage18_slides_ponnapalli.pdf" target="_blank"><img src="../images/paper_mlsm.png" style="width:20vw"></a></span>
</p>  -->


## WineFS: a hugepage-aware file system for persistent memory that ages gracefully 
Proceedings of the VLDB Endowment (pVLDB), 2022 <br>
Rohan Kadekodi, Saurabh Kadekodi, **Soujanya Ponnapalli**, Harshad Shirwadkar, Gregory Ganger, Aasheesh Kolli, Vijay Chidambaram <br>
[Paper](https://dl.acm.org/doi/pdf/10.1145/3477132.3483567)
[Slides](https://www.cs.utexas.edu/~vijay/papers/winefs-sosp21-slides.pdf)
[Talk](https://www.youtube.com/watch?v=16Ami3IsYI8&ab_channel=ACMSIGOPS)
[Citation](https://www.cs.utexas.edu/~vijay/bibtex/winefs-sosp21.bib) <br>


## RainBlock: Faster Transaction Processing for Public Blockchains 
USENIX Annual Technical Conference (ATC), 2021<br>
**Soujanya Ponnapalli**,  Aashaka Shah,  Souvik Banerjee,  Amy Tai,  Malkhi Dahlia,  Vijay Chidambaram,  Michael Wei <br>
[Paper](https://www.usenix.org/system/files/atc21-ponnapalli.pdf)
[Slides](https://www.usenix.org/system/files/atc21_slides_ponnapalli.pdf)
[Talk](https://www.youtube.com/watch?v=oyrWI2LaDq8&ab_channel=USENIX)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:NIvCRZAdxToJ:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UX2tRg:AFWwaeYAAAAAZejwrRjGIK6bzK9zu2owfCzohDg&scisig=AFWwaeYAAAAAZejwrSlgAQcwDgpjj6iKBXWs82U&scisf=4&ct=citation&cd=-1&hl=en)
<br>


## Software-defined data protection: Low overhead policy compliance is within reach 
Proceedings of the VLDB Endowment (pVLDB), 2021 <br>
Zsolt Istvan,  **Soujanya Ponnapalli**,  Vijay Chidambaram <br>
[Paper](https://dl.acm.org/doi/pdf/10.14778/3450980.3450986)
[Slides](https://www.youtube.com/watch?v=beM1qWI7tho&ab_channel=VLDB2021))
[Talk](https://www.youtube.com/watch?v=beM1qWI7tho&ab_channel=VLDB2021)
[Citation](https://scholar.googleusercontent.com/scholar.bib?q=info:lbGn4Hm5ml4J:scholar.google.com/&output=citation&scisdr=ClE48TFbEPS13UQVdM0:AFWwaeYAAAAAZekTbM27vjR36aCY7495-eseBnM&scisig=AFWwaeYAAAAAZekTbM6Bbho1Vqw_ns0yEUMuCUE&scisf=4&ct=citation&cd=-1&hl=en)


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
<!-- <p>
 <span style="float: left"><a href="https://www.usenix.org/system/files/conference/hotstorage18/hotstorage18-paper-raju.pdf" target="_blank"><img src="../images/abstract_mlsm.png" style="width:30vw;margin-left=0"></a></span>
 <span style="float: right"><a href="https://www.usenix.org/sites/default/files/conference/protected-files/hotstorage18_slides_ponnapalli.pdf" target="_blank"><img src="../images/paper_mlsm.png" style="width:20vw"></a></span>
</p>  -->


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
