---
tags:
  - category/note
  - status/finished
  - topic/ingegneria-del-software
  - topic/linguaggi-di-programmazione
date: 22-09-2025 15:26:01
links:
  - "[[lecture-22092025100902|Lecture 22092025100902]]"
  - "[[lecture-14052025105842|Lecture 14052025105842]]"
---
# Late binding
---
## Introduzione
In presenza delle funzioni virtuali ([[sottotipaggio|overriding]]) non è possibile fare binding a compile-time ([[early-binding|early binding]]). Il compilatore al massimo può creare dei meccanismi che consentano a _run-time_ di identificare correttamente il codice della funzione [[invocazione-di-procedura|invocata]].

Si implementa mediante [[vtable|v-tables]].
![[v-tables-1.png]]

L'esecuzione di una chiamata a run-time di una certa funzione su un'oggetto che contiene metodi virtuali, funziona in questo modo:
1. dal puntatore il programma ottiene l'oggetto;
2. dall'oggetto segue la v-table e ottiene i puntatori ai metodi effettivamente implementati di quell'oggetto (sottotipo);
3. cerca la funzione giusta, e dal puntatore ottiene il codice da eseguire.

## Utilizzo
Non usiamo sempre i metodi virtuali perché _il late binding è costoso_!

## Referenze