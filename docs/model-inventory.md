# Model Inventory

Current trained-model inventory for the private Glitch models repository.

## Summary

- Approximate size: `75.19 MB`
- Top-level model families:
  - `viper`
  - `hydra`
  - `king_cobra`
  - `shared`
  - `unified`

## File Counts

- `ml_models/viper`: `3` files
- `ml_models/viper/models`: `3` files
- `ml_models/hydra`: `2` files
- `ml_models/hydra/models`: `3` files
- `ml_models/hydra/research/model_backups/20260331_034001`: `3` files
- `ml_models/hydra/research/model_backups/20260331_041349`: `4` files
- `ml_models/king_cobra`: `5` files
- `ml_models/shared/pro_modules_json`: `4` files
- `ml_models/shared/workspace_models`: `13` files
- `ml_models/unified`: `8` files

## Notable Current Assets

- shared XGBoost JSON exports such as `btc_xgb_super.json` and `xau_xgb_super.json`
- bot-specific XGBoost pickle artifacts for `viper`, `hydra`, and `king_cobra`
- unified ensemble artifacts including classifier, regressor, LightGBM, feature importance, SHAP summary, and training reports
- Hydra dated backup folders for research retention

## Notes

- Some model families exist both as primary working copies and dated backups.
- Unified outputs include both binary classification and regression artifacts.
- This repo should stay model-focused; raw CSV research data belongs in the separate private ML data repo.
- `ml_models/king_cobra/pro_modules` preserves feature manifests, supermodel JSON exports, and training reports from the research pipeline.
- `ml_models/hydra/research` now includes JSON retrain summaries, indicator backtest reports, and backup metadata alongside saved model artifacts.
