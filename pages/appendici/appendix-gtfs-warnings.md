---
title: Glossario degli errori
parent: Appendici
nav_order: 1
---

# 1- Errori di validazione

Gli errori sono consultabili dagli utenti nella sezione dedicata nel manager. La correzione delle segnalazioni non può avvenire nel manager ma solo in fase di modifica del feed.

![img](/img/overview-data-validation.png)

Di seguito sono riportati alcuni degli errori più comuni:

##### Corse spurie nel percorso
Alcuni percorsi risultano avere al loro interno delle corse con km contrattuali diversi da quelli riportati nel percorso. Valutare se spostare tali corse in nuovi percorsi.

*Questo errore deve necessariamente essere corretto ai fini di una corretta gestione del feed.*

##### Codici corsa duplicati a livello di linea
Alcune linee risultano avere corse con codice corsa duplicato. È necessario che il codice corsa sia univoco all'interno di una linea.

*Questo errore deve necessariamente essere corretto ai fini di una corretta gestione del feed.*

##### Codici corsa duplicati a livello di percorso
Alcuni percorsi risultano avere corse con codice corsa duplicato. È necessario che il codice corsa sia univoco all'interno di un percorso della linea.

*Questo errore deve necessariamente essere corretto ai fini di una corretta gestione del feed.*

##### Calendari duplicati
Alcuni calendari risultano avere la stessa definizione di giorni di servizio. Sarebbe opportuno evitare la proliferazione dei calendari.

*È consigliabile evitare di creare calendari uguali tra loro. All'appendice 3 - Nomenclatura calendari si possono trovare maggiori informazioni sull'argomento*

##### Tempo di viaggio nullo
Il veicolo arriva alla fermata allo stesso orario in cui parte dalla precedente.

*Questo errore può essere trascurato in caso di fermate molto vicine, in cui varia solo la cifra relativa ai secondi.*

##### Tempo di viaggio negativo
Il veicolo arriva a questa fermata prima di partire dalla precedente.

*È consigliabile controllare la correttezza degli intertempi e degli orari di partenza e sosta in una fermata.*

##### Data senza servizio
Non vi sono service_id attivi per una data compresa nell'intervallo di date con un servizio definito.

*Questo errore può essere trascurato in caso vi siano giorni in cui non è attivo il servizio di trasporto.*

##### Fermata in area a bassa densità abitativa
Una fermata è posizionata in un'area geografica con una bassa densità di popolazione.

*Questo errore può essere trascurato in caso il posizionamento della fermata sia corretto.*

##### Tragitto troppo lento
Il veicolo sta viaggiando molto lentamente per raggiungere la fermata rispetto a quella precedente.

*Questo segnalazione è sintomo di una errata velocità commerciale rispetto a quanto ammissibile per il tipo di strada. È consigliabile controllare gli intertempi tra le fermate.*

##### Tragitto troppo rapido
Il veicolo sta viaggiando molto velocemente per raggiungere la fermata rispetto a quella precedente.

*Questo segnalazione è sintomo di una errata velocità commerciale rispetto a quanto ammissibile per il tipo di strada. È consigliabile controllare gli intertempi tra le fermate.*

##### Fermata non utilizzata
La fermata non è utilizzata da alcuna corsa.

*Questo errore è presente in ogni feed di Transit Café, in quanto sono presenti tutte le fermate regionali all'interno di ogni feed.*

##### Il nome breve della linea e il nome esteso sono vuoti
Una linea non ha il nome breve della linea o il nome esteso.

*Sia il nome breve che il nome esteso sono richiesti dalle specifiche GTFS.*

##### Il nome breve di una linea è troppo lungo
Il campo nome breve di una linea ha troppi caratteri.

*Il nome breve di una linea non dovrebbe contenere più di 3-4 caratteri, dato che le applicazioni che usano il GTFS potrebbero usare il nome breve in contesti in cui vi sono limiti di spazio per il testo (es. etichette su una mappa).*

##### Il nome esteso della linea contiene il nome breve
Lo nome breve di una linea è incluso nel nome esteso.

*Il nome esteso della linea non deve contenere il nome breve, dato che le applicazioni che usano il GTFS potrebbero combinare il nome esteso e quello breve per un nome combinato (es. una linea con nome breve “A” e nome esteso “Dora Express” può essere indicata come “A - Dora Express”).*

##### La descrizione della linea è uguale al nome della linea
La descrizione e il nome di una linea sono identici.

*La descrizione è un campo opzionale e dovrebbe essere incluso solo se fornisce informazioni aggiuntive oltre a ciò che è incluso nel nome della linea.*

##### Tipo mezzo che opera la linea non valido
Un tipo mezzo specificato non corrisponde a nessuno dei valori di tipo mezzo definiti da GTFS.

*I valori accettati per il campo in analisi sono definiti nelle specifiche del GTFS e attualmente includono 8 differenti modalità di trasporto (tram, metropolitana, treno, bus, traghetto, funivia, funicolare).*

##### Nessun orario per la corsa
Una corsa non contiene informazioni sui passaggi in fermata.

*Questo indica che le informazioni sugli orari per questa corsa non sono corrette.*

##### Orario partenza prima dell'arrivo
Una corsa inizia una fermata prima del suo termine.

*Questo indica che le informazioni sugli orari per questa corsa non sono corrette.*

##### Passaggio in fermata non in sequenza
Una corsa arriva prima di partire dalla fermata precedente.

*Questo indica che le informazioni sugli orari per questa corsa non sono corrette.*

##### Corsa duplicata
Due o più corse condividono la stessa sequenza di fermate e orari di partenza.

*Questo indica che ci possono essere corse duplicate.*

##### Corse sovrapposte nel block
Due o più corse con sovrapposizione di un block.  

*Un block rappresenta una sequenza di corse operate da un singolo veicolo, e il block ID è un campo opzionale che indica a blocco appartiene il veicolo. Se la numerazione del block è usata nella registrazione della corsa, e due o più corse si sovrappongono nel tempo ma condividono un comune block ID, allora questo indica o la presenza di informazioni sbagliate sugli orari programmati o block ID non corretto .*

##### Fermate duplicate
Due fermate hanno la stessa posizione in un feed.

*Considera di unire le fermate che condividono la stessa posizione o usa la gerarchia stazione/fermata per specificare le posizioni di un gruppo di fermate.*

##### Tracciato geometrico della corsa al contrario
La direzione del tracciato geometrico della corsa non corrisponde a quella della sequenza di fermate.

*Invertire o correggere lo shape della corsa in modo da adattarsi all'ordine delle fermate di questa corsa.*

##### Geometria mancante
La corsa non ha un tracciato geometrico di riferimento.

*Gli shape sono opzionali ma raccomandati.*
