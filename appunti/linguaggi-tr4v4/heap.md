---
tags:
  - category/note
  - status/finished
  - topic/programmazione
  - topic/linguaggi-di-programmazione
date: 05-11-2023 19:20:43
links:
  - "[[lecture-03112023110813|Lecture 03112023110813]]"
  - "[[lecture-26022025111603|Lecture 26022025111603]]"
---
# Heap
---
## Definizione
> L'**heap** è quella parte di [[allocazione-dinamica-della-memoria-dei-programmi|memoria]] riservata a un [[processo|processo]] in esecuzione in cui vengono _allocati nuovi blocchi di memoria_, solitamente quindi [[strutture-dati-dinamiche|dati dinamici]].

Lo [[stack|stack]] non e' sufficiente come meccanismo di [[allocazione-dinamica-della-memoria-dei-programmi|allocazione dinamica della memoria]]: non vogliamo limitarci alla sola politica [[lifo|LIFO]], ma essere liberi di allocare memoria dinamica in modo "disordinato". Per esempio, vogliamo poter fare `malloc(A)`, `malloc(B)` e poi `free(A)`, `free(B)`. I blocchi dell'heap devono poter essere allocati e deallocati in momenti arbitrari.

## Implementazione
Le caratteristiche dell'heap devono essere:
- supporto alla [[frammentazione|deframmentazione]];
- velocita' di accesso.

Il tutto si implementa mediante la cosiddetta [[lista-libera|lista libera]].

## Referenze