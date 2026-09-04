# Implementation Plan — Sol & Local: Benevento in uno o due giorni

Guida dinamica, iper-dettagliata e autonoma per la visita a piedi del centro storico di Benevento e della provincia sannita, integrata con le indicazioni logistiche e cliniche della Nuova Clinica Santa Rita.

---

## 1. Visione del Progetto & Brand Philosophy
* **Brand:** *Sol & Local* (stile editoriale, focalizzato su esperienze di viaggio autentiche, logistica a piedi a chilometro zero, trasparenza totale su orari, costi e fonti).
* **Obiettivo:** Fornire un vademecum completo per una visita ottimale (focalizzata su **martedì 1 settembre 2026** e formula 1-2 giorni), eliminando ogni dubbio pratico su parcheggi, orari di apertura, giorni di chiusura dei locali, percorsi del totem **BenOriento** e tariffe.

---

## 2. Architettura Tecnica & Componenti

### 2.1 Stack Tecnologico
* **Frontend Core:** HTML5 semantico puro, zero framework pesanti, caricamento istantaneo (zero layout shift).
* **Styling & Design System:**
  * `quadro-partenze.css`: Estetica da tabellone a palette sferraglianti (split-flap board), tipografia monospazio per orari, badge di stato cromatici (*verificato*, *da confermare*, *chiuso*).
  * `benevento.css`: Layout responsive a griglia/stack, token OKLCH armonici per tema chiaro e scuro, gestione card, pannelli e tabelle dense di dati.
  * **Tema Scuro/Chiaro:** Script inline nell'<head> per applicazione immediata di `data-theme` da `localStorage` / `prefers-color-scheme` senza flash visivo (FOUC).
* **Interattività & Accessibilità:**
  * **Visore Lightbox Foto:** Modal a pieno schermo nativo in Vanilla JS con chiusura via `Esc`, click fuori e pulsante `×`, supporto navigazione da tastiera (`Enter`/`Space`).
  * **Deep Linking Google Maps:** Link diretti di navigazione e ricerca per ogni monumento, B&B e ristorante.
* **Hosting & DevOps:**
  * Distribuzione su rete edge globale tramite **Vercel** (`benevento-xi`).
  * `package.json` con comandi standard per sviluppo locale (`npm run dev`) e deploy (`npm run deploy`).

---

## 3. Ruoli Multi-Agent (Separazione dei Compiti)

* **[FRONTEND-AGENT]**:
  * Progettazione e manutenzione dei componenti UI (Quadro Partenze, tessere monumenti, griglie orari).
  * Ottimizzazione della resa visiva su mobile e desktop.
  * Gestione accessibilità ARIA, contrasto colori OKLCH e comportamento responsive del visore lightbox.
* **[BACKEND-AGENT]**:
  * Audit continuo dei dati fattuali: orari di musei, cattedrale, clinica, sagre e mercatini.
  * Controllo incrociato delle fonti ufficiali (Comune di Benevento, Diocesi, Direzione Musei, siti ufficiali dei ristoranti e delle strutture ricettive).
  * Verifica dello stato delle chiusure per il target temporale (martedì a pranzo).
* **[DEVOPS-AGENT]**:
  * Gestione configurazione Git e sincronizzazione con `origin/main` su GitHub.
  * Manutenzione della configurazione Vercel e dei file di dipendenze Node.js.
  * Monitoraggio performance e validazione build statica.

---

## 4. Fasi di Implementazione

### Fase 1: Struttura Base & Itinerari a Piedi (Completata)
- [x] Stesura dell'itinerario a piedi di 1 giorno e 2 giorni.
- [x] Mappatura del parcheggio di riferimento (Piazza Cardinal Pacca / Megaparcheggio).
- [x] Sezione clinica dedicata alla Nuova Clinica Santa Rita (reparti, CUP, accoglienza).

### Fase 2: Totem BenOriento & Immagini Monumentali (Completata)
- [x] Integrazione delle foto ad alta risoluzione da Wikimedia Commons (Arco di Traiano, Santa Sofia, Hortus Conclusus, Rocca, Teatro Romano).
- [x] Mappatura dei 5 percorsi del totem storico BenOriento con relative palette cromatiche OKLCH dedicate.
- [x] Visore lightbox a schermo intero accessibile.

### Fase 3: Audit Dati & Verifica Fonti Ufficiali (Completata)
- [x] Verifica orario estivo Cattedrale (Duomo) e Museo Diocesano / Ipogeo.
- [x] Verifica orario estivo Villa Comunale (8:30–24:00 fino al 15 settembre).
- [x] Audit ristorazione con identificazione tempestiva delle chiusure del martedì (*Parisio*, *Scialapopolo*, *Roseto a pranzo*).
- [x] Verifica orari CUP, ricoveri e visite ai degenti della Clinica Santa Rita.
- [x] Verifica date sagre (Sagra del Maialetto di Apollosa 11–13 settembre).
- [x] Censimento contatti e prezzi medi dei B&B del centro.

### Fase 4: Tooling & Manutenibilità (Completata)
- [x] Creazione `package.json` con script standard.
- [x] Dynamic documentation suite (`IMPLEMENTATION_PLAN.MD`, `TASKS.MD`, `GEMINI.MD`, `README.MD`).
