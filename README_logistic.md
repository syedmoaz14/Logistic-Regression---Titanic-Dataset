# 🎯 Titanic Survival Prediction — Logistic Regression

Binary classification model predicting whether a Titanic passenger survived, built as part of my AI Engineer learning journey.

---

## What This Project Covers

- **Sigmoid function** — understanding how logistic regression converts any number into a probability
- **Preprocessing** — missing value handling, feature engineering, encoding for classification
- **Baseline comparison** — establishing majority class accuracy before training anything
- **Confusion matrix** — breaking down TP, TN, FP, FN and understanding what each error means
- **Classification metrics** — Precision, Recall, F1 Score, ROC-AUC calculated manually and verified with sklearn
- **Threshold tuning** — finding the optimal decision threshold using the Precision-Recall tradeoff
- **Feature importance** — which features drive survival probability and why they make historical sense
- **Cross validation** — 5-fold CV for reliable model evaluation

---

## Results

| Metric | Score |
|--------|-------|
| Baseline Accuracy | 61.5% |
| Model Accuracy | ~82% |
| F1 Score | ~0.77 |
| ROC-AUC | ~0.88 |

The model improves over the majority class baseline by ~20%. Sex and Pclass are the strongest predictors — consistent with the historical 'women and children first' evacuation policy and restricted lifeboat access for 3rd class passengers.

---

## Key Findings

- **Female passengers** had the strongest positive effect on survival probability — matching the historical evacuation policy
- **Passenger class** was the strongest negative predictor — 3rd class passengers had much lower survival rates
- **False Positives** are the most dangerous error in this context — predicting survival for someone who dies causes them to stop seeking safety
- Threshold tuning improved F1 score over the default 0.5 cutoff

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/your-username/titanic-logistic-regression
cd titanic-logistic-regression

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch notebook
jupyter notebook logistic_regression_clean.ipynb
```

The notebook loads the Titanic dataset directly from a URL — no download needed.

---

## Tech Stack

`Python` · `Pandas` · `NumPy` · `Scikit-learn` · `Matplotlib` · `Seaborn`

