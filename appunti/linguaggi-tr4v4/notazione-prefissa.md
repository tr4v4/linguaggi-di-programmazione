---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 16-03-2025 16:17:58
links:
  - "[[lecture-27022025131944|Lecture 27022025131944]]"
---
# Notazione prefissa
---
## Introduzione
> La **notazione prefissa**, anche detta **polacca**, e' una notazione sintattica per esprimere [[espressione|espressioni]] che prevede che _l'operatore venga posto prima degli operandi_.

Come nel caso della [[notazione-postfissa|notazione postfissa]], la notazione prefissa e' un'alternativa molto semplice a quella [[notazione-infissa|infissa]]:
- non servono regole di precedenza;
- non servono regole di associatività;
- non servono le parentesi;
- l'[[algoritmo|algoritmo]] di valutazione e' naive, utilizza solo una [[pila|pila]], ma necessita un conteggio degli operandi su cui eseguire le operazioni.

## Referenze