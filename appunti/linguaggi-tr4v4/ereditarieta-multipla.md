---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 17-10-2025 21:56:41
links:
  - "[[lecture-14052025105842|Lecture 14052025105842]]"
---
# Ereditarieta' multipla
---
## Introduzione
In alcuni linguaggi l'[[ereditarieta|ereditarieta']] e' singola: la gerarchia di ereditarieta' diventa un [[albero|albero]]. Questo e' il caso di [[java|Java]]. Ci sono invece altri linguaggi in cui l'**ereditarieta' e' multipla**: in tal caso la gerarchia diventa un [[dag|DAG]].

Il problema e' che **questa pone problemi concettuali e implementativi non indifferenti**!

<u>Nota bene</u>: **ereditarieta' singola e [[tipo-intersezione|tipi intersezione]] convivono perfettamente**! Infatti i secondi riguardano la [[sottotipaggio|relazione di sottotipaggio]]! Si puo' fare, per esempio, che _una classe estende due interfacce_, ossia diventa sottotipo di entrambe; invece con l'ereditarieta' singola questa medesima classe non potrebbe estendere due classi.

## Problemi
### DDD - conflitto di nomi
Se _una classe eredita da due classi che forniscono l'implementazione di metodi con lo stesso nome_? Questo problema prende il nome di **deadly diamond of death**:
![[deadly-diamond-of-death.png]]

Soluzioni (parziali):
- **vietare sintatticamente i conflitti**;
- **chiedere allo sviluppatore di risolvere esplicitamente ogni conflitto** --> in [[c|C++]] ogni metodo conflittuale deve esplicitare per disambiguarsi il suo supertipo, per esempio `A::m()` o `B::m()`;
- **stabilire una convenzione per risolvere i conflitti** --> in [[scala|Scala]] "vince" il metodo che compare piu' a sinistra nella clausola di estensione...;

## Referenze