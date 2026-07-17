---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 02-04-2025 00:25:04
links:
  - "[[lecture-05032025111458|Lecture 05032025111458]]"
---
# Ricorsione in coda
---
## Introduzione
> Una [[funzione-informatica|funzione]] `f` si dice di **ricorsione in coda** se contiene solo "_chiamate in coda_", ovvero se restituisce il valore della chiamata di `f'` (in `f`) senza ulteriore computazione.

In tal caso non è necessaria alcuna [[allocazione-dinamica-della-memoria-dei-programmi|allocazione dinamica della memoria]]: è sufficiente un solo [[record-di-attivazione|record di attivazione]]!

## Esempio
Prendiamo la funzione ricorsiva che calcola il [[fattoriale|fattoriale]]:
![[fattoriale.png]]

La sua versione con ricorsione in coda è
![[fattoriale-ricorsione-in-coda.png]]

## Referenze