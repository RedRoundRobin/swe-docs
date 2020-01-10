# Analisi requisiti, settima riunione

## Ruoli e macro-attori

Sono stati trovati i seguenti ruoli per far interfacciare i vari attori al database:

- Amministratore generale
- Moderatore ente
- Utente autorizzato
- Utente non autorizzato

Ciascun ruolo ha diversi permessi generali che gli permettono di avere accesso a determinate sezioni.


### Utente non autorizzato

- non ha accesso al sito (errore al login -> UC)
- non ha permessi che gli permettono di vedere alcuna sezione
- può essere un vecchio amministratore o un vecchio membro di un ente


### Utente autorizzato

- Ha accesso al sito
- Ha accesso alla sezione "Impostazioni", da cui è possibile modificare password ed altre informazioni
- Ha accesso ad un unico ente (-> può far parte di un solo ente)
- Può visualizzare i devices dell'ente autorizzato
- Può gestire le sue view personalizzate sui dati
- Può vedere gli avvisi dei devices impostati dall'ente
- Può gestire un device remoto (-> input)


### Moderatore ente

- Tutti i permessi dell'utente autorizzato
- Può gestire i membri del proprio ente (vedere e rimuovere)
- Può aggiungere nuovi account SOLO al suo ente 
- Può visualizzare le logs dei membri del proprio ente
- Può impostare gli avvisi dei devices


### Amministratore generale

- Tutti i permessi del moderatore ente, a meno delle view personalizzate
- Può gestire tutti gli enti, i devices a loro assegnati e i membri a loro assegnati
- Può aggiungere nuovi account a qualsiasi ente
- Può gestire tutti i devices
- Può gestire tutti gli account registrati
- Può vedere tutte le logs


## Pagina View personalizzate 

Ciascun utente (tranne l'amministratore) ha accesso a una sezione di pagine personalizzabili, usate col fine di raggruppare un set di dati (tabellari o grafici) in un'unica pagina sulla base dei dispositivi messi a disposizione dall'ente


## Grafici da mostrare

Il grafico è una feature desiderabile, la tabella coi dati è sufficiente.
Possibilmente, sarebbe interessante plottare più assi y per fare un controllo crociato dei dati.

> **Esempio:** (assi y) GHZ del processore + Temperatura CPU, (asse x) tempo

Da qui è possibile determinare anche la covarianza in un secondo grafico. 