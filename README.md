# PezzaliHub

**Il territorio in tempo reale.** Meteo, strada, cielo, sensori e dati in movimento:
il punto dell'ecosistema [PezzaliAPP](https://www.pezzaliapp.com) dedicato ai dati che cambiano nel tempo e nello spazio.

🌐 Sito live: <https://pezzalihub.app>

## Progetti

| Progetto | Ambito | Link |
| --- | --- | --- |
| **Finestrino** *(nuovo)* | Aerei, navi e satelliti sopra di te, visti dal finestrino in 3D | <https://www.alessandropezzali.it/finestrino/> |
| **NOWCAST** | Celle temporalesche, grandine e downburst dai mosaici radar | <https://nowcast.pezzalihub.app> |
| **ROAD SENSE** | Anomalie stradali rilevate dai sensori dello smartphone | <https://roadsense.pezzalihub.app> |
| **EarthRadar** | Vista della Terra e di ciò che si muove sopra di noi | <https://www.alessandropezzali.it/EarthRadar/> |
| **Il Quaderno di Micelio** | Pioggia, suolo, habitat e osservazioni nel bosco | <https://ilquadernodimicelio.it> |

## Struttura

- `index.html` — homepage single-file (HTML + CSS inline)
- `quoziente-intellettivo.html` — pagina di approfondimento
- `manifest.json` — manifest PWA
- `sw.js` — service worker (network-first per la navigazione, cache-first per gli asset)
- `sitemap.xml`, `robots.txt` — SEO
- `CNAME` — dominio personalizzato `pezzalihub.app`
- `icon-192.png`, `icon-512.png`, `images/` — icone e immagini social

## Aggiungere un progetto

In `index.html`, dentro `<div class="grid">` della sezione `#live`, duplica un `<article class="card">`.
Varianti di colore disponibili: `nowcast` (ambra), `road` (blu), `sky` (viola, a tutta larghezza), nessuna (verde).
Ricordati di aggiornare il titolo della sezione («Cinque modi di osservare.»).

## Cache busting

A ogni aggiornamento incrementa la versione in `sw.js` e la data `lastmod` in `sitemap.xml`:

```js
const CACHE_NAME = "pezzalihub-v5-finestrino";
```

## Filosofia

Niente framework. Niente build. Niente dipendenze. Prima il segnale, poi l'interpretazione.

## Licenza

© 2026 Alessandro Pezzali. Il codice delle singole app è su <https://github.com/pezzaliapp>.
