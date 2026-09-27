---
title: 'Token Latency Fairness: Performance Isolation for Multi-Tenant LLM Serving'
authors: 'Dev Bali, Soujanya Ponnapalli, Yichuan Wang, Natacha Crooks, Scott Shenker, and Matei Zaharia'
collection: publications
permalink: 'arxiv26/token-latency-fairness'
date: 2026-05-01
venue: 'arXiv 2026'
order: 17
conf: 'arXiv'
confyear: 2026
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: 'Multi-tenant LLM serving equalizes throughput across clients over the long run, which still lets one high-demand client delay individual requests and stretch a well-behaved client''s token latencies by an order of magnitude. With FairInference, we define δ-token fairness instead: a token that takes *d* time units in isolation is produced within *d* + δ under multi-tenant execution. The scheduler enforces per-token deadlines while bounding the delays from GPU compute sharing and the shared KV cache.'
paperurl: 'https://arxiv.org/abs/2609.18112'
pdfurl: 'https://arxiv.org/pdf/2609.18112'
slidesurl: ''
talkurl: ''
citationurl: '/files/bib/token-latency-fairness-arxiv26.bib'
---
