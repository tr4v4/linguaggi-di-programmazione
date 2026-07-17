---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 19-09-2024 11:23:14
links:
  - "[[lecture-17092024110611|Lecture 17092024110611]]"
---
# Evoluzione dei linguaggi di programmazione
---
## Introduzione
I [[linguaggio-di-programmazione|linguaggi di programmazione]] hanno subito un'evoluzione in efficienza, espressività e quindi complessità incredibile nel corso di poco più di 50 anni:
- **anni 40-50**, preistoria: linguaggio macchina e [[assembly|assembly]]
- **anni 50-60**, primi linguaggio ad alto livello
	- _[[fortran|FORTRAN]]_ per calcolo numerico-scientifico, uso di notazione matematica in espressioni
	- _[[algol|ALGOL]]_ come linguaggio universale, per esprimere algoritmi: indipendenza dalla macchina, vicinanza con la notazione matematica, call by name, funzioni ricorsive, type systems, strutture dati (anche dinamiche)
	- _[[lisp|LISP]]_ per l'intelligenza artificiale (List Processor): funzioni su una certa classe di espressioni simboliche, ordine superiore (proto-paradigma funzionale)
	- _[[cobol|COBOL]]_ per applicazioni commerciali (record, archivi)
	- _[[algol-68|ALGOL 68]]_ linguaggio barocco, complessa progettazione ma contiene la nuova idea della struttura a blocchi
	- _[[simula|SIMULA]]_ da ALGOL primo linguaggio con classi e oggetti (proto-paradigma orientato a oggetti)
- **anni 70**:
	- _PL/I_ è FORTRAN + COBOL, primo linguaggio multi-uso
	- _[[pascal|PASCAL]]_ evoluzione e semplificazione di ALGOL W, didattico fino agli anni 80 (poi rimpiazzato da C e Java), portabile grazie a codice intermedio
	- _[[c|C]]_ programmazione di sistema (Unix), notevole successo
	- _[[prolog|Prolog]]_ usa esplicitamente la logica come base di un linguaggio di programmazione (primo [[linguaggio-di-programmazione-logico|linguaggio logico]])
	- _[[smalltalk|SmallTalk]]_ primo vero [[linguaggio-di-programmazione-orientato-a-oggetti|linguaggio orientato a oggetti]]
	- _[[ml|ML]]_ primo vero [[linguaggio-di-programmazione-funzionale|linguaggio funzionale]]
- **anni 80**:
	- _[[ada|ADA]]_ primo linguaggio real-time concorrente, notevole successo
	- _[[postscript|Postscript]]_
	- _[[c|C++]]_
	- _[[standard-ml|Standard ML]]_
	- _[[clp|CLP]]_ linguaggio logico con vincoli
- **anni 90** (nasce [[web|Web]]!):
	- _[[java|Java]]_ altamente portatile (elevata portabilità per JVM e ByteCode!), object-oriented, programmi spediti su rete
	- _[[perl|PERL]]_ linguaggio per text-processing
	- _[[html|HTML]]_
	- _[[xml|XML]]_
- **anni 2000**: service-oriented computing, paradigma che usa i servizi come unità di base di computazione per progettare applicazioni integrate di business
	- _[[wsdl|WSDL]]_
	- _[[ws-bpel|WS-BPEL]]_
	- _[[jolie|Jolie]]_ sviluppato a Bologna!

In poche parole il grande cambiamento è stato il seguente:
- anni 50-60: compilazione dei programmi per ottenere efficienza; connessione diretta fra hardware e linguaggi (integers, reals, goto); "programmers cheap, machines expensive -> keep the machine busy"
- oggi: compilazione di programmi costruiti in modo efficiente; connessione diretta fra software design e linguaggio (encapsulation, records, ereditarietà, dichiaratività); "programmers expensive, machine cheap -> keep the programmer busy"

## Referenze