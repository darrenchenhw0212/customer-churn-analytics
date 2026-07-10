# Customer Churn Analytics using Machine Learning

> Reproducing and enhancing an enterprise SAS Viya customer churn workflow using Python, Explainable AI (SHAP & LIME), and business-driven machine learning.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![SHAP](https://img.shields.io/badge/Explainable%20AI-SHAP-red)
![LIME](https://img.shields.io/badge/Explainable%20AI-LIME-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 🚀 Project Highlights

| Item | Result |
|------|--------|
| 🎯 Business Problem | Predict customer churn for retail banking customers |
| 🏆 Champion Model | Gradient Boosting |
| 📈 ROC AUC | **0.9889** |
| 🎯 Recall | **93.65%** |
| 🧠 Explainability | SHAP & LIME |
| 🏦 Original Platform | SAS Viya |
| 🐍 Reproduced In | Python |
---

# Project Overview

Customer churn is one of the most significant challenges faced by financial institutions. Acquiring new customers is substantially more expensive than retaining existing ones, making early identification of at-risk customers essential for improving profitability and long-term customer loyalty.

This project develops an end-to-end customer churn analytics pipeline capable of accurately identifying customers with a high likelihood of churn using supervised machine learning.

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

Supporting documentation describing the original enterprise workflow is included in the **docs/** directory:

- Project Proposal
- SAS Viya Data Preparation Report
- SAS Viya Predictive Modelling Report

These documents provide the foundation for the Python implementation presented in this repository.

---

## 📊 Project Workflow

The following diagram summarises the complete analytics workflow, from the original enterprise SAS Viya implementation to the enhanced Python-based machine learning pipeline.

<p align="center">
  <img src="images/churn_workflow.svg" alt="Customer Churn Analytics Workflow" width="100%">
</p>
---

## 📒 Notebook Guide

| Notebook | Description |
|-----------|-------------|
| **01 – Data Understanding** | Data exploration, quality assessment and churn analysis |
| **02 – Data Preprocessing** | Missing value handling, encoding and data cleaning |
| **03 – Feature Engineering** | Feature engineering and preparation of modelling datasets |
| **04 – Model Development & Evaluation** | Model training, evaluation and champion model selection |
| **05 – Model Interpretation** | Explainable AI using SHAP and LIME |
| **06 – Business Recommendations** | Business insights, deployment considerations and future recommendations |

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

## 📈 ROC Curve Comparison

<p align="center">
  <img src="images/roc_curve.png" width="85%">
</p>

The Gradient Boosting model achieved the highest ROC AUC (0.9889), demonstrating superior discriminatory performance compared to the other evaluated algorithms.

## 🧠 Explainable AI

### SHAP Summary Plot

<p align="center">
  <img src="images/shap_summary.png" width="90%">
</p>

The SHAP summary plot shows that Total_Trans_Ct,
Total_Trans_Amt and Total_Relationship_Count are
the three most influential predictors.

---

### SHAP Waterfall Plot

<p align="center">
  <img src="images/shap_waterfall.png" width="90%">
</p>

This customer was classified as high-risk primarily
due to low transaction count and reduced spending.

---

### LIME Local Explanation

<p align="center">
  <img src="images/lime_explanation.png" width="90%">
</p>

LIME independently identified the same behavioural
drivers, supporting the robustness of the explanation.

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

## 🛠 Technologies

### Programming Language

- Python

### Machine Learning

- Scikit-Learn
- SHAP
- LIME

### Data Processing

- Pandas
- NumPy

### Visualisation

- Matplotlib

### Development

- Jupyter Notebook
- Joblib

---

## 🚀 Future Improvements

- Deploy the champion model using AWS SageMaker
- Implement GitHub Actions CI/CD
- Add automated unit testing
- Containerise the application using Docker
- Monitor model drift in production
- Develop an interactive Streamlit dashboard
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

# Installation

Clone the repository.

```bash
git clone https://github.com/darrenchenhw0212/customer-churn-analytics.git
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