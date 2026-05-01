# PezzaliHub

L'ecosistema **PezzaliAPP** in un solo luogo: 77 app web per officine, vendite, AI, musica, scienza e altro.

🌐 Sito live: <https://pezzalihub.app>

## Struttura

- `index.html` — homepage in stile Apple, single-file (HTML + CSS + JS inline)
- `manifest.json` — manifest PWA
- `sw.js` — service worker (cache strategy: network-first per la navigazione, cache-first per asset)
- `CNAME` — dominio personalizzato `pezzalihub.app`
- `icon-192.png`, `icon-512.png` — icone PWA

## Filosofia

Niente framework. Niente build. Niente dipendenze.
Un singolo file HTML che si carica all'istante e funziona offline.

## Categorie

Le 77 app sono organizzate in 13 categorie:

- 💼 **PWA Commerciali & Vendite** (31)
- 🛠️ **Officina & Tecnico** (7)
- 🤖 **AI & Assistenti** (8)
- 🧮 **Matematica & Finanza** (7)
- 🔬 **Fisica & Scienza** (5)
- 🎵 **Musica & Audio** (4)
- 🌐 **Hub & Identity** (4)
- 🔐 **Sicurezza & Privacy** (3)
- 🎮 **Giochi** (3)
- 🛰️ **Geo & Drone** (1)
- 📧 **Comunicazione** (1)
- ⏱️ **Produttività & Tools** (1)
- 🧪 **Sperimentali & Lab** (2)

## Aggiornamenti

Per aggiungere o togliere app, modifica l'array `DATA` dentro `<script>` in `index.html`.
Ogni voce ha la struttura:

```js
{
  "name": "lift-engine",
  "desc": "Universal lift configuration & pricing engine…",
  "cat": "🛠️ Officina & Tecnico",
  "domain": "https://www.alessandropezzali.it/lift-engine/",
  "gh": "https://pezzaliapp.github.io/lift-engine/",
  "repo": "https://github.com/pezzaliapp/lift-engine",
  "date": "2026-XX-XX"
}
```

## Cache busting

Quando aggiorni il sito, ricordati di incrementare la versione in `sw.js`:

```js
const CACHE_NAME = "pezzalihub-v5-...";
```

## Licenza

© 2026 Alessandro Pezzali. Tutto il codice delle singole app è open source su <https://github.com/pezzaliapp>.
