# Consegna - Lezione 02

## Obiettivo

Classificare 4 richieste e decidere quale livello di autonomia dare all'AI.

Non devi fare patch. Devi scrivere prompt coerenti con il livello di autonomia scelto.

## Repository Di Lavoro

Lavora nel tuo fork della repo:

```txt
aicu-l02-prompt-autonomy
```

Ogni caso vive in una cartella:

```txt
casi/
  <caso>/
    richiesta.md
    classificazione.md
    prompt-operativo.md
```

Leggi `richiesta.md`, compila `classificazione.md` e scrivi un prompt proporzionato in `prompt-operativo.md`.

## Modalita'

Usa una o piu' modalita' coerenti:

- `Capire`: orientamento senza modificare file.
- `Pianificare`: piano breve prima di autorizzare modifiche.
- `Modificare`: patch piccola solo dopo piano e confini chiari.
- `Fermarsi / Chiarire`: freno quando task, rischio o verifica non sono chiari.

## Termini Base

- `issue`: richiesta di lavoro precisa.
- `plan`: piano prima della modifica.
- `diff`: confronto tra codice prima e dopo.
- `review`: controllo critico della modifica.
- `verify`: prova che il comportamento funziona.
- `handoff`: nota breve per chi revisiona o continua.

## Rubrica Rischio / Autonomia

Per ogni caso considera:

| Criterio | Domanda |
| --- | --- |
| Chiarezza task | Riesci a dire il lavoro in una frase? |
| Sensibilita' dati | Potrebbero entrare dati, credenziali o codice non autorizzato? |
| Blast radius | La richiesta puo' toccare troppe aree o cambiare layout/routing? |
| Reversibilita' | Il risultato sarebbe piccolo e controllabile da diff? |
| Costo di verifica | Sai indicare una prova concreta? |
| Permesso massimo | L'AI puo' leggere, pianificare, modificare o deve fermarsi? |
| Strategia prompt | Bastano istruzioni zero-shot o servono esempi few-shot? |

## Casi

Nel repository trovi quattro cartelle in `casi/`. Le richieste saranno equivalenti a queste:

### Caso 1

```txt
Non so dove viene renderizzata la lista dei ticket.
```

### Caso 2

```txt
Migliora tutta la UX della dashboard ticket, aggiungi filtri, rendila piu' moderna e sistema eventuali problemi.
```

### Caso 3

```txt
Dobbiamo aggiungere un messaggio quando non ci sono ticket aperti, ma prima voglio capire quali file toccherebbe.
```

### Caso 4

```txt
Dopo aver approvato il piano, applica la modifica minima per mostrare il messaggio nello stato senza ticket.
```

## Output Obbligatorio

Per ogni caso compila:

```txt
classificazione.md
prompt-operativo.md
```

Per ogni caso indica:

- modalita' scelta;
- rischio: basso / medio / alto;
- criterio principale che determina il rischio;
- motivazione;
- strategia prompt: zero-shot / few-shot;
- prompt operativo;
- prova di controllo.

## Vincoli

- Non modificare file.
- Non aprire PR.
- Non aggiungere `AGENTS.md` o `prompt-kit/`: arriveranno in L03.
- Non usare "l'AI dice che funziona" come verifica.
- Non chiedere chain-of-thought estesa: chiedi assunzioni, criterio e verifica.
- Se usi few-shot, usa esempi brevi che mostrano formato o criterio, non soluzioni.
- Se la richiesta e' troppo larga, fermati e riscrivila in task piu' piccoli.

## Pronto Quando

- Hai compilato 4 casi.
- Hai motivato il rischio.
- Hai scritto un prompt coerente con il mode.
- Hai indicato se il prompt operativo e' zero-shot o few-shot.
- Hai indicato una prova di controllo concreta.
- Sai spiegare quando useresti `Fermarsi / Chiarire`.
- Hai committato e pushato il lavoro nel tuo fork.

> **Team Mode**
> Prima di lasciare modificare un agent, chiediti se sapresti spiegare a un reviewer perche' quella modalita' era proporzionata al rischio.
