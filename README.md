# React Spectrum API Snapshots

Weekly API diffs for react-spectrum `main`, generated automatically each Monday.

## Structure

- `diffs/YYYY-MM-DD.txt` — weekly diff of current `main` vs the release baseline (output of `compareAPIs.js --isCI`)

## How It Works

Each week the automation compares the current `main` API surface against a fixed release baseline commit. The `.txt` files here are the raw diff output. To see what changed *this week specifically*, diff two consecutive files:

```bash
diff diffs/2026-05-01.txt diffs/2026-05-08.txt
```

## Baseline

Currently using commit `ca748178f7975b914f689dd6d0f164622109b0b9` as the fixed release reference. The baseline is built locally via:

```bash
yarn build:api-branch --githash=ca748178f7975b914f689dd6d0f164622109b0b9 --output=base-api
```

This will eventually be replaced by `yarn build:api-published` once that script is fixed.

## Logs

Each run logs to `/tmp/weekly-tsdiffer.log` on the local machine.

## Setup

See `scripts/weekly-api-diff/README.md` in the [react-spectrum repo](https://github.com/adobe/react-spectrum).
