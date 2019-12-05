# C1 - Highlights


Upload del video, mappatura del video e successivo transocoding.

Va bene anche esports.

- __Sage maker__ input di serie di modelli, dare un insieme di video con degli esempi di cosa succede e capire cosa succedere
- __Dynamo DB__ database per salvare i dati relativi al training


AWS --> concetto di regione sul mondo e avaiability zone

#### S3 

--> Inserire un oggetto (file) in modo altamente scalabile (le cartelle sono anch'esse oggetti)

- Alta disponibilità
- Durabilità del 99,9999999%
- Costo bassissimo
- Registra caricamento / rimozione del file per le lambda functions --> event driven development
- Versionamento dei file
- Per ogni evoluzione / versione --> evento apposito per (ad esempio) cancellare versioni successive


#### Dynamo DB

- Costo e funzionalità basate sulle performance
- Full managed
- Operazioni al secondo
- No SQL (documento JSON)
- Molto buono per eventi di singola tabella

Performance per l'uso della chiave primaria, basse invece per dinamiche di interrogazioni simil join tra le tabelle.


Nei NOSQL, replicazione del dato più che relazione.


#### AWS Lambda

Creiamo piccole funzioni di codice che vengono caricate su AWS e si pagano per la singola operazione (cpu usata, ecc.).
Scalare quasi all'infinito, performance maggiori, problemi solo alla singola funzione e non al resto.

- Stateless, ma con Dynamo DB si può salvare lo stato dell'elaborazione.
- Python o Node (MEGLIO PYTHON !!!)
- Cognito (servizio gestito di autenticazione twitter, google, ecc.)

Monitoraggio sulle lambda (ram e CPU) per capirne l'ottimizzazione delle funzioni.



### Machine learning

--> E' qualcosa che insegnamo non che programmiamo [cit. Zero12 2019]

Dati variabili, non sempre dati strutturati. 

- Informazioni video da analizzare / mappare
- Ripetibilità e velocità durante il cambiamento dei dati

Supervised learning <-- Machine learning --> Unsupervised learning

- Diamo dei suggerimenti / labels ai dati e ricavarne il modello di fondo
- Classificazione

- Bacino di circa 1000 video per andare bene

#### Validation

Creare un data set, taggarne il 70% di tutto il dataset e fare la validazione al 30% dei dati rimanente.

Alternativamente: 
- __cross validation__ faccio la validazione su tre step differenti
- __multi layer validation__ 60% di training, 20% di validazione, 20% di test
