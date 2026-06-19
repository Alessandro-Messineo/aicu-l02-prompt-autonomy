### Prompt Operativo

Strategia prompt: zero-shot

Evidenze richieste:

- Assunzioni: L'utente ha un progetto con una lista di ticket ma non sa dove nel codebase viene renderizzata
- Criterio: Il prompt deve guidare l'AI per esplorare il codebase in modo strutturato
- Verifica: Cercare nei file esistenti pattern di rendering lista

### Prompt Migliorato

```txt
Trova dove nel codebase viene renderizzata la lista dei ticket.

Passi:
1. Cerca file che contengono "ticket" nel nome (glob: **/*ticket*.*)
2. Cerca nei file esistenti pattern di rendering lista (grep: "map", "forEach", "ngFor", "*ngFor", "v-for", "render", "TicketList", "ticket-list")
3. Restituisci: per ogni match, il path del file + la riga rilevante + il contesto (10 righe prima/dopo)

Se non trovi nulla, prova: ricerca per parole chiave correlate ("incident", "issue", "richiesta") o chiedi all'utente il framework.
```

### Prova Di Controllo

```txt
Manualmente vado a cercare se sono presenti cicli per la renderizazzione dei ticket
```