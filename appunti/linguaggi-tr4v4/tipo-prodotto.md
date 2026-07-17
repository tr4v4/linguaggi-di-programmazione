---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 23-09-2025 16:28:00
links:
  - "[[lecture-09042025110710|Lecture 09042025110710]]"
---
# Tipo prodotto
---
## Introduzione
Assumendo l'[[assioma-dell-insieme-potenza|assioma dell'insieme potenza]] e la definizione di [[coppia-ordinata|coppia ordinata]] e [[prodotto-cartesiano|prodotto cartesiano]], definiamo i tipi prodotto nel seguente modo:
> I [[tipi-di-dato|tipi di dato]] [[tipi-composti|composti]] **prodotto**, sono tipi che combinano due o piu' [[tipi-di-base|tipi base]] in una struttura fissa.

Gli [[array|array]], gli [[insieme|insiemi]], i [[riferimento|riferimenti]], prendono tutti "come parametro" un solo tipo.

## Tipologie
I tipi prodotto piu' comuni sono:
- _coppie_
- _tuple_
- _record_
- _varianti_

Per convenzione, il prodotto vuoto e' l'[[tipi-di-base-unit|unita']];

### Coppie e tuple
Dati due tipi $A$ e $B$, la coppia $A \times B$ definisce l'insieme delle coppie possibili dei valori di $A$ con quelli di $B$.

Le tuple sono solo una generalizzazione delle coppie a un numero arbitrario e finito di tipi. Identificano i _componenti mediante la loro definizione posizionale_.
Es.:
```Rust
let coords: (i32,i32);
coords=(89,97);
let x = coords.0;
let y = coords.1;
```

### Record
Sono come le tuple, ma _identificano i componenti usando etichette_ invece che la loro definizione posizionale. I [[c|C]] per esempio sono le `struct`.

Gli elementi di un record sono chiamati campi.

E' fondamentale l'ordine dei campi in un record: _cambia il modo in cui questi vengono rappresentati in memoria_.

## Destrutturazione
Con i tipi prodotto e' facile produrre nuovi tipi di dati strutturati, ma abbiamo bisogno di introdurre dei costrutti che li rendano facili da destrutturare, ossia smontare nei singoli tipi: [[pattern-matching|pattern matching]].

## Referenze