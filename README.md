# Analisi e Predizione del Churn Clienti – Settore Telecomunicazioni

## Contesto e problema di business

Un’azienda di telecomunicazioni che offre servizi di telefonia mobile e internet sta registrando un aumento del tasso di churn, ovvero della percentuale di clienti che abbandonano il servizio.
Il churn rappresenta un problema rilevante poiché l’acquisizione di nuovi clienti è generalmente più costosa rispetto alla retention di quelli esistenti.

Il team marketing dispone di risorse limitate e non può contattare indiscriminatamente tutti i clienti. Diventa quindi necessario individuare in modo mirato i clienti più a rischio di abbandono, così da ottimizzare le azioni di retention e ridurre i costi operativi.

---

## Obiettivo del progetto

L’obiettivo del progetto è prevedere se un cliente abbandonerà il servizio, sulla base delle sue caratteristiche contrattuali e di utilizzo, al fine di supportare il team marketing nell’identificazione dei clienti a maggiore rischio di churn.

Il problema viene affrontato come un task di classificazione binaria, con output una probabilità di abbandono per ciascun cliente.

---

## Dataset utilizzato

L’analisi si basa sul dataset **Telco Customer Churn**, disponibile su Kaggle.
Il dataset contiene informazioni a livello cliente, tra cui:

* durata del rapporto con l’azienda (tenure)
* tipo di contratto
* servizi attivi
* costi mensili e totali
* variabili di pagamento

La variabile target indica se il cliente ha abbandonato o meno il servizio.

---

## Approccio e metodologia

Il progetto segue un processo strutturato composto dalle seguenti fasi:

1. Comprensione del contesto di business e definizione del problema
2. Analisi esplorativa dei dati (EDA) per osservare la distribuzione del churn e le differenze tra gruppi di clienti
3. Preparazione dei dati e trasformazione delle variabili
4. Costruzione di un modello di classificazione interpretabile (Logistic Regression)
5. Valutazione delle prestazioni del modello
6. Interpretazione dei risultati in ottica business

L’obiettivo principale non è massimizzare la complessità del modello, ma ottenere risultati chiari, interpretabili e utilizzabili in un contesto aziendale.

---

## Struttura del repository

Il repository è organizzato come segue:

* `data/`

  * `raw/`: dataset originale non modificato
  * `processed/`: dataset puliti e pronti per la modellazione

* `notebooks/`

  * `01_business_understanding_and_eda.ipynb`
  * `02_feature_engineering_modeling.ipynb`
  * `03_business_insights_and_recommendations.ipynb`

* `tableau/`
  File Tableau utilizzato per la visualizzazione e lo storytelling dei risultati

* `reports/`
  Sintesi degli insight principali e considerazioni di business

* `README.md`
  Descrizione del progetto e guida alla lettura del repository

---

## Risultati principali

### Evidenze da analisi esplorativa

L’EDA mostra che il churn non è distribuito uniformemente, ma risulta più frequente in specifici segmenti:

* clienti con **contratto Month-to-month**
* clienti con **bassa tenure**
* clienti senza **Tech Support**
* clienti con **spesa mensile più elevata**, con interpretazione da considerare con cautela (possibile effetto combinato dei servizi attivi)

---

### Prestazioni del modello

È stato sviluppato un modello di **Logistic Regression**, con ottimizzazione orientata al **recall** per ridurre i falsi negativi (clienti a rischio non identificati).

| Modello       | Accuracy | Precision | Recall |
| ------------- | -------- | --------- | ------ |
| Baseline      | 0.81     | 0.66      | 0.56   |
| Modello tuned | 0.74     | 0.50      | 0.78   |

Il modello finale sacrifica parte della precision e dell’accuracy per aumentare significativamente il recall, risultando più adatto a un contesto in cui è prioritario intercettare clienti a rischio.

---

### Insight dal modello

L’analisi dei coefficienti e degli errori evidenzia che:

* il **contratto Month-to-month** è associato a maggiore rischio di churn
* una maggiore **tenure** è associata a una minore probabilità di abbandono
* i contratti a lungo termine (es. **Two year**) risultano legati a una maggiore stabilità
* alcune variabili di spesa e servizi riflettono configurazioni di offerta più che effetti diretti sul churn

---

### Error analysis

L’analisi degli errori mostra che:

* i **falsi positivi** sono prevalentemente clienti con tenure bassa e contratti flessibili
* i **falsi negativi** presentano caratteristiche più eterogenee, rendendo più difficile la loro identificazione

Questo suggerisce che il modello tende a identificare correttamente i profili più evidenti di churn, ma incontra maggiori difficoltà su segmenti meno chiari.

---

### Implicazioni di business

I risultati suggeriscono alcune possibili direzioni operative:

* focalizzare le campagne di retention sui clienti con **contratti Month-to-month e bassa tenure**
* incentivare la migrazione verso contratti a lungo termine
* approfondire i segmenti meno chiaramente identificati dal modello

Queste indicazioni devono essere considerate come ipotesi operative da validare ulteriormente.

---

## Strumenti utilizzati

* Python
* Pandas, NumPy
* Matplotlib / Seaborn
* scikit-learn
* Tableau (per la visualizzazione dei risultati)

---

## Nota sull’utilizzo di strumenti di supporto

Nel corso del progetto sono stati utilizzati strumenti di intelligenza artificiale come supporto al processo di apprendimento, riflessione e strutturazione dell’analisi.

In particolare, tali strumenti sono stati impiegati per:
- chiarire concetti metodologici,
- migliorare la formulazione dei testi descrittivi,
- supportare l’organizzazione del progetto e delle sue sezioni.

Le scelte analitiche, l’interpretazione dei risultati e le decisioni di modellazione sono state effettuate in modo consapevole e autonomo, con l’obiettivo di sviluppare un progetto coerente, comprensibile e difendibile in un contesto di business.

