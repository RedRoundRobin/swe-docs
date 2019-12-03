# C5 - Zucchetti, predire in grafana 
### Appunti seminario


Zucchetti SPA, seconda azienda con maggior fatturato per software in italia (dopo microsoft).

Software house, non system integrator. Producono bit e vende bit, al contrario del S.i. che vende prodotti pronti e li installa.

Sede centrale a Lodi, 4 sedi a Padova, 2 a Treviso, 1 verona..

Tante robe per dire "venite a lavorare da noi non abbiamo il sole in ufficio :D"

- Gestionali
- Risorse umane
- Fiscale

Alberghi di Las Vegas con rulli che gestiscono la lavanderia. Fanno un po' di tutto.

Da quest'anno, fatturazione elettronica a partire da gennaio 2019. Circa 2 mld di fatture inviate al ministero e rinviata al cliente. La Zucchetti si qualifica come sviluppatori del software, ma anche gestione delle operazioni svolte col fine di far funzionare il programma.

### Development e operations commutano allo stesso attore

Windows lo installavi su tante macchine a suo tempo. I bug potevano essere permessi, non era troppo problematico.

Ma ora sia i programmatori che i sistemisti devono collaborare per tenere in piedi l'infrastruttura.

Il software, specialmente quelli molto grandi, richiedono una attenzione continua, dato che tutto si trova nel cloud ed è il cliente che si connette al servizio in remoto.

Oltre allo sviluppo e alle operazioni, si affianca la figura del **Quality manager**.

### Sistemi agili

Frequenti rilasci del software fatti in maniera trasparente ogni login / logout.

### Grafana e strumenti utilizzati

Sistema di monitoraggio per la macchina e in generale per gli applicativi.

Permette di controllare lo stato del servizio, i livelli di SLA.

Si utilizza influx-db per salvare i dati.

Java JMX (java mission control), da lì è possibile installare delle bins che monitorano tutte le informazioni legate all'applicativo nella Java virtual machine. In questo modo è possibile analizzare meglio con degli appositi logs cosa succede a basso livello nell'applicativo.

Java JMeter per il calcolo degli utenti e robe varie...

### Capitolato: sviluppo di un plugin di Grafana

- Obiettivo: nuove modalità di monitoraggio.
- Prevedere valori avendo già in possesso alcuni valori.

Oltre al dato grezzo, si possono creare dei dati sintetici (nuovi) in base al comportamento, così da poter fare delle previsioni per cosa sta succedendo e cosa succederà.

Ad esempio: molta latenza sul disco, grande uso di CPU --> interpretazione dati --> predizione --> (!) Avviso: rallentamento del sistema imminente

Due grandi tipi di previsioni:

- __Regressione__ a partire dai dati vecchio ne creo di nuovi che assume valori di tipo continuo.
- __Classificazione__ a partire da dei dati ne viene prodotto un nuovo numerico o stringhe con valori di tipo discreto.

--> __Support vector machine__

In generale, nel contesto della previsione si vuole comprenderne la qualità della previsione.

#### Regressione lineare

Punti su un piano e una retta rossa entro cui stanno i punti. La formula di previsione:

y = a\*x+b

Dove __a__ e __b__ vengono determinati con il metodo dei minimi quadrati. Sistema estremamente semplice, ma è possibile allargarlo a più dimensioni. In tale caso si ottiene dei punti nello spazio e un piano per cui passano dei punti:

y = a1\*x1+a2\*x2+...+b

Andando a verificare cosa può succedere coi dati, tramite il quartetto Anscombe, si possono verificare casi estremi:

1. Dati ottimali per la regressione lineare (retta sul piano, punti ok)
2. Dati non lineari (parabola sul piano)
3. Outliner che sfalsa la regola (dati errati sul piano)
4. Dati che non si prestano in alcun modo all'analisi con la regressione lineare (punti disposti in modo non continuo)

- _Omoschedasticità_ le variabili hanno la stessa varianza, gli errori di previsione sono omogenei
- _Eteroschedasticità_ le variabili aleatorie __non__ hanno la stessa varianza, gli errori dipendono dalla posizione.

Effetti moltiplicativi dei dati.

Per comprendere meglio le informazioni, si dispone il tutto con il __grafico dei residui__.

Coefficiente R^2 che nasce dal rapporto tra gli errori rispetto alla retta e gli errori rispetto alla media della variabile __y__. Si osservano i dati, si cerca si capire se la natura sottende una retta ==> predittore e qualità del predittore.

__Support vector machine__ algoritmi per classificare (e per ottenere un predittore) inventati da Vapnik. 

Le SVM sono robuste in caso di aumento del numero di predittori (==> aumento dimensioni). 

In sostanza si può eseguire una trasformazione polinomiale così da spostare sullo spazio i dati e ottenere una retta.

#### Misure di qualità

- Precision: quanti di quelli che dico essere veri lo sono davvero?
- Recall: quanti di quelli che sono veri non sono stato capace di trovare? 

Per queste analisi si parte dalla __Confusion matric__:
- riporta i veri positivi, i falsi positivi, i veri negativi e i falsi negativi 

Oltre a ciò, i predittori possono essere cambiati e calibrati usando ad esempio la Curva ROC che mostra il comportamento del sistema riportando il tasso di veri positivi al variare del tasso di falsi positivi.


#### Domande e info aggiuntivo

- Realizzare plugin in JS, node.js
- Librerie fornite da applicarle al flusso in ingresso
- Ciò produce un ulteriore dato che verrà aggiunto ad altri grafici di grafana

- Es: 3 predittori CPU, RAM, DISCO, li applico alla SVM e creo la classe stress / no stress mostrata in un grafico.
- Niente proprietà intellettuale, open source.
- Competenze molte richieste sul mercato.