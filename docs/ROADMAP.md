# Roadmap — NODUS

La roadmap è indicativa. Le priorità potranno cambiare dopo la validazione dei flussi con store e laboratori.

---

## Fase 0 — Analisi e progettazione
- [ ] Validare il modello operativo.
- [ ] Definire ruoli e permessi.
- [ ] Definire stati e transizioni (Oggetto, Lavorazione, Spedizione).
- [ ] Approvare modello dati e architettura.
- [ ] Scegliere stack e infrastruttura.
- [ ] Definire i principi di separazione dati e multi-tenancy.
- [ ] Documentare le decisioni aperte (ADR).

---

## Fase 1 — Fondamenta
- [ ] Repository e ambienti (dev / staging / prod).
- [ ] Autenticazione.
- [ ] Organizzazioni (Store, Laboratorio, Admin) e utenti.
- [ ] Autorizzazioni e separazione dei dati (row-level / tenant isolation).
- [ ] Sistema di audit log di base.
- [ ] Gestione ruoli e permessi granulari.

---

## Fase 2 — Pratiche e oggetti
- [ ] Creazione pratiche.
- [ ] Gestione di più oggetti per pratica.
- [ ] Foto e documentazione allegata.
- [ ] Stati e storico dell’oggetto.
- [ ] Tipologia oggetto (Orologio / Gioiello / Altro) con implicazioni sul flusso di preventivo.
- [ ] **Spedizione (priorità attuale)**  
  - Creazione di un lotto di invio verso un laboratorio  
  - Raggruppamento di uno o più oggetti  
  - Stati della spedizione (in preparazione → pronta → in transito → ricevuta → pronta per ritorno → restituita → chiusa)  
  - Aggiornamento automatico dello stato degli oggetti contenuti  
  - Documento di accompagnamento + QR code / etichette  
  - Supporto a spedizioni di sola andata (preventivo) e di ritorno

---

## Fase 3 — Laboratori e preventivi
- [ ] Anagrafica laboratori.
- [ ] Catalogo operazioni e competenze (il laboratorio espone le operazioni che è in grado di eseguire).
- [ ] Richieste di valutazione (preventivo).
- [ ] Preventivi multipli per oggetto.
- [ ] Revisione e approvazione del preventivo.
- [ ] Modalità di valutazione flessibili (documentazione / supporto store / smontaggio / ibrida) — *base*.
- [ ] Collegamento tra richiesta di preventivo e necessità di spedizione fisica.

---

## Fase 4 — Lavorazioni e risorse
- [ ] Assegnazione delle lavorazioni.
- [ ] Gestione attività parallele e sequenziali.
- [ ] Attrezzature.
- [ ] Ricambi e inventario di base (dichiarazione nel preventivo di ricambio in magazzino vs da acquistare).
- [ ] Avanzamento e controllo qualità.
- [ ] Stati completi della Lavorazione.

---

## Fase 5 — Consolidamento
- [ ] Notifiche di base (eventi principali).
- [ ] Report e statistiche essenziali.
- [ ] Test di sicurezza e prestazioni.
- [ ] Backup e procedure operative.
- [ ] Preparazione al rilascio (MVP).

---

## Fasi future / Advanced (post-MVP)

Queste funzionalità sono state analizzate e documentate, ma restano fuori dallo scope del primo rilascio.  
Verranno pianificate dopo la validazione dell’MVP con gli utenti.

### Logistica e scomposizione avanzata
- [ ] Scomposizione dell’oggetto in **Componenti** (es. movimento + cassa + quadrante).
- [ ] Spedizione di singoli componenti a laboratori diversi.
- [ ] Stato di ricomposizione dell’oggetto.
- [ ] Lavorazione di riassemblaggio.

### Materiali e tracciabilità (RJC-ready)
- [ ] Entità MaterialeUtilizzato (oro, pietre, altro).
- [ ] Registrazione provenienza dell’oro aggiunto (cliente / magazzino laboratorio / fornitore / ricambista).
- [ ] Tracciabilità pietre (caratteristiche, certificati, provenienza).
- [ ] Report di tracciabilità per conformità RJC.
- [ ] Allegati documentali (fatture, certificati, dichiarazioni di origine).

### Ruolo Ricambista
- [ ] Nuovo tipo di organizzazione: Ricambista.
- [ ] Richiesta di offerta ricambi collegata allo stato `in_attesa_ricambio`.
- [ ] Collegamento ricambio ordinato → lavorazione.
- [ ] Flusso di accettazione e tracciamento del ricambio.

### Notifiche e SLA avanzati
- [ ] Sistema di notifiche completo (in-app, email, push).
- [ ] SLA configurabili per tipo di operazione, urgenza e laboratorio.
- [ ] Alert automatici su sforamento tempi.
- [ ] Dashboard di monitoraggio tempi e performance.

### Conformità TULPS
- [ ] Modulo **Registro Oggetti Preziosi** (carico/scarico).
- [ ] Generazione automatica delle scritture da eventi di Spedizione (ingresso/uscita laboratorio).
- [ ] Vista giornaliera e mensile del registro.
- [ ] Esportazione PDF / stampa.
- [ ] Firma digitale o marca temporale sul registro periodico (mensile o a chiusura periodo) per garantire immodificabilità e validità legale.
- [ ] Conservazione a norma con tracciabilità delle modifiche.
- [ ] Predisposizione a eventuali invii telematici futuri alle autorità.

### Altre evoluzioni
- [ ] Preventivi ibridi e workflow di conferma post-smontaggio.
- [ ] Matching automatico laboratori in base a competenze + carico + localizzazione.
- [ ] Valutazioni e rating tra store e laboratori.
- [ ] Integrazioni corrieri (tracking automatico).
- [ ] App mobile dedicata (store e laboratorio).
- [ ] Multi-lingua e multi-valuta (se necessario).

---

## Note di priorità

| Priorità     | Elemento                          | Motivazione |
|--------------|-----------------------------------|-----------|
| Alta (ora)   | **Spedizione**                    | Rende automatico e tracciabile il flusso fisico degli oggetti |
| Media        | Registro TULPS + firma digitale   | Conformità normativa + valore percepito dai laboratori |
| Bassa        | Componenti, Materiali/RJC, Ricambista, SLA avanzati | Da validare dopo l’uso reale dell’MVP |

---

*Ultimo aggiornamento: basato sull’analisi funzionale di novembre 2026.*