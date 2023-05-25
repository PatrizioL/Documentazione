# Console Unix

Una console Unix, nota anche come **terminale,shell o prompt dei comandi**, è un'interfaccia testuale che consente agli utenti di interagire con il sistema operativo **Unix o Unix-like**(in questo caso unix-like). La console Unix fornisce un prompt in cui gli utenti possono inserire comandi di testo/istruzioni per eseguire operazioni sul sistema.

Attraverso la console Unix, gli utenti possono eseguire una vasta gamma di attività, tra cui:

1. **Navigazione nel file system**: È possibile spostarsi tra le directory, visualizzare elenchi di file e cartelle, creare e cancellare file e cartelle, rinominare file, copiare o spostare file da una posizione all'altra.

2. **Gestione dei processi**: Gli utenti possono avviare, interrompere o monitorare processi in esecuzione sul sistema. Possono eseguire comandi in background o in primo piano, mettere in pausa o riprendere processi, visualizzare l'elenco dei processi in esecuzione e terminare i processi non necessari.
* Il building degli asset, il server locale

3. **Configurazione del sistema**: La console Unix consente agli utenti di modificare le impostazioni del sistema, come le variabili di ambiente, le preferenze dell'utente e le autorizzazioni dei file.

4. **Gestione dei pacchetti e del software**: Attraverso la console, è possibile installare, aggiornare o rimuovere pacchetti e software sul sistema. Ciò è particolarmente utile nelle distribuzioni di Linux, dove spesso vengono utilizzati gestori di pacchetti come apt, yum o dnf.
* composer o npm

5. **Automazione delle attività**: Gli utenti possono creare script o programmi di shell per automatizzare compiti ripetitivi o complessi. I comandi possono essere organizzati in script per automatizzare processi di elaborazione dei dati o attività di sistema.
* Le code dei jobs

6. **Networking**: La console Unix fornisce strumenti per la gestione e la configurazione della rete, consentendo agli utenti di stabilire connessioni remote, controllare lo stato della rete, eseguire ping, tracciare route, ecc.

Queste sono solo alcune delle funzionalità principali offerte dalla console Unix..

## Git Bash
Git Bash è una console **Unix-like** sviluppata specificamente per il sistema operativo **Windows**, che fornisce un'interfaccia a riga di comando simile a quella di Unix su un ambiente Windows.

Windows *non é un sistema operativo unix-like* come (linux-android-macOs), ma la git bash permette di interfacciarsi ad esso come se lo fosse.

### Sintassi
Non utilizzare spazi nei nomi delle cartelle o dei file, si puo usare(**\_**) oppure \ seguita da uno spazio(questo per creare spazi)

### Comandi Git Bash
* `help`:per vedere tutti i comandi di git bash
* `<comando> --help`: per la descrizione del comando
* `tab`:autocompletamento
* `clear`: pulisce il terminale dalla cronologia dei comandi
* `Ctrl+c`: interrompe l'esecuzione del terminale
* `&&`: concatenare comandi diversi
* `explorer .`: apre la cartella corrente, il **\.** indica genericamente la posizione corrente
* `code .`: apre vs code sulla cartella corrente

##### Comandi per la navigazione e la gestione di file e cartelle in Git Bash:

* `pwd`: Mostra il percorso completo della directory corrente.
* `ls`: Elenca i file e le cartelle nella directory corrente.
* `ls-a`:mostra i file nascosti come .git
* `cd`: ci riporta nella home, da qualunque posizione
* `cd <directory>`: Sposta il terminale nella directory specificata.
* `cd ..`: Sposta il terminale nella directory genitore (superiore), in generale il doppio **\.\.**, indica la posizione del genitore
* `cd <percorso_relativo>`:Sostituisci *percorso_relativo*(percorso per il file dalla posizione corrente) con il percorso relativo della directory in cui desideri spostarti.
* `cd /path/to/directory`:Sostituire */path/to/directory* con il *percorso assoluto*(in windows dall'unita di memoria es. C:\Users\user\Documents\file.txt) permette di spostarmi direttamente nella cartella di mio interesse, indipendentemente dalla posizione corrente
* `cd ../subdir/nested_directory`: concatenare il comandi
* `mkdir <nome_cartella>`: Crea una nuova cartella con il nome specificato.
* `rmdir <nome_cartella>`: Elimina una cartella vuota
* `rm <nome_file>`: Rimuove un file specificato.
* `rm <nome_file1> <nome_file2> ...`: rimuove piu fali contemporaneamente, funziona anche per creare cartelle e file
* `rm -r <nome_cartella>`: Rimuove una cartella e il suo contenuto in modo ricorsivo.
* `rm -rf <nome_directory>`: viene utilizzato per rimuovere in modo ricorsivo e forzato una directory e tutti i suoi contenuti, inclusi file e sotto-directory.
* `mv <file_cartella_origine> <file_cartella_destinazione>`: Sposta un file o una cartella.
* `mv <nome_file_attuale> <nuovo_nome_file>`:rimomina un file
* `cp <file_cartella_origine> <file_cartella_destinazione>`: Copia un file o una cartella.
* `touch <nome_file>`: Crea un nuovo file con il nome specificato.
* `cat <nome_file>`: Visualizza il contenuto di un file.
* `less <nome_file>`: Visualizza il contenuto di un file in modo paginato, consentendo di scorrere l'output.
* `head <nome_file>`: Mostra le prime righe di un file.
* `tail <nome_file>`: Mostra le ultime righe di un file.
* `grep <pattern> <nome_file>`: Cerca un pattern all'interno di un file.
* `chmod <permessi> <nome_file>`: Modifica i permessi di accesso a un file.


##### Comandi per l'editor di testo Vim
Vim è un potente editor di testo a riga di comando ampiamente utilizzato nei sistemi Unix-like.
Ecco alcuni comandi di base per utilizzare Vim:

`vim <nome_file>`: permette di aprire l'editor di testo, su uno specifico file

Sotto l'editor, possimo utilizzare dei comandi specifici dell'editor vim
* `i`: per inserire testo nel file aperto dall'editor
* `Esc`: per passare dall'editor ai comandi dell'editor
*  `:w` e premi `Enter`: per salvare rimanendo nell'editor
* `:wq`: salva e chiudi vim
* `:help`: per tutti i comandi di vim

## Sistema di controllo di versione Git
Git è un sistema di controllo versione, per la gestione del codice sorgente durante lo sviluppo software. È stato creato da Linus Torvalds nel 2005 per supportare lo sviluppo del kernel di Linux, ma è diventato uno degli strumenti più diffusi nel mondo dello sviluppo software.

Git registra le modifiche apportate ai file nel **repository** in modo incrementale nel tempo, consentendo ai team di sviluppatori di collaborare in modo efficace. Offre funzionalità come il tracciamento delle modifiche(**commit**), la gestione dei rami (**branch**), la fusione dei rami(**merge**), il ripristino delle versioni precedenti(**reset**), la gestione delle modifiche conflittuali(**conflitti di merge**) e altro ancora.

Le caratteristiche chiave di Git includono:

1. Controllo versione distribuito: Ogni sviluppatore ha una copia completa del repository(*locale*) sul proprio computer, consentendo loro di lavorare in modo indipendente offline e di sincronizzarsi successivamente con il repository centrale(*repository online GitHub*).

2. Struttura a snapshot(**commit**): Git registra le modifiche apportate ai file come snapshot, che consentono di recuperare facilmente qualsiasi versione precedente

* Le modifiche fatte al file, vanno salvate nella repository locale con un commit, in questo modo possiamo tenere traccia di tutte le modifiche apportate al file, ogni commit é per l'appunto una versione del file da questo il nome **controllo versione**

3. Supporto per rami (**branch**): Git consente di creare rami separati per sviluppare nuove funzionalità o risolvere problemi senza influire sul ramo principale. I rami possono essere uniti in modo pulito quando le modifiche sono pronte.

4. Fusione (**merge**): Git facilita la fusione di rami, consentendo di combinare le modifiche da un ramo all'altro in modo sicuro e senza perdita di dati.

5. Gestione dei conflitti(**conflitti di merge**): Quando più sviluppatori apportano modifiche alla stessa parte di un file, Git aiuta a gestire e risolvere i conflitti che potrebbero sorgere durante la fusione.

* In prima istanza git prova sempre a fare un **merge automatico**, talvolta peró se due o piú sviluppatori lavorano sulle stesse righe di codice, sorge un *conflitto di merge* che va risolto con un **merge manuale** cioé dobbiamo noi specificare a git, quale modifiche deve salvare

* Subito dopo aver risolto il merge dobbiamo fare un commit delle modifiche e salvare nella nostra repository locale, per risolvere definitivamente il conflitto di merge

6. Integrazione con servizi di hosting: Git si integra con piattaforme di hosting come **GitHub**, GitLab e Bitbucket, facilitando la condivisione, la collaborazione e la revisione del codice.

### Comandi da terminale per il controllo di versione con git
Creo la repository locale all'interno della cartella principale del progetto

Ecco un elenco di alcuni comandi comuni e importanti di Git:

* `git`: questo comando lanciato da solo mi fa vedere alcuni dei comandi disponibili per il controllo di versione, la lista non é completa
* `git help <nome_camando>`: istruzioni sull'uso del comando, si puó usare anche `git help` da solo visualizza categorie di comandi disponibili

##### Configurazione:
- `git config --global user.name "<nome>"`: Imposta il nome utente associato ai tuoi commit.
- `git config --global user.email "<email>"`: Imposta l'email associata ai tuoi commit.
- `git config --global core.editor "<editor>"`: Imposta l'editor di testo predefinito per i messaggi di commit.

##### Inizializzazione e clonazione:
- `git init`: Inizializza un nuovo repository(locale) Git nella directory corrente, si gnererá un file nascosto **.git**, che sará la nostra repository locale
- `git clone <url>`: Clona un repository Git esistente da una specifica URL.

##### Gestione dei cambiamenti:
- `git add <file>`: Aggiunge un file alla staged area in preparazione per il commit.
- `git commit -m "<messaggio>"`: Esegue un commit delle modifiche, registrando uno snapshot del repository con un messaggio descrittivo.
- `git diff`: Mostra le differenze tra i file non ancora aggiunti alla staged area e l'ultima versione registrata nel repository, quindi va lanciato prima di un commit

Se andiamo a modificare una linea di codice giá salvata nella repository di git, anche semplicemente aggiungendo una parola, per git é come se avessimo cancellato e riscritto per intero la riga é chiedera all'utente di scegliere quale delle due righe vuole salvare nella repo, quindi modificando o riscrivendo linee di codice gia committate si origina un *conflitto di merge*

- `git restore <file>`: Ripristina un file alla versione precedente non ancora aggiunta alla staged area.


- `git checkout main`:per tornare rimettere la head sul commit di default
- `git checkout -- <file>`: Annulla le modifiche apportate a un file nella directory di lavoro, ripristinando la versione precedente(vs rimane sul vecchio commit)
- `git checkout <id_commit>`: mi sposta la *HEAD* sul commit selezionato, non cancella gli altri commit mi sposto solamente

###### peró mi mette in una condizione chiamata *detachedHEAD*, il che significa che non sei più su un branch specifico. Se desideri lavorare su quel commit e creare nuovi commit basati su di esso, è consigliabile creare un nuovo branch a partire da quel commit utilizzando il comando `git branch <nome-branch>`

###### **N.B** utilizzarlo solamente se non si volgiono cancellare i commit

- `git reset --help`:utilizzi di git reset
- `git reset main`: mi riporta sull'Head del main
- `git reset <id_commit>`: : Questo comando riposiziona il puntatore **HEAD** sul commit specificato e cancella tutti i commit successivi. Tuttavia, le modifiche apportate in questi commit non saranno perse e saranno ancora presenti nella tua directory di lavoro
###### in alternativa all'id del commit si puo usare anche il messaggio del commit tra apici se univoco
- `git reset --mixed <id_commit>`: opzione di default di git reset, quindi se non scrivo --soft o hard mi fa un mixed
- `git reset --soft <id_commit>`:sposta la HEAD cancellando i commit, ma conservandoli nella **staged area**, non aggiorna la directory di lavoro
- `git reset --hard <id_commit>`: il comando git reset --hard annulla i commit successivi, aggiorna la staged area e modifica anche la directory di lavoro al nuvo commit

- `git rm <file>`: Rimuove un file dal repository e dalla directory di lavoro.

##### Gestione dei rami e delle fusioni:
Quando creo un nuovo ramo nella repo, é come se creassi una nuova repo semparata da quella originale
- `git branch`: Mostra l'elenco dei rami presenti nel repository.
- `git branch <nome_nuovo_branch`: Creo un nuovo branch
- `git checkout <nome_branch>`: Passa a un ramo specifico nel repository.
- `git merge <branch>`: Esegue la fusione di un ramo specifico nel ramo attuale.
Quindi se voglio prendere i cambiamenti fatti in ramo e passarli al ramo in cui mi trovo é all'interno di quest'ultimo che dovró lanciare **git merge**
**N.B** Ricordasi sempre di fare git add e git commit, per salvare i cambiamenti, finquando non si fa quest'operazione il merge non sará risolto
- `git pull`: Recupera le modifiche dal repository remoto e le fonde con il ramo attuale.
- `git push`: Carica i commit locali sul repository remoto.

##### Gestione delle origini remote:
- `git remote add <nome> <url>`: Aggiunge una nuova origine remota al repository.
- `git remote -v`: Mostra l'elenco delle origini remote associate al repository.
- `git push -u <origine> <branch>`: Carica il ramo locale sul repository remoto e lo associa come branch di tracciamento.

**N.B** Per origini remote si riferisce al collegamento tra la repository locale e quella online(appunto remota)

##### Altri comandi utili:
- `git status`: Mostra lo stato attuale del repository.
- `git log`: Mostra la cronologia dei commit.
- `git stash`: Salva temporaneamente le modifiche non ancora committate per poter passare a un altro ramo.
- `git tag <nome>`: Aggiunge un tag al commit corrente per segnare una versione specifica.

#### Sequenza dei comandi da lanciare per il controllo versione in locale
Dopo aver creato il progetto, posso creare all'interno della cartella principale del progetto la repository locale di git per quel progetto

1. `git init`: creazione repo

2. `git status`: vedo lo stato corrente della repo, se i file sono tracciati e commitatti

3. `git add <nome_file>`: utilizzo git add per aggiungere un file alla **staged area**(area di preparazione),rappresenta un'area intermedia tra la tua directory di lavoro (dove apporti le modifiche ai file) e il repository locale.

* Per effettuare un commit in Git, devi prima "aggiungere" le modifiche specifiche che desideri includere nel commit alla staged area.

* `git add .`: per aggiungere tutti i file modificati alla staged area, contemporaneamente

4. `git commit -m'messaggio'`: dopo aver tracciato le modifiche aggiungedole alla staged area, possiamo salvare nella repository, creando una versione del progetto, che sará identificata da un messaggio che noi allegheremo ad esso per identificarlo

5. `git status`: ora se rilancio git status avró un mex di conferma che tutte le modifiche sono tracciate e committate

6. `git log`: mi permette di vedere il registro di tutti i commit salvati nella repo, per uscire da git log digitare **q**
* Per ogni commit, sará presente autore, data e messaggio allegato da noi al momento del salvataggio
* Ogni commit identificato da un codice univoco ID chiamato **hash**
* Il commit corrente, cioé la versione del progetto in cui ci troviamo sará identificata con (**HEAD**)
* Di deafault la (HEAD) é sempre posizionata sull'ultimo commit, head é un file all'interno della repo che si occupa di tenere traccia dei commit


#### Trasferire la nostra repository(locale) in remoto(online)
Dopo aver creato la repository locale, vogliamo trasferire la repository su un server online in maniera da porterci lavorare in team

Questo passaggio nella pratica clona la nostra repo locale, su un servizio di hosting in questo **GitHub**(ci permette di creare cloni della nostra repo locale in remoto), rendola accessibile online a tutto il nostro team

Le repository locoli e quelle in remoto(online), saranno collegate e aggiornando quella in locale potremo anche aggiornare quella in remoto o viceversa, tramite  git push o pull

Passaggi per collegare le repository locale alla repo in remoto su git hub:

1. `ssh-keygen`:comando da digitare nella home(~), dare invio fino alla generazione delle chiavi ssh:

* `ls-a` che si sia generata una cartella .ssh(conterra le chiavi)
* `cd .ssh`:entriamo nella cartella
* `ls`: i file *id_rsa* e *id_rsa.pub* contengono le chiavi ssh, utilizzare quella pubblica
* `cat id_rsa.pub`:stampare in console la chiave ssh, copiarla senza tralasciare ssa....

2. Andare su GitHub -> profilo -> settings -> ssh and gpg keys -> New ssh key -> assegnare un nome alla chiave e incollare la chiave ssh copiata -> add ssh key

###### Completato questo passaggio abbiamo collegato il nostro computer a gitHub

3. Per collegare la nostra repository locale a git hub, creiamo prima una nuova repository su git hub, poi come forma di collegamento selezioniamo chiavi `ssh` invece di `https`

* creo la repository locale e la salvo `git init`->`git add .`->`git commit -m''`

* su gitHub nella copiare i comandi dalla sezione push una repository esistente
- `git remote add origin <url>`: Aggiunge una nuova origine remota al repository, di fatto questo comando collega le due repo
- `git branch -M main`: rinomina il branch principale da master a main
- `git push -u origin main`: Carica il ramo locale sul repository remoto

**N.B** potevamo anche non rinominare il branch da name a master, ma in quel caso nel terzo comando va scritto il nome del branch master al posto di main

4. Comandi per aggiornare una repository in remoto o viceversa

* Aggiornare la repo in locale
`git status`:verifichiamo se ci sono modifiche non aggiunte alla repo locale, se ci sono modifiche non committate proseguo
`git add .`:traccio i file aggiornati e li aggiungo alla staged area
`git commit -m''`: salvo le modifiche nella repo locale

* Aggiornare la repo in remoto
`git push`: invio le modifiche fatte in locale alla repo online

* Aggiornare la repo locale
`git pull`: comando per predere le modifiche alla repo in remoto e passarle a quelle in locale

5. Quando lavoro con altre persone la **Best pratice** é lanciare questi comandi in sequenza:
* `git clone <url> `: Questo comando permette di copiare una repo in remoto in locale, prendendo l'url da GitHub sezione `<code>` e selezionando come metodo SSH, copiare l'url che compare e aggiungerlo al comando

###### **N.B** git clone copia anche la cartella del progetto non é necessario creane una apposita

* entro nella cartella del progetto clonato `cd <nome_progetto>`

* `code .`: apro il progetto

* Siccome é possibile che la repository in remoto sia stata aggiornata dal clone, prima di lanciare *git push* per aggiornare la repo in remoto con nostre eventuali modifiche, lanciare
`git pull`: mi permette di prendere l'ultima versione della repo remota, questa procedura puó dare origine a dei merge, in quel caso risolvere il merge e committare

* Se io modifico un file, prima salvo le modifiche nella repo locale, git add e git commit, git pull e poi infine `git push`
###### Se la nostra repo in locale non é aggiornata con l'ultima versione della repo in remoto, git bloccare il push fino a che le due repo non vengono allineate alla stessa versione, per questo é importante fare prima git pull per asssicurarsi di ció

6. Ricapitolando la comandi in sequenza
* `git status`: verificare lo stato della repo locale
* `git add .`: tracciare le modifiche
- `git commit -m`: salvare le modifiche
- `git status`:verifica che il commit sia andato a buon fine
- `git pull`: verifica se ci sono nuove versione, se ci sono committarle, in caso di **merge** risolvere i merge prima di committare
###### una best pratice in caso di merge se in dubbio, accettare entrambe le modifiche da vs code, piú semplice che risolvere il merge da terminale
- `git push`: salvare le proprie modifiche nella repo in remoto su GitHub



##### Vs code feedback, della repo
Vs code é la repository di vengono collegati insieme dopo la sua creazione, vicino ai file compariranno alcuni feedback testuali per indicarci lo stato dei file all'interno della repo
* Possiamo tenere traccia del numero di file modificati, dal contatore sul simbolo a tre pallini nella side bar
* M: file modificato
* U: file aggiornato
