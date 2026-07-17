---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 17-10-2025 20:26:39
links:
  - "[[lecture-14052025105842|Lecture 14052025105842]]"
---
# Shadowing
---
## Introduzione
> Nei [[linguaggio-di-programmazione-orientato-a-oggetti|linguaggi orientati agli oggetti]] ([[oop|OOP]]) per **shadowing** si intende il caso in cui una sotto[[classe|classe]] puo' mascherare i campi della sua superclasse definendo campi con lo stesso nome.

Tale mascheramento _avviene secondo le regole di [[scope|scope]] a livello di blocco_: la superclasse appartiene al blocco esterno e la sottoclasse al blocco interno, per cui quest'ultimo puo' mascherare qualsiasi variabile del blocco esterno (e dell'eventuale blocco ancora piu' esterno!). Si dice quindi che lo shadowing e' risolto in [[early-binding|early binding]].

Lo shadowing e' SEMPRE risolto in early binding: se abbiamo un oggetto `o` di classe `A` e `o` viene inizializzato a un'istanza di `B` sottoclasse di `A`, e questa fa shadowing di un campo di `A`, quel campo riferito a `o` e' quello di `A`! Viceversa avviene con i metodi, risolti con polimorfismo in [[late-binding|late binding]].

Per accedere a una variabile della sua superclasse, [[java|Java]] impone l'utilizzo del `super` per evitare errori.

## Referenze