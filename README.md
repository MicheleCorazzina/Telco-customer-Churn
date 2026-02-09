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
- durata del rapporto con l’azienda (tenure)
- tipo di contratto
- servizi attivi
- costi mensili e totali
- variabili di pagamento

La variabile target indica se il cliente ha abbandonato o meno il servizio.

---

## Approccio e metodologia
Il progetto segue un approccio strutturato end-to-end:

1. Comprensione del contesto di business e del problema analitico  
2. Analisi esplorativa dei dati (EDA) per comprendere la distribuzione del churn e le differenze tra segmenti di clientela  
3. Preparazione dei dati e feature engineering  
4. Costruzione di un modello di classificazione interpretabile  
5. Valutazione delle prestazioni del modello  
6. Interpretazione dei risultati in chiave business  

L’obiettivo principale non è massimizzare la complessità del modello, ma ottenere risultati interpretabili e utilizzabili in un contesto aziendale.

---

## Struttura del repository
Il repository è organizzato come segue:

- `data/`  
  - `raw/`: dataset originale non modificato  
  - `processed/`: dataset puliti e pronti per la modellazione  

- `notebooks/`  
  Notebook Jupyter utilizzati per l’analisi esplorativa, il feature engineering e la modellazione  

- `tableau/`  
  File Tableau utilizzato per la visualizzazione e lo storytelling dei risultati  

- `reports/`  
  Sintesi degli insight principali e considerazioni di business  

- `README.md`  
  Descrizione del progetto e guida alla lettura del repository  

---

## Risultati principali
L’analisi evidenzia come il churn non sia distribuito in modo uniforme tra i clienti, ma sia più concentrato in specifici segmenti, in particolare in relazione a:
- tipologia di contratto
- durata del rapporto con l’azienda
- livello di spesa mensile

Il modello di classificazione consente di stimare la probabilità di churn a livello individuale, supportando la definizione di strategie di retention mirate.

*(Questa sezione verrà aggiornata e dettagliata al completamento dell’analisi.)*

---

## Strumenti utilizzati
- Python  
- Pandas, NumPy  
- Matplotlib / Seaborn  
- scikit-learn  
- Tableau (per la visualizzazione dei risultati)

---

## Possibili sviluppi futuri
- Integrazione di dati temporali per una definizione più dinamica del churn  
- Confronto tra diversi modelli di classificazione mantenendo un focus sull’interpretabilità  
- Valutazione dell’impatto economico delle strategie di retention basate sulle previsioni del modello  


## Nota sull’utilizzo di strumenti di supporto

Nel corso del progetto sono stati utilizzati strumenti di intelligenza artificiale come supporto al processo di apprendimento, riflessione e strutturazione dell’analisi.

In particolare, tali strumenti sono stati impiegati per:
- chiarire concetti metodologici,
- migliorare la formulazione dei testi descrittivi,
- supportare l’organizzazione del progetto e delle sue sezioni.

Le scelte analitiche, l’interpretazione dei risultati e le decisioni di modellazione sono state effettuate in modo consapevole e autonomo, con l’obiettivo di sviluppare un progetto coerente, comprensibile e difendibile in un contesto di business.

