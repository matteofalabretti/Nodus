# NODUS
### Gestionale per riparazioni e rete di laboratori

**Una rete. Competenze diverse. Un unico flusso di lavoro.**

NODUS è una piattaforma gestionale B2B per coordinare riparazioni di gioielleria e orologeria tra negozi, laboratori e professionisti specializzati.

Il sistema organizza ogni pratica, i singoli oggetti che la compongono, i preventivi, le lavorazioni e le attività assegnate ai diversi operatori.

## Obiettivi

- Gestire le pratiche aperte dai negozi e gli oggetti associati.
- Richiedere e confrontare più preventivi per lo stesso oggetto.
- Coordinare lavorazioni affidate a uno o più laboratori.
- Gestire utenti, ruoli e responsabilità.
- Mappare competenze, operazioni, attrezzature e ricambi dei laboratori.
- Tracciare stati, assegnazioni e modifiche lungo tutto il processo.

## Modello operativo

- **Pratica:** richiesta creata da uno store; può contenere più oggetti.
- **Oggetto:** elemento autonomo, con stato, documentazione e storico propri.
- **Preventivo:** proposta economica e tecnica riferita a un singolo oggetto. Uno stesso oggetto può ricevere preventivi da più laboratori.
- **Lavorazione:** attività tecnica necessaria per intervenire sull'oggetto. Può essere assegnata a un laboratorio e coordinata con altre lavorazioni.
- **Laboratorio:** organizzazione con utenti, competenze, operazioni eseguibili, attrezzature e inventario.
- **Utente:** persona che opera per uno store, un laboratorio o come amministratore della piattaforma.

## Flusso principale

1. Lo store apre una pratica e registra uno o più oggetti.
2. Per ciascun oggetto richiede una o più valutazioni ai laboratori.
3. I laboratori esaminano l'oggetto e inviano i propri preventivi.
4. Lo store valuta e approva una proposta.
5. Le lavorazioni vengono assegnate ai laboratori competenti.
6. I laboratori aggiornano attività e avanzamento.
7. L'oggetto viene verificato, restituito allo store e consegnato al cliente.

Il flusso dovrà gestire anche revisioni, rifiuti, sospensioni, annullamenti, rilavorazioni e attività parallele o sequenziali.

## Moduli principali

- Pratiche e oggetti
- Preventivi
- Laboratori e competenze
- Lavorazioni e assegnazioni
- Attrezzature e inventario
- Utenti e autorizzazioni
- Stati, notifiche e storico
- Report e statistiche

## Principi di progettazione

- **Separazione dei dati:** ogni organizzazione accede solo ai dati per cui è autorizzata.
- **Permessi granulari:** accesso definito da ruolo, organizzazione e responsabilità.
- **Tracciabilità:** le azioni rilevanti devono lasciare uno storico.
- **Modularità:** i moduli devono avere responsabilità chiare.
- **Flessibilità:** il flusso non deve imporre una sequenza unica a tutte le riparazioni.
- **Integrità:** relazioni e stati devono rimanere coerenti.

## Documentazione del progetto

La cartella `docs/` raccoglie le decisioni e le specifiche che evolveranno durante lo sviluppo:

- `docs/ARCHITETTURA.md` — struttura tecnica e principi architetturali.
- `docs/MODELLO-DATI.md` — entità principali e relazioni.
- `docs/FLUSSI-OPERATIVI.md` — processi e casi particolari.
- `docs/RUOLI-E-PERMESSI.md` — organizzazioni, ruoli e autorizzazioni.
- `docs/ROADMAP.md` — fasi di sviluppo.
- `docs/DECISIONI-APERTE.md` — scelte ancora da prendere.
- `docs/decisioni/ADR-TEMPLATE.md` — modello per registrare decisioni architetturali.

## Stato del progetto

**Fase:** definizione funzionale e progettazione architetturale.

Stack tecnologico, infrastruttura, database e modalità di distribuzione saranno definiti prima dell'avvio dello sviluppo applicativo.

## Identità

**NODUS — Connette competenze. Coordina lavorazioni.**
