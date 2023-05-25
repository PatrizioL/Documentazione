
### Definizione html
Html5 (**Hyper text markup language**) é un linguaggio di markatura per **hyper-texts**, serve a creare la struttura a blocchi base(*una sorta di scheletro delle pagine web*) e ad assegnare un significato **semantico** all hyper-text, grazie all'utilizzo di marcatori/etichette chiamate **tag**

Il browser riceve il documento html da un server e lo **reinderizza**(lo mostra al client).

**Hyper-text** é un testo in formato digitale con al suo interno dei **link**(porzioni di testo o altri elementi, es immagini, bottoni ecc che funguono da collegamento con altre risorse), che lo possono collegare a posizioni differenti dello stesso testo, pagine differenti dello stesso sito o a pagine web di siti esterni

### Definizione di web
Il web é una rete d'informazioni testuali che sono stati traferiti in formato digitale e collegati tra loro tramite *link*; quindi una rete di **hyper-texts**

### Principio SOC
**Separation of concerns**, ovvero la separazione dei compiti dei linguaggi


## Sintassi html5

La sintassi in html5 si basa sull'uso dei **tag** che sono delle etichette, che applicato ad elemto testuale principalmente, ma in generale a tutti gli elementi di una pagina web sono in grado di definirne la struttura base e gli assegnano anche un significato semantico che viene poi interpretato dal browser al fine di ottimizzare il punteggio *SEO*

### Elemento html
In HTML, un **elemento** è un'unità fondamentale di un documento HTML, che definisce la struttura e il contenuto del documento. Un elemento HTML è costituito da un **tag** HTML, che contiene il nome dell'elemento, gli **attributi** e il contenuto dell'**elemento**.

I tag possono essere **aperti/chiusi** questi tipi di tag vanno usati insieme e in quel caso al loro interno va posizionato il *contenuto*(l'elemto htm in questo caso sará costituito da tag di apertura e chiusura) o possono essere **self-closing** tag e non aver bisogno di un contenuto in questo caso l'elemento html é costituito da un solo tag

Un **tag HTML** è un elemento utilizzato per definire la struttura base, il contenuto e il comportamento di un documento HTML

Un documento html5 viene sempre aperto con una con dichiarazione al browser `<!DOCTYPE html>` indica al browser il tipo di file

#### Tag <html>
Il primo tag che viene inserito é il tag `<html>` che abbraccia tutti gli altri tag, all'interno di questo tag troviamo due tag principali il tag `<body>` e il tag `<head>`

1. ##### head
Contiene le meta informazioni(*In informatica, una meta informazione è una informazione che descrive o fornisce informazioni su altre informazioni*) e link di collegamento a risorse esterne al nostro file, *ció che si trova all'interno di questo tag non é visibile al client*

Esempio di meta informazioni, sono il nome dell'autore della pagina web, una descrizione della pagina, il tipo di carattere usato o le parole chiave, queste sono per l'appunto informazioni/dati che vanno a descrivere il contenuto della pagina web che é sua volta un informazione/dato

2. ##### body
Contiene invece tutto il contenuto che vogliamo rendere visulizzabbile al client

#### Attributi html
In HTML, gli attributi sono utilizzati per definire le proprietà degli elementi HTML. Gli attributi forniscono informazioni aggiuntive sugli elementi HTML, come il colore del testo, la dimensione del carattere, l'URL di un'immagine, e così via.

* Devono essere sempre inseriti nel **tag di apertura**

* Sono costituiti da coppie **chiave-valore**, dove la chiave é il nome dell'attributo e il valore puó essere anche piu di uno

* Gli attributi possono essere specifici per il tag o globali, come **class**, **style** , **id** e **title**

* title fa apparire un toltip con un messaggio per il client

#### Principali tag
* `<p>` tag paragrafo, per inserire contenuto testuale generico, che non costituisce un titolo

* `h1,...,h6` tag per i titoli

* `strong` ed `em` significato semantico al testo, lo evidenziano specificando alla seo un importanza maggiore

* `div` e `span` tag contenitori generici il primo ha comportamento **bloccante**, il secondo comportamento **inline**

Il comportamento **"bloccante"** del tag "div" significa che il contenuto all'interno del tag "div" viene visualizzato come un blocco separato all'interno della pagina web. Ciò significa che qualsiasi contenuto HTML che segue il tag "div" viene visualizzato su una nuova riga.

* `img` per l'iserimento delle immagini, importante per la seo attributo *alt*

* `a` serve a creare un altro *link*, quando vado a specificare il percorso del link, se é interno uso **./** il punto in informatica indica la *posizione corrente*
l'attributo **target** ci permette quando clicchiamo sul link di essere reindirizzati ad una nuova pagina se inseriamo il il valore *_blank*
Il contenuto del tag link puó essere qualsiasi cosa anche un immagine, una card ecc

##### tag per la creazione di liste

* tag `ul` per la creazione di una lista indeterminata, al suo interno si usano  tag `li` per gli elementi della lista, come list item  possiamo avere anche un altra lista **ul**, inserendola come contenuto di uno dei tag li

* tag **dl** lista determinata, con al suo interno tag **dt**
e tag **dd** il primo tag é una sorta di titolo della descrizione in dd successiva

* tal **ol** per liste ordinate, sempre con tag **li** per i vari elementi della lista

* tag **address** per l'autore di un articolo, tag **time** per una data

### tag form
Questo tipo di tagconsente agli utenti di inserire e inviare dati al server web, per registrarsi, login, iscrizioni a news letter o ad esempio anche la ricerca su motere di ricerca é un tag form, *tipo google*

* l'attributo **action**, specifica l'URL del server web a cui i dati del form devono essere inviati.

* l'attributo **method** è un attributo dell'elemento HTML "form" e specifica il metodo HTTP da utilizzare per inviare i dati del form al server web.

L'attributo "method" può assumere uno dei due valori possibili: **"get"** o **"post"**.

Il metodo **"get"** è particolarmente adatto per i form di ricerca

Il metodo **"post"** è spesso utilizzato per inviare dati al server per l'elaborazione o l'inserimento nel database.

#### tag all'interno del tag form

* tag **input** é un self-closing che fa apparire un campo d'input al client, l'attributo *type* definisce il tipo di dato che é possibile inserire all'interno del campo d'input

Se il type é number possiamo utilizzare gli attributi, *max*, *min*, *step* e *value*. Che specificano il minimo valore possibile il massimo valore posssibile, incremento/decremento del valore e il value il valore di default

Attributo *placeholder* é un esempio di ció che richiede il campo

Attributo **name** molto importante quando si lavoro con linguaggi lato server, perché all'interno della richiesta i dati sono salvati in coppie chiave-valore, in cui il valore inserito nell'attributo name costituisce la chiave per accedere a questi valori

###### type del tag input

type **radio** serve per rendere due tag input mutualmente esclusivi come maschio e femmina, in questo caso inserire anche l'attributo value con valore m o f, affinche il dato sia effettivamente inviato al server in quanto l'utente non inserisce m o f clicca solo sul bottone

type **datetimelocal**

type date

type **checkbox** valori multipli da checckare, con l'attributo checked posso pre-ckeccare l'accettazione della pryvacy, il client troverá la casella giá checcata

* tag label é un etichetta che viene fatta associare al campo d'input tramite al valore dell'attributo *for* che deve corrispodere al valore dell'attributo *id* del tag input

* tag textarea é un tipo di tag input che ci consente d'inserire del testo, con gli attributi *rows* e *col* ne definisco la dimensione

###### tag per l'invio di dati
Abbiamo bisogno di creare un bottone su cui cliccare per inviare i dati possiamo utilizzare un tag **input** o **button**

* Il type puó essere di tre tipi *reset* resetta il form, in questo caso poi va aggiunto un atro bottone per l'invio dei dati

* **submit** che invia i dati

* **button** da solo lo style al bottone

* attributo *autofocus* e *disable*, il primo per evidenziare il bottone, disable invece rende il bottone non cliccabile

###### tag select
utilizzato per creare un menu a tendina o una lista di opzioni tra cui l'utente può scegliere una o più voci.

* utilizzare il tag **option** che indica le possibili opzioni, con il valore da inviare al server nel campo *value*

* tag orgroup per creare un indice nel menu a tendina

## Tag semantici
Hanno un comportamento **bloccante** come un tag div, la differenza é che hanno un valore semantico importante per la *SEO*(ottimizzazione dei motori di ricerca)

* "header": utilizzato per il contenuto in testa alla pagina o di una sezione;

* "nav": utilizzato per definire la navigazione principale della pagina;

* "article": utilizzato per definire un contenuto autonomo, come un articolo o una notizia;

* "section": utilizzato per raggruppare contenuti correlati;

* "aside": utilizzato per definire contenuti collaterali, come annunci pubblicitari o menu di navigazione;

* "footer": utilizzato per il contenuto in fondo alla pagina.

* "figure": utilizzato per inserire le immagini, al suo interno trova posto il tag img e il tag figcaption per la descrizione delle immagini

* "main": contenuto unico di ogni pagina é principale di ogni pagina, al suo interno inseriamo tutti i tag tranne *navbar* e *footer* che si ripetono sulle altre pagine del sito

### Struttura Html di una pagina web

All'interno del tag body, inseriamo:

* tag nav per la navigazione

* tag header intestazione pagina

* tag main all'interno del main inseriamo il contenuto principale ed unico delle pagina che quindi non si ripete in altre pagine del sito

* **Section** e all'interno delle section gli **article**

* possiamo creare una sezione contatti e utilizzare i tag **fieldset** per racchiudere i campi d'input affini tra di loro ad esempio dati personali, e un tag **legend** che funge da intestazione della sezione del form
