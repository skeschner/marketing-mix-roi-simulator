# Marketing Mix Modeling & Budget Optimization

## Overview

This project builds a regression-based marketing mix model to estimate incremental revenue contribution across multiple advertising channels and evaluate budget reallocation strategies.

The objective is to identify which channels generate the highest marginal ROI and support data-driven media optimization decisions.

---

## Business Problem

Marketing budgets are distributed across channels such as:

- Search  
- Social  
- Display  
- Connected TV (CTV)

Given a fixed budget:
- Which channels drive the highest incremental revenue?
- How should funds be reallocated to maximize total revenue?

---

## Modeling Approach

The analysis includes:

- Time-based train/test validation to simulate real-world forecasting
- Log-transformed marketing variables to capture diminishing returns
- Lagged CTV effects to reflect delayed brand impact
- Control variables for price and seasonality
- Comparison of OLS and Ridge regression models

Channel contribution is estimated using a model ablation approach (setting each channel to zero and measuring the reduction in predicted revenue).

---

## Key Results

- Log-transformed specification improved attribution stability (R² ≈ 0.98 out-of-sample)
- CTV and Search demonstrated the highest modeled ROI
- Reallocating 10% of Display spend to CTV increased total predicted revenue by ~$96K
- Regularization (Ridge) did not outperform the correctly specified OLS model

---

## Project Structure

- `01_generate_data.ipynb` – Simulates multi-channel marketing dataset  
- `02_model_attribution.ipynb` – Builds attribution model and runs optimization simulations  
- `data/` – Simulated dataset  

---

## Tools Used

Python, pandas, NumPy, scikit-learn, matplotlib

