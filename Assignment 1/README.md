<p align="center"><span style="font-size:28px;font-family:Fantasy;color:#C96363"><strong>Assignment 1 — PM10 prediction</strong></span></p>

<p align="center"> <img alt="python" src="https://img.shields.io/badge/python-3.8%2B-blue" /> <img alt="notebook" src="https://img.shields.io/badge/notebook-Jupyter-orange" /> <img alt="status" src="https://img.shields.io/badge/status-ready-brightgreen" /> </p>

<p><em>A short, practical assignment: implement multiple linear regression (closed-form), evaluate and improve it to predict daily PM10 using meteorological data.</em></p>

**Contents**
- `main.ipynb` — example solution notebook with preprocessing, models and diagnostics.
- `data/podatki_PM.csv` — dataset
- `Assignment1.pdf` — original assignment sheet.
- `requirements.txt` — Python dependencies to run the notebook.

**Core tasks**
- Preprocess the data and handle missing values (temporal imputation where appropriate).
- Split data by time (do NOT shuffle). Keep `Datum` for splitting, but exclude it from model features.
- Implement closed-form OLS and verify results vs scikit-learn's `LinearRegression`.
- Produce diagnostic plots: residuals vs fitted, Q–Q, residuals vs leverage / Cook's distance.
- Try improvements: target/feature transforms (e.g. `log1p`), regularization (Ridge/Lasso), and feature engineering (interactions, polynomials).

**Deliverable**
- A Jupyter notebook named `main.ipynb` containing code, commentary, plots and brief conclusions.

**Quick start**
1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Open `main.ipynb` in Jupyter Lab/Notebook and run the cells.

3. The notebook reads `data/podatki_PM.csv`.

**Evaluation metrics**
- Report: R², RMSE and MAE. Compare models over an expanding-window time split.