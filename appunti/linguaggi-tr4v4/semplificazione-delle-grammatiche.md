---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 19-08-2025 19:42:56
links:
  - "[[lecture-05112024110833|Lecture 05112024110833]]"
---
# Semplificazione delle grammatiche
---
## Introduzione
Il motivo per cui e' fortemente richiesta la semplificazione di una [[grammatiche|grammatica]], riguarda l'efficienza e la possibilita' stessa di creare dei [[automa-a-pila|PDA]] che ne riconoscano il [[linguaggio-generato|linguaggio generato]].

## Casi
Nella pratica, semplificare le grammatiche si traduce in:
1. **eliminare le produzioni-$\epsilon$** ($A \to \epsilon$), inadatte al [[parser-bottom-up|bottom-up parsing]] --> [[produzioni-epsilon|produzioni epsilon]];
2. **eliminare le produzioni unitarie** ($A \to B$), che possono creare cicli ($A \implies^{+} A$) --> [[produzioni-unitarie|produzioni unitarie]];
3. **eliminare simboli inutili**, ossia terminali/nonterminali non raggiungibili/generabili a partire da $S$ --> [[simboli-inutili|simboli inutili]];
4. **eliminare le ricorsioni sinistre** ($A \to A\alpha$), inadatte al [[parser-top-down|top-down parsing]] --> [[ricorsione-sinistra|ricorsione sinistra]];
5. **fattorizzare la grammatica**, per ottenere grammatiche con meno nondeterminismo nel top-down parsing --> [[fattorizzazione-a-sinistra|fattorizzazione a sinistra]].

## Forme normali
Studiamo ora delle forme di grammatiche standard che garantiscono certe proprieta':
- [[forma-normale-di-chomsky|forma normale di Chomsky]];
- [[forma-normale-di-greibach|forma normale di Greibach]].

## Referenze