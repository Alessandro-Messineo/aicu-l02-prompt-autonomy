### Prompt Operativo

Strategia prompt: zero-shot

Evidenze richieste:

- Assunzioni: 
    - Esiste una lista/array di ticket aperti nel frontend o API
    - Il componente/pagina che mostra i ticket ha già una logica condizionale
    - Il messaggio è un semplice testo statico (no localizzazione per ora)

- Criterio:
    L'output deve listare i file coinvolti con:
        1. Il percorso del file
        2. La riga/i dove si trova la logica dei ticket
        3. Cosa andrebbe aggiunto/modificato (senza scrivere codice)

- Verifica: 
    - Che l'elenco dei file sia coerente con la struttura reale del progetto
    - Che non manchino file dipendenti (es. stili, tipizzazioni, mock dati)

### Prompt Migliorato

```txt
Contesto: sto lavorando su [DESCRIZIONE PROGETTO], un'app [React/Vue/Angular] 
che mostra una lista di ticket aperti.

Obiettivo: aggiungere un messaggio "empty state" quando la lista dei ticket 
è vuota, da visualizzare al posto della tabella/elenco.

Prima di implementare:
1. Identifica i file che gestiscono il caricamento e la visualizzazione dei ticket
2. Indica quali righe contengono la logica condizionale (lista vuota vs piena)
3. Suggerisci il pattern migliore (se esiste un componente EmptyState già usato)

Non implementare: limitati a listare i file, le righe rilevanti, 
e il tipo di modifica necessaria.
```

### Prova Di Controllo

```txt
Bisogna controllare se i file che va a modificare sono effettivamente quelli interessati 
```