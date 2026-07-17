---
tags:
  - "#category/note"
  - "#status/finished"
  - topic/programmazione
  - topic/linguaggi-di-programmazione
date: 20-09-2023 19:23:34
links:
  - "[[lecture-20092023091613|Lecture 20092023091613]]"
  - "[[lecture-09102023151504|Lecture 09102023151504]]"
  - "[[lecture-19022025111150|Lecture 19022025111150]]"
---
# Dichiarazione
---
## Definizione
> La **dichiarazione** è quel processo grazie al quale viene comunicato al [[compilatore|compilatore]] l'[[identificatore|identificatore]] e il suo _tipo_. Piu' precisamente, e' il meccanismo (implicito o esplicito) col quale si crea un [[binding|binding]] in un [[ambiente|ambiente]].

Grazie alla dichiarazione, infatti, il compilatore è in grado di **allocare sufficiente memoria a contenere i valori utilizzati dal programma**: _scannerizza_ tutte le dichiarazioni all'interno del codice per poter definire a priori quanto occuperà in [[ram|RAM]] il programma (nella sezione dedicata ovviamente ai _dati_).

Ogni **tipo** di identificatore occupa un determinato volume di spazio in memoria, e in assembly esistono istruzioni differenti a seconda dei tipi di dati. Per esempio l'istruzione `ADD` si usa per sommare due valori reali, `ADDI` per due interi: queste hanno [[clock|cicli di clock]] differenti, quindi un efficienza diversa.

In breve potremmo dire che la dichiarazione serve a:
- instradare il programma su un set di istruzioni eseguibili per quell'identificatore;
- ottimizzare l'uso del processore per quel tipo di dato specificato;

<u>Attenzione</u>: la dichiarazione di un identificatore ha una valenza definita dal suo [[scope|scope]].

## Referenze