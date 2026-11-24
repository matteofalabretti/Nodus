# Architettura — NODUS

Documento di lavoro: descrive i principi da rispettare, non impone ancora uno stack tecnologico.

## Obiettivi architetturali

- Supportare più store e laboratori.
- Separare i dati delle diverse organizzazioni.
- Consentire a un utente di appartenere a una o più organizzazioni, se previsto dalle regole di prodotto.
- Separare interfaccia, logica applicativa e persistenza.
- Esporre API documentate per eventuali integrazioni future.
- Registrare le operazioni rilevanti in uno storico verificabile.

## Aree funzionali suggerite

1. Identità, autenticazione e autorizzazioni
2. Organizzazioni e sedi
3. Pratiche e oggetti
4. Preventivi
5. Laboratori e capacità operative
6. Catalogo lavorazioni
7. Assegnazioni e avanzamento
8. Attrezzature e inventario
9. Notifiche
10. Reportistica

## Indicazioni da valutare

- Applicazione monolitica modulare come prima implementazione.
- Database relazionale per entità e relazioni strutturate.
- Archiviazione separata per fotografie e allegati.
- API versionate.
- Test automatici sulle regole di business.
- Backup, monitoraggio e gestione sicura dei segreti.

## Scelte da formalizzare

Registrare ogni decisione rilevante in `docs/decisioni/` usando il modello ADR.
