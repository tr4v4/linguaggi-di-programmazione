---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 25-02-2025 10:46:31
links:
  - "[[lecture-20022025131602|Lecture 20022025131602]]"
  - "[[lecture-27022025131944|Lecture 27022025131944]]"
---
# Scope dinamico
---
## Introduzione
> Per **scope dinamico** si intende la valutazione dello [[scope|scope]] degli [[identificatore|identificatori]] basata sul programma "dinamico" (a _run-time_), e dice che _un [[nome|nome]] non locale e' risolto nella prima occorrenza del [[blocco|blocco]] attivato piu' di recente_ (in senso temporale) _e non ancora disattivato_.

![[scope-dinamico.png]]

E' il meno usato, ma piu' semplice da implementare nel [[compilatore|compilatore]].

## Implementazione
Per implementare lo scope dinamico e' _sufficiente risalire i [[record-di-attivazione|record di attivazione]] nello [[stack|stack]] fino a trovare il blocco che contiene la variabile cercata_.

Esistono 2 tecniche per rendere efficiente tale ricerca:
- [[a-list|A-list]]
- [[crt|CRT]]

## Referenze