# MSc-Final-Project
# An Explainable Multi-Feature Machine Learning Framework for Predicting Soccer Pass Outcomes

## Overview
This framework predicts soccer pass outcomes (success/failure) using 33 features organised into five methodologically distinct categories — spatial, temporal, contextual, player-based and sequential-lag — built on StatsBomb open event data. Explainability is provided via Tree-SHAP and validated through the Remove And Retrain (ROAR) faithfulness protocol.

## Key Results
- Dataset: 199,899 passes across 4 competitions (Euro 2024, World Cup 2022, La Liga 2019/20 & 2020/21)
- Best model: XGBoost-Optuna — AUC 0.9367 on held-out test set
- 5-fold CV: AUC 0.9366 ± 0.0044
- Temporal holdout (La Liga → Euro+WC): AUC 0.9357
- Controlled decomposition: model capacity +0.1229, feature diversity +0.0423
- ROAR: monotonic AUC decline from 0.9367 to 0.8844 at 20% masking — confirmed faithful

## Reproducing the Results
Open the notebook in Google Colab or Jupyter and run all cells top to bottom. Dependencies are installed in Cell 1.

```bash
pip install statsbombpy shap xgboost optuna
```

## Files
- `MSc_Project_Code.ipynb` — main notebook (all 30 cells, 12 stages)

## Citation
If you use this framework, please cite the dissertation:
> Thapa Magar, A. (2026). *An Explainable Multi-Feature Machine Learning Framework for Predicting Soccer Pass Outcomes*. MSc dissertation, University of Roehampton.

## Licence
MIT for the code. StatsBomb data is distributed under StatsBomb's own open-data licence.
