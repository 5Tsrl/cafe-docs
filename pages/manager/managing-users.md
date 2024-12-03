---
title: Gestione utenti
parent: Manager
---


# Gestione utenti

### Concetti generali

Ogni utente di Transit Café ha un account gestito tramite *Auth0*, un servizio di autenticazione di terze parti.
L'account usa un'autenticazione di tipo  username-password, in cui l'indirizzo mail dell'utente è utilizzato come unico username.

Per la creazione di nuove utenze si prega di inoltrare la richiesta a cafe@5t.torino.it.

### Permessi dell'utente

Transit Café utilizza un sistema di permessi utente per regolamentare l'accesso alle varie funzioni dell'applicazione. Gli utenti possono essere di tipo amministratore e non amministratore.

##### Utenti amministratori

Ci sono due tipi di utenza per il livello amministratore:

- *Amministratore a livello dell'applicazione*: ha pieno accesso alle funzionalità dello strumento, incluso l'accesso a tutti i progetti e tutti i feed, la capacità di creare nuovi progetti, di creare e gestire utenti.
- *Amministratore (a livello di progetto)*: ha pieno accesso ad un singolo progetto. Non è abilitato alla creazione di nuovi progetti o all'amministrazione di utenti.

##### Utenti non amministratori

Per gli utenti non amministratori, i permessi possono essere assegnati su base individuale scegliendo l'opzione `Personalizzato`. I permessi di utenti non amministratori possono essere applicati solo a livello di feed in un progetto. Tutti gli utenti con accesso ad un progetto hanno accesso di sola lettura a tutti i feed del progetto come default. Selezionando il feed e/o la tipologia di permesso è possibile personalizzare ulteriormente l'accesso ai dati. I permessi disponibili sono:

- *Gestisce configurazione feed*: possibilità di modificare le impostazioni del feed dal tab `Impostazioni`;
- *Modifica feed nell'editor*: possibilità di modificare il dato nell'editor.

![zoom](../img/user-admin-detail.png)

In caso non sia selezionato alcun permesso per il tipo di accesso personalizzato, l'utente potrà solo visualizzare quanto presente nel manager.

##### Esempi permessi utente

1. Un utente potrebbe aver bisogno di modificare i privilegi di un feed: in questo caso saranno selezionati `Modifica feed GTFS` e il feed in questione (es. Ente X).
2. Gli enti potrebbero aver bisogno di garantire l'accesso ad alcuni utenti in modo da poter visualizzare reportistica di base (visibile nella parte manager), ma senza fornirgli la possibilità di modificare o gestire nulla nell'applicativo. In questo caso, si dovrà selezionare `Personalizzato`, senza indicare altri permessi o feed.

### Gestione utenti

Per creare nuovi utenti, è necessario inoltrare la richiesta alla mail cafe@5t.torino.it ed indicare nome, cognome e indirizzo email della persona da abilitare allo strumento.
Una volta creata l'utenza, verrà inviata una email automatica di conferma all'indirizzo email fornito.

## Le mie impostazioni

### Profilo

In questa sezione è possibile gestire alcune funzionalità legate alla singola utenza:

- *Indirizzo email*: la mail usata come username dall'utente;
- *Avatar*: associazione di un avatar all'utente corrente utilizzando [Gravatar](http://it.gravatar.com/);
- *Password*: gestione del cambio password.

#### Reset della password

Hai dimenticato la password o hai bisogno di modificarla? Quando non hai ancora eseguito l'accesso, clicca su `Accedi` e poi `Non ricordo la password`. Dopo aver inserito la mail associata al tuo account utente, ti sarà inviata una mail contenente un link per resettare la password.

![screenshot](../img/password-reset-logged-out.png)

Hai già eseguito l'accesso, ma vuoi cambiare la password? Clicca sul'icona dell'utente (Account) in basso a sinistra nella sidebar e clicca `Il mio profilo`. Seleziona il tasto `Cambia password` per inserire il tuo indirizzo email.

![screenshot](../img/password-reset-logged-in.png)
