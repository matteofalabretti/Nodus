# Ruoli e permessi — NODUS

## Tipologie di organizzazione

- **Store:** apre pratiche, registra oggetti, richiede preventivi e coordina la consegna.
- **Laboratorio:** valuta oggetti, formula preventivi ed esegue lavorazioni.
- **Amministratore piattaforma:** gestisce configurazione e amministrazione globale.

## Ruoli indicativi

| Ruolo | Ambito | Responsabilità |
|---|---|---|
| Amministratore piattaforma | Piattaforma | Configurazione e gestione globale |
| Responsabile store | Store | Gestione completa delle pratiche del negozio |
| Operatore store | Store | Inserimento e aggiornamento delle pratiche assegnate |
| Responsabile laboratorio | Laboratorio | Gestione del laboratorio, utenti e attività |
| Tecnico | Laboratorio | Valutazione ed esecuzione delle lavorazioni |

## Regole da definire

- Un utente può appartenere a più organizzazioni?
- Un utente può ricoprire ruoli diversi in organizzazioni differenti?
- Chi può vedere i dati identificativi del cliente?
- Chi può modificare o annullare un preventivo?
- Chi può approvare una lavorazione aggiuntiva?
- Quali dati sono condivisi tra store e laboratorio?
- È previsto un accesso temporaneo per collaboratori esterni?

## Principio di sicurezza

Non basare l'accesso esclusivamente sul ruolo. Ogni richiesta deve verificare anche l'organizzazione di appartenenza, la relazione con il record e l'eventuale assegnazione all'attività.
