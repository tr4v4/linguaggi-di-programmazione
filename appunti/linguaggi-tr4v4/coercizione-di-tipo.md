---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 28-09-2025 15:29:20
links:
  - "[[lecture-16042025110927|Lecture 16042025110927]]"
---
# Coercizione di tipo
---
## Introduzione
> Per **coercizione di tipo** si intende la conversione _implicita_ di tipo canonica/arbitraria, da un [[tipi-di-dato|tipo]] a un altro. Questo puo' avvenire solo se _i due tipi sono [[compatibilita-di-tipo|compatibili]]_!

Un esempio possibile e' una [[funzione-informatica|funzione]] `sum` che accetta due tipi `float`, e un programma che la [[invocazione-di-procedura|invoca]] passandoci due `int`: il **[[compilatore|compilatore]]/[[interprete|interprete]] inserisce le conversioni necessarie in modo implicito**, senza sollevare alcun errore di compatibilita'.
```C
float x = 1 + 1.5;  // quell'1 diventa 1.0
printf("%f", x);    // --> 2.5
```

## Referenze