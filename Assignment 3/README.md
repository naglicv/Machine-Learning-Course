<p align="center"><span style="font-size:30px;font-family:Fantasy;color:#C96363"><strong>Assignment 3 — Regularization, BGD & SGD</strong></span></p>

<p align="center"> <img alt="python" src="https://img.shields.io/badge/python-3.8%2B-blue" /> <img alt="notebook" src="https://img.shields.io/badge/notebook-Jupyter-orange" /> <img alt="status" src="https://img.shields.io/badge/status-ready-brightgreen" /> </p>

<p><em>Explore Ridge and Lasso, tune regularization, and implement gradient-descent solvers for ridge regression.</em></p>

**Contents**
- `main.ipynb` — example solution notebook (preprocessing, Ridge/Lasso, hyperparameter search, BGD/SGD implementations).
- `data/` — dataset folder with `communities+and+crime/` and `wine+quality/` subfolders.
- `Assignment3.pdf` — original assignment sheet.
- `requirements.txt` — Python dependencies to run the notebook.

**Core tasks**
- Reuse the `Communities and Crime` preprocessing from Assignment 2. Fit Ridge and Lasso (scikit-learn), perform hyperparameter search, and compare selected attributes vs forward selection.
- Download and preprocess the white `Wine quality` dataset. Implement batch gradient descent (BGD) and stochastic gradient descent (SGD) for ridge regression from scratch.
- Tune learning rates and compare convergence speed and final performance between BGD and SGD.
- Report results and comment on differences in convergence, stability and selected features.

**Deliverable**
- A Jupyter notebook named `main.ipynb` with code, plots and concise conclusions.

**Quick start**
1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Open `main.ipynb` in Jupyter Lab/Notebook and run cells.
3. Ensure the `data/` folder exists and contains the two datasets:
   - `data/communities+and+crime/`
   - `data/wine+quality/winequality-white.csv`

**Notes & tips**
- Keep train/test splits strict: avoid using test data during any training, tuning or preprocessing steps.
- Use `RidgeCV` / `LassoCV` for efficient alpha selection and compare with manual grid search if desired.
- When implementing BGD/SGD, add a bias column (constant 1) to inputs and do not regularize the bias term.
- Compare timing and iterations to convergence for BGD vs SGD; report chosen learning rates and stopping criteria.

**Evaluation metrics**
- Report RMSE, MAE, MSE and R2 for all evaluated models and datasets. Discuss pros/cons of the metrics and behaviour under regularization.