# Flussi operativi — NODUS

## Flusso standard

1. Lo store crea una pratica.
2. Registra uno o più oggetti, con descrizione, condizioni iniziali e immagini.
3. Per un oggetto invia una richiesta di valutazione a uno o più laboratori.
4. Ogni laboratorio prepara una proposta indipendente.
5. Lo store confronta, accetta o rifiuta le proposte.
6. Le lavorazioni approvate vengono pianificate e assegnate.
7. Il laboratorio aggiorna lo stato delle attività e segnala eventuali imprevisti.
8. Le lavorazioni vengono completate e sottoposte ai controlli previsti.
9. L'oggetto rientra allo store e viene consegnato al cliente.

## Stati da definire

### Pratica
Esempi: aperta, in gestione, parzialmente completata, completata, annullata.

### Oggetto
Esempi: registrato, in valutazione, in attesa di approvazione, in lavorazione, in verifica, rientrato allo store, consegnato.

### Preventivo
Esempi: in preparazione, inviato, da revisionare, approvato, rifiutato, scaduto, ritirato.

### Lavorazione
Esempi: da pianificare, assegnata, in attesa, in corso, sospesa, completata, da verificare, da rifare, annullata.

Gli stati definitivi, le transizioni ammesse e gli utenti autorizzati a eseguirle devono essere specificati prima dello sviluppo.

## Casi particolari da coprire

- Più oggetti nella stessa pratica con avanzamenti indipendenti.
- Più preventivi alternativi per lo stesso oggetto.
- Più lavorazioni complementari sullo stesso oggetto.
- Lavorazioni sequenziali o parallele.
- Trasferimento dell'oggetto tra laboratori.
- Preventivo revisionato dopo una prima proposta.
- Lavorazione sospesa per mancanza di ricambi.
- Intervento aggiuntivo richiesto dopo l'ispezione.
- Rilavorazione dopo il controllo qualità.
- Annullamento con attività già avviate.
