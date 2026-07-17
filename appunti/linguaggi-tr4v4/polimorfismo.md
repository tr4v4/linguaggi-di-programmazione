---
tags:
  - category/note
  - status/finished
  - topic/ingegneria-del-software
  - topic/linguaggi-di-programmazione
date: 22-09-2025 13:57:36
links:
  - "[[lecture-22092025100902|Lecture 22092025100902]]"
  - "[[lecture-23042025111218|Lecture 23042025111218]]"
---
# Polimorfismo
---
## Definizione
> Per **polimorfismo** si intende la _capacita' di un [[sistema-di-tipi|sistema di tipi]] di esprimere che alcuni [[tipi-di-dato|tipi]] accettano altri tipi come parametri_. In altre parole, un sistema di tipi polimorfico consente agli sviluppatori di specificare un insieme di operazioni su un dato tipo parametrico che **astrae da alcuni dettagli dell'istanziazione concreta del tipo**.

Se il sistema non lo permette allora si dice essere _monomorfico_; se il sistema lo permette invece si dice _polimorfico_.

## Tipologie
Esistono 3 tipi di polimorfismo:
- _ad hoc_ --> [[overloading|overloading]];
- _subtyping/virtual function_ --> [[sottotipaggio|overriding]];
- _parametrico/universale_ --> [[generics|generics]].

Esistono poi i [[tipi-monadici|tipi monadici]].

## Referenze
- [[binding|Binding]]