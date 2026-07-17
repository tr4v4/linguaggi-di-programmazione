---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 08-09-2025 16:27:40
links:
---
# Relazione tra linguaggi LL(k) e LR(k)
---
## Introduzione
Abbiamo visto il diagramma che mette in [[relazione-tra-grammatiche-ll-k-e-lr-k|relazione]] le [[grammatiche-ll-k|grammatiche]] $LL(k)$ con [[grammatiche-lr-k|quelle]] $LR(k)$. Ma _dal punto di vista dei linguaggi, questo si semplifica moltissimo_!

Ricordando che
- un [[linguaggio-libero-deterministico|linguaggio e' libero deterministico]] se accettato da un [[dpda|DPDA]] per stato finale,
- ogni [[linguaggio-regolare|linguaggio regolare]] e' generato da una [[grammatiche-ll-1|grammatica]] di classe $LL(1)$,
- esistono linguaggi regolari che non sono $LR(0)$ (come $L = \{a, ab\}$[^1]),

possiamo enunciare i seguenti teoremi.

## Teoremi
### Generazione
> 1. un linguaggio e' libero deterministico $\iff$ e' [[linguaggio-generato|generato]] da una grammatica $LR(k)$, per qualche $k \geq 0$;
> 2. un linguaggio e' libero deterministico $\iff$ e' generato da una [[grammatiche-slr-1|grammatica]] $SLR(1)$;
> 3. i linguaggi generati da grammatiche $LL(k)$ sono strettamente contenuti nei linguaggi generati da grammatiche $SLR(1)$ (ossia i liberi deterministici), per qualche $k \geq 0$.

![[relazione-linguaggi-llk-lrk.png]]

Chiaramente il punto piu' incredibile e' il secondo: **i linguaggi liberi deterministici corrispondono a quelli generati da grammatiche $SLR(1)$**.

Di conseguenza, **se $G \in LR(k)$, allora esiste $G' \in SLR(1)$ [[grammatiche-equivalenti|equivalente]], ma $G'$ puo' essere molto piu' complessa di $G$**!

### Operazioni
> Valgono le seguenti proposizioni:
> - _l'unione di due linguaggi $LL(1)$ puo' non essere $LL(1)$_;
> - _l'unione di due linguaggi $LR(0)$ puo' non essere $LR(0)$_;
> - _la concatenazione di due linguaggi $LL(1)$ puo' non essere $LL(1)$_.

## Referenze

[^1]: perche' e' _finito_ e _non_ gode della _prefix-property_!
