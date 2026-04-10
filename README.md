# Glitch Models

Private trained-model repository for the Glitch Executor ecosystem.

This repo is intended to hold trained model artifacts, backups, and ensemble outputs that should stay separate from both the public code repositories and the raw ML data repository.

## Purpose

This repository exists to:

- preserve trained model artifacts and checkpoints
- keep production-ready and research models separate from raw datasets
- centralize unified ensemble outputs
- make future retrains and model versioning easier to manage

## Privacy Rule

This repository must remain private.

Do not publish it, mirror it, or copy it into any public Glitch repository.

## Current Model Set

- Approximate current size: `57.84 MB`
- Current sources:
  - `viper`
  - `hydra`
  - `king_cobra`
  - `shared`
  - `unified`
- Inventory: [docs/model-inventory.md](./docs/model-inventory.md)

## Structure

```text
glitch-models-private/
|-- ml_models/
|   |-- viper/
|   |-- hydra/
|   |-- king_cobra/
|   |-- shared/
|   `-- unified/
`-- docs/
```

## What Belongs Here

- trained `.pkl`, `.joblib`, `.h5`, `.onnx`, `.model`, `.bin`, `.pt`, `.pth`, `.xgb` artifacts
- model JSON exports
- unified ensemble outputs
- training reports, feature-importance outputs, and SHAP exports tied to saved model versions

## What Does Not Belong Here

- raw ML CSV data
- live broker credentials
- running bot state
- logs that are not directly tied to saved model versions
- Python environments or cache folders

## Future Model Drops

When adding new model versions:

- preserve bot-level folders where possible
- use dated backup folders for major retrains
- keep training reports alongside the model family they describe
- treat model changes as versioned research assets, not disposable outputs

## Relationship To Other Glitch Repos

- public repos hold architecture and strategy code
- `glitch-executor-ml-data` holds the raw training and labeled-outcome data
- this private repo holds the trained artifact layer derived from that data
