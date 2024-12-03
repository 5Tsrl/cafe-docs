---
title: Reportistica
parent: Manager
---

# Reportistica

### Introduzione

Dalla pagina del manager sono disponibili 3 documenti (report linee, report corse, report orari) che offrono una panoramica più completa sul servizio di trasporto descritto nei feed. Questi report sono disponibili in diversi formati:

- **Visualizzazione web**: è possibile navigare all'interno del feed selezionando la linea di interesse;
- **Csv**: permette di effettuare ulteriori analisi sui dati del feed utilizzando un foglio elettronico;
- **Pdf**: permette di creare un file pdf da allegare ad altra documentazione.

![img](../img/reports.png)

### Report linee

Il report comprende una tabella in cui sono indicate, per ogni linea appartenente al contratto di servizio analizzato, le seguenti informazioni:

- l'azienda che opera il servizio;
- il codice numerico della linea;
- il nome per esteso della linea;
- il numero di percorsi;
- il numero di corse;
- il tipo di linea (urbana/extraurbana);
- i km della linea previsti a contratto;
- i km contribuiti della linea;
- i km a conferma.

![img](../img/report-linee.png)

Sopra la tabella sono inoltre posizionati alcuni tasti che permettono di scaricare i dati visualizzati su web come csv (dati correnti, di preventivo e in proiezione) e in pdf.

Nell'intestazione del file pdf è inoltre indicato il periodo di validità del feed e il codice del contratto di servizio.

![img](../img/report-linee-pdf.png)


### Report corse

Nel report è necessario selezionare la linea di interesse (ed eventualmente il percorso), in modo da visualizzare l'azienda che effettua il servizio, il numero di km percorsi, contribuiti e a conferma.

Per ogni percorso è inoltre indicato il codice numerico, il nome esteso, la lunghezza in km del percorso e il tipo di servizio (urbano/extraurbano).

È possibile scaricare l'intera base dati dei percorsi del feed cliccando sul tasto `Scarica CSV completo`, oppure cliccando sul tasto `Scarica CSV della linea` saranno scaricate esclusivamente le informazioni della linea selezionata.

Sotto il tasto `Scarica CSV completo` è presente il link `Scarica stringhe calendari` che permette di scaricare in formato csv le stringhe calendario presenti nel feed.

![zoom](../img/download-calendar-string.png)

Questo file contiene:

- codice del calendario;
- n° di giorni di servizio;
- stringa composta di "1" (servizio attivo) o "0" (servizio non attivo) che descrive la frequenza del servizio.

Se non si seleziona una linea specifica, è possibile scaricare il file csv contenente tutte le linee esercite nel contratto di servizio.

Per ogni percorso della linea è disponibile una tabella che riporta informazioni su:

- codice corsa;
- calendario associato alla corsa;
- n° di giorni di servizio;
- indicazione se la corsa sia o meno contribuita;
- indicazione se la corsa sia o meno a conferma;
- totale km percorsi in riferimento ai giorni di servizio di una  corsa (km percorso x giorni di servizio);
- posti a sedere e posti in piedi;
- inizio e fine validità calendario, indicate in grigio se fanno riferimento all'intero anno (default 01/01 - 31/12) e in nero se fanno riferimento a corse/percorsi versionate.

![img](../img/report-corse.png)

Il formato csv contiene inoltre l'indicazione dei giorni della settimana in cui è operativa la corsa.

Nell'intestazione del file pdf è indicato il periodo di validità del feed e il codice del contratto di servizio.

![img](../img/report-corse-pdf.png)


### Report orari

Nel report è necessario selezionare la linea di interesse (ed eventualmente il percorso), in modo da visualizzare l'azienda che effettua il servizio e alcune informazioni di dettaglio sulle corse.
Selezionando la linea di interesse, è possible visualizzare la lunghezza in chilometri di ogni percorso e il tipo di servizio.

![img](../img/report-orari.png)

Per ogni percorso della linea è disponibile una tabella che riporta informazioni su:

- la sequenza ordinata delle fermate della corsa;
- il codice fermata;
- il nome della fermata;
- il codice corsa;
- il calendario di riferimento;
- l'orario di partenza dalla fermata.

Il formato csv contiene inoltre l'indicazione della velocità commerciale della corsa.

Nell'intestazione del file pdf è indicato il periodo di validità del feed e il codice del contratto di servizio.

![img](../img/report-orari-pdf.png)
