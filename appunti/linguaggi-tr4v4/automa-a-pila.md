---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 28-10-2024 18:03:19
links:
  - "[[lecture-17102024120438|Lecture 17102024120438]]"
---
# Automa a pila
---
## Introduzione
Possiamo definire gli **automi a pila** (o **pushdown automata**, **PDA**) come degli [[automa-a-stati-finiti|automi a stati finiti]] che _utilizzano una memoria ausiliaria, di tipo [[pila|stack]], per definire il loro comportamento_.

Prendiamo come esempio il linguaggio delle palindrome (pari)
$$L = \{ww^{R} | w \in \{a, b\}^{*}\}$$
che già sappiamo essere [[linguaggio-libero|libero]] perché [[linguaggio-generato|generato]] dalla [[grammatiche-libere|grammatica libera]]
$$S \to \epsilon | aSa | bSb$$
e non [[linguaggio-regolare|regolare]][^1].

Per consentire a un automa di riconoscere tale linguaggio, _è per forza necessario che questo ricordi la prima metà dell'input_, così da _poterla confrontare con la seconda metà in ordine inverso_. Proprio per questo aggiungiamo una memoria ausiliaria di tipo pila all'automa, che può crescere illimitatamente.
![[automa-a-pila.png]]

In particolare la pila:
- può _leggere solo l'elemento_ `top`;
- può _rimuovere solo l'elemento_ `top`;
- può _inserire un nuovo elemento solo in testa_;

## Tipologie
I PDA si dividono in:
- [[npda|NPDA]]
- [[dpda|DPDA]]

## Referenze
[^1]: si veda [[pumping-lemma|pumping lemma]]