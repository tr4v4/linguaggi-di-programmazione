---
tags:
  - category/note
  - status/finished
  - topic/linguaggi-di-programmazione
date: 23-09-2025 17:10:09
links:
  - "[[lecture-09042025110710|Lecture 09042025110710]]"
---
# Tipo ricorsivo
---
## Introduzione
> I [[tipi-di-dato|tipi di dato]] [[tipi-composti|composti]] **ricorsivi** sono _tipi che nella loro definizioni contengono loro stessi_.

Anche se da un punto di vista astratto/logico non hanno alcun senso[^1], i tipi ricorsivi sono _estremamente utili per definire [[struttura-dati|strutture dati]] modificabili dinamicamente_, come [[lista|liste]], [[albero|alberi]], ecc...

Si esprimono, di solito, attraverso i [[tipo-prodotto|tipi prodotto]]. Ma si possono anche esprimere attraverso i [[tipo-somma|tipi somma]] (per evitare di dover scrivere il `NULL` per indicare la fine).

Esempio in [[java|Java]] con le `sealed` classes:
```Java
sealed class IntList permits IntList.Cons, IntList.End {
	static class Cons extends IntList {
		int n; IntList cons;
		Cons( int n, IntList cons ) {…}
	}
	static class End extends IntList {
		End() {}
	}
}

IntList l = new IntList.Cons(1,
			new IntList.Cons(2,
			new IntList.Cons(3,
			new IntList.End())));
```

## Referenze

[^1]: manca il caso base!
