---
tags:
  - category/note
  - status/finished
  - topic/logica-per-informatica
  - topic/linguaggi-di-programmazione
date: 06-11-2023 19:14:57
links:
  - "[[lecture-31102023161330|Lecture 31102023161330]]"
  - "[[lecture-02112023091408|Lecture 02112023091408]]"
  - "[[lecture-08112023131119|Lecture 08112023131119]]"
  - "[[lecture-19092024125624|Lecture 19092024125624]]"
---
# Semantica
---
## Introduzione
> La **semantica** di un linguaggio è la parte della linguistica che attribuisce e studia il _significato delle parole_, degli _insiemi di parole_, delle _frasi_ e dei _testi_, e quindi la relazione tra segni ([[sintassi|sintassi]]) e significato.

Per analizzare la correttezza di una frase da un punto di vista semantico è necessario:
1. _sapere a quale linguaggio la frase appartiene_;
2. _su quale linguaggio basarmi per dare significato_ (tale linguaggio dev'essere noto, cioè non dev'essere a sua volta spiegato).

Nel _linguaggio naturale_ questo è il modo in cui funziona la traduzione: per capire la semantica di una frase inglese c'è bisogno di un traduttore che la traduca in italiano di cui già nativamente comprendiamo la semantica.

Nel _linguaggio artificiale_ questo avviene quando si vuole eseguire uno script scritto in un linguaggio di programmazione che dev'essere semanticamente compreso dal calcolatore attraverso un traduttore ([[interprete|interprete]] o [[compilatore|compilatore]]).

Nel contesto della logica la **semantica è una [[funzione-matematica|funzione]] che associa a ogni [[connotazione|connotazione]] una [[denotazione|denotazione]] in un [[dominio-di-interpretazione|dominio di interpretazione]] fissato**.

Si considerino:
- [[connotazione|Connotazione]] --> parte di una frase corretta sintatticamente
- [[denotazione|Denotazione]] --> significato attribuito a una connotazione
- [[dominio-di-interpretazione|Dominio di interpretazione]] --> [[insieme|insieme]] dei possibili significati
- [[sintassi|Sintassi]] --> insieme di tutte le connotazioni

In poche parole, se scomponiamo una frase in un insieme $A$ di _connotazioni_, corrette sintatticamente, e abbiamo un insieme $B$ _dominio di interpretazione_, la funzione _semantica_ associa ogni elemento di $A$ alla sua [[immagine-di-funzione|immagine]] _denotazione_ in $B$ ([[definizione-di-essere-sottoinsieme|sottoinsieme]] del dominio di interpretazione)[^1][^2].

### Rapporto con sintassi
> La sintassi è l'insieme delle regole del regno della connotazione; un esempio di sintassi usata in logica è la [[logica-proposizionale|logica proposizionale]].
> La semantica è l'insieme delle regole del regno della denotazione; un esempio di semantica usata in logica è la [[semantica-classica|semantica classica]], da cui deriva la [[logica-classica|logica classica]].

## Conseguenze
Punti di vista differenti sul mondo, non per forza giusti o sbagliati, portano alla costruzione di differenti semantiche, quindi a _diversi significati associati a stesse connotazioni_.

Dalle semantiche si formano le logiche su cui sono basate le matematiche: **il ruolo della semantica è fondamentale**. 

## Tipologie
- [[semantica-intesa|Semantica intesa]], detta anche _naturale_ o _principale_
- [[semantica-classica|Semantica classica]]

## Referenze
[^1]: la semantica non è [[funzione-suriettiva|suriettiva]]! Non potrebbe associare infatti tutti i significati denotativi a una connotazione
[^2]: è lo stesso rapporto _dicotomico_ che si presenta tra **bit** e **significato dei bit**, per cui _[[ram-definizione|è il programma a dare un significato ai dati]]_