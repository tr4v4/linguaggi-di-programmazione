---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 28-08-2025 19:23:02
links:
  - "[[lecture-21112024121059|Lecture 21112024121059]]"
---
# Grammatiche LR(0)
---
## Introduzione
> Una **[[grammatiche|grammatica]] e' $LR(0)$** se ogni casella nella [[tabella-di-parsing-lr|tabella di parsing]] $LR(0)$ contiene al piu' un elemento.

## Teoremi
### Limiti
> Le grammatiche $LR(0)$ sono limitate dalle seguenti osservazioni:
> - _se $G$ ha [[produzioni-epsilon|produzioni]]-$\epsilon$ allora difficilmente e' $LR(0)$[^1]_;
> - _se $L$ e' [[linguaggio-libero-deterministico|libero deterministico]] e gode della prefix-property, allora $L$ e' $LR(0)$_[^2];
> - _se $L$ e' $LR(0)$ ed e' finito, allora gode della prefix-property_[^3];
> - _se $L$ e' $LR(0)$ ed e' infinito, puo' non godere della prefix-property_;

## Referenze
- [[grammatiche-slr-1|Grammatiche SLR(1)]]
- [[grammatiche-lr-1|Grammatiche LR(1)]]

[^1]: il caso banale si ha per quelle grammatiche che hanno uno stato del [[dfa-dei-prefissi-viabili|DFA dei prefissi viabili]] con item $A \to .$ che non ha un altro item del tipo $B \to \alpha . a \beta$
[^2]: quindi, se invece e' libero deterministico ma non e' $LR(0)$ allora non gode della prefix-property
[^3]: e quindi, se e' finito e non gode della prefix-property, allora $L$ non e' $LR(0)$
