---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 05-04-2025 17:46:07
links:
  - "[[lecture-12032025111631|Lecture 12032025111631]]"
---
# Chiusura
---
## Introduzione
> Una **chiusura** e' la coppia ([[variabile|variabile]], [[ambiente|ambiente]]), che lega quindi un [[nome|nome]] all'ambiente in cui sara' valutato.

## Funzioni di ordine superiore
Nel caso del passaggio di [[funzione-di-ordine-superiore|funzioni di ordine superiore]] come parametri, le due regole di [[deep-binding|deep]] e [[shallow-binding|shallow binding]] sono implementate mediante la chiusura: _come parametro attuale si passa la coppia `(puntatore alla funzione, ambiente non locale)`_.

<u>Nota bene</u>: nel caso di [[scope-statico|scope statico]], l'ambiente non locale sara' sempre lo stesso sia con deep che con shallow binding.

## Referenze