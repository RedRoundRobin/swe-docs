# Qualita dei Processi

Documento organizzativo

## Processi 

Per ogni processo definiamo delle metriche pescate dall'ISO 12207

- Gestione delle Attività (da rimuovere)
- Gestione dei Costi
- Gestione dei Rischi
- Analisi dei Requisiti
- Progettazione (logica e in dettaglio)
- Verifica del Software (test)



### Gestione dei costi

- Budget variance (BV)

> (Costo reale a revisione - Costo pianificato a revisione) 

- Schedule Variance (SV)

> (Costo risparmiato per la conclusione delle attività  - Costo pianificato per la conclusione delle attività)
> Earned value = soldi salvati dal completare una certa attività
> Planned Value = soldi pianificati per completare una certa attività

- Estimated at Completation (EAC)

> (Costo effettivo per le attività fino ad oggi - Costo stimato per le attività mancanti)


### Gestione dei Rischi

- Unbudgeted Risks (UR)

> Numero incrementale che parte da 0


### Analisi dei Requisiti


- Satisfied Mandatory Requirements (SMR)

> (Requisiti obbligatori soddisfatti fino a quel momento / Requisiti obbligatori da rispettare) * 100

- Satisfied Desirable Requirements (SDR)

> (Requisiti desiderabili soddisfatti fino a quel momento / Requisiti desiderabili totali) * 100

- Satisfied Optional Requirements (SOR)

> (Requisiti opzionali soddisfatti fino a quel momento / Requisiti opzionali totali) * 100


### Progettazione


- Structural Fan-In (SFI)

> Numero di componenti che utilizza un certo modulo del software


- Structural Fan-Out (SFO)

> Numero di componenti utilizzate da un certo modulo


### Verifica del Software

- Function Coverage (FCOV)

> Percentuale di copertura delle funzioni del software

- Branch coverage (BCOV)

> Percentuale di copertura delle ramificazioni del software

- Condition coverage (COCOV)

> Percentuale di copertura delle espressioni booleane negli if statement

- Passed Tests Percentage (PTP)

> Percentuale dei Test Passati

- Failed Tests Percentage (FATP)

> Percentuale dei Test Falliti

- Fixed Tests Percentage (FITP)

> Percentuale dei Test Fixati

- Average Bug Resolution Time (ABRT)

> Tempo medio di risoluzione di un bug

- Test Effectiveness Scale (TES)

> Scala da 0 a 2: 
	0 = nessun bug trovato grazie al test, 
	1 = un bug trovato, 
	2 = più bug trovati grazie al test

## Riferimenti 

- https://www.qasymphony.com/blog/64-test-metrics/

## Altro

- Schedule Variance ([rif. 1](https://www.wrike.com/project-management-guide/faq/what-is-schedule-variance-in-project-management/), [rif. 2](https://pmstudycircle.com/2012/05/schedule-variance-sv-cost-variance-cv-in-project-cost-management/), [rif. 3](https://hygger.io/blog/how-to-calculate-schedule-variance/))

> (Costo effettivo per la conclusione delle attività  - Costo pianificato per la conclusione delle attività)

- Statement coverage (SCOV)

> Percentuale di copertura degli if statement del software