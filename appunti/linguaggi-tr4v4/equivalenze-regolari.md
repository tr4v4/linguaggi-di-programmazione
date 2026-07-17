---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 20-10-2024 16:03:49
links:
  - "[[lecture-10102024120505|Lecture 10102024120505]]"
  - "[[lecture-15102024110302|Lecture 15102024110302]]"
---
# Equivalenze regolari
---
## Introduzione
> Le [[espressione-regolare|espressioni regolari]], gli [[nfa|NFA]], i [[dfa|DFA]] e le [[grammatiche-regolari|grammatiche regolari]] sono _tutti formalismi equivalenti_. Rispettivamente questi _denotano/riconoscono/generano_ i [[linguaggio-regolare|linguaggi regolari]].

![[equivalenze-regolari.canvas|Equivalenze regolari]]

Si noti che questo è possibile per via di 5 teoremi affrontati in precedenza:
- [[equivalenza-tra-nfa-ed-espressioni-regolari|Equivalenza tra NFA ed espressioni regolari]]
- [[costruzione-per-sottoinsiemi-teorema|Costruzione per sottoinsiemi#Teorema]]
- [[equivalenza-tra-dfa-e-grammatiche-regolari|Equivalenza tra DFA e grammatiche regolari]] (ed [[equivalenza-tra-nfa-e-grammatiche-regolari|Equivalenza tra NFA e grammatiche regolari]])
- [[grammatiche-regolari-teorema|Grammatiche regolari#Teorema]]

## Passaggi
Di solito quello che si fa è:
1. definire un'espressione regolare;
2. costruire l'NFA associato;
3. ricavare il DFA equivalente;
4. [[minimizzazione-di-dfa|minimizzare il DFA]];
5. ricavare la grammatica regolare del DFA minimo;
6. semplificare la grammatica (rimuovendo i simboli inutili);
7. ricavare dalla grammatica semplificata l'espressione regolare associata.

Ciò che si dovrebbe ottenere alla fine è un'espressione regolare $s'$ equivalente a quella originale $s$:
$$s' \simeq s$$

Questo è sufficiente per dire che **il diagramma delle equivalenze regolari commuta**.

## Referenze