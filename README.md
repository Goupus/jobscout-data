# jobscout-data (privat)

Private Daten für [jobscout](https://github.com/Goupus/Jobscout): Profil, Quellen, Einstellungen und die Ergebnisdatenbank.

- `profile/` – Profil (CV, Interessen, Interview, Persönlichkeitsanalysen)
- `sources.yaml` – gescannte Quellen
- `settings.yaml` – Modell, Schwellwerte, Sprache
- `jobscout.db` – Ergebnisse (wird von der Action aktualisiert)

Der Scan läuft Mo + Do per GitHub Action (`.github/workflows/scan.yml`).
Benötigtes Secret: `ANTHROPIC_API_KEY`.

## Die App

```bash
git clone https://github.com/Goupus/jobscout-data && cd jobscout-data
pip install "jobscout[app] @ git+https://github.com/Goupus/Jobscout.git"
jobscout app -d .
```

Dort: Unterlagen hochladen, Interview führen, Quellen bearbeiten und testen, Matches ansehen.
Änderungen mit **Save to GitHub** (Seitenleiste) hochladen, neue Ergebnisse mit **Get latest results** holen.
Status und Notizen zu Stellen liegen in `tracker.yaml`.
