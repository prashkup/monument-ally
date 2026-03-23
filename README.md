# Monument Ally, Monument Research Platform

An interactive research and data visualisation platform exploring three significant Indian monuments — the **Taj Mahal**, **Brihadeeswarar Temple**, and **Virupaksha Temple at Hampi** — through interconnected historical, architectural, and cultural data.

Built as an open source project and developed as a speculative pitch for a commissioned cultural heritage platform.

---

## Motivation

Existing resources on Indian monuments are scattered across Wikipedia articles, ASI documents, and academic papers with no unified, navigable interface. This project attempts to bring structured, interconnected data together in a form that is explorable rather than just readable — closer to a research tool than a tourist guide.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | ClojureScript + Reagent + Re-frame |
| Data visualisation | D3.js |
| Backend / data store | TiddlyWiki (Node.js) |
| Storage | Cloudflare R2 |
| Hosting | Cloudflare Pages + Hetzner VPS |

The choice of ClojureScript and Re-frame is deliberate: immutable state and unidirectional data flow make the complex interconnections between monument data (architectural lineages, patronage networks, chronologies) much easier to reason about than a mutable component tree would allow.

---

## Monuments

### Taj Mahal, Agra
Mughal funerary architecture at its apex. The platform traces the patronage network of Shah Jahan, the Persian and Central Asian design influences, the craftsmanship traditions employed, and the monument's evolving symbolic status across centuries.

### Brihadeeswarar Temple, Thanjavur
A Chola imperial statement in stone. Focus areas include Rajaraja I's political use of temple architecture, the Dravidian *vimana* construction techniques, the copper plate inscriptions that document the temple's endowments, and its relationship to the broader Chola administrative system.

### Virupaksha Temple, Hampi
The sacred centre of the Vijayanagara Empire. The platform maps the temple's growth across dynastic periods, the *mandapa* typologies, the relationship between the sacred complex and the surrounding market and palatial zones, and the aftermath of the 1565 sack of Hampi.

---

## Architecture

```
monuments-platform/
├── src/
│   ├── cljs/
│   │   ├── core.cljs          # Re-frame app entry point
│   │   ├── events.cljs        # State transitions
│   │   ├── subs.cljs          # Derived data subscriptions
│   │   └── views/
│   │       ├── monument.cljs  # Monument detail views
│   │       └── visualisation.cljs  # D3 integration layer
│   └── tiddlers/              # TiddlyWiki data store
├── resources/
│   └── public/
│       └── index.html
└── shadow-cljs.edn
```

---

## Status

Early development. The data model and frontend architecture are being designed; the TiddlyWiki backend is being configured for structured tiddler storage. Visualisation components are being prototyped in D3.

Contributions, corrections to historical data, and feedback on the architectural approach are welcome.

---

## Licence

MIT
