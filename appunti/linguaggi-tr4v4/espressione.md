---
tags:
  - category/note
  - status/finished
  - topic/programmazione
  - topic/linguaggi-di-programmazione
date: 26-09-2023 09:12:41
links:
  - "[[lecture-25092023151613|Lecture 25092023151613]]"
  - "[[lecture-27022025131944|Lecture 27022025131944]]"
---
# Espressione
---
## Definizione
> Un'**espressione** è una _sequenza di operazioni che restituiscono un valore_. Formalmente e' un'_entita' sintattica che produce un valore oppure non termina_.

### Composizione
Un'espressione può essere:
- una [[identificatore|variabile]]
- una [[costante-informatica|costante]]
- una [[funzione-informatica|chiamata di funzione]]
- una combinazione di tutte quelle elencate sopra

In ogni caso, **il tipo di un'espressione è determinato dalle operazioni e dal tipo degli operandi**.

## Sintassi
Un'espressione puo' essere scritta in forma:
- _[[notazione-infissa|infissa]]_;
- _[[notazione-prefissa|prefissa]]_ (polacca);
- _[[notazione-postfissa|postfissa]]_ (polacca inversa).

<u>Nota bene</u>: in generale e' molto piu' semplice valutare espressioni nelle ultime due forme!

## Valutazione
Di solito le espressioni vengono valutate usando [[albero-sintattico|alberi sintattici]].

### Ordine di valutazione
A seconda della [[dfs|visita sull'albero]] si producono le notazioni precedenti, e di conseguenza un ordine di valutazione delle espressini differente. Questo e' fondamentale per vari motivi:
- _effetti collaterali_
	- se si prende per esempio l'espressione `(a+f(b)) * (c+f(b))` e `f(b)` modifica `a` o `c`, allora l'ordine di valutazione e' fondamentale;
- _aritmetica finita_
- _operandi non definiti_
	- se si prende come esempio l'espressione `a == 0 ? b : b/a`;
	- se c'è _lazy evaluation_ ([[short-circuit-evaluation|short-circuit evaluation]]) allora il problema non si presenta;
	- se c'è _eager evaluation_ tutti gli operandi di una qualunque espressione sono valutati, e quindi l'espressione in esempio genererebbe un errore;
- _ottimizzazione_
- in generale: a seconda dell'ordine di valutazione potrebbero esserci risultati diversi di una stessa espressione

Ci sono diversi criteri per i quali un'espressione valuta l'ordine di esecuzione delle operazioni che contiene:
- parentesi
- precedenza tra operatori
- operatori con stessa precedenza
	- se binari (+, -, ...) da sx a dx
	- se unari (!, &, \*) da dx a sx
- per `&&` e `||` usa [[short-circuit-evaluation|short-circuit evaluation]]

## Referenze