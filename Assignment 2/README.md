<p align="center"><span style="font-size:30px;font-family:Fantasy;color:#C96363"><strong>Assignment 2 — Communities & Crime</strong></span></p>

<p align="center"> <img alt="python" src="https://img.shields.io/badge/python-3.8%2B-blue" /> <img alt="notebook" src="https://img.shields.io/badge/notebook-Jupyter-orange" /> <img alt="status" src="https://img.shields.io/badge/status-ready-brightgreen" /> </p>

<p><em>Predict violent crime rates using resampling, attribute selection and bootstrap evaluation.</em></p>

**Contents**
- `main.ipynb` — example solution notebook implementing preprocessing, CV, feature selection and bootstrap.
- `communities+and+crime/` — dataset folder (raw data and `.names`).
- `Assignment2.pdf` — original assignment sheet.
- `plots/` — generated figures (e.g. selection and diagnostics).
- `requirements.txt` — Python dependencies to run the notebook.

**Core tasks**
- Download and preprocess the "Communities and Crime" dataset. Target: `ViolentCrimesPerPop`. Remove identifying columns (`state`, `county`, `community`, `communityname`, `fold`).
- Implement k-fold cross-validation and leave-one-out (LOOCV) without leaking test data.
- Implement forward (greedy) attribute selection using your CV routine; pick a metric (RMSE/MSE/MAE/R2) and justify it.
- Fit the final closed-form linear regression using the selected features and evaluate on an independent test set.
- Implement bootstrap (n = 1000) on the training set to obtain confidence intervals for the test metrics.
- Report and comment: compare errors (MAE, RMSE, MSE, R2), stability and interpretation of selected features.

**Deliverable**
- A Jupyter notebook named `main.ipynb` with code, explanations, plots and concise conclusions.

**Quick start**
1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Open `main.ipynb` in Jupyter Lab/Notebook and run cells.
3. Ensure the folder `communities+and+crime/` is present and contains the dataset files.

**Notes & tips**
- Do not use the same data for any stage of training and testing — keep a strict train/test split.
- Use the custom CV functions (k-fold and LOOCV) so that imputation and scaling are fit only on training folds.
- When doing forward selection, reuse the same folds across candidate-feature evaluations to keep comparisons fair.
- For bootstrap CI, report 95% intervals (2.5th and 97.5th percentiles) for your chosen metric(s).

**Evaluation metrics**
- Report RMSE, MAE, MSE and R2. Discuss pros/cons of the metric used for feature selection.
