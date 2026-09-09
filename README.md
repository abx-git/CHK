# CHK Checklisten

Öffentliches Listen-Repo für die CHK-App.

Die App lädt `catalog.json` und die Dateien unter `lists/`. Änderungen hier (Commit auf `main`) sind nach einem Refresh in der App sichtbar.

## Neue Liste hinzufügen

1. JSON im Format `chk.list` nach `lists/` legen (aus der App: Listen verwalten → Teilen-Symbol an der Liste).
2. Eintrag in `catalog.json` ergänzen:

```json
{
  "id": "MEINE-LISTE",
  "name": "Musterflugzeug",
  "registration": "D-XXXX",
  "description": "Kurzbeschreibung",
  "file": "lists/musterflugzeug.json"
}
```

3. Nach `main` pushen.

## Dateiformat

```json
{
  "kind": "chk.list",
  "schemaVersion": 3,
  "description": "…",
  "aircraft": { "id": "…", "name": "…", "registration": "…" },
  "checklist": { "id": "…", "aircraftId": "…", "mode": "", "phases": [] },
  "emergencies": []
}
```
