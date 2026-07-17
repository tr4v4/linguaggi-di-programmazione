---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 18-10-2025 12:13:24
links:
  - "[[lecture-14052025105842|Lecture 14052025105842]]"
---
# VTable
---
## Introduzione
> Le **vtable** (**virtual function table**) sono una [[struttura-dati|struttura dati]] usata per gestire l'[[sottotipaggio|overriding]] nei [[linguaggio-di-programmazione-orientato-a-oggetti|linguaggi a oggetti]] con [[ereditarieta|ereditarieta' singola]]. In particolare e' l'implementazione primaria del [[dynamic-dispatch|dynamic dispatch]].

## Funzionamento
Ogni definizione di [[classe|classe]] corrisponde a una vtable, e tutte le istanze ([[oggetto|oggetti]]) di quella classe puntano alla stessa vtable. Questa **contiene i puntatori ai metodi della classe**.

Se `A` e' una classe con la sua vtable, e definiamo `B::A` (sottoclasse di A), allora **la vtable di `B` copiera' quella di `A` andando pero' a ridefinire i metodi overriddati da `B`** (funzioni virtuali di `A`), e poi aggiungendo ovviamente i nuovi metodi introdotti da `B`.

Per esempio, il codice:
```Java
class A {
	int a;
	void f(){...}
	void g(){...}
}
class B extends A {
	int b;
	int c;
	void f(){...}
	void h(){...}
}

A o1 = new A();
A o2 = new B();
```
apparira' nelle vtable in questa maniera:
![[vtable-1.png]]

## Complessita' computazionale
Questa implementazione fornisce effettivamente dei vantaggi in termini di [[complessita-computazionale|complessita' computazionale]] rispetto alla [[lista-liste-concatenate|lista concatenata]] di classi e sottoclassi (la seguente)?
![[oggetti-implementazione.png]]

La risposta e' si': l'invocazione di un metodo avviene al prezzo costante di 2 accessi. Infatti **il suo offset e' noto staticamente** ([[early-binding|early binding]])! Questo sembra strano, perche' abbiamo detto che l'overriding e' risolvibile solo dinamicamente ([[late-binding|late binding]]). Ma possiamo far si' che il compilatore calcoli uno stesso offset di ogni metodo, sia che questo appartenga ad `A` che a `B`. Per intenderci, la funzione `f` e' in `A` ed e' ridefinita in `B`: **l'offset tuttavia e' lo stesso all'interno della vtable, per cui se si accede ad `f` il compilatore staticamente sa che questo metodo si trova ad un certo offset**, indipendentemente dal fatto che sia la vtable di `A` o di `B`.

In altri termini, **i metodi devono rimanere nello stesso posto all'interno delle vtable per far funzionare il meccanismo staticamente**!

Questo ci permette di risolvere facilmente una situazione del tipo:
```Java
A o1 = new B();
```
dove **`o1` e' di tipo `A`, quindi puo' accedere solo ai metodi `f` e `g`, ma la sua vtable sara' quella di `B`, e gli offset di `f` e `g` sono gli stessi per cui e' trasparente a `o1` questa differenza di vtable**!

## Referenze
- [[classe-base-fragile|Classe base fragile]]