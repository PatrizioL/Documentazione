# Javascript
JavaScript è un linguaggio di programmazione **interpretato** ad **alto livello** che viene utilizzato principalmente per aggiungere interattività e funzionalità dinamiche alle pagine web.

Interpretato perché viene letto ed eseguito riga per riga, senzo l'utilizzo di un compilatore

Alto livello, perché possiede una sintassi semplice ed un alto livello di astrazione del codice(funzioni, metodi,OOP, manipolazione del DOM, api)

Javascript é un linguaggio di programmazione lato client e quindi viene eseguito dal browser web

##### Altre caratteristiche di Javascript sono:

1. Tipizzazione debole:  La tipizzazione debole si riferisce alla capacità di un linguaggio di programmazione di eseguire automaticamente conversioni implicite tra tipi di dati in determinate situazioni

2. Tipizzazione dinamica:significa che le variabili non sono associate a un tipo di dato specifico e possono contenere valori di diversi tipi durante l'esecuzione del programma; ad esempio in Js possiamo riassegnare una variabile con dati di tipo diverso durante l'esecuzione

3. Funzioni di ordine superiore:le funzioni possono essere trattate come valori e passate come argomenti ad altre funzioni.

4. Gestione degli eventi: consentendo agli sviluppatori di creare funzioni che verranno eseguite quando si verificano determinati eventi, come un clic del mouse, il caricamento di una pagina o la pressione di un tasto.

5. Asincronia: JavaScript supporta l'esecuzione asincrona mediante il concetto di callback, Promises e async/await. Ciò consente di eseguire operazioni non bloccanti, come richieste di rete o operazioni di input/output, senza interrompere il flusso del programma. Questa caratteristica è cruciale per la gestione di operazioni lunghe o costose senza bloccare l'interfaccia utente.

5. Manipolazione delle stringhe: JavaScript offre potenti funzionalità per la manipolazione delle stringhe, come la concatenazione, la suddivisione, la sostituzione e la formattazione.

6. Moduli e librerie: Ci sono anche numerose librerie e framework JavaScript disponibili che forniscono funzionalità avanzate per lo sviluppo web, come React, Angular e Vue.js.

7. Supporto per la programmazione lato server: Ciò consente di utilizzare JavaScript per lo sviluppo di applicazioni web complete, comprese le operazioni di back-end.

8. Supporta la programmazione ad oggetti OOP

9. Manipolazione del DOM:

## Come aggiungere JS al file Html

### Interno
Embedded come contenuto di tag script, da inserire in fondo al body o nella head del file

### In linea
Come valore di un attributo html

### Esterno
Colegare un file js esterno mediante un tag scripr e specificare nel suo attributo src il path per il file js

##### Il metodo esterno e il migliore, ci permette di non violare il principio SOC(separation of concern)

## Locazioni di memoria in JS
Le locazioni di memoria in js sono di due tipi, **variabili** e **costanti**

### Variabili
Nelle locazioni di memoria variabili possiamo salvare qualsiasi tipo di dato ed puó cambiare, cioé la locazione di memoria variabile puó essere riassegnata

#### Dichiarare una variabile
Esistono 2 keyword

`let nome_variabile`: non posso dichiarare una varibile con lo stesso 2 volte

`var nome_variabile`: posso dichiarare piú volte una variabile con lo stesso nome

###### é meglio utilizzare let, per non rischiare di sovrascrivere inavvertitamente una variabile

#### Assegnare una variabile
Consiste nell'assegnare un dato ad una variabile
`let a = 1`

#### Inizializzazione variabile
Quando dichiariamo e assegnamo una variabile nello stesso statement


#### Riassegnare una variabile
Possiamo assegnare un nuovo dato ad una variabile gia assegnata, con un dato anche di tipo diverso (questo perché é tipizzazione dinamica), senza specificare il tipo di dato

### Locazioni di memoria costanti
Vengono dichiarate con la keyword const, non possono essere dichiarate e assegnate in due istruzioni diverse, ma va inizializzata in un unica istruzione/statement
`const  NOME_VARIABILE = 1`

## Tipi di Dato in JS
Possiamo dividere i tipi di dato in Js in due tipi, **primitivi** e **strutturali**

### Primitivi
In JavaScript, ci sono cinque tipi di dati primitivi:

1. Number: rappresenta i numeri, sia interi che decimali. Ad esempio: `let age = 25;`, `let price = 9.99;`.

2. String: rappresenta una sequenza di caratteri. Le stringhe sono racchiuse tra apici singoli o doppi. Ad esempio: `let name = "John";`, `let message = 'Hello, world!';`.

3. Boolean: (`true`) o (`false`). Ad esempio: `let isLogged = true;`, `let hasPermission = false;`.

4. Null: rappresenta un valore nullo o vuoto intenzionale. Ad esempio: `let data = null;`.

5. Undefined: rappresenta una variabile dichiarata ma non inizializzata o una variabile alla quale non è stato assegnato alcun valore. Ad esempio: `let value;`, `let result = undefined;`.

6. Symbol: é un tipo di dato che serve a generare un token utilizzato come identificatore univoco, creato tramite una funzione **Symbol()**, quando la utilizziamo JS crea un valore unico

i tipi di dati primitivi vengono assegnati per **valore e non per riferimento**. Ciò significa che quando assegni un valore primitivo a una variabile, viene creato una copia indipendente del valore.

Ecco un esempio di assegnazione di valori primitivi:

```javascript
let age = 25;           // Number
let name = "John";      // String
let isLogged = true;    // Boolean
let data = null;        // Null
let value;              // Undefined
```

I tipi di dati primitivi sono **immutabili**, il che significa che una volta assegnato un valore a una variabile di tipo primitivo, quel valore non può essere modificato direttamente. Tuttavia, è possibile assegnare nuovi valori alle variabili primitivie nel corso del programma.

### Dati strutturali
Sono gli array e oggetti

#### La differenza tra passaggio per valore e passaggio per riferimento
Riguarda il modo in cui i dati vengono passati tra le funzioni o assegnati a variabili in un linguaggio di programmazione.

##### Passaggio per valore tipico dei dati primitivi

Quando viene passato un dato per valore, viene effettuata una copia indipendente del valore originale e questa copia viene passata o assegnata a una nuova variabile.
Le modifiche apportate alla copia non influiscono sul valore originale.


##### Passaggio per riferimento tipico dei dati strutturali

Quando viene passato un dato per riferimento, viene passato il riferimento alla posizione di memoria in cui è memorizzato il valore. Non viene creata una copia indipendente del valore.
Le modifiche apportate al valore attraverso il riferimento influenzano direttamente il valore originale.

### La type coercion (coercizione di tipo)
è il processo **implicito** di conversione automatica dei tipi di dati in una determinata operazione o contesto in JavaScript. Si verifica quando un operatore o una funzione viene applicato a valori di tipi diversi.

La type coercion avviene nei linguaggi a tipizzazione debole

## Condizioni