# 🏛️ Sol & Local — Benevento in uno o due giorni

> **Guida a piedi, logistica, BenOriento e provincia del Sannio.**  
> *Progettato per la visita di martedì 1 settembre 2026 e pronto per qualsiasi itinerario a piedi nel centro storico di Benevento.*

---

## 🌟 Cos'è questo progetto
**Benevento-XI** è una guida iper-dettagliata e compatta concepita secondo la filosofia di viaggio **Sol & Local**:
* **Itinerario a piedi**: Parcheggiata l'auto (Piazza Cardinal Pacca / Megaparcheggio), la città si gira completamente a piedi senza più riprendere il mezzo.
* **BenOriento sul posto**: I 5 percorsi ufficiali del totem storico beneventano (Museale, Romano, Longobardo, Pontificio Ecclesiastico, Pontificio Nobiliare) con cromie OKLCH conformi alla segnaletica reale.
* **Orari & Prezzi Verificati**: Ogni orario, prezzo o chiusura è verificato su fonti ufficiali (Diocesi, Comune di Benevento, portali museali e contatti diretti dei locali), distinguendo chiaramente i dati confermati da quelli da riverificare.
* **Nuova Clinica Santa Rita**: Scheda clinica e logistica completa con orari CUP, prenotazione ricoveri e visite ai degenti.
* **Tavola e Ospitalità**: Mappa dei ristoranti con evidenziazione speciale per i giorni di chiusura (focus sulle aperture a pranzo del martedì) e recapiti dei B&B del centro.

---

## 🚀 Come installare ed eseguire in locale

Il progetto è una web application ultra-leggera costruita con HTML5 semantico puro e Vanilla CSS, senza dipendenze pesanti o framework che rallentino il caricamento.

### Requisiti
* [Node.js](https://nodejs.org/) (versione 18 o superiore consigliata)

### 1. Clona il repository
```bash
git clone https://github.com/mich-de/benevento-xi.git
cd benevento-xi
```

### 2. Avvia il server di sviluppo locale
Puoi avviare il server web locale tramite `npm`:
```bash
npm run dev
```
oppure direttamente con `npx`:
```bash
npx serve .
```
Apri il browser su `http://localhost:3000` (o sulla porta indicata a terminale).

---

## ☁️ Come fare il deploy su Vercel

Il progetto è pre-configurato per il deploy su **Vercel** (`benevento-xi`):

```bash
npm run deploy
```
oppure:
```bash
npx vercel --prod
```

---

## 🧭 Struttura del Progetto

```text
benevento-xi/
├── index.html                   # Pagina principale dell'applicazione (guida interattiva)
├── package.json                 # Script e metadati del progetto
├── static/
│   ├── benevento.css            # Token OKLCH, stili responsive, card e layout editoriale
│   ├── quadro-partenze.css      # Tabellone orari stile split-flap e badge di stato
│   └── img/                     # Fotografie ad alta risoluzione (Arco, Santa Sofia, Totem...)
├── IMPLEMENTATION_PLAN.MD       # Strategia tecnica, architettura e fasi implementative
├── TASKS.MD                     # Tabella di marcia dinamica per Agent ([FRONTEND], [BACKEND], [DEVOPS])
├── GEMINI.MD                    # Log persistente di contesto e decisioni per le future sessioni
└── README.MD                    # Questo manuale d'uso e installazione
```

---

## 💡 Funzionalità Chiave dell'Interfaccia
1. **Modalità Notte / Giorno**: Selettore rapido nell'header con salvataggio preferenza in `localStorage` e script anti-flash pre-caricamento.
2. **Visore Lightbox Foto**: Cliccando su qualsiasi foto del sito (o premendo `Invio`/`Spazio` da tastiera) si apre l'immagine a piena risoluzione a tutto schermo con didascalia e crediti; si chiude con `Esc`, clic sullo sfondo o pulsante `×`.
3. **Deep Linking Google Maps**: Ogni monumento, B&B e ristorante dispone di link diretto di navigazione su Google Maps.
4. **Layout Ottimizzato per la Stampa**: Con `@media print` la barra di navigazione, i pulsanti di cambio tema e i controlli non essenziali vengono nascosti automaticamente per generare un perfetto promemoria cartaceo o PDF.

---

## 👤 Autore & Licenza
* **Autore:** [mich-de](https://github.com/mich-de) (`mic.deangelis@gmail.com`)
* **Licenza:** MIT
