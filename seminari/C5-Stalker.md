
# Capitolato 5 - Stalker
### Appunti seminario

- Gruppo imola, richiedono molta documentazione.
- Si occupano di sicurezza, privacy e delivery.

### Codebase e build automation per l'azienda

Cenni su Git e cenni su Factor application

- Per l'azienda è importante una codebase condivisa, unico punto centralizzato, in cui tutti lavorano.
- Le dipendenze devono essere pubbliche (es. tramite manifest), evitare di tenere le cose in locale o in modo isolato. 
- La configurazione deve essere anch'essa disponibile e funzionante.
- Scalabilità per l'applicazione in modo da gestire moli di chiamate diverse.
- Si deve ragionare in ottica cloud e SaaS (software as a service).
- Importante uso di docker con logs centralizzate (importante leggere le logs).

### Wall of confusion e devops

Agile vs old style: in tutti e due i modi di fare le cose, si hanno problemi a livello enterprise. 
Development team e team operations non si riescono sempre a collaborare. La nascita del devops è quindi imminente col fine di risolvere questa problematica, tutti hanno la stessa responsabilità.

La maggior parte delle informazioni andranno in automatico e andranno in produzione velocemente (magari fallendo appositamente ==> fail fast). Questo processo promette maggior velocità di sviluppo e di rilascio, essendo ripetibile e perlopiù affidabile.

In altre parole:

- __C. Integration__ = integro il mio lavoro con quello degli altri
- __C. Delivery__ = gestione degli artefatti in produzione con relativi versionamenti
- __C. Testing__ = la parte più importante, documentazione migliore che si potrà trovare nel codice, permette di capire cosa funziona e cosa no. In generale, importante avere una copertura del 85% - 90%.

> cfr. __Martin Fowler__ per quanto concerne Continous Integration
> cfr. Tecnologie open source
> Opzionalmente docker e kubernetes sono molti interessanti come pratiche


Importante uso dei test unitari, opzionale il TDD. 
Pratiche white box e black box, dove so oppure non so cosa sto testando.

### Informazioni utili sul way of working

1. Redmine: issue tracker
2. Gitlab: versionamento
3. Jenkins: Maven + WM + SonarQube + Docker ==> Artifactory
4. Da docker ==> image registry con Gitlab e continous delivery.
- Consiglio: non accentrare tutto su una unica cosa (nel caso del progetto va bene).

## Informazioni capitolato

#### GPS

- **Dead recoking**: dato un punto di partenza, la velocità, la direzione del movimento, il tempo trascorso e la distanza percorsa si può comprendere il punto di arrivo.

- **Proximity sensing**: la posizione del punto mobile è ricavata dalle coordinate di determinate stazioni che tracciano il segnale che viene trasmesso da esse (cell ID). Ogni stazione ha un suo pattern di segnale.


In genere con il GPS usano la **trilaterazione**, usando la posizione nota di due o più punti di riferimento e la distanza misurata tra il punto mobile ciascun punto di riferimento. La **triangolazione** permette di calcolare la posizione sulla base di angoli di arrivo (AOA) tra punto mobile e punti di riferimento e la distanza stessa tra i punti di riferimento (==> vedere le slide).

Spiegazioni sul funzionamento e limiti del GPS (==> vedere le slide)

#### Strategie da realizzare

> Riferimento slides 29/40 - Tabella riassuntiva.

Attenzione alla batteria e all'uso dei beacon.

#### Altro e domande

- Tenere conto del GDPR (struttura dati, ecc.) come se fosse gestito lato aziendale
- Informazioni inviate in modo anonimo (nel caso della fiera).
- Precisione non deve essere perfetta. Pensare magari a come venderla, analizzando i compromessi.
- Coordinate edificio inserirle o tracciare in automatico? Parte view potrebbe avere una mappa con il rettangolino della zona.
- Infrastrutture fornite? Forse qualcosa.. Idealmente i gruppi di quel capitolato che si parlino tra loro, oltre che con l'azienda. VPS con tot ram, hdd. L'azienda ha un laboratorio in cui ci fanno diverse cose, dunque alcune cose potrebbero non essere recuperabili ==> andare di recovery.