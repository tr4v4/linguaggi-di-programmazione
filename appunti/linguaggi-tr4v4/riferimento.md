---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 23-09-2025 16:05:39
links:
  - "[[lecture-09042025110710|Lecture 09042025110710]]"
---
# Riferimento
---
## Introduzione
> Il [[tipi-di-dato|tipo di dato]] [[tipi-composti|composto]] **riferimento** contiene valori che danno accesso diretto a un'altro valore, ossia fanno riferimento a un dato.
> Le operazioni tipiche supportate sono:
> - _creazione_;
> - _controllo di uguaglianza_;
> - _dereferenziazione_;

L'implementazione piu' comune di questo tipo di dato sono i [[puntatore|puntatori]].

<u>Nota bene</u>: i riferimenti possono fare riferimento a riferimenti!

<u>Nota bene</u>: nei [[linguaggio-di-programmazione|linguaggi di programmazione]] con un modello di variabili a riferimento (come [[java|Java]]), non ci sono tipi riferimento --> ogni variabile lo e'!

## Problematiche
I riferimenti richiedono al programmatore di pensare in termini dinamici anziche' statici. Di fatto i riferimenti possono diventare:
- **wild** --> sono nella pratica puntatori non inizializzati, il loro accesso puo' causare comportamenti inaspettati;
- **dangling** --> quando il dato referenziato e' stato deallocato e l'accesso puo' portare a un comportamento inaspettato.

## Funzionamento
I linguaggi che supportano i riferimenti, di solito, definisco un abitante canonico: il `NULL`. Questo serve per "invalidare" un puntatore a run-time: infatti _quando si dichiara un puntatore, questo potrebbe gia' contenere al suo interno valori magari non validi_ (magari in zone proibite della memoria).

Quando si usa il `malloc` in [[c|C]], questo non conosce il tipo di puntatore che deve restituire (alloca solo dello spazio), e quindi restituisce un tipo `*void`: questo **non e' il [[tipi-di-base-unit|tipo unita']], ma solo un modo semantico per segnalare un qualunque tipo di ritorno[^1]**.

## Fenomeni
Nei linguaggi che supportano i riferimenti puo' avvenire:
- _deallocazione implicita_ - rendo irraggiungibile la cella nell'[[heap|heap]], mettendo il puntatore a `NULL` o cambiando il suo valore[^2];
- _deallocazione esplicita_ - con l'operazione `free` si rilascia la memoria referenziata da un puntatore.

<u>Nota bene</u>: chiamare `free` su un puntatore allo [[stack|stack]] e' un errore semantico (puo' portare a un comportamento imprevedibile).

## Referenze

[^1]: i [[generics|generics]]

[^2]: se non c'e' il [[garbage-collector|garbage collector]] questo causa _memory leak_!
