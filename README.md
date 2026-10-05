# Zen Meditation Timer 🧘‍♂️

![Version](https://img.shields.io/badge/version-1.1-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Active-brightgreen.svg)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-orange.svg)

Una web application essenziale, fluida e reattiva progettata per accompagnare la sessione di meditazione con il suono sintetizzato di campane tibetane. 

Disponibile come **Progressive Web App (PWA)**, installabile su dispositivi Android, iOS e Desktop per un utilizzo offline senza interruzioni.

📍 **Live Demo:** [https://tagtthespellcaster.github.io/Meditation-Timer/](https://tagtthespellcaster.github.io/Meditation-Timer/)

---

## 📋 Caratteristiche (v1.1)

- **Sintesi Audio in Tempo Reale:** Suoni di campane tibetane generati tramite Web Audio API (nessun file audio esterno o ritardo di caricamento).
- **Selezione del Tono:** 6 differenti profili sonori selezionabili (dalle frequenze basse dei gong alle campane ad alta risonanza).
- **Gestione Fasi di Preparazione:** Possibilità di impostare un periodo di riscaldamento iniziale (regolabile a intervalli di 10 secondi, fino a un massimo del 20% del tempo totale).
- **Suddivisione in Intervalli:** Possibilità di ripartire la sessione in più periodi uguali, separati da un rintocco a volume ridotto (50%).
- **Persistenza delle Impostazioni:** Salvataggio automatico delle preferenze correnti in `localStorage`.
- **Tracciamento Statistiche:** Monitoraggio dei minuti totali di meditazione accumulati nel tempo.
- **Supporto PWA Offline:** Installabile direttamente sulla schermata Home dello smartphone o del computer tramite Service Worker.
- **Interfaccia Zen:** Design scuro ad alto contrasto con anello di avanzamento circolare e animazioni fluide.

---

## 🛠️ Modello Logico degli Intervalli

Il tempo di preparazione è **incluso** nel tempo totale di meditazione selezionato.

*Esempio:*
- **Tempo totale:** 10 minuti
- **Preparazione:** 1 minuto
- **Intervalli:** 2 periodi

**Sequenza temporale:**
1. **00:00** — Suono iniziale (inizio preparazione)
2. **01:00** — Suono principale a pieno volume (fine preparazione / inizio meditazione effettiva)
3. **05:30** — Suono di metà percorso a volume ridotto (50%)
4. **10:00** — Suono finale a pieno volume (conclusione)

---

## 📦 Struttura del Progetto

```text
├── index.html       # Applicazione principale (HTML5, CSS3, JS ES6)
├── manifest.json    # Configurazione Progressive Web App
├── sw.js            # Service Worker per la gestione della cache offline
├── icon-192.png     # Icona app (192x192)
├── icon-512.png     # Icona app (512x512)
└── LICENSE          # Licenza MIT
