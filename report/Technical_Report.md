# AI Agent Customer Support for ACME Corporation

## 1. Obiettivo

Il progetto implementa un AI Agent sviluppato in n8n per automatizzare la gestione dei ticket di supporto di ACME Corporation.

L'agente analizza ogni richiesta, recupera le informazioni del cliente, consulta una knowledge base tramite Retrieval-Augmented Generation (RAG) e determina l'azione più appropriata.

## 2. Architettura

La soluzione è composta da due workflow:

- **Load FAQ**: genera gli embedding della knowledge base e li carica nel Simple Vector Store.
- **Project Work**: elabora i ticket, recupera i dati del cliente, interroga il Vector Store tramite AI Agent e produce un output JSON.

## 3. Tecnologie

- n8n
- Docker
- OpenAI GPT-5 mini
- OpenAI Embeddings
- Simple Vector Store
- JSON
- Retrieval-Augmented Generation (RAG)

## 4. Dataset

Il progetto utilizza i seguenti file:

| File | Descrizione |
|------|-------------|
| `tickets.json` | Ticket di supporto |
| `clients.json` | Anagrafica clienti |
| `FAQ.md` | Knowledge base utilizzata dal RAG |

## 5. Flusso di elaborazione

1. Lettura dei ticket.
2. Lettura dei dati cliente.
3. Associazione ticket-cliente.
4. Elaborazione tramite AI Agent.
5. Consultazione della knowledge base.
6. Generazione dell'output JSON.
7. Instradamento tramite nodo Switch.

## 6. Output

L'AI Agent restituisce una delle seguenti azioni:

- `auto_reply`
- `pending_reply`
- `dispatch`

## 7. Risultati

| Metrica | Valore |
|---------|-------:|
| Ticket elaborati | 59 |
| Auto Reply | 44 |
| Pending Reply | 5 |
| Dispatch | 10 |
| Fallback | 0 |

Il workflow ha elaborato correttamente tutti i ticket senza errori di instradamento.

## 8. Test

Sono stati verificati:

- recupero dati cliente;
- consultazione della knowledge base;
- classificazione automatica dei ticket;
- gestione delle richieste fuori dominio;
- resistenza ai tentativi di prompt injection;
- validazione dell'output JSON.

## 9. Conclusioni

L'AI Agent automatizza il processo di triage dei ticket utilizzando una knowledge base basata su RAG e produce un output JSON conforme alle specifiche progettuali.