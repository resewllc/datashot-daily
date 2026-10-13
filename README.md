# DataShot Daily

Signed daily stage manifests for the iOS game **DataShot** (a bullet-hell game whose stages are
generated from real-world data). One immutable manifest per UTC day:

- `daily/<YYYY-MM-DD>.json` — the day's stage manifest (Ed25519-signed; the app verifies the
  signature, date, versions and stage hash before play)
- `daily/index.json` — the latest date and recent dates

Published automatically around 23:50 UTC for the next day. Files are never modified after publication.

## Data sources

The manifests contain values derived from:

- Wikimedia pageviews (all projects, aggregate totals) — Wikimedia Foundation, CC0
- Weather data by [Open-Meteo.com](https://open-meteo.com/) — CC BY 4.0
- Earthquake times and magnitudes (M4.5+) — U.S. Geological Survey
- Real-time solar wind and planetary Kp — NOAA Space Weather Prediction Center

The game converts these values for play. They are not forecasts or warnings.
