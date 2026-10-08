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
# Shown on the homepage's Selected Publications despite being in review;
# without this the list is accepted work only.
selected: true
# Key insight: 2-3 lines, shown under the venue on the publications page.
keyinsight: 'In state machine replicated systems, every replica writes to a persistent write-ahead log before committing, so that it can recover from a crash. Logging at every replica is both inefficient and unnecessary: tolerating *f* crash-stop failures requires only a majority (*f* + 1) of replicas to log persistently. With Metronome, we log only at a majority of replicas, improving both commit throughput and I/O efficiency.'
paperurl: 'https://github.com/SoujanyaPonnapalli/Metronome/blob/main/Tech_Report.pdf'
pdfurl: 'https://github.com/SoujanyaPonnapalli/Metronome/blob/main/Tech_Report.pdf'
# GitHub's raw URL downloads rather than renders, so it is the download
# target only; the title above opens the blob view in a new tab instead.
downloadurl: 'https://github.com/SoujanyaPonnapalli/Metronome/raw/main/Tech_Report.pdf'
slidesurl: ''
talkurl: 'https://www.youtube.com/watch?v=KqOtzIuAmFk&list=PLfwvyNe91s6h17_c8zlCO2wxOYGg6HBVf'
citationurl: ''
---
