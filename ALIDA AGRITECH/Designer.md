# Designer

## Il Designer di ALIDA

Il **Designer** è la sezione visiva della piattaforma ALIDA dedicata alla **creazione di applicazioni** (workflow) in modo semplice e intuitivo.

## Benefici del Designer

- **Costruzione visuale intuitiva:** Creazione di workflow tramite semplice drag & drop dei componenti, eliminando la necessità di scrivere codice.
- **Flessibilità nei flussi di lavoro:** Supporto per workflow ramificati e complessi, permettendo esecuzioni parallele e aggregazioni multiple.
- **Identificazione immediata dei componenti:** Distinzione chiara tra dataset, servizi e modelli attraverso codici colore e forme specifiche.
- **Connessioni intelligenti:** Verifica automatica della compatibilità tra input e output durante il collegamento dei blocchi.
- **Gestione centralizzata:** Controllo completo su metadati e configurazioni dell'applicazione attraverso il pannello laterale.
- **Configurazione avanzata integrata:** Possibilità di personalizzare dettagliatamente ogni servizio direttamente nel Designer.

# Porte di Input e Output dei Servizi

Ogni servizio nel Designer di ALIDA è caratterizzato da specifiche porte di input (poste sulla parte superiore del blocchettino) e output (sulla parte inferiore) che ne definiscono le interfacce di comunicazione. I colori e le forme delle porte indicano il tipo di collegamento consentito:

- **Porte di Input (IN):** Rappresentano i punti di ingresso dei dati nel servizio, posizionate nella parte superiore del blocco. Possono accettare diversi tipi di dati come:
    - 🟢 **Tondo Verde**: Dataset
    - 🔵 **Tondo Blu**: Modelli di machine learning / matematici
    - 🟪 **Quadrato Viola**: Flusso dati streaming
    - 🟩 **Rettangolo Verde**: *Generic I/O*
    - 🟨 **Giallo**: Chiamata REST API
- **Porte di Output (OUT):** Posizionate nella parte inferiore del blocco, definiscono i risultati prodotti dal servizio dopo l'elaborazione. Possono generare dataset trasformati, modelli addestrati o metriche di valutazione, seguendo lo stesso schema di colori delle porte di input.

### Caratteristiche delle Porte

- **Compatibilità tipizzata:** Le porte seguono un sistema di tipizzazione che garantisce la compatibilità tra le connessioni. Solo porte con tipi compatibili possono essere collegate tra loro.
- **Feedback visivo:** Durante il collegamento, il Designer fornisce feedback immediato sulla compatibilità delle porte, evidenziando in verde le connessioni valide e in rosso quelle non valide.
- **Multi-porta:** Alcuni servizi possono avere multiple porte di input o output, permettendo operazioni complesse come l'aggregazione di dati o la distribuzione dei risultati.

<aside>
La chiara definizione delle porte di input e output rende intuitiva la costruzione dei workflow, prevenendo errori di collegamento e garantendo la corretta propagazione dei dati tra i servizi.

</aside>


[Struttura del designer](Designer/Struttura%20del%20designer.md)


<br>

<br>

[**HOME**](../ALIDA%20AGRITECH.md)