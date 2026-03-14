# Europa Wanderkarte – Webmap-Prototyp

## Enthalten
- `index.html`
- `styles.css`
- `app.js`
- `routes_top50_clean.geojson`
- `shelters.geojson`
- `countries_wildcamp.geojson`
- `wildcamping_admin1_de_be_pl_tr_at.geojson`
- `wildcamping_rules.json`
- `quellen.html`
- `workflow.html`

## Start
Die Dateien müssen über einen kleinen lokalen Webserver geladen werden, weil `fetch()` bei einem direkten Doppelklick auf `index.html` oft blockiert wird.

Im Ordner `webmap_prototype_v6` z. B.:

```bash
python -m http.server 8000
```

Danach im Browser:
`http://localhost:8000`

## Aktueller Funktionsumfang
- 51 Wanderwege als interaktiver Linienlayer
- 8.328 Schutzhütten mit Clustering
- Seitliche Routenauswahl und Suche
- Popups für Routen, Hütten und Wildcamping
- europaweiter Länder-Layer für Wildcamping
- Admin-1-Layer für Deutschland, Belgien, Polen, Türkei und Österreich
- eigene Seiten für Quellen und Workflow über Link in der Sidebar

## Hinweise
- In Popups werden nur echte http/https-Weblinks angezeigt
- Textfelder ohne gültige URL werden nicht als anklickbare Links gerendert
- Für konkrete Tourenplanung sollten rechtliche Details immer zusätzlich lokal geprüft werden


Version v8:
- Dokumentationsseiten als transparentes Overlay in der Karte statt als separate Ansicht
- Routen-Layer über Polygonen und Schutzhütten angeordnet
- Länderlayer für DE, PL, BE und AT ausgeblendet, wenn Admin-1-Daten vorhanden sind
- nur ein Popup gleichzeitig sichtbar
- Statusmeldung blendet sich automatisch aus
