# Customer Churn Analytics using Machine Learning

> Reproducing and enhancing an enterprise SAS Viya customer churn workflow using Python, Explainable AI (SHAP & LIME), and business-driven machine learning.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![SHAP](https://img.shields.io/badge/Explainable%20AI-SHAP-red)
![LIME](https://img.shields.io/badge/Explainable%20AI-LIME-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

# Project Overview

Customer churn is one of the most significant challenges faced by financial institutions. Acquiring new customers is substantially more expensive than retaining existing ones, making early identification of at-risk customers essential for improving profitability and long-term customer loyalty.

This project develops an end-to-end customer churn analytics pipeline capable of identifying customers with a high likelihood of churn using supervised machine learning.

Unlike a typical university assignment, this repository reproduces and extends an enterprise workflow originally developed using **SAS Viya** by implementing the entire analytics pipeline in **Python**, while improving reproducibility, model explainability, and documentation.

---

# Objectives

The objectives of this project are to:

- Develop an accurate customer churn prediction model
- Compare multiple supervised machine learning algorithms
- Select the optimal champion model using comprehensive evaluation metrics
- Interpret model behaviour using Explainable AI (SHAP & LIME)
- Translate technical findings into actionable business recommendations

---

# Original SAS Viya Workflow

Prior to this Python implementation, the complete analytics workflow was developed using **SAS Viya**, including:

- Data Preparation
- Feature Engineering
- Model Studio Pipelines
- Champion Model Selection
- Model Manager Scoring
- Business Recommendation Report

This repository reproduces that workflow using open-source Python libraries while extending it with:

- additional evaluation metrics
- SHAP explainability
- LIME explainability
- improved reproducibility
- GitHub documentation
- engineering best practices

Supporting documentation can be found in the `docs/` directory.

---

# Workflow

```text
Raw Customer Data
        │
        ▼
Notebook 1
Data Understanding
        │
        ▼
Notebook 2
Data Preprocessing
        │
        ▼
Notebook 3
Feature Engineering
        │
        ▼
Notebook 4
Model Development
        │
        ▼
Notebook 5
Model Interpretation
(SHAP & LIME)
        │
        ▼
Notebook 6
Business Recommendations
        │
        ▼
Champion Model
```

---

# Repository Structure

```text
customer-churn-analytics/

├── data/
│   ├── raw/
│   └── processed/
│
├── docs/
│   ├── project_proposal.pdf
│   ├── sas_viya_data_preparation.pdf
│   └── sas_viya_predictive_modelling.pdf
│
├── images/
│
├── models/
│   └── gradient_boosting_model.pkl
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_data_preparation.ipynb
│   ├── 04_model_development_and_evaluation.ipynb
│   ├── 05_model_interpretation.ipynb
│   └── 06_business_recommendations_and_conclusion.ipynb
│
├── requirements.txt
├── LICENSE
└── README.md
```

---

# Machine Learning Models

Five supervised learning algorithms were evaluated.

| Model | Purpose |
|--------|----------|
| Logistic Regression | Linear baseline classifier |
| Decision Tree | Interpretable tree-based model |
| Random Forest | Ensemble learning |
| Gradient Boosting | Champion model |
| Support Vector Machine | Maximum-margin classifier |

---

# Champion Model

**Gradient Boosting** achieved the strongest overall performance.

| Metric | Score |
|---------|------:|
| Accuracy | **95.43%** |
| Precision | **80.89%** |
| Recall | **93.65%** |
| F1-score | **86.80%** |
| ROC AUC | **0.9889** |

---

# Explainable AI

To improve transparency and stakeholder trust, the champion model was interpreted using two complementary Explainable AI techniques.

## SHAP

- Global feature importance
- SHAP Summary Plot
- Local Waterfall Explanation
- Behavioural interpretation

## LIME

- Local prediction explanation
- Model-agnostic interpretation
- Comparison against SHAP

Both techniques consistently identified customer transaction behaviour as the primary driver of churn.

---

# Key Findings

The analyses consistently demonstrated that:

- Transaction behaviour is substantially more predictive than demographic characteristics.
- Low transaction count is the strongest indicator of customer churn.
- Reduced customer spending increases churn probability.
- Customers with fewer banking relationships are significantly more likely to churn.
- SHAP and LIME independently produced highly consistent explanations, increasing confidence in the model's robustness.

---

# Business Recommendations

The model supports proactive customer retention by identifying high-risk customers before they churn.

Recommended actions include:

- personalised retention campaigns
- spending incentives
- cross-selling banking products
- proactive customer engagement
- CRM-based churn monitoring

---

# Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- SHAP
- LIME
- Joblib
- Jupyter Notebook

---

# Future Improvements

Potential extensions include:

- GitHub Actions CI/CD
- Unit testing
- AWS SageMaker deployment
- Model monitoring
- Automated retraining
- Interactive Streamlit dashboard
- Docker containerisation

---

# Installation

Clone the repository.

```bash
git clone https://github.com/YOUR_USERNAME/customer-churn-analytics.git
```

Install dependencies.

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook.

```bash
jupyter notebook
```

---

# Acknowledgements

- Kaggle Credit Card Customers Dataset
- SAS Viya Model Studio
- SHAP
- LIME
- Scikit-Learn

---

# License

This project is released under the MIT License.