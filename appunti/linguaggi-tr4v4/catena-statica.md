---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 16-03-2025 13:22:58
links:
  - "[[lecture-26022025111603|Lecture 26022025111603]]"
---
# Catena statica
---
## Introduzione
> La **catena statica** e' la _[[lista|lista]] di puntatori di link statici dei [[record-di-attivazione|record di attivazione]] dello [[stack|stack]]_, fondamentale per implementare lo [[scope-statico|scope statico]].

<u>Nota bene</u>: l'informazione di contenimento dei blocchi e' direttamente fornita dal [[compilatore|compilatore]], che e' in grado di riconoscere i livelli di annidamento a partire da un'analisi statica (a _compile-time_) del programma.

<u>Nota bene</u>: in realta', per sapere dove trovare la variabile in un blocco, **non si scorre tutta la catena statica**. Il **compilatore** e' in grado di fornire un'**indicazione precisa di dove cercare la variabile**, in particolare di **quanti livelli di annidamento bisogna rilasire per trovarla**. Tuttavia, **e' necessario scorrere la catena statica per il numero di livelli indicato**: il compilatore non puo' fornire l'indirizzo esatto della variabile nello stack[^1].

<u>Osservazione</u>: se un programma ha un massimo livello di annidamento di $k$, allora la catena statica sara' lunga al massimo $k$.

### Esempio
Se per esempio, il programma fosse composto nel seguente modo
![[catena-statica-1.png]]

e la sequenza di chiamate fosse `A, B, C, D, E, C`, allora lo stack sarebbe
![[catena-statica-2.png]]

dove le freccie tratteggiate indicano i link statici. Per esempio, sia il `C` chiamato da `B`, che il `C` chiamato da `E`, avra' come link statico il blocco padre, ovvero `A`: quindi tutti i [[nome|nomi]] non risolvibili nell'[[ambiente|ambiente]] locale di `C` verranno cercati in `A`, implementando lo scope statico!

## Implementazione
Sappiamo che il compilatore e' in grado di rilevare, da un'analisi statica, i livelli di annidamento dei blocchi. Tuttavia, **come vengono implementati i link statici**? Ossia, come sa un blocco dove trovare il blocco padre all'interno dello stack? Come gia' detto, questo e' un procedimento che dev'essere per forza svolto a _run-time_.

Infatti, si sfruttano le informazioni fornite dal compilatore, per determinare il link statico. Quando un chiamante `Ch` in esecuzione chiama un chiamato `P`, ci sono 2 casi:
- _`P` e' interno_, ossia e' un blocco figlio di `Ch`, e quindi questo passera' al link statico di `P` il proprio [[sp|SP]] ($k = 0$);
- _`P` e' esterno_, ossia e' un blocco non figlio di `Ch`, e quindi `Ch` risalira' la catena statica di $k$ passi (dove $k$ e' il livello di annidamento di `P` rispetto a `Ch`, ossia quanti passi bisogna fare da `Ch` per arrivare al blocco che contiene `P`), e passera' al link statico di `P` l'SP del blocco trovato.

A questo punto, ricapitolando, il compilatore associa:
- $k$ ad ogni chiamata (all'interno di un blocco) - di quanto risalire la catena statica per ottenere il blocco (RdA) corretto;
- $h$ ad ogni [[nome|nome]] - se e' $0$ allora e' nell'ambiente locale, altrimenti e' un nome non-locale definito $h$ blocchi sopra;

## Miglioramenti
Per migliorare le performance della ricerca, viene proposta come alternativa quella del [[display|display]].

## Referenze

[^1]: si tratta di un [[problema-indecidibile|problema indecidibile]]
