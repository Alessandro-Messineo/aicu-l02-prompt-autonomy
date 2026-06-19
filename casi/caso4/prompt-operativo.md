### Prompt Operativo

Strategia prompt: few-shot

Evidenze richieste:

- Assunzioni: 
    - Il messaggio è statico (non dinamico/condizionale)
    - La modifica è in un singolo file
    - Non servono test aggiuntivi
  
- Criterio: La modifica è corretta se il messaggio appare solo quando non ci sono ticket, senza alterare altri stati.

- Verifica: stato con ticket (nessun messaggio) vs stato senza ticket (messaggio visibile)


### Prompt Migliorato

```txt
Sei un assistente che applica modifiche minime a un codebase.

## Contesto
- Progetto: [inserisci linguaggio/framework]
- File target: [inserisci percorso file]
- Stato attuale: quando non ci sono ticket, non viene mostrato nessun messaggio

## Compito
Dopo aver approvato il piano, applica la modifica minima per mostrare il seguente messaggio nello stato "nessun ticket":
"[INSERISCI TESTO MESSAGGIO]"

## Vincoli
- Non risolvere altri task
- Non modificare la logica esistente
- Inserisci il messaggio solo nel branch condizionale appropriato

## Output atteso
1. Elenco delle modifiche necessarie (file, riga, tipo di modifica)
2. Codice della modifica (snippet)
3. Verifica: come testare che funziona

## Esempio di output atteso
Modifica: `src/components/TicketList.tsx` riga 42
Cambio: aggiungi `{tickets.length === 0 && <p class="empty">Nessun ticket</p>}`
Test: aprire la pagina senza ticket → messaggio visibile
```

### Prova Di Controllo

```txt
 Prova manuale per vedere se effettivamente appare il messaggio appare quando non sono presenti ticket
```