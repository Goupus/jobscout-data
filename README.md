# jobscout-data (privat)

Private Daten für [jobscout](https://github.com/Goupus/Jobscout): Profil, Quellen, Einstellungen und die Ergebnisdatenbank.

- `profile/` – Profil (CV, Interessen, Interview, Persönlichkeitsanalysen)
- `sources.yaml` – gescannte Quellen
- `settings.yaml` – Modell, Schwellwerte, Sprache
- `jobscout.db` – Ergebnisse (wird von der Action aktualisiert)

Der Scan läuft Mo + Do per GitHub Action (`.github/workflows/scan.yml`).
Benötigtes Secret: `ANTHROPIC_API_KEY`.

Lokal ansehen:
```bash
git pull
pip install "jobscout[dashboard] @ git+https://github.com/Goupus/Jobscout.git"
jobscout dashboard -d .
```
