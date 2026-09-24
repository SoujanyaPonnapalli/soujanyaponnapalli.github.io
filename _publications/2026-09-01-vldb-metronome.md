---
title: 'Metronome: I/O-Efficient Logging for State Machine Replication'
authors: 'Harald Ng, Soujanya Ponnapalli, Kevin Harrison, Reginald Frank, Audrey Cheng, Natacha Crooks, and Paris Carbone'
collection: publications
permalink: 'vldb27/metronome'
date: 2026-09-01
venue: 'VLDB 2027'
order: 1
conf: 'VLDB'
confyear: 2027
status: 'Under revision'
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: 'In state machine replication, every replica writes to a persistent write-ahead log before committing, so that it can recover from a crash. This is both inefficient and unnecessary: tolerating *f* crash-stop failures requires only a majority (*f* + 1) of replicas to log persistently. Logging at a majority rather than at every replica improves commit throughput and I/O efficiency.'
paperurl: 'https://github.com/SoujanyaPonnapalli/Metronome/blob/main/Tech_Report.pdf'
slidesurl: ''
talkurl: ''
citationurl: ''
---
