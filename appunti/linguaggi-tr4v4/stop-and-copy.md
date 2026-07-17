---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 05-10-2025 20:28:32
links:
  - "[[lecture-30042025110449|Lecture 30042025110449]]"
---
# Stop and copy
---
## Introduzione
> Per **stop and copy** si intende una tecnica implementata dai [[garbage-collector|garbage collector]].

E' un'evoluzione del [[mark-and-sweep|mark and sweep]].

## Funzionamento
Dividiamo l'[[heap|heap]] in 2 regioni di uguale dimensione. Si alloca e dealloca solo su una delle due porzioni. Quando questa e' quasi piena, **tutto cio' che e' raggiungibile dallo stack viene copiato in modo contiguo nell'altra porzione libera di heap**; quindi si brasa la porzione occupata.

Quindi, aggiorno i puntatori, in modo che puntino nella nuova porzione.

E si invertono i ruoli delle due porzioni!
![[stop-and-copy.png]]

### Vantaggi
Il grande vantaggio di questa tecnica e' la _[[defrag|deframmentazione]] automatica_! Questo avviene in quanto incollo gli oggetti in modo contiguo.

Inoltre, il copia e incolla e il cambio di puntatori costa, ma _in modo proporzionale alla quantita' di oggetti non garbage_!

### Svantaggi
Viene dimezzata la dimensione di heap disponibile.

## Referenze