---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 30-09-2024 21:52:27
links:
  - "[[lecture-24092024110820|Lecture 24092024110820]]"
  - "[[lecture-26092024120454|Lecture 26092024120454]]"
  - "[[lecture-17102024120438|Lecture 17102024120438]]"
---
# Derivazione
---
## Introduzione
> Data $G = (NT, T, R, S)$ una [[grammatiche|grammatica]], diciamo che _da $v$ si deriva immediatamente $w$_, denotandolo con $v \implies w$, se
> $$v = xAy, \ \ \ (A \to z) \in R, \ \ \ w = xzy$$
> con $x, y, z \in (T \cup NT)^{*}$.
> Inoltre, si dice che _da $v$ si deriva $w$_, denotandolo con $v \implies^{*} w$, se esiste una sequenza finita (eventualmente vuota) di derivazioni immediate
> $$v \implies w_{0} \implies \cdots \implies w$$[^1]

<u>Nota bene</u>: _ci possono essere più derivazioni diverse che generano la stessa stringa_.

<u>Nota bene</u>: _posso partire da simboli non iniziali, e otterrò delle derivazioni valide ma che non appartengono alla grammatica_!

## Tipologie
Esistono due fondamentali tipologie di derivazioni:
- [[derivazione-canonica-sinistra|derivazione canonica sinistra]]
- [[derivazione-canonica-destra|derivazione canonica destra]]

## Referenze
- [[albero-di-derivazione|Albero di derivazione]]

[^1]: $\implies^{*}$ è la chiusura riflessiva e transitiva della [[relazione|relazione]] $\implies$