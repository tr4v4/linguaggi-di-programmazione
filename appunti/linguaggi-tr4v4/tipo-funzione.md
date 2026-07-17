---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 24-09-2025 23:26:05
links:
  - "[[lecture-10042025131105|Lecture 10042025131105]]"
  - "[[lecture-16042025110927|Lecture 16042025110927]]"
---
# Tipo funzione
---
## Introduzione
Nei [[linguaggio-di-programmazione|linguaggi di programmazione]] ad alto livello, spesso c'e' il supporto alla definizione di [[funzione-informatica|funzioni]]. Alcuni di loro denotano il loro tipo; per esempio:
```C
R f(P p) { ... }
```
denota una funzione del tipo $P \to R$.

Nella realta' sono solo i [[linguaggio-di-programmazione-funzionale|linguaggi funzionali]] a rendere i tipi di funzione esprimibili.

L'unica operazione supportata dalle funzioni e' la loro applicazione: ossia l'[[invocazione-di-procedura|invocazione]].

<u>Nota bene</u>: le funzioni in realta' non devono confondersi con quelle matematiche; potrebbero infatti esserci dei **side effects**! Se per esempio, pero', sappiamo che la funzione non ha side effect, allora possiamo usare tecniche come la [[memoization|memoization]] per velocizzare la sua computazione!

## Referenze