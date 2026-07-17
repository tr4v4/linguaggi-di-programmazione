---
tags:
  - category/note
  - status/finished
  - topic/programmazione
  - topic/linguaggi-di-programmazione
date: 03-12-2023 16:34:12
links:
  - "[[lecture-29112023092601|Lecture 29112023092601]]"
  - "[[lecture-08052025131742|Lecture 08052025131742]]"
  - "[[lecture-14052025105842|Lecture 14052025105842]]"
---
# Classe
---
## Introduzione
> Per **classe** in informatica, nell'ambito della [[oop|programmazione a oggetti]], si intende un [[tipi-di-dato|tipo di dato]] che _specifica come i suoi elementi, detti [[oggetto|oggetti]], possono essere creati e usati_.

Storicamente il primo [[linguaggio-di-programmazione|linguaggio di programmazione]] ad aver introdotto il concetto di classe è stato [[simula67|Simula67]].

Prima delle classi esistevano comunque gli oggetti: ogni oggetto specificava esplicitamente la proprio implementazione, un po' come in [[c|C]] con le `struct` e le funzioni. Le classi sono nate come canovaccio, come modello di implementazione di riferimento per oggetto che hanno stessi campi e stessi metodi in comune (ma comunque con stati distinti!).

<u>Nota bene</u>: le classi non sono per forza dei tipi! Dipende dalla loro implementazione.

## Composizione
Una classe si compone di:
- _attributi_/campi, ovvero le [[identificatore|variabili]] della classe
- _metodi_, le [[funzione-informatica|funzioni]] della classe, tra cui il _[[costruttore|costruttore]]_

In poche parole **la classe estende il concetto di [[struttura-dati|struttura]]**, racchiudendo in un unico costrutto sintattico la _definizione dei valori_ (attributi) e delle _operazioni attuabili su quei valori_ (metodi).

### Esempio
```cpp
class Rectangle {
	public:
		int base;
		int altezza;

		int area() {
			return base*altezza;
		}
		int perimetro() {
			return (base+altezza)*2;
		}
}

int main() {
	Rectangle r;
	r.base = 10;
	r.altezza = 30;
	cout << r.area() << "\t" << r.perimetro() << endl;
	
	return 0;
}
```

## Implementazione
Generalmente, le classi nella loro essenza contengono solo il codice dei metodi invocati dagli oggetti; mentre lo stato e' salvato all'interno degli oggetti.
![[classi-e-oggetti.png]]

Attraverso il **`this` o il `self` nei metodi delle classi si fa riferimento all'oggetto che li ha invocati**. Infatti tali metodi ricevono implicitamente l'oggetto che li ha invocati.

<u>Nota bene</u>: gli attributi `static` sono invece campi della classe!

## Tipaggio
### Sottotipaggio
Nella [[oop|OOP]] il [[sottotipaggio|sottotipaggio]] vede le [[classe|classi]] come dei [[tipi-di-dato|tipi di dato]] cui abitanti sono gli [[oggetto|oggetti]] di quella classe. Questa relazione e' anche una **relazione di [[compatibilita-di-tipo|compatibilita' di tipo]]**!

Per quanto riguarda l'[[equivalenza-di-tipo|equivalenza di tipo]], in un sistema [[equivalenza-strutturale|strutturale]] avverrebbe che l'equivalenza si ha tra $S$ e $T$ (con $S <: T$) se c'e' una corrispondenza tra i loro elementi; ma di solito si preferisce un sistema [[equivalenza-nominale|nominale]] che _aiuta a prevenire possibili equivalenze accidentali_!

Verificando l'equivalenza, tuttavia, si pone un livello si' di sicurezza, ma che pone delle limitazioni: **l'utente deve dichiarare le relazioni di sottotipaggio previste tra i tipi**.

Per esempio, io potrei dichiarare una classe `Animal` e successivamente una classe `Dog` senza esplicitare che `Dog <: Animal`: semplicemente `Dog` avra' gli stessi campi e metodi di `Animal` e qualcosa in piu'. Ma a quel punto, il sistema dei tipi, per verificare un'istruzione come la seguente:
```C++
Animal c = new Dog();
```
dovrebbe usare un sistema strutturale e confrontare se tutti i campi e metodi di `Animal` ci sono anche in `Dog`. Se pero' ora _creassi la classe `House` che ha la stessa struttura di `Animal`, potrebbe capitare che `House` sia considerato un valido sottotipo di `Animal`_! Per evitare cio', si preferisce quindi usare l'equivalenza nominale. Ma `Dog != Animal`! Quindi devo esplicitare che `Dog <: Animal` e il gioco e' fatto.

### Interfaccia
Vedere le classi come tipi di dato potrebbe essere fuorviante: i tipi di dato definiscono strutture, e al massimo operazioni (con gli [[adt|ADT]]); _una classe invece definisce dei vincoli di visibilita', mantiene lo stato e contiene anche le implementazioni delle operazioni_.

#### Sottotipaggio classe-interfaccia
Per tale motivo, di solito, consideriamo sempre una classe accompagnata dalla sua **[[interfaccia|interfaccia]], che rappresenta la vista pubblica di quella classe**. Di fatto, quindi, la classe implementa tale interfaccia.

#### Sottotipaggio interfaccia-interfaccia 
Nella realta', quando diciamo che `A` implementa l'interfaccia `C`, stiamo presupponendo l'esistenza di un'altra interfaccia `B`, quella effettivamente implementata da `A`, che **estende** l'interfaccia `C`.

In altri termini, il sottotipaggio c'e' anche tra interfacce! Questo si chiama appunto **estensione**.

#### Sottotipaggio classe-classe
E infine, quando applichiamo il sottotipaggio a livello di classi, _stiamo applicando la stessa estensione interfaccia-interfaccia, ma coprendo anche lo stato, i vincoli di incapsulamento e l'implementazione dei metodi delle classi_. Questa relazione prende il nome di [[ereditarieta|ereditarieta']].

## Metodi statici
Sono i metodi "di classe", ma si chiamano cosi' perche' **il [[compilatore|compilatore]] puo' risolverli staticamente**, implementando di fatto [[early-binding|early binding]] (o [[static-dispatch|static dispatch]] visto che siamo in OOP)!

E' per questa ragione che questi **[[sottotipaggio|non possono essere sovrascritti]], ma solo [[overloading|sovraccaricati]]**.

E' possibile anche staticamente mascherare i metodi statici.

## Utilità
Oggigiorno le classi sono il _mattone elementare per costruire grossi programmi_.

## Referenze
- [[ereditarieta|Ereditarietà]]
- [[classe-astratta|Classe astratta]]
- [[costruttore|Costruttore]]