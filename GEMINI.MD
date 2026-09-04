# Gemini Memory & Context Log — Benevento-XI

## 2026-08-31 / 2026-09-03 (Fondazione & Sviluppo Iniziale)
- **Goal**: Creazione di una guida web statica, ricca di dettagli e orientata all'esperienza a piedi nel centro storico di Benevento in data martedì 1 settembre 2026.
- **Decisioni Architetturali**:
  - Adozione dello stile editoriale **Sol & Local** con il tabellone a scorrimento sferragliante tipico delle stazioni ferroviarie (`quadro-partenze.css`) combinato con un design pulito ed elegante (`benevento.css`).
  - Zero framework JS: tutto il codice HTML e CSS è nativo e leggero.
  - Fotografia ad alta risoluzione da Wikimedia Commons e scatti reali del totem "BenOriento" sul posto.
  - Implementazione dei 5 percorsi storici del totem BenOriento (Museale, Romano, Longobardo, Pontificio Ecclesiastico, Pontificio Nobiliare) con triple OKLCH dedicate.
  - Integrazione visore modale a schermo intero (lightbox) accessibile tramite click e scorciatoie tastiera (`Esc`, `Invio`, `Spazio`).

## 2026-09-04 (Audit Dati Mancanti, Verifica Fonti & Tooling Setup)
- **Goal**: Effettuare l'audit completo di tutti gli orari, recapiti, chiusure e dati mancanti o contrassegnati come "da confermare" e standardizzare il tooling di progetto secondo le linee guida di sistema.
- **Azioni Eseguite**:
  - Spawned **Senior Full Stack Expert**, **Backend-Agent**, **Frontend-Agent** e **DevOps-Agent**.
  - **Audit Dati Fattuali [Backend-Agent]**:
    - **Nuova Clinica Santa Rita**: verificati orari CUP ambulatori (lun–sab 14:00–19:30), ricoveri (08:00–13:00) e visite scaglionate estive (Ortopedia/Ginecologia 17:00–18:00, Chirurgia/Urologia/Medicina 18:00–19:00). Tel. 0824 311475.
    - **Duomo di Benevento**: verificato orario cattedrale (7:00–12:00 / 16:30–19:30 estivo) ed orari Ipogeo / Museo Diocesano (mar–sab 9:00–13:00 / 16:00–19:00, tel. 371 1951770).
    - **Villa Comunale**: verificato orario estivo di apertura dalle 8:30 alle 24:00 (fino al 15 settembre, Comune di Benevento).
    - **Ristorazione**: scoperta critica per la visita di martedì a pranzo. *Locanda Scialapopolo* e *Parisio* sono chiusi il martedì; *Il Roseto all'Arco* è aperto solo a cena nei giorni feriali. Confermato che le opzioni ideali a pranzo in centro sono *Trattoria Nunzia* (chiusa la domenica, aperta lun–sab), *Il Posto* (aperto a pranzo 12–15) e *Osteria Sapori di Corte*. *Pascalucci* (San Nicola Manfredi) è chiuso il giovedì ed è aperto il martedì.
    - **Spazio Strega**: confermate visite gratuite su prenotazione obbligatoria (0824 50102), lun–ven e 1ª domenica del mese.
    - **B&B & Ospitalità**: censiti recapiti telefonici diretti e fasce prezzo medie per *Guest House Orsini*, *B&B Le Streghe*, *Le Stanze del Sogno*, *La Fara B&B* e *B&B Benevento Centro*.
    - **Sagre**: confermata la data ufficiale della *Sagra del Maialetto di Apollosa* (11–13 settembre 2026).
  - **Tooling & Setup [DevOps-Agent]**:
    - Creato `package.json` con metadati e script di esecuzione locale (`npm run dev`) e deploy su Vercel (`npm run deploy`).
    - Redatti `IMPLEMENTATION_PLAN.MD`, `TASKS.MD`, `GEMINI.MD` e `README.MD`.
