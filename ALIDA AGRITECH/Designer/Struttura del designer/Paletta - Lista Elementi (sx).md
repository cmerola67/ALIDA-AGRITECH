# Paletta - Lista Elementi (sx)

Sul lato sinistro dell'interfaccia si trova la palette degli elementi utilizzabili attraverso drag and drop nel Designer, divisa in tre tab

- **Services**: l'elenco dei microservizi disponibili da utilizzare nel workflow.

![image.png](Paletta%20-%20Lista%20Elementi%20(sx)/image.png)

- **Datasets**: i dataset registrati sulla piattaforma.

![image.png](Paletta%20-%20Lista%20Elementi%20(sx)/image%201.png)

- **Models**: i modelli di machine learning disponibili.

![image.png](Paletta%20-%20Lista%20Elementi%20(sx)/image%202.png)

Per tutte e tre le sezioni della palette è possibile:

- Scorrere l'elenco su più pagine.
- Utilizzare la **barra di ricerca** per trovare rapidamente il dataset desiderato.
- Trascinare i dataset direttamente nel canvas per utilizzarli come input dei workflow.

### Service

Qui si trova l'elenco dei **servizi disponibili**, ciascuno rappresentato con un piccolo riquadro arancione che contiene:

- Il nome del servizio (es: `PROCESSOR-TESTER`, `LINGOJAM-TRANSLATOR`, `TF-REGRESSOR-MLFLOW`)
- La versione del servizio (es: `1.0.1`, `1.0.2`)

È possibile scorrere le pagine per cercare il servizio desiderato oppure usare la **barra di ricerca**.

All'interno del pannello **Services** del Designer, ALIDA offre la possibilità di **filtrare i servizi** disponibili secondo il concetto di **Area**.

![image.png](Paletta%20-%20Lista%20Elementi%20(sx)/image%203.png)

Cliccando sull'icona del filtro, si apre un menù a tendina dove è possibile selezionare diverse aree funzionali, tra cui:

- **INGESTION**: servizi per l'acquisizione di dati.
- **PREPARATION**: servizi per la preparazione e la pulizia dei dati.
- **PROCESSING**: servizi di elaborazione.
- **ANALYSIS**: servizi di analisi dati.
- **VISUALIZATION**: servizi per la rappresentazione grafica dei dati.
- **EVALUATION**: servizi di valutazione delle performance.
- **FML AGGREGATOR** e **FML PARTICIPANT**: servizi dedicati alla gestione di flussi di federated machine learning.

Questo filtro consente di **navigare più facilmente** l'elenco dei servizi e di **selezionare rapidamente** solo quelli pertinenti all'area di interesse del workflow che si sta costruendo.

### Dataset

Quando si seleziona la categoria **Datasets** nel pannello sinistro del Designer, ALIDA mostra l’elenco dei dataset disponibili.

![image.png](Paletta%20-%20Lista%20Elementi%20(sx)/image%204.png)

I dataset sono rappresentati con **riquadri verdi**, ognuno dei quali include:

- **Nome del dataset** (ad esempio: `TESTER`, `SCIKIT-LEARN/AUTO-MPG`, `IRIS`).
- **Tipo**: indicato come `TABLE`, che rappresenta un dataset strutturato tabellare.

### Model

Quando selezioni la categoria **Models** nel pannello sinistro del Designer, ALIDA mostra l’elenco dei modelli disponibili.

![image.png](Paletta%20-%20Lista%20Elementi%20(sx)/image%205.png)

I modelli sono rappresentati con **riquadri blu** e ogni riquadro contiene:

- **Nome del modello** (ad esempio: `MODEL CREATED BY TEST MLFLOW`, `MODEL CREATED BY KNN ON NOCC`).
- **Data e ora di creazione** del modello.