# React Spectrum API Snapshots

Weekly rolling API surface diffs for react-spectrum, generated automatically each Monday.

## Structure

- `snapshots/YYYY-MM-DD/` — weekly copy of `dist/branch-api/` from react-spectrum
- `diffs/YYYY-MM-DD.md` — human-readable API diff for that week (output of `compareAPIs.js --isCI`)
- `latest/` — copy of the most recent snapshot, used as baseline for the next run

## First Run

On first run (when `latest/` is absent), the baseline is built from published npm packages via `yarn build:api-published`.

## Logs

Each run logs to `/tmp/weekly-tsdiffer.log`.
