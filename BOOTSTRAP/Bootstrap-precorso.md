# Bootstrap
Bootstrap è un **framework front-end** open-source ampiamente utilizzato per lo sviluppo di siti web e applicazioni web(sono siti che permettono una maggiore interattivitá un ecommerce). È stato creato da Twitter e offre un set di **strumenti** e **componenti** predefiniti che consentono di progettare, sviluppare e personalizzare rapidamente l'aspetto e la funzionalità dei siti web.

Le caratteristiche principali di Bootstrap includono:

1. **Grid System**: Bootstrap offre un sistema di *griglia* responsivo che consente di creare layout flessibili e adattabili a diverse dimensioni di schermo. La griglia si basa su *colonne* e *righe* che facilitano la disposizione e l'allineamento degli elementi sulla pagina.

2. **Componenti UI**: Bootstrap fornisce una vasta gamma di componenti UI predefiniti come pulsanti, modali, barre di navigazione, form, carousel, tabelle, card e molti altri. Questi componenti possono essere facilmente personalizzati

3. **Tipografia**: Bootstrap offre uno stile di base per la tipografia, che comprende una selezione di font, dimensioni dei caratteri, colori e stili di testo predefiniti. Ciò semplifica la creazione di testo coerente e leggibile.

4. **Responsività**: Bootstrap è progettato per creare siti web responsivi, che si adattano automaticamente a diverse dimensioni di schermo, come desktop, tablet e dispositivi mobili. Utilizzando le classi di Bootstrap, è possibile gestire in modo intuitivo la disposizione e la visibilità degli elementi su schermi di diverse dimensioni.

5. **Temi personalizzabili**: Bootstrap offre una serie di temi predefiniti che possono essere utilizzati come punto di partenza per la progettazione di siti web. Inoltre, è possibile personalizzare facilmente i colori, le dimensioni, i margini e altri stili utilizzando vari strumenti di personalizzazione forniti da Bootstrap.

L'utilizzo di Bootstrap può semplificare lo sviluppo web fornendo componenti pronti all'uso, uno stile coerente e un approccio responsivo, ció fornisce la **base** per la creazione di sito web che poi andrá personalizzato

## Creazione progetto con Bootstrap

1. #### **CDN**(*Content Delivery Network*)
rete di distribuzione dei contenuti è un servizio che distribuisce contenuti web su dei server distribuiti in diverse posizioni geografiche. La sua principale funzione è quella di fornire contenuti web in modo rapido ed efficiente agli utenti finali, riducendo i tempi di caricamento delle pagine e migliorando l'esperienza utente

La rete ha a disposione molteplici server CDN, l'utente che ne fará richiesta si collegherá a quello piú vicino/funzionante

Quando un utente accede a un sito web che utilizza Bootstrap, il server invia i file richiesti direttamente al browser dell'utente. Questi file includono i fogli di stile CSS, gli script JavaScript e le risorse necessarie per rendere il sito funzionante. I file vengono recuperati dalla **memoria statica** del server e inviati come risposta alla richiesta del client.

I server CDN, memorizzano temporaneamente i file richiesti nella **cache del server CDN** per ridurre il tempo di latenza e migliorare le prestazioni.


##### Vantaggi:

* **Velocitá di caricamento**: perché le risorse di bootstrap sono prese da un server cdn e non vanno ad appesantire il sito

* **Cache**: Le risorse di Bootstrap fornite attraverso la CDN sono generalmente memorizzate nella cache del browser degli utenti. Questo significa che se un utente visita più pagine del tuo sito, i file di Bootstrap verranno caricati dalla cache del browser invece di dover essere scaricati nuovamente da Internet, migliorando ulteriormente i tempi di caricamento delle pagine successive.

Inoltre anche quando mi sposto su altro sito, le CDN di bootstrap rimangono salvate nel **cache del browser** e quindi non servirá richiederle al server CDN ottimizzando le prestazioni

La cache è un meccanismo utilizzato per archiviare temporaneamente i dati o i contenuti frequentemente richiesti al fine di ridurre i tempi di accesso e migliorare le prestazioni complessive di un sistema.

* **Scalabilità**: L'utilizzo di una CDN per fornire i file di Bootstrap può aiutare a distribuire il carico di traffico in modo più efficiente, riducendo il carico sul tuo server principale.

La scalabilità si riferisce alla capacità di un sistema o di una piattaforma di adattarsi e gestire un aumento della domanda o del carico di lavoro senza compromettere le prestazioni o l'affidabilità

* **Aggiornamenti semplificati**: Quando una nuova versione di Bootstrap viene rilasciata, i file vengono aggiornati sul server CDN

Le CDN nella pratica sono codici che vanno inseriti nell'**head** del documento html (*importiamo il css*) e in fondo al **body** va inserito uno *script* che serve ad *importare il JS* di bootstrap; permettono di collegarci ai server CDN dove sono ospitati i dati per il funzionamento di bootstrap

Per velocizzare la procedura si puó usare lo **starter template di bootstrap** dove le CDN sono giá incluse, sia quelle nell'head che lo script nel body

Possiamo visualizzare il css di bootstrap che stiamo importando nel punto min, dove sono minificati(*La minificazione è un processo di ottimizzazione dei file di codice, come HTML, CSS e JavaScript, che consiste nella riduzione delle dimensioni del file eliminando spazi bianchi, commenti e altri caratteri non essenziali. L'obiettivo della minificazione è quello di ridurre la dimensione dei file per migliorare le prestazioni di caricamento delle pagine web*.)
Possiamo togliere il punto min per visualizzare il css in modo normale

2. #### Grid system

Il sistema di griglia di Bootstrap è una componente chiave del framework e consente di creare *layout responsivi* in modo rapido e semplice. Il sistema di griglia di Bootstrap è basato su un **sistema a 12 colonne**(12 col 1), che consente di suddividere orizzontalmente la pagina in 12 unità di larghezza; ogni unitá sará uguale ad una *col 1*

Il grid system é costituito da 3 classi

1.  Classe**container**: la *best pratice* é quella di assegnare alla diverse sezioni di una pagina web, quindi al tag *section* la classe *container* di boorstrap

* La classe container ha come proprietá caratteristiche una *width: 100%* e un *margin-left e right:auto*, queste proprietá permettono per l'appunto di contenere un contenuto

Una variante della classe container é **container-fluid**, usato per header e footer

2. Classe **row**, questa classe ha la proprietá *display:flex* e *flex:wrap*, all'interno dell'elemento con classe container possiamo inserire un qualunque numero di elementi con classe row

3. Classe **col**, questa classe assegnata ad elemento che si trova annidato dentro una row e un container; permette di suddivedere la with dell'elemento con classe row in 12 elementi, ad ogni elemento corrisponde una **col 1**

**N.B** Se una colonna é una col 12 occuperá tutta la width della row, se inserisco una nuova colonna nella row questa va capo e crea una nuova riga nella colonna, questo accede anche se la somma delle due colonne supera 12

**N.B** Possiamo anche creare un grid sistem all'interno di una colonna inserendo una row in una colonna

3. #### Breakpoint
Sono essenzialmente delle **media query**, integrate all'interno di bootstrap che possono essere utilizzate semplicemente aggiungendo dei **suffissi** alle proprietá di bootstrap

**XS** é il valore di default, questo perché bootstap da priritá ai dispositivi mobili é **mobile first**

* Extra small (xs): schermi con larghezza inferiore a 576px.
* Small (sm): schermi con larghezza uguale o superiore a 576px.
* Medium (md): schermi con larghezza uguale o superiore a 768px.
* Large (lg): schermi con larghezza uguale o superiore a 992px.
* Extra large (xl): schermi con larghezza uguale o superiore a 1200px.

```
<div class="row">
  <div class="col-12 col-md-6 col-lg-4">Contenuto colonna 1</div>
  <div class="col-12 col-md-6 col-lg-4">Contenuto colonna 2</div>
  <div class="col-12 col-md-6 col-lg-4">Contenuto colonna 3</div>
</div>
```
