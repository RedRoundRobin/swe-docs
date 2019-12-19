## C6 - IoT

Molteplici dispositivi (da robottini a fit band). Dal piccolo macchinario a macchinari industriali.

Protocollo OPC UA con SDK in Java, molto ad alto livello pur essendo per sistemi embedded.

Simulatore software e macchine fisiche con protocollo dedicato.


--> Device (edge data-point)
	--> Driver (pilotare e comunicare col device)
		--> Gateway 
			--> Producer / consumer to Cloud (basato su Kafka by Apache)

Kafka = parte dell'infrastruttura remota che gestisce grossi volumi di dati senza troppa latenza, a grossa velocità, usufruendo del concetto di topic.
--> Container docker già pronti
--> Buona documentazione

#### Producer e Consumer 

- librerie java per ricevere dati dal sistema, il tutto gestito tramite servizi KafkaREST (per gli altri linguaggi)
- Kafka schema registry --> il dato ricevuto è trasformato in JSON
- Kafka Stream --> Manipolazione dei dati da un topic all'altro.
- KafkaSQL --> Accesso al singolo dato con una sintassi simile a SQL.
- Kafka Connect (source & sink) --> Scrivo sul DB / acquisisco input da dati premasticati.

#### Obiettivo

Nascondere la complessità che c'è dietro. Mettere nello stesso ecosistema dispositivi diversi.

- Censimento del device (oggetti diversi)
- Struttura ad albero (gateway per connessione al cloud) = quali dispositivi posso gestire come se fosse ad albero

#### Requisiti del progetto

Web application: gestione dell'utente, ruoli e gruppi (ente singolo o più grande per verificare i dati di tutti)

- Far vedere che dati può mandare un certo dispositivo (es: macchinari industriali avrà dati diversi da una fitness band)
- In base ai ruoli, far accedere a dati diversi.
- Notifiche in base al quantitativo di dati.
- Facoltativo: per ogni edge data point dire con quale frequenza si aggiornano i dati e con quale funzione di accumulo.

Da qui il gateway deve auto-configurarsi quando richiedo un certo tipo di dato. 

I dati vengono salvati su Time-Series DB con cui mantenere i dati (es. massimo 6 mesi). Almeno 2 chiavi nel DB:

- Timestamp
- ID dispositivo

Timescale deriva da PostGree. 

- Container docker già pronto per queste cose.


#### Sezione della Webapp monitoraggio per ente

- Avvisi per ente che accede alla sezione
- Possibilità di rappresentare i dati (es: ultime 10 ore) in forma tabellare o grafico


#### Correlazione tra variabili

- Trovare una correlazione tra variabili (covarianza, ecc.)

#### Invio dati al gateway

- Riavvio, accensione, ecc.
- Su webapp o bot telegram


### Problemi e Tips

- Dispositivi molto diversi --> generalizzare il più possibile
- Usare cose open, nessuna libreria proprietaria
- In caso di dubbi, c'è supporto completo.