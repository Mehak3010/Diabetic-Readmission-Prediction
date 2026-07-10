# 🏥 Clinical Readmission Risk Prediction using Electronic Health Records (EHR)

An end-to-end machine learning project that predicts **30-day hospital readmission risk** for diabetic patients using Electronic Health Records (EHR). The project demonstrates a production-inspired machine learning workflow, including data preprocessing, clinical feature engineering, class imbalance handling, hyperparameter tuning, threshold optimization, and model explainability.

---

## 📌 Problem Statement

Hospital readmissions within 30 days increase healthcare costs, hospital workload, and patient risk. Identifying patients with a high probability of readmission before discharge enables hospitals to provide targeted interventions and improve patient outcomes.

This project develops predictive models using historical Electronic Health Records collected from **130 US hospitals**.

---

## 📊 Dataset

This repository includes the **Diabetes 130-US Hospitals** dataset used for training and evaluation.

**Dataset Details**

- **Patient Encounters:** 101,766
- **Hospitals:** 130 US hospitals
- **Time Period:** 1999–2008
- **Features:** 50+ demographic and clinical attributes
- **Target:** 30-day hospital readmission

Dataset location:

```
data/raw/
```
---

## 🚀 Project Workflow

```
Business Understanding
        │
        ▼
Data Cleaning
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Clinical Feature Engineering
        │
        ▼
Preprocessing Pipeline
        │
        ▼
Baseline Models
(Logistic Regression,
Random Forest,
XGBoost)
        │
        ▼
Class Imbalance Handling
        │
        ▼
Threshold Optimization
        │
        ▼
Hyperparameter Tuning
        │
        ▼
Model Explainability (SHAP)
```

---

## ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib
- Seaborn
- Joblib

---

## 🧠 Machine Learning Pipeline

### Data Preprocessing

- Missing value handling
- Feature selection
- Clinical feature engineering
- ICD-9 diagnosis grouping
- Train-test split
- Standardization
- One-Hot Encoding
- Scikit-learn Pipeline & ColumnTransformer

---

### Models Evaluated

- Logistic Regression
- Random Forest
- XGBoost

---

### Handling Class Imbalance

Instead of relying solely on accuracy, the project includes:

- Class-weighted learning
- Balanced Accuracy
- PR-AUC
- Threshold Optimization
- ROC-AUC Evaluation

---

## 📈 Final Model Performance

| Metric | Tuned XGBoost |
|---------|--------------:|
| Accuracy | **0.740** |
| Balanced Accuracy | **0.620** |
| Precision | **0.206** |
| Recall | **0.465** |
| F1 Score | **0.285** |
| ROC-AUC | **0.686** |
| PR-AUC | **0.234** |

---

## 🔍 Feature Importance

The most influential predictors included:

- Previous inpatient admissions
- Discharge disposition
- Diabetes medication
- Total hospital visits
- Number of diagnoses
- Time spent in hospital
- Patient age

---

## 📊 Model Explainability

SHAP (SHapley Additive Explanations) was used to interpret model predictions and understand how individual clinical features contributed to readmission risk.

---

## 📁 Project Structure

```
clinical-readmission-prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── clinical_readmission_prediction.ipynb
│
├── model/
│   └── best_xgboost_model.pkl
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ▶️ Installation

Clone the repository

```bash
git clone https://github.com/Mehak3010/clinical-readmission-prediction.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

---

## 💡 Key Insights

- Previous inpatient admissions were the strongest predictor of hospital readmission.
- Clinical utilization features were more informative than demographic features.
- Threshold optimization significantly improved minority-class detection.
- SHAP enhanced model transparency by identifying clinically relevant predictors.

---

## 🔮 Future Improvements

- External validation using additional hospital datasets
- Bayesian hyperparameter optimization (Optuna)
- Probability calibration
- Streamlit/FastAPI deployment
- Integration with hospital decision-support systems

---

## 👩‍💻 Author

**Mehak Arora**

---
