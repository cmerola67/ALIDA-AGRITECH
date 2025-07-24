# Dettagli elementi (dx)

Questa porzione del designer contiene il dettaglio del workflow o di ciò che si è selezionato:

Se non si è selezionato nulla si vedranno le informazioni del workflow, come

- **Name**: il nome dell'applicazione
- **Description**: una descrizione testuale facoltativa
- **Tags**: parole chiave utili per la categorizzazione
- **Access Level**: il livello di visibilità (ad esempio Team o Public)
- e il tasto Create Application per salvare l’applicazione

Quando invece si clicca un elemento del designer la parte destra del designer si popola con le caratteristiche del blocchetto selezionato. Entriamo nel dettaglio con qualche esempio:

## Selezionando un dataset

![image.png](Dettagli%20elementi%20(dx)/image.png)

Quando si seleziona un dataset nel designer di ALIDA, il pannello informativo sulla destra mostra i **dettagli strutturali e funzionali del dataset**. Questo permette di comprendere immediatamente il contenuto e la tipologia dei dati disponibili.

Il pannello mostra le seguenti informazioni:

### **1. Nome del Dataset**

- Visualizzato in alto in grassetto, ad esempio: `IRIS`

### **2. Tipo**

- Indica il tipo di asset, in questo caso **Type: table**

### **3. Data Source**

- Indica la sorgente dati del dataset. Nel nostro esempio, **Data Source: public** significa che il dataset risiede in una sorgente dati pubblica, accessibile a tutti gli utenti della piattaforma.
- Nota: Elemento cliccabile, al clicca rimanda al dettaglio del datasorce, in questo caso:
    
    ![image.png](Dettagli%20elementi%20(dx)/image%201.png)
    

### **4. Dataset Columns**

- Mostra l'elenco delle colonne del dataset con i rispettivi tipi di dato:
    - **Name**: nome della colonna
    - **Type**: tipo di dato (es. `Number`, `String`, ecc.)
- L'esempio include le seguenti colonne:
    - `sepal_length` (Number)
    - `sepal_width` (Number)
    - `petal_length` (Number)
    - `petal_width` (Number)
    - `variety` (String)

### 5. Pulsante "Show Preview"

Dove il formato e lo storage lo consentono (ad esempio per i dataset tabellari su Minio), è possibile visualizzare un'anteprima del dataset.

![image.png](Dettagli%20elementi%20(dx)/image%202.png)

## Selezionando un Modello

Quando si seleziona un blocco modello (colore blu) all'interno del designer di ALIDA, il pannello laterale destro mostra una serie di informazioni descrittive e tecniche relative a quel modello. Queste informazioni aiutano l’utente a comprendere l’origine del modello, i dati su cui è stato costruito, e il contesto applicativo.

![image.png](Dettagli%20elementi%20(dx)/image%203.png)

Ecco i campi visibili nel pannello:

### **1. Nome del Modello**

- Visualizzato in alto in grassetto. In questo esempio:
    
    `MODEL CREATED BY AMT – AUTONOMY FORECASTING ANALYTICS`
    
- È accompagnato da una breve descrizione esplicativa sulla provenienza del modello, utile per il contesto.

### **2. Algorithm**

- Indica l’algoritmo di machine learning utilizzato per addestrare il modello. Nell’esempio: tf-regressor-mlflow (un modello di regressione sviluppato con TensorFlow e tracciato tramite MLflow)

### **3. Input Columns**

Elenco delle colonne del dataset utilizzate come input nel modello.
In questo caso: sepal_length, sepal_width, petal_length e petal_width.

### **4. Dataset**

- Mostra il nome del dataset di origine utilizzato per l’addestramento del modello.
    
    Nell’esempio, si tratta del dataset: iris
    
- Nota: Cliccando su questo elemento, l’utente può esplorare il dataset collegato.
    
    ![image.png](Dettagli%20elementi%20(dx)/image%204.png)
    

### **5. Application / Workflow**

- ID o riferimento all'applicazione o workflow originario in cui è stato creato il modello. In questo caso: **73018**
- Nota: cliccabile per accedere al contesto di creazione del modello
    
    ![image.png](Dettagli%20elementi%20(dx)/image%205.png)
    

### **6. Data Source**

- Indica la visibilità della sorgente dati che ospita il modello.
    
    Nell'esempio è:
    
    **public**, quindi disponibile a tutti gli utenti della piattaforma.
    

## Selezionado un Service

Quando si seleziona un **service** nel designer di ALIDA (identificabile dal colore salmone), il pannello laterale destro mostra le informazioni sulla configurazione e i parametri del microservizio.

![image.png](Dettagli%20elementi%20(dx)/image%206.png)

Attraverso questa vista, l'utente può personalizzare l'esecuzione del servizio e comprenderne il funzionamento.

- **Pannello di configurazione avanzata sulla destra**: Quando selezioni un **blocco** (in questo caso un servizio `SKLEARN-MODEL`), il pannello laterale destro **non mostra solo informazioni generali**, ma permette di **configurare i parametri interni** del servizio.

➔ Si vedono ad esempio:

- Il nome della label di classificazione (`LabelColumn`).
- L'algoritmo scelto (`RandomForestClassifier`).
- I parametri di algoritmo (`algorithm_params`) come numero di alberi, profondità massima, ecc.
- I parametri di split del dataset (`train_test_split_args`).

### Caratteristiche Principali

- **Parametri con tipi flessibili**: I parametri dei servizi possono essere di vari tipi (stringhe, numeri, JSON, ecc.) definiti dal creatore del servizio, e sono **modificabili direttamente nell'interfaccia** senza necessità di scrivere codice esterno.
- **Parametri obbligatori e opzionali**: Lo sviluppatore del servizio può specificare quali parametri sono requirements (obbligatori) e quali sono opzionali, guidando così l'utente nella corretta configurazione.
- **Editing puntuale per ogni servizio**: Il Designer ti consente di **personalizzare ogni singolo blocco** con parametri molto specifici **senza uscire** dal canvas di disegno.
- **Immediato riscontro visivo**: Appena clicchi su un nodo, **vedi subito i suoi dettagli e puoi modificarli**. Non servono ricaricamenti o aperture di finestre esterne.

---

🛈 **Nota**: I parametri configurabili specifici del servizio sono divisi in due tab. I valori appartenente al tab Application saranno passati al service attraverso *args,* mentre quelli appartenenti al tab STATIC saranno passati come *variabili d’ambinte.* La scelta di come dividere i parametri dipende dalle considerazioni di chi ha sviluppato e registrato il servizio.