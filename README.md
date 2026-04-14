> **⚠️ FROZEN HISTORICAL ARCHIVE — as of 2026-04-14**
>
> This repository is no longer updated. All ML data collection now lives
> on the server at `/opt/ml/` and stays there — no new pushes land here.
>
> - **Authoritative live data:** PostgreSQL tables `ml_signals`, `ml_trades`,
>   `ml_bars` on the production server
> - **Daily CSV snapshots:** `/opt/ml/live/YYYY-MM-DD/` (systemd timer
>   `glitch-ml-export.timer`)
> - **Historical MT5-era archive** (what used to be pushed here): moved to
>   `/opt/ml/historical/` on the server
>
> Keep this repo around as read-only history. Archive in the GitHub UI
> when convenient (Settings → Danger Zone → Archive this repository).

---
# Glitch Executor ML Models

Private trained-model repository for the Glitch Executor ecosystem.

This repository stores the trained artifact layer derived from Glitch’s raw and cleaned ML datasets: checkpoints, ensemble outputs, metadata, and model-family snapshots that should stay separate from public code and from the raw data repository.

## Repo Role

This repo exists to preserve:

- trained model artifacts and checkpoints
- production-ready and research model versions
- unified ensemble outputs
- model metadata and report snapshots
- versioned backups for retrains

## Structure

- `ml_models/` for saved model families and artifacts
- `docs/` for inventories, report notes, and model organization

## Privacy

This repository must remain private.

Do not mirror it to public repos. Do not mix in raw training datasets, secrets, broker state, or unrelated runtime logs.

## Relationship To Other Repos

- public repos hold architecture and strategy code
- `glitch-executor-ml-data` holds the raw and cleaned dataset layer
- this repo holds the trained artifact layer derived from that data

## Working Notes

When adding new model versions:

- preserve model-family folders where possible
- keep reports alongside the model family they describe
- treat retrains as versioned research assets, not disposable outputs
