---
title: Feed
parent: Manager
---

# Feed

### Crea un feed

Un feed può essere creato dalla pagina principale di un progetto selezionando il tasto `Azioni`. Sono disponibil diverse opzioni:

- *Nuovo*: crea nuovo feed;
- *Aggiorna tutto*: aggiorna i feed automaticamente, utilizzabile solo se è indicata una url per il download automatico della base dati;
- *Unisci tutto*: unisce in un unico feed le basi dati presenti nel progetto;
- *Scarica il sommario come csv*: scarica come csv i dati visualizzati nella schermata.

![screenshot](../img/actions.png)

Cliccando sul tasto `Nuovo` si aprirà una pagina dedicata alla nuova base dati: digita il nome del feed e salva.

È presente anche un'opzione che permette di impostare un eventuale prelievo automatico della base dati da una URL per mantenere sempre il feed aggiornato: questa opzione è sconsigliata nella modifica di un PEA.

![screenshot](../img/create-feed.png)

### Gestire i feed

Dopo aver creato un feed, questo apparirà nell'elenco dei feed nel progetto: selezionandolo, si apre una pagina di dettaglio che analizza la base dati.

Nella parte superiore della schermata sono presenti una serie di schede, che includono:

- **Versioni**: punto di accesso ai feed;
    - *Sommario della versione:* vedi informazioni sul feed, ad esempio linee, percorsi e fermate;
    - *Problemi di validazione:* vedi e filtra una lista di anomalie emerse in fase di validazione;
    - *Commenti alla versione:* scrivi e vedi i commenti su una specifica versione di un feed.
- **Snapshot**: lista degli snapshot (o punti di salvataggio);
- **Note**: area in cui gli utenti possono scrivere e leggere commenti su un feed;
- **Impostazioni**: accesso alle impostazioni di un feed.

![screenshot](../img/summary-feed.png)

Per vedere le impostazioni per uno specifico feed, clicca sul tab `Impostazioni`. Da questa sezione è possibile:

- modificare le proprietà di base di un feed (es. nome, aggiornamento tramite URL);
- eliminare un feed (per gli utenti con particolari permessi) dall'area `Zona pericolosa`.

![screenshot](../img/feed-settings.png)


### Crea una versione di un feed

Le versioni sono create dalla pagina del feed.

![screenshot](../img/create-version-feed.png)

Sono disponibili tre opzioni per questa operazione:

a. **Aggiorna da URL**: Seleziona `Recupera` dalla tendina `+ Crea nuova versione`.

*Nota:* per recuperare una nuova versione, nel campo `Prelievo automatico del feed da URL` deve essere impostata una URL valida in `Feed → Impostazioni`.

b. **Caricare manualmente un file**: Seleziona `Carica` dalla tendina `+ Crea nuova versione`. Clicca su `Scegli file` per selezionare un file GTFS disponibile in locale e importalo nel sistema.

![screenshot](../img/load-version.png)

Selezionando `Modifica feed in Editor`, si può scegliere se importare anche nella parte editor il dato presente nel manager selezionando `Importa l'ultima versione`, o se creare un nuovo file da zero e trascurare il file del manager selezionando `Inizia da zero`.

Per utilizzare il PEA precaricato sul sistema è necessario selezionare `Importa l'ultima versione`.

![screenshot](../img/editor-from-scratch.png)

c. **Importa da Editor**: Seleziona `Da snapshot` dalla tendina `+ Crea nuova versione`e sarà visualizzata la lista degli snapshot disponibili per il feed in analisi. Seleziona lo snapshot desiderato e clicca il tasto `Promuovi a versione` per pubblicare lo snapshot come nuova versione.

*Nota:* quando si carica o recupera da una URL un feed e il file caricato o recuperato non è differente dall'ultima versione, non vengono create nuove versioni del feed.


### Caricare versioni di un feed nell'editor

Selezionando il tasto `Carica versione nell'Editor`, verrà importata nell'editor la versione in analisi di un feed. In caso i dati presenti nell'editor differiscano da quelli che si vogliono visionare, si aprirà una finestra popup indicante la sovrascrizione dei dati precedenti. Per poter vedere i dati aggiornati nella parte manager, è necessario caricare l'ultima versione di una base dati nell'editor.

![screenshot](../img/load-version-editor.png)

### Vedere e gestire versioni di un feed

Il navigatore di versioni permette di visualizzare le versioni disponibili di un feed specifico usando i tasti `←` e `→`. Dall'interfaccia è anche possibile:

- scaricare una versione del feed in locale in formato GTFS;
- caricare una versione nell'editor;
- eliminare una versione di un feed dal manager. (*Nota:* la cancellazione di una versione del feed non può essere annullata.)

![screenshot](../img/feed-version-navigator.png)

Nella parte sinistra dello schermo è presente una lista di opzioni disponibili per la versione corrente del dato, ad esempio statistiche di base sul feed, un dettagliato report di validazione e i commenti degli utenti su un feed.

### Accesso in sola lettura

Selezionando il tasto `Accedi in sola lettura` è possibile accedere all'editor e  visualizzare la stessa base dati già aperta da un altro utente in modifica.

![screenshot](../img/manager-read-only.png)

Ogni feed può essere aperto e modificato nell'editor da un solo utente alla volta; viene infatti attivato un blocco temporaneo per la base dati di interesse per evitare conflitti nelle modifiche. In caso di tentativo di accesso alla stessa base dati da parte di un altra persona, verrà visualizzato un messaggio di avvertimento con l'indicazione dell'utente già attivo. Dopo 9 minuti in cui non si effettuano modifiche ai dati, il blocco viene rimosso automaticamente ed il feed torna disponibile per la modifica da parte di altri utenti.

![zoom](../img/blocked-feed.png)

Questa funzionalità è particolarmente utile quando 2 utenti differenti hanno necessità di aprire la stessa base dati: un utente potrà modificare il dato nell'editor, l'altro potrà accedervi ma non avrà la possibilità di salvare o modificare nulla.
L'accesso in sola lettura viene indicato nell'editor con una banda rossa attigua alla barra laterale degli strumenti.  

![screenshot](../img/read-only.png)

Per fare in modo che l'utente in sola lettura possa visualizzare le modifiche effettuate dall'utente in scrittura, è necessario che quest'ultimo faccia uno snapshot. L'utente in lettura potrà quindi aprire nel suo editor lo snapshot di interesse e visualizzare le modifiche.

### Ulteriori funzionalità

Dalla pagina `Versione` si può accedere alla funzionalità di scaricamento del dato presente nel manager:

- selezionando `Download versione`, è possibile scaricare il feed in formato *GTFS* (classico) o *GTFS +* (contenente i campi aggiuntivi previsti dal PEA);

 ![screenshot](../img/export-gtfs.png)

- selezionando `Esporta shapefile`, è possibile scaricare in formato shapefile le fermate o la geometria dei percorsi delle linee visualizzate dal manager.

 ![screenshot](../img/export-shp.png)
