---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 16-03-2025 12:01:25
links:
  - "[[lecture-26022025111603|Lecture 26022025111603]]"
---
# Liste libere multiple
---
## Introduzione
> Le **liste libere multiple** sono una tecnica usata per _rendere piu' efficiente l'allocazione di memoria nell'[[heap|heap]]_ a partire dalla [[lista-libera|lista libera]].

## Implementazione
L'idea e' di **avere tante liste libere, ognuna composta da blocchi di dimensione specifica**.

La ripartizione dei blocchi, a seconda della loro dimensione, puo' essere:
- _statica_ - ogni lista libera ha una dimensione specifica;
- _dinamica_ - ogni lista libera ha una dimensione determinata dal suo livello di profondita';
	- [[buddy-system|Buddy system]]
	- [[fibonacci-system|Fibonacci system]]

## Referenze