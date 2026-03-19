# Report sintetico – Analisi del churn clienti

## Business problem
Un’azienda di telecomunicazioni che offre servizi di telefonia e internet sta registrando un aumento del tasso di churn, percentuale di clienti che abbandonano il servizio.

Il team marketing dispone di risorse limitate e non può contattare l’intera clientela. Diventa quindi necessario individuare in modo mirato i clienti a maggiore rischio di abbandono, al fine di ottimizzare il retention e contenere i costi.

## Approach
L’analisi è stata condotta partendo da una fase esplorativa dei dati (EDA), con l’obiettivo di comprendere il contesto del dataset e individuare pattern associati al churn.

Successivamente i dati sono stati puliti, trasformati e preparati per la modellazione.

È stato quindi sviluppato un modello di classificazione interpretabile, ottimizzato per individuare il maggior numero possibile di clienti a rischio di churn, i cui risultati sono stati infine interpretati in ottica business.

## Key insights

L’analisi evidenzia che il churn non è distribuito in modo uniforme tra i clienti, ma si concentra in specifici segmenti.

In particolare, il tipo di contratto emerge come uno dei principali fattori associati al churn: i clienti con contratto Month-to-month mostrano una probabilità di abbandono più elevata, mentre i contratti a lungo termine risultano associati a una maggiore stabilità.

Anche la durata del rapporto con il cliente (tenure) risulta rilevante: i clienti acquisiti più recentemente presentano un rischio di churn più elevato rispetto a quelli con maggiore anzianità.

Infine, l’analisi degli errori mostra che il modello tende a identificare come a rischio soprattutto clienti con caratteristiche tipiche del churn, mentre intercetta con maggiore difficoltà clienti a rischio con profili meno evidenti e più eterogenei.

## Business implications
- focalizzare le attività di retention sui clienti con contratto Month-to-month e bassa tenure, che rappresentano i segmenti a maggiore rischio di churn  

- incentivare la migrazione verso contratti a lungo termine, associati a una maggiore stabilità della clientela  

- utilizzare il modello come strumento di supporto per identificare i clienti a rischio più evidenti, integrandolo con ulteriori analisi per i casi meno distinti