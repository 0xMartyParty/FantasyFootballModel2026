# FantasyFootballModel2026

A season-level fantasy football projection model for Wide Receivers using player, team, and QB context features.  
Compares linear models (OLS, Ridge, Lasso) vs XGBoost with strict time-based validation.

---

## 🎯 Objective

Predict:

- FantasyPoints_t  
or  
- FantasyPPG_t  

Each (Player_id, season_t) pair is treated as one observation.

All features are constructed using information available prior to season_t to prevent data leakage.

---

## 🧠 Modeling Approaches

The following models are evaluated:

- Linear Regression (OLS)
- Ridge Regression
- Lasso Regression
- XGBoost

Time-based train/test splits are used instead of random splits.

---

## 📊 Feature Design

Feature categories include:

- Player profile & age curve
- QB continuity & QB efficiency
- Team environment projections
- Prior season opportunity metrics (targets, target share, air yards share)
- Efficiency metrics (YPRR, catch rate, TD rate, xFP)
- Rolling stability metrics (2-year, 5-year)
- Injury and volatility indicators
- Optional interaction terms for linear models

---

## 📈 Evaluation Metrics

Models are evaluated using:

- MAE (Mean Absolute Error)
- RMSE
- R²
- Spearman Rank Correlation
- Top-N Finish Accuracy (Top 12 / Top 24)



