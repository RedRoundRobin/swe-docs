#Possibili strutture dei documenti 

Nelle seguenti strutture sono presenti (dove sono riuscito) dei consigli su come riempire le sezioni. 

## Analisi dei Requisiti

1. Introduzione (come le altre ma togliendo la parte di descrizione del prodotto)

2. Analisi del prodotto
	-	Scopo del prodotto
	-	Descrizione e analisi della sua struttura (i vincoli poi si troveranno nell'apposita sezione)
	-	Attori principali e secondari (se presenti)	
	-	Come gli attori interagiscono con il prodotto

3. Casi d'uso

4. Classificazione dei requisiti
	-	Requisiti funzionali
	-	Requisiti non funzionali
	-	Requisiti di vincolo (Vincoli)

5. Tracciamento
	-	Dominio
	-	Capitolato
	-	Altre fonti



## Piano di Progetto

1. Introduzione (solita come le altre)
	- 	Consiglio (da modificare q.b.) per lo scopo del documento:
		-	Organizzare le attività con efficienza per produrre risultati efficaci;
		-	Facilitare la misurazione dell'avanzamento fissando "milestone"
2. Analisi dei rischi
	-	 Gestione dei rischi
		-	Identificazione	(nel progetto, nel prodotto, nel mercato)
		Rischi di progetto: Sforamento di costi, tempi, risulati insoddisfacenti.
		Fonti di rischio: Tecnologie di lavoro e produzione software, rapporti interpersonali, Organizzazione del lavoro, requisiti e rapporti con gli stakeholder, tempi e costi.
		-	Analisi (probabilità di occorrenza e possibili conseguenze)
		-	Pianificazione (come evitare o ridurre quei rischi)
		-	(?) Controllo (Utilizzo di indicatori, raffinamento delle strategie)

3. Modello di sviluppo

4. Risorse disponibili (tempo e persone)
	-	Tabella con le risorse 

6. Suddivisione del lavoro (work breakdown)
	-	Individuare le attività 

5. Organizzazione del progetto / Preventivo 
	-	Preventivi
	-	Riepilogo 

6. Consuntivo
	-	Quanto è stato investito inizialmete dal gruppo

7. Calendario delle attività 
	-	Tabella con tutte le attivita e relativo tempo di inizio - tempo di fine.
	-	Sono presenti anche le scadenze

8. Componenti	


## Piano di qualifica

1. Introduzione 

2. Qualità di Prodotto (Non farle tutte ma solo le più importanti/Semplici)
	Per le seguenti qualità descriverle e poi nella sezione metriche scrivere le metriche da utilizzare per misurarle. Nelle sezioni ci sono alcuni collegamenti tra qualità e da cosa è data (complessità ciclomatica, taglia del programma , etc...).
	-	Adeguatezza funzionale 
			Completezza, correttezza, adeguatezza
	-	Efficienza prestazionale 
			Nel tempo, nelle risorse, nella capacità
	-	Compatibilità 
			Coesiste con il resto del sistema ?, può usare funzioni di altri prodotti senza creare conflitti? 
	-	Usabilità 
			Apprendibilità, Operabilità, Protezione da errori, User experience, Accessibilità
			Data da: lunghezza del manuale utente, numero dei messaggi d'errore
	-	Affidabilità 
			Maturità, Disponibilità, Tolleranza ai guasti, Riparabilità
			Data da: complessità ciclomatica, taglia del programma in linee di codice, numero dei messaggi d'errore
	-	Sicurezza 
			Confidenzialità, Integrità, Tracciabilità
	-	Manutenibilità
			Moduliarità, Riusabilità, Modificabilità, Verificabilità
			Data da: numero dei parametri nelle procedure, complessità ciclomatica, taglia del programma in linee di codice, lunghezza del manuale utente
	-	Portabilità
			Cambiamenti sono poco costosi(Dato dall'isolamento delle dipendenze)
			Data da: numero dei parametri nelle procedure, taglia del programma in linee di codice
3. Qualità di Processo 
	-	Per ogni processo descriverlo brevemente e come facciamo ad essere sicuri che sia di qualità, ovvero le tecniche che adottiamo per renderlo di qualità	
4. Metriche
	-	Scopo delle metriche 
		-	Per quantificare prodotti e processi
		-	Le metriche riguardanti il prodotto possono essere usate per fare delle predizioni generali sul prodotto stesso o per identificare delle componenti con un comportamento anomalo.
	-	Lista delle metriche per tipo con formula per calcolarle:
		Es: Programma : SLOC
			Effort: Persone/Giorni
			Testo: Gunning's Fog index (Fog index = [(average # words / sentence) + (# words of 3 syllables or more)] * 0.4)
5. Test
	-	Come facciamo i vari tipi di test (Vedere RIGHT BICEP e A TRIP di TOS)
	-	Test di accettazione, test di sistema, test di integrazione e test di unità.			





