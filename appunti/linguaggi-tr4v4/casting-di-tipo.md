---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 28-09-2025 15:34:35
links:
  - "[[lecture-16042025110927|Lecture 16042025110927]]"
---
# Casting di tipo
---
## Introduzione
> Per **casting di tipo** si intende la conversione _esplicita_ di tipo, ossia mediante annotazione indicata dall'utente. Questo puo' avvenire solo se _i due tipi sono [[compatibilita-di-tipo|compatibili]]_!

A volte il [[sistema-di-tipi|sistema di tipi]] non fa [[coercizione-di-tipo|coercizione]] perche' potrebbe dare risultati che il programmatore non si aspetta, allora segnala il problema al programmatore suggerendogli di fare il casting.
```C
int x = 1 + 1.5;    // da' errore, bisogna esplicitare come convertire quell'1.5
int x = 1 + (int)1.5;    // e' il modo corretto
```

## Referenze