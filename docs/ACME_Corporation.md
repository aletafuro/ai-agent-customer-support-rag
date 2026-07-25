## ACME Corporation

ACME Corporation è un'azienda SaaS B2B. Offre in abbonamento **ACME Board**, una piattaforma di project management usata da team aziendali per organizzare progetti, attività e collaborazione: board condivise, task con scadenze e responsabili, commenti, notifiche, integrazioni con altri strumenti e reportistica sull'avanzamento dei progetti.

I clienti sono aziende, con piani ad abbonamento mensile o annuale differenziati per numero di utenti e funzionalità (Free, Pro, Business, Enterprise). Il supporto riceve ogni giorno ticket eterogenei da questi clienti: dubbi sull'uso del prodotto, problemi tecnici, questioni su abbonamento e fatturazione, commenti e recensioni.

Queste informazioni sono il riferimento che il sistema usa per capire dove instradare ciascun ticket e per costruire le risposte automatiche alle domande note.

## Reparti interni

Il sistema, quando un ticket va instradato, deve indirizzarlo al reparto competente. I reparti disponibili sono quattro, ciascuno identificato dal codice da usare nel campo `department` della funzione `dispatch`:

- **Supporto Tecnico** (`technical_support`): malfunzionamenti, bug, errori dell'applicazione, problemi di accesso o prestazioni, integrazioni che non funzionano.
- **Amministrazione e Fatturazione** (`billing`): abbonamenti, rinnovi, pagamenti, fatture, cambi di piano, rimborsi.
- **Commerciale** (`sales`): richieste di upgrade, preventivi, nuove licenze, informazioni su piani Enterprise, esigenze di clienti in crescita.
- **Customer Care generico** (`customer_care`): tutto ciò che non ricade chiaramente in uno dei reparti sopra, o le richieste generiche che non rientrano nelle altre categorie.

Il criterio di instradamento tra questi reparti è parte del lavoro dello studente. Un ticket ben instradato arriva al reparto giusto corredato di un riepilogo strutturato di cosa chiede il cliente e eventuali informazioni di contorno utili per il reparto specifico.


