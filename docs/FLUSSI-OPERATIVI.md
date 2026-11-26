# Flussi operativi — NODUS

## Flusso standard

1. Lo store crea una pratica.
2. Registra il cliente e i suoi dati di contatto.
3. Registra uno o più oggetti, con descrizione, condizioni iniziali e immagini.
4. Per un oggetto invia una richiesta di valutazione (aperta a tutti i laboratori da qui è gia stata servita), se necessarie ulteriori informazioni può richiedere la spedizione dell'oggetto.
5. Ogni laboratorio prepara una proposta indipendente.
6. Lo store confronta, accetta o rifiuta le proposte.
l'oggetto viene spedito al laboratorio selezionato e veine effettuata una variazione del registro TULPS
7. il laboratorio riceve l'oggetto conferma il preventivo o comunica eventuali modifiche, e registra le lavorazioni da eseguire e l'oggetto ricevuto nel suo registro TULPS.
8. Le lavorazioni approvate vengono pianificate e assegnate. vengono definiti attrezzature, ricambi e risorse necessarie. se le risorse non dispobibili comunica l'attesa dei ricambi.
9. Il laboratorio aggiorna lo stato delle attività e segnala eventuali imprevisti.
10. Le lavorazioni vengono completate e sottoposte ai controlli previsti.
11. il laboratorio registra la chiusura del preventivo e procede alla spezione di ritorno e la variazione del suo registro TULPS
12. L'oggetto rientra allo store e viene consegnato al cliente. la pratica viene chiusa e registrata la variazione nel registro TULPS dello Store

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
