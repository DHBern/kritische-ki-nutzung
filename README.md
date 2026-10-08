# Kritische KI-Nutzung

Website für den Workshop **«Kritische KI-Nutzung»** der AG Interne Weiterbildung (AG IWB) der
Universität Bern, geleitet von Prof. Dr. Tobias Hodel (Digital Humanities, Walter Benjamin
Kolleg).

🌐 <https://dhbern.github.io/kritische-ki-nutzung/> (bewusst nicht von dhbern.github.io verlinkt)

|              |                                               |
| ------------ | --------------------------------------------- |
| Datum        | Mittwoch, 14. Oktober 2026, 13:00–17:00       |
| Ort          | UniS, Schanzeneckstrasse 1, Seminarraum A-124 |
| Form         | Workshop, max. 25 Personen                    |
| Organisation | AG IWB (Andrea Stettler)                      |

## Struktur

```
index.qmd               Startseite: Eckdaten, Beschreibung, Lernziele, Ablauf, QR-Code
contents/
  programm.qmd          detailliertes Programm 13:00–17:00
  werkzeuge.qmd         Toolübersicht, GPUStack, KI-Angebote der Uni Bern
  aufgaben.qmd          Gruppenaufgaben und Präsentation
  agenten.qmd           LLM, Bot, Agent; Swiss History Bot; Agentic Historian
  reflexion.qmd         Grenzen, Leitfragen, Strategien
  folien.qmd            Folien (PDF in assets/)
assets/
  qr-code.svg/.png      QR-Code auf die Website
```

## Lokale Entwicklung

Benötigt [Quarto](https://quarto.org/docs/get-started/).

```bash
quarto preview      # Live-Vorschau
quarto render       # Build nach _site/
npm install         # Dev-Tooling (prettier, husky, commitizen)
npm run format      # Quellen formatieren
```

## Deployment

Ein Push auf `main` startet `.github/workflows/quarto-publish.yml` (Lint, Render, Optimierung,
Dead-Link-Check, Deployment auf GitHub Pages). In den Repository-Einstellungen muss unter
_Settings → Pages_ als Quelle **GitHub Actions** gewählt sein.

Die Seiten tragen `<meta name="robots" content="noindex">` (in `_quarto.yml`), damit die nicht
verlinkte Seite auch nicht in Suchmaschinen auftaucht.

## Lizenz

- Texte und Lehrmaterialien: [CC BY-SA 4.0](LICENSE-CCBYSA.md)
- Code: [AGPL-3.0](LICENSE-AGPL.md)
