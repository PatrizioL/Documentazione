# CSS

Il CSS (Cascading Style Sheets)  è un linguaggio di stile utilizzato per definire l'aspetto,  la posizione degli elementi all'interno della pagina, la gestione dei layout e molto altro.

### Metodi per utilizzare il css in un documento Html

1. #### Esterno
Si utilizza un file css esterno e lo di collega al file html grazie al tag link posizionato nel tag head

2. #### Interno
Utilizzando il tag style nell'head del documento html

3. #### In linea
Tramite l'attributo style d'assegnare al tag dicui si vuole modificare lo stile

**N.B** conviene sempre utilizzare il primo metodo, il file esterno di css, gli altri metodi abbassano il punteggio SEO del sito, violano anche il principio DRY (non ripeterti)


## Sintassi CSS
Un foglio di style css si compone di una serie di **regole css** che sono interpretate dal browser e poi applicate all'elemento html a cui si riferiscono

#### Regola CSS
Una regola css si compone di due parti un **selettore** e una o piú **dichiarazioni**, a sua volta ogni dichiarazione é costituita da una coppia **chiave-valore**
* *le dichiarazioni vengono inserite all'interno di parentesi graffe*
* ogni dichiarazione deve terminare con un **;**
```
selettore {
  proprietà: valore;
  /* altre dichiarazioni di stile */
}
```

* Il *Selettore* seleziona l'elemento o gli elementi a cui applicare lo stile

* La *dichiarazione* é costituita da una coppia chiave-valore in cui la chiave é una **proprietá css** a cui assegnamo uno o piú valori di diverso tipo a seconda dell'esigenza

##### Selettori css piú utilizzati

- **\*** *selettore universale* seleziona tutti gli elementi html

- **Element type** seleziona tutti gli elementi con lo stesso tag
Si possono anche selezionare piú element type insieme concatenandoli con una **,**

- **id** seleziona un elemento unico `id="selettoreId"` `#selettoreId{}"`

- **class** seleziona tutti gli elementi con la stessa classe `class=selettoreClass` `.selettoreClass{}`
*si puó concatenare un element type al selettore classe `p.selettoreClass`*

Possiamo assegnare molteplici classi ad elemento html, specificandole come valori dell'attributo class, semparando poi questi valori/classi dell'attributo con uno spazio

- **selettore nipoti** `ul li` permette di selezionare tutti i tag `li` all'interno di un tag genitore `ul` anche se non sono figli diretti, basta che siano annidati al suom interno

- **selettore figli diretti** `div>p` seleziona solo i tag p figli diretti di un tag div

### Principi di cascata, specificitá ed ereditarietá

Queste regole sono importanti per determinare, quale selettore css si applica ad un elemento html che viene selezionato da piú selettori css

1. #### Principio di specificitá

Ogni selettore che targetta un elemento html ha un proprio **grado di specificitá** che viene espresso da un volore *numerico*, il selettore con il grado di specificitá piú alto per quel elemento sará quello che verra applicato.

*https://www.w3schools.com/css/css_specificity.asp*

2. #### Principio d'ereditarietá

Nel contesto del CSS, **l'ereditarietà** si applica a *tutti gli elementi html annidati o discendenti di un elemento html a cui è stato applicato uno stile.*

Quindi gli elementi discendenti dall'elemento a cui viene apllicato uno stile da un selettore verranno selezionati da quel selettore a loro volta

**N.B** Ci sono delle **eccezioni** Non tutti i tag html posso ereditare le proprietá css da un parent, ne tutte le proprietá possono essere ereditate

3. #### Principio della cascata

Quando un elemento html é targhettato da uno o piú **regole css** con la **stessa specificitá**, lo style che viene apllicato all'elemento html sará quello della **regola css** tra quelle che lo selezionano, scritta per **ultima** nel *codice sorgente*

**Codice sorgente**:  è il **testo** scritto dagli sviluppatori di software che contiene le istruzioni per creare programmi e applicazioni.

**N.B** Se un elmento html é targhettato/selezionato da piú regole css, che si trovano ad esempio una nel **css interno** ed una in quello **esterno**; la regola che verrá applicata all'elemento html a **paritá di specificitá**, dipende non dal codice sorgente del foglio esterno di css, ma dal codice sorgente del file html, dipende se il link di collegamento al file css viene prima o dopo nel codice sorgenge del tag style del css interno.

Infatti il css inline ha una specificitá altissima é vince su entrambi

4. ##### !Important

Aggiungendo quest'istruzione ad una regola css, questa regola prende il sopravvento sulle altre regole che targettano l'elemento.
*Utile quando si lavoro con codice css importato*


## Unita di misura del css
Le unità di misura più comuni utilizzate in CSS sono le seguenti:

Le unità di misura più comuni utilizzate in CSS sono le seguenti:

1. **Pixel (px)**: Il pixel è l'unità di misura più comune utilizzata in CSS. Un pixel rappresenta un singolo punto su uno schermo. È una misura fissa e non si adatta in base alle dimensioni dello schermo.

2. **Percentuale (%)**: La percentuale è una misura relativa che fa riferimento a una percentuale della grandezza di un elemento genitore. Ad esempio, se si imposta la larghezza di un elemento al 50%, esso occuperà la metà della larghezza del suo elemento genitore.

3. **Em (em)**: L'em è una misura relativa che fa riferimento alla dimensione del carattere dell'elemento genitore. Ad esempio, se si imposta il valore di `font-size` di un elemento a 1.5em, esso avrà una dimensione del carattere pari a 1,5 volte la dimensione del carattere del suo elemento genitore.

4. **Rem (rem)**: Il rem è una misura relativa simile all'em, ma fa riferimento alla dimensione del carattere dell'elemento radice (di solito l'elemento `html`). A differenza dell'em, il rem non dipende dai livelli di annidamento degli elementi.

5. **Viewport Units (vw, vh, vmin, vmax)**: Le unità viewport sono relative alle dimensioni dello schermo (viewport) dell'utente. `vw` rappresenta l'1% della larghezza del viewport, `vh` rappresenta l'1% dell'altezza del viewport, `vmin` rappresenta l'1% del minimo tra larghezza e altezza del viewport, mentre `vmax` rappresenta l'1% del massimo tra larghezza e altezza del viewport.

Oltre a queste, ci sono anche altre unità di misura come `rem`, `ch`, `ex`, `pt`, `cm`, `mm`, `in`, `pc` che vengono utilizzate in casi specifici o per scopi particolari. La scelta dell'unità di misura dipenderà dal contesto e dalle esigenze specifiche del progetto.

### Unitá di misura per i colori
In CSS, le unità di misura utilizzate per i colori sono principalmente tre:

1. **Valori hexadecimal**: I colori possono essere definiti utilizzando il sistema esadecimale, che rappresenta i colori con una combinazione di sei cifre esadecimali. Ad esempio, il colore bianco è rappresentato come #FFFFFF e il colore nero come #000000.

2. **Valori RGB**: I colori possono anche essere definiti utilizzando il modello RGB (Red, Green, Blue). I valori RGB consistono in tre numeri che rappresentano l'intensità dei colori rosso, verde e blu nell'intervallo da 0 a 255. Ad esempio, il colore rosso puro è rappresentato come rgb(255, 0, 0).

3. **Valori RGBA**: Simile al sistema RGB, il sistema RGBA (Red, Green, Blue, Alpha) consente di specificare anche il livello di trasparenza del colore. L'opacità è rappresentata da un valore compreso tra 0 e 1, dove 0 indica la completa trasparenza e 1 indica l'opacità totale. Ad esempio, rgba(255, 0, 0, 0.5) rappresenta un colore rosso semi-trasparente.

Inoltre, CSS supporta anche altri formati di colore come i nomi dei colori predefiniti (ad esempio "rosso", "blu", "verde") e valori HSL (Hue, Saturation, Lightness) che utilizzano l'intensità del colore, la saturazione e la luminosità per rappresentare il colore.

È possibile utilizzare queste diverse unità di misura dei colori in CSS per specificare il colore degli elementi del tuo sito web.

## Poprietá css principali

### Position

Questa proprietá permette di cambiare la posizione di un elemento, viene utilizzata per **micro-spostamenti** come il box-model

* il valore di **default é static**, l'elemento sará posizionato il alto a sinistra sulla finestra del browser.

* **relative** permette di cambiare la posizione di un elemento rispetto alla sua posizione static, possiamo usare le proprietá *top,left,right,bottom*

* **absolute** simile a relative ma la posizione dell'elemento sará rispetto all'elemento parent, importante che il parent abbia *position relative* altrimenti l'elemto con position abasolute si posiziona rispetto al all'elemto *body*

* **fixed** viene posizionato in posizione fissa rispetto alla finestra del browser, quindi anche scrollando l'elemento rimane visibile nella stessa posizione

* **sticky** combina le caratteristiche di position: **relative** e position: **fixed**, consentendo a un elemento di muoversi liberamente fino a un punto di scorrimento specifico, dopodiché rimane bloccato nella sua posizione.

Questo non é un valore della proprietá position ma una proprietá as se stante, **z-index**(posizione sull'asse z) di default questa proprietá vale 1, é importante per determinare quale elemento viene visualizzato nel caso due elementi html si **sovrappongano**, di default verra visualizzato quello che é scritto per ultimo nel codice sorgente html

Possiamo cambiare questo comportamento assegnando agli elementi un valore dell proietá z-index, quello che con valore maggiore si sovrapporrá all'altro

**N.B** due elementi possono sovrapporsi solo se hanno entrambi *position relative*

### Box Model

Il "box model" è un concetto fondamentale nel CSS che descrive come gli elementi HTML sono rappresentati come **"scatole"** rettangolari nel layout della pagina. Queste scatole sono composte da quattro componenti principali: **content (contenuto), padding (riempimento), border (bordo) e margin (margine)**.

Questo modello **box model**, descrive come questi elementi sono *reinderizzati* sulla pagina

**N.B** Di default quando assegnamo delle dimensioni ad un elmento html quello che dimensioniamo é solamente il **content**

Per cambiare questo comportamento cambiare il valore della proprietá **box-sizeing** dal valore di default **content-box** a **border-box**, cosi le dimensioni che assegnamo comprendono anche il padding e il bordo dell'elemento


##### Proprietá del box model

Possiamo modificare le componenti dell'elemento html, con le proprietá, *padding, border, margin*, la manipolazione di queste proprietá ci permette di fare delle micro-correzioni nel layout
`padding:1px 1px 1px 1px`
il padding dell'elemento verrá modificato a partire da top, in senso orario

**N.B** per arrontondare i bordi fino rendere il box una circonferenza usare la proprietá *border-radius*


## Flexbox (*Insieme proprieta css per la creazione di layout*)

Flexbox è un **modulo**(*un insieme di proprietá css*) del CSS che fornisce un sistema flessibile per la disposizione degli elementi all'interno di un contenitore

è possibile definire un contenitore principale/genitore (**flex container**) e disporre gli elementi al suo interno/figli in modo *flessibile*(justify,align,order ecc), per abilitare il Flexbox, si applica la proprietà `display: flex` o `display: inline-flex` al contenitore principale.

**N.B** il contenitore genitore dispone spazialmente i **figli diretti**, se ci sono elementi annidati al loro interno é bene tenere a mente che la proprietá agisce direttamente solo sui figli diretti, anche se sponsatando questi ultimi anche gli elementi contenuti al loro interno verranno riposizionati

Elementi figli (**Flex Items**): Sono gli elementi contenuti all'interno del contenitore principale. Possono essere disposti orizzontalmente o verticalmente

**Flusso principale** (*Main Axis*): È la direzione principale in cui gli elementi figli vengono posizionati all'interno del contenitore principale. Può essere orizzontale (*row*) o verticale (*column*).

**Flusso trasversale** (Cross Axis): é la direzione trasversale(perpendicolare) a quella principale

**Flexbox Properties**: Esistono diverse proprietà CSS specifiche di Flexbox per controllare il comportamento degli elementi. Alcune delle più comuni sono *justify-content*, *align-items* e *flex*.

*Con l'utilizzo delle proprietà Flexbox, è possibile controllare l'allineamento, la distribuzione, lo spazio tra gli elementi e la crescita o la riduzione degli elementi in base allo spazio disponibile. Questo approccio è particolarmente utile per creare layout responsive e adattivi, in cui gli elementi si adattano in modo dinamico alle diverse dimensioni dello schermo*.


### Proprietá display
viene utilizzata per specificare come un elemento HTML deve essere visualizzato nel layout.

* **block**: l'elemento viene visualizzato come un blocco, occupando l'intera larghezza disponibile e iniziando una nuova riga.

* **inline**: l'elemento viene visualizzato come un elemento inline, adattandosi alla larghezza dei contenuti e consentendo ad altri elementi inline di stare sullo stesso livello orizzontale.

* **inline-block**: l'elemento viene visualizzato come un elemento inline, ma mantiene le caratteristiche di un blocco, come l'altezza e la larghezza personalizzate.

* **none**: l'elemento non viene visualizzato, rimanendo completamente nascosto nella pagina.

* **grid**: l'elemento viene trattato come un contenitore flessibile utilizzando il layout CSS Grid.

* **inline-flex**:  viene utilizzata per rendere un elemento un contenitore flessibile con **layout Flexbox**, ma con comportamento "inline" anziché "block"

* **flex**: l'elemento viene trattato come un contenitore flessibile utilizzando il **layout Flexbox**.

**N.B** *Flessibile*: trasformano un elemento in un contenitore flessibile che consente di gestire la posizione, l'allineamento e la dimensione dei suoi elementi figli in modo più dinamico.

### Proprietá del Flexbox
Una volto assegnata la proprieta `display: flex | inline-flex` ad un elemento html, rendiamo flessibili i suoi elementi figli e possiamo applicargli le proprietá del modulo *flexbox*, per disporli spazialmente


#### Proprietá flex-direction:
Questa proprieta viene utilizzata per definire l'**orientamento principale** degli elementi figli;il valore di default é **row**

`flex-direction: row | row-reverse | column | column-reverse;`

* **row** (*valore predefinito*): Gli elementi figli vengono disposti in una riga orizzontale da sinistra a destra.

* **row-reverse**: Gli elementi figli vengono disposti in una riga orizzontale da destra a sinistra.

* **column**: Gli elementi figli vengono disposti in una colonna verticale dall'alto verso il basso.

* **column-reverse**: Gli elementi figli vengono disposti in una colonna verticale dal basso verso l'alto.

#### Proprietá flex-wrap

`flex-wrap: nowrap | wrap | wrap-reverse;`

* **nowrap** (*valore predefinito*): Gli elementi figli vengono disposti su una sola riga o colonna, senza avvolgimento. Se gli elementi superano la dimensione del contenitore, verranno *ridimensionati* o *sovrapposti*.

* **wrap**: Gli elementi figli vengono avvolti su più righe o colonne se necessario. Verranno quindi visualizzati in righe o colonne multiple, a seconda dell'orientamento impostato con flex-direction.

* **wrap-reverse**: Gli elementi figli vengono avvolti su più righe o colonne, ma in ordine inverso rispetto al valore wrap.

#### Proprietá justify-content

La proprietà justify-content viene utilizzata per **allineare gli elementi figli** all'interno di un contenitore Flexbox lungo **l'asse principale**. Questa proprietà definisce come viene distribuito lo spazio libero tra gli elementi o come vengono allineati quando non c'è spazio libero.
`justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;`


* **flex-start** (*valore predefinito*): Gli elementi figli vengono allineati all'inizio del contenitore, lungo l'*asse principale*.

* **flex-end**: Gli elementi figli vengono allineati alla fine del contenitore, lungo l'*asse principale*.

* **center**: Gli elementi figli vengono allineati al centro del contenitore lungo l'*asse principale*.

* **space-between**: Gli elementi figli vengono distribuiti in modo uniforme lungo l'*asse principale*, con spazio tra di loro. Il primo elemento è all'inizio del contenitore e l'ultimo elemento è alla fine del contenitore.

* **space-around**: Gli elementi figli vengono distribuiti in modo uniforme lungo l'*asse principale*, con spazio uguale attorno a ciascun elemento. Questo significa che c'è spazio sia tra gli elementi che all'inizio e alla fine del contenitore.

* **space-evenly**: Gli elementi figli vengono distribuiti in modo uniforme lungo l'*asse principale*, con spazio uguale tra di loro, incluso lo spazio all'inizio e alla fine del contenitore.


#### Proprietá align-Items

La proprietà align-items viene utilizzata per **allineare gli elementi figli** all'interno di un contenitore Flexbox lungo **l'asse trasversale**, cioè l'asse perpendicolare all'asse principale. Questa proprietà definisce come gli elementi vengono allineati verticalmente (se l'orientamento è "row") o orizzontalmente (se l'orientamento è "column").
`align-items: stretch | flex-start | flex-end | center | baseline;`

* **stretch** (*valore predefinito*): Gli elementi figli vengono allungati per adattarsi all'altezza del contenitore, se necessario.

* **flex-start**: Gli elementi figli vengono allineati all'inizio del contenitore lungo *l'asse trasversale*.

* **flex-end**: Gli elementi figli vengono allineati alla fine del contenitore lungo *l'asse trasversale*.

* **center**: Gli elementi figli vengono allineati al centro del contenitore lungo *l'asse trasversale*.

* **baseline**: Gli elementi figli vengono allineati in base alla loro linea di base, che di solito corrisponde alla *linea di testo base*. Questo può essere utile quando gli elementi figli hanno *altezze diverse*.

**N.B** Il *Flexbox* viene utilizzato per dei *macro-spostamenti* degli elementi, mentre il *Box Model* o le *Position* per dei *micro-spostamenti*

#### Align-content

La proprietà CSS align-content viene utilizzata per **allineare le righe di elementi figli** all'interno di un contenitore Flexbox lungo l'*asse trasversale*, quando i figli sono *disposti su più righe*, come ad esempio quando abbiamo piú cards di prodotti

`align-content: flex-start | flex-end | center | space-between | space-around | stretch;`

* **stretch** (valore predefinito): Le righe di elementi figli vengono allungate per adattarsi all'altezza del contenitore, se necessario.

* **flex-start**: Le righe di elementi figli vengono allineate all'inizio del contenitore lungo l'asse trasversale.

* **flex-end**: Le righe di elementi figli vengono allineate alla fine del contenitore lungo l'asse trasversale.

* **center**: Le righe di elementi figli vengono allineate al centro del contenitore lungo l'asse trasversale.

* **space-between**: Le righe di elementi figli vengono distribuite in modo uniforme lungo l'asse trasversale, con spazio tra di loro. La prima riga è all'inizio del contenitore e l'ultima riga è alla fine del contenitore.

* **space-around**: Le righe di elementi figli vengono distribuite in modo uniforme lungo l'asse trasversale, con spazio uguale attorno a ciascuna riga. Ciò significa che c'è spazio sia tra le righe che all'inizio e alla fine del contenitore.

#### Align-self
Permette di spostare un solo elemento figlio selezionato dal selettore

#### Proprietá order

La proprietà CSS **order** viene utilizzata all'interno di un layout Flexbox per specificare l'ordine di visualizzazione degli elementi figli diretti all'interno del contenitore. Essa consente di modificare l'ordine di presentazione degli elementi senza modificarne la struttura nell'albero del documento HTML.
`order: numero;`


## Media Query
Una media query è un'**istruzione CSS** che consente di applicare stili diversi in base alle caratteristiche del dispositivo o del viewport(finestra del browser *vh-vw*); consentono di creare layout e stili **responsive** che si adattano a diverse dimensioni dello schermo e dispositivi.

Inserire le media query infondo al codice sorgente del file css

```
@media screen and (max-width: 768px) {
  /* Stili da applicare quando la larghezza del viewport è massimo 768px */
  body {
    font-size: 14px;
  }

  .container {
    display: flex;
    flex-direction: column;
  }
}
```
La sintassi con **media screen and** , é meglio delle alternative perché specifica che il layout responvice va applicato solo quando si visualizza la pagina web da un dispositivo, infatti `screen` indica per l'appunto lo schermo e `and` é una condizione

Possiamo anche concatenare piú condizioni con ulteriori `and`
`@media screen and (max-width: 576px) and (max-width: 798px) {}`

## Pseudo-elementi

In CSS lo psudo elemento e una **::keyword**, che aggiunta al *selettore* di un elemento html permette di stilizzare alcune parti specifiche dell'elemento
*non sono elementi html ma lo sembrano, da questo il nome*

##### I principali pseudo-elementi disponibili sono:

1. `::before`: inserisce contenuto aggiuntivo prima del contenuto dell'elemento selezionato. Può essere utilizzato per aggiungere decorazioni o icone prima dell'elemento.
2. `::after`: inserisce contenuto aggiuntivo dopo il contenuto dell'elemento selezionato. Può essere utilizzato per aggiungere elementi decorativi o contenuto generato dinamicamente.
3. `::first-letter`: seleziona la prima lettera di un elemento di testo. Può essere utilizzato per applicare stili specifici alla prima lettera di un paragrafo o di un titolo.
4. `::first-line`: seleziona la prima linea di un elemento di testo. Può essere utilizzato per applicare stili specifici alla prima linea di un paragrafo.
5. `::selection`: seleziona il testo selezionato dall'utente. Può essere utilizzato per applicare stili al testo selezionato, come il colore di sfondo o il colore del testo.

Ecco un esempio di utilizzo di un pseudo-elemento `::before` per inserire un'icona prima del contenuto di un elemento:

```
.icon::before {
  content: url('path/to/icon.png');
}
```

In questo caso, l'elemento con la classe "icon" avrà l'icona specificata come contenuto aggiuntivo prima del suo contenuto effettivo.

I pseudo-elementi offrono una maggiore flessibilità nello stilizzare parti specifiche degli elementi HTML e consentono di creare effetti visivi interessanti senza dover modificare direttamente la struttura HTML.

###### Ne caso si utilizzino gli psudo-elementi *after* e *before* la proprietá **content**, specifica il tipo di contenuto aggiunto
```
selettore::before {
  content: valore;
}

selettore::after {
  content: valore;
}
```
Il valore della proprietà content può essere di diversi tipi, tra cui:
`content: "Testo da aggiungere";`
`content: attr(data-nome-attributo);`
`content: url("percorso/immagine.jpg");`
`content: counter(nome-contatore);`


## Pseudo-classi
Le pseudo-classi in CSS si creano quando aggiungiamo una **:keyword** ad un selettore css, i selettori cosi creati si applicano all'elemento solo nel caso siano soddisfatte le condizioni di quel selettore
*anche in questo caso il nome indica che non sono delle vere e proprie classi*

Alcune delle pseudo-classi più comuni includono:

1. `:hover`: seleziona un elemento quando il cursore del mouse si trova sopra di esso.
2. `:active`: seleziona un elemento quando viene attivato, ad esempio quando viene premuto un pulsante del mouse o viene toccato su un dispositivo touchscreen.
3. `:focus`: seleziona un elemento quando riceve il focus, ad esempio quando viene selezionato tramite la tastiera o tramite un dispositivo di input.
4. `:first-child`: seleziona l'elemento figlio che è il primo figlio di suo genitore.
5. `:last-child`: seleziona l'elemento figlio che è l'ultimo figlio di suo genitore.
6. `:nth-child()`: seleziona l'elemento figlio che corrisponde a un determinato indice specificato.

Ci sono molte altre pseudo-classi disponibili in CSS che consentono di selezionare gli elementi in base a varie condizioni o stati.

## Animazioni

Le animazioni in CSS consentono di creare transizioni fluide e effetti di animazione senza l'uso di JavaScript o altre tecnologie.
Per creare un animazione, ci sono due passaggi da fare:

1. Assegnare all'elemento che si vuole animare alcune delle seguenti proprietá(specificare il nome dell'animazione e fondamentale per collegarla all'elemento)

- `animation`: è una proprietà shorthand che consente di impostare contemporaneamente tutte le proprietà di animazione (ad esempio `animation-name`, `animation-duration`, `animation-timing-function`, ecc.).

- `animation-name`: specifica il nome dell'animazione definito con `@keyframes`.

- `animation-delay`: specifica un ritardo prima che l'animazione inizi a eseguirsi.

- `animation-direction`: specifica la direzione dell'animazione (es. "normal", "reverse", "alternate", ecc.).

- `animation-duration`: specifica la durata dell'animazione.

- `animation-fill-mode`: specifica lo stile dell'elemento prima e dopo l'esecuzione dell'animazione.

- `animation-iteration-count`: specifica il numero di volte che l'animazione viene ripetuta.

- `animation-play-state`: specifica se l'animazione è in esecuzione o in pausa.

- `animation-timing-function`: specifica la curva di velocità dell'animazione (es. "linear", "ease", "ease-in", "ease-out", ecc.).


2. Le animazioni CSS sono definite utilizzando la regola `@keyframes`, che specifica una serie di stadi o frame dell'animazione e gli stili da applicare a ciascun frame.
La regola @keyframes specifica es. tre stadi dell'animazione (0%, 50%, 100%) e gli stili da applicare a ciascun stadio.

Le proprietà più utilizzate all'interno di un `@keyframes` sono:

1. `opacity`: controlla l'opacità dell'elemento durante diversi stadi dell'animazione. Può essere utilizzato per creare transizioni di dissolvenza.
2. `transform`: permette di applicare trasformazioni all'elemento, come la rotazione, la scalatura, la traslazione o lo sfalsamento. È ampiamente utilizzato per creare effetti di animazione complessi.
3. `width` e `height`: consentono di animare le dimensioni dell'elemento, rendendolo più grande o più piccolo nel corso dell'animazione.
4. `background-color`: permette di animare il colore di sfondo dell'elemento, creando transizioni di colore fluide.
5. `border-width`, `border-color` e `border-radius`: permettono di animare i bordi dell'elemento, rendendoli più spessi o sottili, cambiando colore o modificando la forma del bordo.
6. `box-shadow`: permette di animare l'ombra dell'elemento, rendendola più evidente o scomparendo nel corso dell'animazione.

```
@keyframes myAnimation {
  0% {
    opacity: 0;
    transform: scale(0);
  }

  50% {
    opacity: 1;
    transform: scale(1.2);
  }

  100% {
    opacity: 0;
    transform: scale(1);
  }
}
```
### Variabili :root
Le variabili root, anche conosciute come variabili CSS personalizzate, sono variabili definite nel selettore **:root** all'interno di un foglio di stile CSS. Queste variabili sono accessibili e utilizzabili in tutto il documento CSS, consentendo di dichiarare e assegnare valori a variabili che possono essere riutilizzate in diverse parti dello stile.

Le variabili root sono dichiarate nel selettore :root, esso seleziona l'elemento radice, che è l'elemento `<html>`, questo fa si che le variabili :root siano accessibili in tutto il documento

Di solito, viene utilizzato il selettore :root per definire le variabili all'inizio del foglio di stile, al di fuori di qualsiasi selettore specifico.

Il loro utilizzo prevede due passaggi

1. Creare all'interno del selettore :root le variabili che volgliamo utilizzare
```
:root {
  --colore-primario: #ff0000;
  --dimensione-font: 16px;
}
```
2. Assegnare le proprietá definite all'interno del selettore :root, alle proprietá css come valore precedute dalla funzione **var()**
```
h1 {
  color: var(--colore-primario);
  font-size: var(--dimensione-font);
}
```