### Prompt Operativo

Strategia prompt: few-shot

Evidenze richieste:

- Assunzioni: 
    - Dashboard web esistente da ristrutturare
    - Filtri: stato, priorità, data, assegnatario
    - Design responsive

- Criterio:
    - Usabilità: accessibilità filtri < 2 click
    - Performance: caricamento < 2s
    - Mobile-first

- Verifica: 
    - Test utente con 3-5 persone
    - A/B test layout
    - Metriche: tempo risoluzione ticket, errori utente

### Prompt Migliorato

```txt
Sei uno specialista UX/UI. Analizza la dashboard tickets esistente (file: [PATH]) e proponi miglioramenti strutturati.

CONTESTO:
- Stack: [tech stack]
- Utenti: [descrizione utenti]
- Tipo ticket: [categoria]

OBIETTIVI:
1. Rendi la dashboard moderna e professionale
2. Aggiungi filtri per: stato, priorità, data, assegnatario, categoria
3. Migliora la navigazione e l'usabilità
4. Correggi eventuali bug di UX

VINCOLI:
- Rispetta il design system esistente
- Responsive (mobile-first)
- Accessibilità WCAG 2.1 AA

OUTPUT ATTESO:
1. Analisi problemi attuali
2. Proposta wireframe testuale
3. Specifiche filtri e interazioni
4. Codice da implementare (in ordine di priorità)

ESEMPIO OUTPUT DESIDERATO:
[Inserisci 1 esempio di come vorresti la risposta - es. struttura sezioni, formato specifiche]
```

### Prova Di Controllo

```txt
testare manualmente se i filtri funzionano e il layout sia migliorato
```