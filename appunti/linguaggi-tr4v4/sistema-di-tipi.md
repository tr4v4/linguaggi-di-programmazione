---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 06-04-2025 12:53:48
links:
  - "[[lecture-02042025112213|Lecture 02042025112213]]"
---
# Sistema di tipi
---
## Introduzione
> Un **sistema di tipi** è un _insieme di regole che definisce come i [[tipi-di-dato|tipi di dato]] possono essere utilizzati all'interno di un [[linguaggio-di-programmazione|linguaggio di programmazione]]_. Formalmente potremmo definire un sistema di tipi come _un metodo sintattico praticabile per dimostrare l'assenza di determinati comportamenti del programma, fatto classificando le unità sintattiche in base ai tipi di valore che assumono_.

Ogni linguaggio di programmazione ha un proprio sistema di tipi, composto da **abitanti**, ossia informazioni che governano i tipi e i loro valori.

## Composizione
In particolare un sistema di tipi comprende:
- _insieme di [[tipi-di-base|tipi di base]]_;
- _meccanismi per definire [[tipi-composti|nuovi tipi]]_;
- meccanismi di computazione sui tipi:
	- _[[equivalenza-di-tipo|regole di equivalenza]]_ --> quando due tipi corrispondono allo stesso tipo
	- _[[compatibilita-di-tipo|regole di compatibilità]]_ --> quando si può usare un tipo al posto di un altro
	- _[[inferenza-di-tipo|regole/tecniche di inferenza]]_ --> come assegnare un tipo a un'espressione
- _definizione sul controllo dei vincoli di tipo statico o dinamico_.

## Referenze
- [[polimorfismo|Polimorfismo]]