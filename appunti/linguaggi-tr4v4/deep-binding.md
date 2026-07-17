---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 05-04-2025 18:25:15
links:
  - "[[lecture-12032025111631|Lecture 12032025111631]]"
  - "[[lecture-19032025113725|Lecture 19032025113725]]"
---
# Deep binding
---
## Introduzione
> Il **deep binding** e' una delle due regole di valutazione dell'[[ambiente|ambiente]] delle [[funzione-di-ordine-superiore|funzioni di ordine superiore]] passate come parametro ad altri funzioni, che _risolve le variabili non locali nell'ambiente al momento del passaggio della funzione alla funzione come parametro attuale_.

In definitiva:
- in caso di [[scope-statico|scope statico]] --> dobbiamo legare la funzione passata al suo ambiente, per cui puntiamo a una [[chiusura|chiusura]] `<codice, ambiente>` come parametro formale, dove `ambiente` puntera' al record di attivazione dell'ambiente corretto (sulla base del livello di annidamento, ecc...);
- in caso di [[scope-dinamico|scope dinamico]] --> il deep binding si risolve mettendo il puntatore all'ambiente al momento del passaggio della funzione come parametro attuale nella chiusura.

Fondamentalmente il deep binding si implementa nello stesso modo con cui si fa il [[passaggio-per-nome|passaggio per nome]].

Fatto sta che di solito il deep binding viene associato allo scope statico.

## Referenze