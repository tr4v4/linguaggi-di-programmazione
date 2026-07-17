---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 22-09-2024 21:53:09
links:
  - "[[lecture-17092024110611|Lecture 17092024110611]]"
---
# Linguaggio macchina
---
## Introduzione
> Ogni [[macchina-astratta|macchina astratta]] $M$ presenta un suo **linguaggio** $L_{M}$, compreso e tradotto dall'[[interprete|interprete]]. Il linguaggio $L_{M}$ consente di accedere alle componenti di $M$.

<u>Nota bene</u>: i programmi scritti in $L_{M}$ sono, a pensarci bene, i dati primitivi su cui opera l'interprete.

### Linguaggio macchina fisica
La [[macchina-fisica|macchina fisica]] $M_{F}$, ossia quella astratta di livello più basso, ha quindi il suo linguaggio $L_{M_{F}}$, che a prescindere dal tipo di [[isa|ISA]] adottato ([[cisc-e-risc|CISC e RISC]]), presenta solitamente delle istruzioni a due operandi del tipo: `ADD R5 R0`.

Queste istruzioni, dal punto di vista dell'[[assembler|assembler]] hanno una semantica propria - **rappresentazione esterna**. Nel caso dell'istruzione precedente "_somma il contenuto del registro R0 con quello nel registro R5 e salva il risultato in R5_". Dal punto di vista della macchina fisica, invece, queste non sono altro che opportune sequenze di bit (_word_), che compongono codice operativo - **rappresentazione interna**.

## Referenze