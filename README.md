# Curriculum Vitae

CV personale in HTML, CSS e vanilla JS — nessun framework, nessun build step.

## Come funziona

Tutto il contenuto del CV è nel file **`data.json`**. L'HTML lo legge e genera le sezioni automaticamente. Per aggiornare il CV basta modificare il JSON.

```
cv/
├── index.html   ← template (non serve toccarlo per aggiornare i contenuti)
├── style.css    ← stile grafico
├── data.json    ← ✏️  i tuoi dati vanno qui
└── README.md
```

## Uso rapido

1. Clona il repo
2. Apri `data.json` con un editor di testo
3. Sostituisci i dati di esempio con i tuoi
4. Apri `index.html` nel browser

> **Nota:** serve un server locale per il fetch del JSON.
> Il modo più semplice: `npx serve .` oppure l'estensione Live Server di VS Code.

## Personalizzazione

### Contenuti (`data.json`)

Ogni sezione ha una chiave dedicata:

| Chiave           | Cosa contiene                          |
|------------------|----------------------------------------|
| `persona`        | Nome, cognome, ruolo, sommario         |
| `contatti`       | Città, telefono, email, link           |
| `competenze`     | Skill con livello e percentuale barra  |
| `lingue`         | Lingua e livello                       |
| `interessi`      | Lista di tag                           |
| `esperienze`     | Ruolo, azienda, periodo, punti/desc    |
| `formazione`     | Titolo, istituto, indirizzo, anno      |
| `certificazioni` | Titolo, ente, anno                     |

### Colori e font (`style.css`)

Le variabili CSS sono in `:root` — cambia lì per modificare palette e dimensioni della sidebar.

### Icone

Le icone SVG sono definite nell'oggetto `ICONS` dentro `index.html`. Per aggiungerne una nuova, copia un SVG e assegnagli una chiave, poi usa quella chiave nel campo `icona` del contatto in `data.json`.

## Pubblicazione su GitHub Pages

1. Push del repo su GitHub
2. Vai in **Settings → Pages**
3. Seleziona il branch `main` e la cartella `/` (root)
4. Il CV sarà online su `https://tuousername.github.io/nome-repo/`

## Stampa / PDF

Usa `Ctrl+P` (o `⌘+P`) nel browser. Gli stili di stampa sono già inclusi per un risultato pulito.

## Licenza

Progetto personale — usa e adatta liberamente.
