---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 29-08-2025 17:55:54
links:
  - "[[lecture-21112024121059|Lecture 21112024121059]]"
---
# Tabella di parsing SLR(1)
---
## Introduzione
Purtroppo le [[tabella-di-parsing-lr|tabelle di parsing]] $LR$ non sono sufficienti: _le [[grammatiche-lr-0|grammatiche]] $LR(0)$ non coprono tutti i [[linguaggio-libero|linguaggi liberi]] (almeno i [[linguaggio-libero-deterministico|deterministici]])_.

Per esempio la grammatica $G$
- $S' \to S$
- $S \to a$
- $S \to ab$

non e' di classe $LR(0)$! Infatti il [[dfa-dei-prefissi-viabili|DFA dei prefissi viabili]] risulta essere il seguente:
![[dfa-prefissi-viabili-conflitto.png]]

Notiamo che se ci troviamo nello stato 1 possiamo:
- fare _shift $2$_ leggendo e accumulando $b$ sullo stack dei simboli, per poi passare allo stato $2$;
- fare _reduce $S \to a$_ tornando allo stato $0$ e (con il _goto_ corrispondente) andare nello stato $3$ e fare _accept_.

Abbiamo un **conflitto shift-reduce**! La tabella di parsing $LR(0)$ conferma questo conflitto:
![[tabella-di-parsing-lr0-conflitto.png]]

Per risolvere il conflitto, allora, possiamo usare il [[look-ahead|look-ahead]]! In particolare, in questo caso, ci e' sufficiente soffermarci sui [[first-e-follow|follow]] di $S$:
- se $b \in \text{Follow}(S)$ allora il conflitto e' (puo' essere) reale, ossia non e' risolvibile facilmente con il look-ahead;
- se $b \notin \text{Follow}(S)$ allora ci basta risolvere il conflitto a favore dello shift.

Nel nostro caso $\text{Follow}(S) = \{\$\}$, per cui $b$ non ci appartiene: **allora andiamo a mettere la _reduce_ nello stato 1 solo per i caratteri appartenenti al follow di $S$**!

Se la _prima produzione fosse stata $S' \to Sb$, allora $b \in \text{Follow}(S)$, e li' si' che ci sarebbe stato un reale conflitto_! Infatti avremmo potuto fare una _reduce_ anche leggendo $b$ in input, perche' in tal modo sulla pila si sarebbe accumulata comunque una maniglia $Sb$ da cui si poteva ricavare $S'$ e accettare la stringa!

Quindi **ha senso mettere la reduce solo per i follow del nonterminale della produzione**, perche' _se dopo tale nonterminale si ha un carattere che non appartiene ai suoi follow significa che la stringa non appartiene al [[linguaggio-generato|linguaggio generato]]_!

La tabella di parsing modificata in tal modo si chiama **tabella di parsing $SLR(1)$**, dove la $S$ sta per _simple_ e $1$ per 1 carattere di look-ahead. Per la grammatica di prima questa e':
![[tabella-di-parsing-slr1-1.png]]

Quindi $G \in SLR(1)$ e $G \notin LR(0)$.

## Definizione
> La **tabella di parsing $SLR(1)$** e' una tabella usata dai [[parser-lr|parser LR]] per risolvere il nondeterminismo su [[grammatiche-slr-1|grammatiche]] $SLR(1)$.
> Formalmente si compone:
> - _sulle colonne di $T \cup \{\$\} \cup NT$_;
> - _sulle righe degli stati dell'automa canonico $LR(0)$_;

## Riempimento
In realta' si tratta di una lieve variazione dell'algoritmo di riempimento della tabella di parsing $LR(0)$:
- per ogni stato $s$ dell'automa canonico $LR(0)$:
	- se $x \in T$ e $s \to^{x} t$ nell'automa $LR(0)$, inserisci _shift $t$_ in $M[s, x]$;
	- se $A \to \alpha . \in s$ e $A \neq S'$, inserisci _reduce $A \to \alpha$_ in $M[s, x]$ per tutti gli $x \in \text{Follow}(A)$[^1];
	- se $S' \to S. \in s$, inserisci _accept_ in $M[s, \$]$;
	- se $A \in NT$ e $s \to^{A} t$ nell'automa $LR(0)$, inserisci _goto $t$_ in $M[s, A]$;

Fondamentalmente l'obiettivo e' quello di **limitare l'uso della reduce solo a casi plausibili, ossia in cui la stringa appartiene al linguaggio**!

## Referenze

[^1]: e' qui il cambiamento! Nel caso del parser $LR(0)$ si aveva per tutti gli $x \in T \cup \{\$\}$
