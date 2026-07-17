---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 05-10-2024 19:23:57
links:
  - "[[lecture-26092024120454|Lecture 26092024120454]]"
---
# Semantica statica
---
## Introduzione
> Ci sono regole, nei [[linguaggio-di-programmazione|linguaggi di programmazione]] che non possono essere catturati da [[grammatiche-libere|grammatiche libere]]. Vengono chiamate **vincoli sintattici contestuali**, e costituiscono la **semantica statica** (o **sintassi contestuale**).
> La caratteristica primaria della semantica statica è che _riguarda quell'insieme di controlli che possono essere fatti sul testo di un programma **senza eseguirlo**_.

Per esempio
- la verifica della [[dichiarazione|dichiarazione]] di una [[identificatore|variabile]] prima del suo utilizzo;
- la compatibilità tra tipo di variabile e valore dell'[[assegnamento|assegnamento]] ([[type-checking|type checking]]);
- l'uguaglianza tra il numero/tipo di parametri attuali di una [[invocazione-di-procedura|chiamata di procedura]] e il numero/tipo dei parametri formali della dichiarazione della [[funzione-informatica|funzione]];

sono _tutti vincoli contestuali_, perché esulano da ciò che una grammatica libera riesce a esprimere.

<u>Nota bene</u>: in realtà, _questi controlli dovrebbero appartenere alla sintassi, ma dato che solitamente si associa la sintassi alla grammatica libera, allora si fa riferimento alla sintassi contestuale come semantica statica_.

## Soluzioni
Esistono due tecniche alternative per la cattura di vincoli contestuali:
1. usare _[[grammatiche-dipendenti-dal-contesto|grammatiche dipendenti dal contesto]]_ --> si tratta di una soluzione poco pratica perché riconoscere una stringa $w$ appartenente a un [[linguaggio-generato|linguaggio generato]] da una [[grammatiche|grammatica]] del genere diventa un problema di [[complessita-computazionale|complessità]] esponenziale ($w \in L(G)$?);
2. usare _controlli "ad hoc"_ --> i [[compilatore|compilatori]] possiedono una fase di [[analisi-semantica|analisi semantica]] che fa questi controlli.

Ovviamente la seconda opzione è quella usata effettivamente. Di fatto **si lascia la descrizione della sintassi del linguaggio di programmazione alla grammatica libera** e **durante la fase di analisi semantica il compilatore verifica i vincoli sintattici contestuali** (semantica statica);

## Referenze
- [[semantica-dinamica|Semantica dinamica]]