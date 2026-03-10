# 🏦 Bank Churn Prediction — ML · Deep Learning · Quantum ML

> **End-to-end churn prediction pipeline benchmarking Classical ML, Deep Learning, and Quantum ML — achieving 94% accuracy on 10,000+ customer records.**

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=flat-square&logo=tensorflow)
![Qiskit](https://img.shields.io/badge/Qiskit-Quantum%20ML-6929C4?style=flat-square)
![Accuracy](https://img.shields.io/badge/Best%20Accuracy-94%25-brightgreen?style=flat-square)
![Dataset](https://img.shields.io/badge/Dataset-10%2C000%2B%20records-blue?style=flat-square)

---

## 🎯 What This Does

Customer churn costs banks billions annually. This project builds and **benchmarks three generations of ML** — Classical, Deep Learning, and Quantum — to predict which customers are likely to leave, enabling proactive retention strategies.

**Business impact: 25% reduction in simulated customer attrition using model-driven interventions.**

---

## 📊 Model Performance Comparison

| Model | Accuracy | AUC-ROC | Notes |
|---|---|---|---|
| Logistic Regression | 79% | 0.81 | Baseline |
| Random Forest | 88% | 0.91 | Strong classical baseline |
| XGBoost | **94%** | **0.96** | Best classical model |
| Deep Neural Network | 91% | 0.93 | 4-layer feedforward |
| Quantum-Classical Hybrid | ~72% | 0.74 | Proof-of-concept on subset |

> **Key finding:** XGBoost outperforms DNN on this tabular dataset. Quantum ML shows promise but requires larger qubit counts to be competitive — a hardware limitation, not a model limitation.

---

## 🔬 What Makes This Different

Most churn projects stop at XGBoost. This one goes further:

1. **Rigorous benchmarking** — all models evaluated on identical train/test splits with the same features
2. **Quantum ML exploration** — hybrid classical-quantum circuit using Qiskit + PennyLane, benchmarked for computational efficiency
3. **Feature importance analysis** — SHAP values reveal which customer behaviors drive churn
4. **Production-ready pipeline** — modular notebooks, reproducible seeds, requirements file

---

## 🏗️ Pipeline Architecture

```
Raw Data (BankChurners.csv — 10,000+ records)
       │
       ▼
┌─────────────────────────────┐
│  Data Preprocessing         │
│  • Missing value imputation │
│  • Feature encoding         │
│  • Normalization & scaling  │
│  • Train/test split (80/20) │
└────────────┬────────────────┘
             │
     ┌───────┼───────┐
     ▼       ▼       ▼
┌────────┐ ┌────┐ ┌──────────┐
│Classical│ │ DL │ │Quantum ML│
│ ML     │ │    │ │ (Qiskit) │
└────────┘ └────┘ └──────────┘
     │       │       │
     └───────┴───────┘
             │
             ▼
    Evaluation & Benchmarking
    (Accuracy, AUC, Confusion Matrix, SHAP)
```

---

## 📁 Notebooks

| Notebook | Description |
|---|---|
| `Bankchurn_prediction_using_ml,dl.ipynb` | Classical ML + Deep Learning pipeline |
| `Bankchurn_prediction_with_Quantum_ml_with_full_dataset_.ipynb` | Quantum ML on full dataset |
| `Bankchurn_prediction_using_optimized_Quantum_Classical_Binary_Classifier_model_.ipynb` | Optimized hybrid quantum-classical model |

---

## 📦 Dataset

**File:** `BankChurners.csv` (included in repo)
- **Records:** 10,127 customers
- **Features:** 23 (demographics, account activity, product holdings, transaction history)
- **Target:** `Attrition_Flag` — binary churn label
- **Source:** Public Kaggle dataset (Credit Card Customers)

---

## 🛠️ Setup

```bash
# Clone
git clone https://github.com/Sheshaadhri14/Bank-Churn-Prediction-ML-DL-Quantum-ML-.git
cd Bank-Churn-Prediction-ML-DL-Quantum-ML-

# Install dependencies
pip install -r requirements.txt

# For Quantum ML notebooks
pip install qiskit pennylane pennylane-qiskit

# Launch Jupyter
jupyter lab
```

**Core dependencies:** `numpy, pandas, scikit-learn, tensorflow, xgboost, shap, matplotlib, seaborn`

---

## 🧠 Key Insights

- **Top churn predictors** (via SHAP): Total transaction count, total revolving balance, contacts count in 12 months
- **XGBoost dominates** on tabular data due to its ability to handle feature interactions without normalization
- **Quantum ML bottleneck:** Current NISQ-era hardware limits qubit count, making classical methods superior on large tabular datasets — but the gap will narrow
- **Deep learning underperforms XGBoost** here because the dataset lacks the scale where neural networks shine

---

## 👤 Author

**Sri Sheshaadhri R**
- 🔗 [GitHub](https://github.com/Sheshaadhri14)
- 📧 sheshaadhri14@gmail.com
- 🏫 VIT Chennai | Computer Science & Engineering

---

## 📄 License

MIT License
