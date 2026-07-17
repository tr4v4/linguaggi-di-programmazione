---
tags:
  - category/note
  - status/finished
  - topic/programmazione
  - topic/linguaggi-di-programmazione
date: 26-09-2023 09:08:32
links:
  - "[[lecture-25092023151613|Lecture 25092023151613]]"
  - "[[lecture-27022025131944|Lecture 27022025131944]]"
---
# Assegnamento
---
## Introduzione
> L'istruzione di assegnamento **memorizza un valore o il risultato di un calcolo in una variabile**. Segue la sintassi:
> `variabile = espressione`
> dove
> - `variabile` ([[variabile|variabile]]) è un [[identificatore|identificatore]];
> - `espressione` è un'[[espressione|espressione]].
> 
> Segue la [[dichiarazione|dichiarazione]].

## Sintassi
E' necessario comprendere bene la sintassi dell'assegnamento. Per esempio, considerata l'operazione `X = X + 1`, avremo che:
- la prima `X` è **l-value**, ovvero la variabile vera e propria, il contenitore del [[nome|nome]] `X`;
- la seconda `X` è **r-value**, ossia vale come il contenuto della variabile di nome `X`;

Inoltre, normalmente l'assegnamento non restituisce un valore, piuttosto produce un _side-effect_... Tuttavia, in alcuni linguaggi tra cui [[c|C]], l'assegnamento restituisce il valore della variabile dell'assegnamento (es. `X = 2` restituisce 2).

## Referenze