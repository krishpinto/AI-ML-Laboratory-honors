# AI & ML Laboratory — Honors Practicals

Coursework for **HMLAL701 (AI & ML Laboratory)**. Each practical is a self-contained
Jupyter notebook that walks an end-to-end ML pipeline — data collection, EDA, cleaning,
modelling, evaluation — and closes with a result analysis and an ethics/sustainability
reflection, so every step can be explained rather than just run.

## Practicals

| # | Notebook | Topic | Status |
|---|---|---|---|
| 1 | [practical1_bmi_regression.ipynb](practical1_bmi_regression.ipynb) | Linear Regression predicting BMI from health-survey indicators, with a privacy audit. R² ≈ 0.125. | ✅ Complete |
| 2 | [practical2_fintech_classification.ipynb](practical2_fintech_classification.ipynb) | Credit-card fraud detection — Logistic Regression vs SVM vs XGBoost, SMOTE for class imbalance, ROC-AUC comparison. Best AUC ≈ 0.976 (SVM). | ✅ Complete |
| 3 | — | Not started. | ⬜ Pending |
| 4 | [practical4_dnn_mnist_cifar10.ipynb](practical4_dnn_mnist_cifar10.ipynb) | Deep neural networks on MNIST and CIFAR-10, comparing activation functions (ReLU/Sigmoid) and optimizers (Adam/SGD/RMSProp). | ⚠️ Written, needs a full re-run |

Also here: [diabetes_prediction_pipeline.ipynb](diabetes_prediction_pipeline.ipynb) — an
earlier end-to-end diabetes-prediction pipeline (EDA → cleaning → correlation analysis)
that predates the numbered practicals.

## Data

| File | Used by |
|---|---|
| `diabetes_binary_health_indicators_BRFSS2015.csv` | Practical 1, diabetes pipeline — CDC BRFSS 2015 survey, 253,680 rows × 21 features |
| `diabetes_binary_5050split_…csv`, `diabetes_012_…csv` | Balanced and 3-class variants of the above |
| `creditcard.csv.zip` | Practical 2 — unzip before running (the 144 MB CSV exceeds GitHub's file limit) |

```powershell
Expand-Archive creditcard.csv.zip -DestinationPath .
```

## Setup

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost imbalanced-learn tensorflow jupyter
```

Then open any notebook in Jupyter, VS Code, or Colab and run the cells top to bottom.
Practical 4 needs TensorFlow (or any Keras 3 backend); the rest run on scikit-learn.
