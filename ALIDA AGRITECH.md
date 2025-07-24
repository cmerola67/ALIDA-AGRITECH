# ALIDA AGRITECH

## Introduzione

ALIDA è una Data Science & Machine Learning Platform progettata per semplificare la gestione, l'esecuzione e il monitoraggio di progetti di data science e machine learning. La piattaforma offre un ambiente integrato che permette di:

- Gestire dataset e modelli di machine learning
- Creare, eseguire e monitorare workflow basati su microservizi
- Lavorare sia su dati batch sia su dati streaming
- Facilitare scalabilità e tracciabilità delle elaborazioni
- Permettere a utenti non esperti di sviluppo di creare applicazioni di analisi dati

## **Tipologie di Utenti (Attori)**

ALIDA è pensata per diversi tipi di utenti, ognuno con il suo ruolo e le sue necessità:

- Il **Citizen User** è chi, senza essere sviluppatore o data scientist, sfrutta l'interfaccia grafica per creare, configurare ed eseguire workflow in modo intuitivo.
- Il **Data Scientist** usa ALIDA per sviluppare modelli avanzati, impostare analisi sofisticate e ottimizzare pipeline di machine learning.
- Il **Data Engineer** si occupa dell'integrazione di nuove fonti dati, della gestione dei flussi e dell'ottimizzazione dei processi.
- L'**Administrator** gestisce utenti, permessi e configura i parametri operativi della piattaforma.
- Il **Developer** crea nuovi microservizi o integra API esterne, estendendo il catalogo di ALIDA.

## Concetti base

In ALIDA tutto ruota intorno ad alcuni concetti fondamentali:

- I **Servizi** sono microapplicazioni autonome che elaborano input e producono output.
- I **Workflow** sono sequenze di servizi che trasformano dati e modelli.
- Gli **Asset** rappresentano risorse fondamentali come dataset, modelli, sorgenti dati e i workflow stessi.

Ogni asset ha un livello di accesso:

- Private: visibile solo al proprietario
- Team: visibile e modificabile dai membri del team
- Public: visibile a tutti

> Nota: Regola di visibilità: i workflow "Team" non possono utilizzare asset "Private", e i workflow "Public" non possono utilizzare asset "Team" o "Private".
> 

## Project

Un Project è uno spazio di lavoro organizzato dove l'utente può raccogliere e gestire tutti gli elementi necessari per un determinato obiettivo o presentazione. Come una scrivania ben ordinata, un Project permette di:

- Raccogliere dataset, modelli, e workflow in un unico spazio
- Dare un nome significativo al progetto
- Accedere rapidamente a tutto il necessario per uno specifico caso d'uso
- Esempio pratico
    
    Project "Previsione Vendite 2025" che raccoglie dataset di vendita, modelli di regressione, e workflow di predizione.
    

## Workflow Designer

ALIDA offre un'interfaccia grafica per costruire workflow collegando service. 

Ogni service:

- Può essere collegato ad altri service attraverso archi
- Può essere collegato ad altri asset come dataset e modelli addestrati
- Riceve parametri configurabili (es. il valore di "K" per un K-Means)
- Può richiedere risorse specifiche (es. GPU per il training)

[Designer](ALIDA%20AGRITECH/Designer.md) 

> Nota: I microservizi possono essere sviluppati in qualsiasi linguaggio purché rispettino alcune regole minime per interoperare.
> 

## Esecuzione dei Workflow

Alida consente di:

- Eseguire manualmente un workflow cliccando "Run"
- Schedulare esecuzioni periodiche con espressioni cron
- Esportare il workflow in Docker Compose per l'esecuzione mediante docker (su una macchina locale, server etc)
- Scegliere il cluster di esecuzione da una lista di cluster Kubernetes federati disponibili

## Data source

Un data source in ALIDA è un metadato che contiene informazioni utili alla connessione ad uno storage (es. url, tipo di storage, chiavi di accesso etc…) 

Ogni utente registrato in piattaforma dispone di uno spazio personale dedicato alla gestione delle proprie risorse. Nel dettaglio, ALIDA mette a disposizione di default per ogni utente tre data source, basati su MinIO, ciascuno corrispondente a un diverso livello di accesso (PRIVATE, TEAM, PUBLIC), e un ulteriore data source per i topic Kafka, utile per la gestione dei flussi dati stream.

L’utente è libero di creare nuovi data source, puntando magari a storage esterni, allo scopo di rendere i propri dati visibili e facilmente gestibili all’interno della piattaforma.

## Sistema di Notifiche dei “Media” in Tempo Reale

Il Sistema di Notifiche dei “Media” in Tempo Reale è una funzionalità che permette agli utenti di monitorare l'avanzamento e lo stato delle loro elaborazioni. Gli **Eventi** sono aggiornamenti dinamici inviati dai servizi durante l'esecuzione allo scopo di informare l'utente in tempo reale sullo stato dei processi, l'avanzamento delle elaborazioni, e eventuali risultati intermedi o errori. Questo sistema è cruciale per:

- Monitorare lo stato di esecuzione dei workflow in tempo reale
- Identificare rapidamente problemi o errori durante l'elaborazione
- Visualizzare risultati intermedi senza attendere il completamento
- Prendere decisioni informate basate sul feedback immediato

### Architettura

1. Ogni service può emettere notifiche durante l'esecuzione
2. Le notifiche vengono inviate tramite Kafka su topic specifici
3. Un sistema di gestione:
    - Inoltra immediatamente le notifiche al browser via Server-Sent Events (SSE)
    - Salva tutte le notifiche nel catalogo, per consultazioni successive

<aside>
Non serve aggiornare la pagina per vedere le nuove notifiche.

</aside>

### Tipi di notifiche supportate

- Log di esecuzione
- Immagini (es. grafici, preview)
- Parametri aggiornati
- File compressi (es. .zip)
- File HTML
- Altro contenuto utile per il monitoraggio o il debug
- Esempio pratico
    
    Durante il training di un modello K-Means, il service invia ogni 10 iterazioni:
    
    - Un'immagine del clustering corrente
    - Un file di log con i valori di costo (inertia)
    - Un file ZIP con snapshot intermedi del modello
    
    L'utente vede tutto in tempo reale, direttamente nel browser.
    

## Storia degli Asset

ALIDA registra per ogni dataset o modello prodotto:

- Workflow che l'ha generato
- Service che l'ha elaborato
- Parametri utilizzati
- Storage di salvataggio
- Formato e caratteristiche tecniche

Questo permette auditing completo e riproducibilità dei processi.

- Esempio pratico
    
    Modello "Segmentazione Clienti 2025" salvato nello storage “S”, addestrato dal workflow “X”, con l’esecuzione del dd/mm/yyyy hh:mm:ss, dal service K-MEANS “Y”, (di version “V” creato dall’utente “U”)  con i parameti “A,B e C”, utilizzando i dataset “D” etc…
    

## Scalabilità

### Verticale

I service possono richiedere GPU.

ALIDA schedula automaticamente il deploy su nodi che dispongono di GPU.

- Esempio pratico
    
    Training di una rete neurale su immagini, deployato su nodo GPU.
    

### Orizzontale

I workflow batch intensivi possono essere distribuiti tramite Spark.

I dati vengono suddivisi in partizioni per elaborazione parallela.

## Federazione di Cluster

ALIDA supporta la federazione di cluster:

- Un workflow può essere eseguito in un cluster secondario federato tramite Liqo, che permette la condivisione dinamica delle risorse tra cluster Kubernetes
- L'utente seleziona il cluster federato di destinazione durante l'esecuzione del workflow, scegliendo tra i namespace disponibili

Vantaggi:

- Scalabilità inter-cluster
- Esecuzione vicino ai dati

## API REST

ALIDA fornisce API REST per:

- Creazione e modifica di asset
- Gestione di progetti
- Modifica dinamica di parametri di workflow
- Avvio di esecuzioni programmatiche
- Avvio di workflow con parametri nuovi
    - Esempio pratico
        
         via API (senza cambiare manualmente il designer): avvia il workflow “X” dopo aver modificato il parametro “K” (numero di cluster) da 3 a 5 del service “K-Means” all’interno del workflow.
        

## Architettura e Integrazione

ALIDA integra e coordina numerosi strumenti open source per fornire un ambiente completo di data science:

- MinIO per lo storage distribuito di dataset e modelli
- Kafka per la gestione di dati in streaming
- Spark per elaborazioni dati distribuite
- MLflow per il versioning e tracking di esperimenti
- Seldon per il deployment di modelli in produzione
- Argo per l'orchestrazione di workflow
- Jupyter Notebook per analisi interattive

L'architettura è basata su microservizi deployati su Kubernetes e supporta la federazione di cluster esterni per scalabilità e flessibilità.

[Designer](ALIDA%20AGRITECH/Designer.md)

[Guida Asset](ALIDA%20AGRITECH/Guida%20Asset.md)

[Overview UI](ALIDA%20AGRITECH/Overview%20UI.md)

[Architettura](ALIDA%20AGRITECH/Architettura.md)

[Casi d’uso](ALIDA%20AGRITECH/Casi%20d%E2%80%99uso.md)