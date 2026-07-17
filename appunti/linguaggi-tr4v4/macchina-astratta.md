---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 22-09-2024 21:26:12
links:
  - "[[lecture-17092024110611|Lecture 17092024110611]]"
---
# Macchina astratta
---
## Introduzione
> Una **macchina astratta** è come una [[macchina-fisica|macchina fisica]], perché ha una sua memoria e una lista di operazioni eseguibili, ma in più è composta da
> - _controllo sequenza_
> - _controllo dati_
> - _gestione memoria_
> 
> per consentire un'attuazione delle istruzioni del suo linguaggio nella macchina al livello inferiore. Il processo di **traduzione** delle operazioni e della memoria è gestito dall'**[[interprete|interprete]]**.
> Ogni macchina astratta ha un suo [[linguaggio-macchina|linguaggio]].
> Formalmente una macchina astratta e' un _insieme di [[struttura-dati|strutture dati]] e [[algoritmo|algoritmi]] in grado di memorizzare ed eseguire programmi_.

<u>Nota bene</u>: la macchina $M$ al livello inferiore potrebbe essere un'altra macchina astratta o la macchina fisica (quella al livello più basso $0$).

![[macchina-astratta.png]]

## Gerarchie
Di fatto ogni macchina astratta può basarsi su una macchina astratta di livello più basso e fare da base (offrire servizi) a una macchina astratta di livello più alto. Teoricamente la macchina $M_{i}$ dovrebbe nascondere alla macchina $M_{i+1}$ la macchina $M_{i-1}$.

Nella pratica, la gerarchia di macchine astratte si ritrova in più campi dell'informatica:
- schema "a cipolla" del [[sistema-operativo|sistema operativo]];
- schema di una [[applicazione-web|applicazione web]];
- i protocolli di [[internet|internet]], come il [[modello-iso-osi|modello ISO-OSI]].

## Referenze
- [[realizzazione-di-una-macchina-astratta|Realizzazione di una macchina astratta]]