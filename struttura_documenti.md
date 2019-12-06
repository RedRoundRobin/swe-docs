# Struttura dei documenti

## Studio di fattibilità

1. Introduzione
	- Scopo del documento
	- Glossario
	- Riferimenti
		- Normativi
		- Informativi

2. Valutazione capitolato scelto
	- Info generali
	- Descrizione capitolato
	- Finalità del Progetto
	- Tecnologie e Linguaggi di Programmazione
	- Aspetti positivi
	- Criticità e Fattori di Rischio
	- Conclusioni

3. Valutazione capitolati rimanenti (C1 ... C6)
	- Info generali
	- Descrizione capitolato
	- Finalità del Progetto
	- Tecnologie e Linguaggi di Programmazione
	- Aspetti positivi
	- Criticità e Fattori di Rischio
	- Conclusioni

4. Valutazioni finali (cosa ci ha spinto alla scelta)


### Timeline ruoli

- [x] Alessandro --> Stesura Introduzione, C1, C2, C3 (conclusioni mancanti)
- [x] Giovanni --> Stesura C4, C5, C6 (bozza conclusioni)
- [x] Giuseppe --> Redazione C4, C5
- [x] Alessandro --> Redazione C6 (parole glossario)
- [ ] Mariano --> Stesura valutazioni finali
- [ ] Lorenzo e Foued --> Revisione totale
- [ ] ??? --> Approvazione



## Norme di progetto

1.	Introduzione
	-	Scopo del documento
	-	Scopo del prodotto
	-	Glossario
	-	Riferimenti
		-	Normativi
		-	Informativi

2.	Processi primari (cfr. ISO 12207)
	-	Fornitura
		-	Scopo
		-	Aspettative
		-	Descrizione
		-	Attività
			-	Studio di fattibilità (riportare descr. documento, idem per altri)
			-	Piano di progetto
			-	Piano di qualifica
		-	Strumenti (strumenti utilizzati)
	-	Sviluppo
		-	Scopo
		-	Aspettative
		-	Descrizione
		-	Attività
			-	Analisi dei requisiti
			-	Progettazione
			-	Codifica (subsubsubsubsubsection senza numero)
		-	Strumenti (strumenti utilizzati)
		
> Le norme non considerano la qualità 8lab

3.	Processi di supporto
	-	Documentazione
		-	Scopo
		-	Aspettative
		-	Descrizione
		-	Ciclo di vita
		-	Template LaTeX
		-	Strutture dei documenti
			-	Frontespizio
			-	Registro modifiche
			-	Indice
			-	Contenuto principale
			-	Note a piè di pagina
		-	Classificazione dei documenti (?, chiedere a Tullio)
			-	Documenti ufficiosi
			-	Documenti ufficiale
			- 	Verbali
			-	Glossario
			- 	Lettere 
		-	Norme tipografiche
			-	Convenzioni sui nomi dei file
			-	Glossario
			-	Stile del testo
			-	Elenchi puntati
			-	Formati comuni
			-	Sigle
		-	Elementi grafici
			-	Tabelle
			-	Immagini
			-	Diagrammi UML
		-	Strumenti
			-	Latex
			- 	TexStudio, TexMaker e TexLive con IDE
	-	Gestione della configurazione
		-	Scopo
		-	Versionamento
			-	Codice di versionamento
			-	Tecnologie
			-	Repository (elenco in basso)
				-	Struttura
				-	Utilizzo di git
				-	Tipi di file e .gitignore
			-	Gestione delle modifiche
	-	Garanzia della qualità
		-	Scopo
		-	Aspettative
		-	Descrizione
		-	Controllo qualità di prodotto
		- 	Controllo qualità di processo
		-	Classificazione metriche
		-	Strumenti (? --> es. code coverage)
	-	Verifica
		-	Scopo
		-	Aspettative	
		-	Descrizione
		-	Attività	
				- 	Analisi (statica, dinamica)
				- 	Test (--> elenco di unità, integrazione, sistema, regressione, accettazione)
		-	Strumenti
				- 	Verifica ortografica
				- 	(strumenti usati in base al capitolato scelto)
	
	-	Validazione
		-	Scopo
		- 	Aspettative
		- 	Descrizione
		-	Attività

4.	Processi organizzativi (?)
	-	Gestione dei processi
		-	Scopo
		-	Descrizione
		-	Ruoli di progetto
			-	Responsabile di progetto
			-	Amministratore di progetto
			-	Analista
			-	Progettista
			-	Programmatore
			-	Verificatore
		- 	Procedure
			- 	Gestione delle comunicazioni
			-	Gestione degli incontri
			- 	Gestione degli strumenti di coordinamento
			-	Gestione dei rischi
		-	Strumenti

	-	Formazione del personale
		-	Scopo
		-	Descrizione
		-	Guida sui linguaggi di programmazione
		-	Guida sugli strumenti di programmazione
		- 	Corsi formativi aggiuntivi (dipende se esiste)

> Potrebbero includere formazione 8lab

> Da aggiungere, metriche


## Piano di Progetto

1. Introduzione
	-	Scadenze
2. Analisi dei rischi
	-	Valutazione
	-	Classificazione
	-	Lista dei rischi possibili
3. Modello di sviluppo
4. Pianificazione	
(Ogni sotto sezione contiene la divisione in periodi delle attività da svolgere e un diagramma di Gantt corrispondente)
	-	Analisi dei requisiti
	-	Consolidamento dei requisiti
	-	Progettazione architetturale / base tecnologica
	-	Progettazione di dettaglio e codifica
	-	Validazione e collaudo
5. Preventivo	
(Ogni fase contiene il prospetto orario ed economico corripondente)
Può essere diviso in 2 sezioni: la prima per l'aspetto orario e la seconda per quello economico.
	-	Fase di analisi
	-	Fase di consolidamento dei requisiti
	-	Fase di progettazione architetturale
	-	Fase di progettazione di dettaglio e codifica
	-	Fase di validazione e collaudo
	-	Riepilogo
6. Consuntivo
	-	Fase di analisi
	-	Conclusioni 
	-	Preventivo a finire
7. Appendice A - Riscontri dei rischi
8. Appendice B - Organigramma
	-	Redazione
	-	Approvazione
	-	Accettazione componenti
	-	Componenti
	-	Note

### Timeline ruoli

- [ ] Alessandro --> Stesura 1.x Introduzione
- [ ] Foued --> Stesura 2.x Fornitura
- [ ] Giovanni --> Stesura 2.x Sviluppo + 4.x Formazione
- [ ] Giuseppe --> Stesura 3.x Documentazione
- [ ] Nicolò --> Stesura 3.x Verifica e Validazione
- [ ] Mariano --> Stesura 3.x TUTTO IL RESTO
- [ ] Lorenzo --> Stesura 4.x Gestione dei processi
- [ ] Mariano e Giuseppe --> Revisione
- [ ] Alessandro e Nicolò --> Revisione
- [ ] Giovanni --> Approvazione


## Verbali

- [ ] Mariano --> Stesura dei verbali dal markdown al LaTeX