---
title: Gestione dei dati
parent: Manager
nav_order: 1
---

# Gestione dei dati

Questa sezione fornisce informazioni generiche sui dati che compongono il PEA. Le basi dati sono suddivise in progetti, feed e snapshot, che verranno illustrati di seguito.

### Progetti

I progetti sono raccolte di feed e relativi versionamenti. Un progetto può, ad esempio, rappresentare una determinata area geografica e contenere tutti i contratti di servizio attivi nell'area. In Café viene associata l'icona di una cartella ad ogni progetto.

![zoom](../img/project-vs-feed.png)

### Feed

Ogni feed può essere identificato con un contratto di esercizio del PEA. Per visualizzare i feed presenti in un progetto è sufficiente cliccare su `Vedi nome_progetto`.

![screenshot](../img/overview-project.png)

Si apre quindi una pagina contenente una tabella con la lista dei feed disponibili e alcune informazioni aggiuntive:

- *informazioni sui feed*: riporta il nome e la data dell'ultimo aggiornamento. Può inoltre essere presente il simbolo 🔒, che indica se la base dati è stata pubblicata sul web o se è privata e disponibile solo in Café. Il default per questa opzione è *privata*;
- *stato*: fornisce informazioni sullo stato di validità del feed. Le opzioni possibili sono: attivo, in scadenza, scaduto, futuro;
- *date di validità*: indica gli estremi di validità della base dati in analisi;
- *errori*: indica la presenza di eventuali errori nel feed. Gli errori sono rilevati con riferimento alla struttura/correttezza di un file GTFS; per maggiori informazioni si prega di consultare la sezione [Errori di validazione](appendix-gtfs-warnings).

![screenshot](../img/feed-overview.png)

Al fondo di ogni riga della lista di feed è presente il tasto `Menu`, che permette di accedere alle seguenti opzioni:

1. **Apri nell'Editor**: apre il feed direttamente nell'editor per poter apportare  le modifiche necessarie;
2. **Aggiorna**: permette di aggiornare i feed per cui è disponibile una URL per il caricamento automatico. Questa funzionalità può essere utilizzata se è compilata la sezione *Prelievo automatico* nelle impostazioni del feed;
3. **Carica**: caricamento manuale di feed forniti da una fonte esterna al sistema o presenti in locale sul computer;
4. **Osserva**: permette di seguire gli aggiornamenti/modifiche relative ad uno specifico feed. Eventuali variazioni sulla base dati effettuate da un altro utente ad un feed osservato verranno tracciate nella homepage nella sezione `Notifiche`;
5. **Elimina**: elimina il feed caricato nel sistema e tutti i dati ad esso correlati (versioni e snapshot).

![screenshot](../img/upload-feed.png)


### Versione di un feed

Una *versione* di un feed rappresenta una variante contrattuale della base dati originale. Ogni versione ha un file GTFS associato e gestito in Transit Café: le versioni non più in uso sono visualizzabili nel navigatore di versioni e possono essere ripristinate nell'editor in ogni momento.

Per gli utenti è inoltre disponibile un report contenente dettagli sulla validazione del dato e una pagina in cui è possibile riportare commenti sulla base dati in analisi.

![zoom](../img/available-versions.png)

### Snapshot

Uno *snapshot* è una versione "di lavoro" di un set di dati e rappresenta un punto di salvataggio: può infatti essere usato come punto di partenza per modifiche future. È possibile creare uno *snapshot* cliccando sul simbolo della macchina fotografica in basso a destra nell'editor 📷.

Gli snapshot esistenti per un determinato feed sono raccolti nel tab `Snapshot`.

![screenshot](../img/make-snapshot.png)

Il tasto `Ribalta` è abilitato solo per gli utenti amministratori di sistema; gli altri utenti non potranno utilizzare questa funzionalità.
Uno snapshot può diventare una versione cliccando sul tasto `Promuovi a versione` nel tab `Snapshot`: con questa operazione lo snapshot scompare dall'elenco nel tab `Snapshot` e appare con lo stesso nome nell'elenco delle versioni.

![screenshot](../img/available-snapshots.png)

Per maggiori dettagli sulla creazione di uno snapshot e la promozione a versione, è possibile consultare il seguente *video tutorial*:

[![Snapshot e Versioni](../img/video-snapshot-versioni.png)](http://www.youtube.com/watch?v=RTKJdkwbokk "Tutorial Café 8 - Snapshot e Versioni")

#### Esempio di utilizzo delle versioni e degli snapshot

Nella cartella di lavoro è presente una base dati che rappresenta il PEA di interesse.
Vi è la necessità di modificare una linea, quindi si accede all'editor di Café. Si inizia a modificare il dato di interesse ma non si riesce a concludere il lavoro: in questo caso è consigliabile fare un salvataggio per poter riprendere il lavoro successivamente → uso uno *snapshot*.

![zoom](../img/add-snapshot.png)

Ci sono poi 2 possibili scenari:

1) *Promuovi a versione*: in un secondo momento si ha la possibilità di promuovere lo snapshot a versione contrattuale. Lo snapshot diventa una versione e scompare dall'elenco.

![zoom](../img/create-version.png)

2) *Ripristina nell'editor*: il procedimento da seguire per riprendere da dove si era interrotto il lavoro e completare le modifiche nell'editor è:

- cliccare sul tab `Snapshot` e selezionare lo snapshot che si era creato in precedenza;
- cliccare sul tasto `Ripristina nell'editor`;
- aprire l'editor, terminare le modifiche e creare un nuovo snapshot,
- cliccando nel tab `Snapshot` sul tasto `Promuovi a versione` si trasforma lo snapshot in versione;
- la nuova versione è accessibile dal manager.

![zoom](../img/snapshot-toolbar.png)

La seguente immagine riassume i possibili flussi di dati da snapshot, versioni e editor e i tasti da utilizzare.

![zoom](../img/version-vs-snapshots-editor.png)


Per maggiori dettagli sulla creazione di snapshot e versioni si consiglia di consultare la sezione [Feed](managing-feeds).
