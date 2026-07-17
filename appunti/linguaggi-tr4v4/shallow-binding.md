---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 05-04-2025 18:31:29
links:
  - "[[lecture-12032025111631|Lecture 12032025111631]]"
  - "[[lecture-19032025113725|Lecture 19032025113725]]"
---
# Shallow binding
---
## Introduzione
> Lo **shallow binding** e' una delle due regole di valutazione dell'[[ambiente|ambiente]] delle [[funzione-di-ordine-superiore|funzioni di ordine superiore]] passate come parametro ad altri funzioni, che _risolve le variabili non locali nell'ambiente al momento dell'[[invocazione-di-procedura|invocazione]] della funzione passata come parametro attuale_.

In definitiva:
- in caso di [[scope-statico|scope statico]] --> usa sempre la [[chiusura|chiusura]] con puntatore a [[catena-statica|catena statica]] per determinare l'ambiente di valutazione delle variabili non locali della funzione;
- in caso di [[scope-dinamico|scope dinamico]] --> _e' automatico_! si usa lo stesso principio dello scope dinamico, per cui basta scorrere i record di attivazione (usando [[a-list|A-list]] o [[crt|CRT]]) e si implementa automaticamente lo shallow binding.

Fatto sta che di solito lo shallow binding viene associato allo scope dinamico.

## Referenze