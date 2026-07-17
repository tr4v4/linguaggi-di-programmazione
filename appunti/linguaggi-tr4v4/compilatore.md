---
tags:
  - "#category/note"
  - "#status/finished"
  - topic/programmazione
  - topic/linguaggi-di-programmazione
date: 18-09-2023 22:15:25
links:
  - "[[lecture-18092023150410|Lecture 18092023150410]]"
  - "[[lecture-17092024110611|Lecture 17092024110611]]"
  - "[[lecture-26092024120454|Lecture 26092024120454]]"
---
# Compilatore
---
## Introduzione
L'[[assembly|assembly]] presenta 2 principali difetti:
- è specifico al processore della macchina
- costringe a ragionare come la macchina

Per questo si scrivono i programmi in **linguaggi ad alto livello**, che devono però essere tradotti in codice assembly (**codice oggetto**).

Dovendo tradurre da linguaggi ad alto livello a linguaggi a basso livello _specifici per ogni processore_, in fase di installazione il compilatore **si adatta** al processore su cui viene installato.

## Definizione
> Un **compilatore** ${C_{L, L_{O}}}^{L_{A}}$ è un programma scritto in $L_{A}$ ([[linguaggio-di-programmazione|linguaggio]] di una terza [[macchina-astratta|macchina astratta]] $M_{A}$), che realizza una [[funzione-matematica|funzione]]
> $$C_{L,L_{O}}: {P_{r}}^{L} \to {P_{r}}^{L_{O}} \ \ | \ \ \forall {P_{r}}^{L}. \ \ C_{L,L_{O}}({P_{r}}^{L})={{P_{r}}c}^{L_{O}} \implies \forall \text{input}. \ \ P^{L}(\text{input}) = Pc^{L_{O}}(\text{input})$$

ovvero il compilatore (come anche l'[[interprete|interprete]]) deve fare in modo che _la [[semantica|semantica]] del programma in input sia la stessa del programma in output_.
![[traduzione-compilatore.png]]

Pros:
- _alta efficienza_

Cons:
- _difficoltà d'implementazione_ (per lontananza da $L$ a $L_{O}$)
- _scarsa flessibilità_
- _perdita di informazione sulla struttura del programma_

Difatti, di un errore a run-time di un programma compilato è poco facile identificare la causa: anche se la semantica è la stessa, si è completamente perso il riferimento al programma scritto in $L$.

## Referenze
- [[workflow-di-compilazione|Workflow di compilazione]]
- [[struttura-di-un-compilatore|Struttura di un compilatore]]