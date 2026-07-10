# Customer Churn Analytics using Machine Learning

Reproducing and enhancing an enterprise SAS Viya customer churn workflow using Python, Explainable AI (SHAP & LIME), and business-driven machine learning.

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

## ⭐ Why This Repository?

Unlike a typical machine learning project, this repository reproduces an enterprise customer churn analytics workflow originally developed in **SAS Viya Model Studio**, then enhances it using modern open-source Python tools.

The project demonstrates the complete lifecycle of a production-oriented machine learning workflow:

- Enterprise data preparation using SAS Viya
- Python reproduction of the entire modelling pipeline
- Multi-model comparison and champion model selection
- Explainable AI using SHAP and LIME
- Business-focused recommendations for customer retention
- Reproducible notebook-based workflow with version control

Rather than treating Python as a replacement for SAS, this repository shows how enterprise analytics workflows can be translated into reproducible open-source machine learning pipelines.

---

## 📊 Project Workflow

The following diagram summarises the complete analytics workflow, from the original enterprise SAS Viya implementation to the enhanced Python-based machine learning pipeline.

<p align="center">
  <img src="images/churn_workflow.svg" alt="Customer Churn Analytics Workflow" width="100%">
</p>

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

## 📄 Original Enterprise Documentation

The Python implementation in this repository is based on an enterprise analytics workflow originally developed using **SAS Viya**.

The original project documentation is included for reference:

- 📘 [Project Proposal](docs/project_proposal.pdf)
- 📙 [Data Preparation Report](docs/data_preparation_report.pdf)
- 📗 [Predictive Modelling Report](docs/predictive_modelling_report.pdf)

These reports document the original SAS Viya implementation, including enterprise data preparation, model development, champion model selection, and business recommendations that were later reproduced and enhanced using Python.

---

# 🏦 Enterprise SAS Viya Workflow

Before reproducing the workflow in Python, the complete analytics pipeline was originally developed using **SAS Viya Model Studio** as part of an enterprise predictive modelling workflow.

The Python implementation follows the same modelling lifecycle while extending it with modern explainability techniques and improved reproducibility.

<p align="center">
    <img src="images/sas_pipeline2.png" width="90%">
</p>

The original SAS implementation included:

- Data preparation
- Feature engineering
- Variable clustering
- Model comparison
- Champion model selection
- Model registration

The Python implementation preserves this workflow while adding SHAP, LIME, richer evaluation metrics, and notebook-based reproducibility.

---
# 🔄 Enterprise SAS Viya → Python Reproduction

| Enterprise SAS Viya | Python Implementation |
|---------------------|-----------------------|
| Data Preparation Node | Notebook 02 |
| Feature Engineering Pipeline | Notebook 03 |
| Model Studio | Scikit-Learn |
| Variable Selection / Clustering | Feature Engineering |
| Model Comparison | Cross-model Evaluation |
| Champion Model | Gradient Boosting |
| Variable Importance | SHAP + Feature Importance |
| Model Manager | Joblib Model Serialization |
| Business Report | Notebook 06 |

The objective of this repository was not simply to rebuild an existing workflow, but to demonstrate how an enterprise analytics solution can be migrated to an open-source, reproducible machine learning pipeline while maintaining business interpretability.

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

## 📈 ROC Curve Comparison

<p align="center">
  <img src="images/roc_curve.png" width="85%">
</p>

Gradient Boosting consistently outperformed the remaining machine learning algorithms, achieving the highest ROC AUC (**0.9889**).

The ROC curve rises sharply toward the upper-left corner, indicating excellent discrimination between churned and retained customers while maintaining a very low false positive rate.

This makes the model well suited for identifying high-risk customers early, enabling proactive customer retention strategies.

# 🧠 Explainable AI

Traditional enterprise workflows often rely on feature importance rankings to explain model behaviour.

This repository extends that capability using modern Explainable AI techniques that provide both global and local model interpretations.

The explainability workflow progresses from traditional model feature importance to SHAP and LIME for greater transparency and stakeholder trust.

## Enterprise Variable Importance (SAS)

<p align="center">
    <img src="images/sas_variable_importance.png" width="85%">
</p>

The original SAS workflow identified transaction behaviour as the dominant predictor of customer churn.

| Metric | Score |
|---------|------:|
| Accuracy | **95.43%** |
| Precision | **80.89%** |
| Recall | **93.65%** |
| F1-score | **86.80%** |
| ROC AUC | **0.9889** |

---

### SHAP Summary Plot

<p align="center">
  <img src="images/shap_summary.png" width="90%">
</p>

The SHAP summary plot reveals that **customer behaviour**, rather than demographic characteristics, drives the majority of churn predictions.

Transaction frequency (`Total_Trans_Ct`), transaction amount (`Total_Trans_Amt`), and the number of banking relationships (`Total_Relationship_Count`) consistently contribute the greatest impact on model predictions.

This indicates that declining customer engagement is a stronger predictor of churn than static customer demographics.
---

### SHAP Waterfall Plot

<p align="center">
  <img src="images/shap_waterfall.png" width="90%">
</p>

The waterfall plot explains an individual customer's prediction by showing how each feature contributes to the final churn probability.

For this customer, a **low transaction count**, **reduced spending**, and **limited banking relationships** collectively pushed the prediction towards the churn class.

This level of local interpretability enables relationship managers to understand *why* a customer has been identified as high risk and supports personalised intervention strategies.

---

### LIME Local Explanation

<p align="center">
  <img src="images/lime_explanation.png" width="90%">
</p>

LIME provides an independent local explanation of the same prediction using a surrogate interpretable model.

The explanation closely aligns with SHAP by highlighting low transaction activity and reduced customer engagement as the primary drivers of churn.

The agreement between SHAP and LIME increases confidence that the Gradient Boosting model is making consistent and reliable predictions rather than relying on spurious correlations.

---

# 🏆 Champion Model Lifecycle

The enterprise workflow concluded with deployment of the champion model into **SAS Model Manager** for operational scoring.

<p align="center">
    <img src="images/sas_model_manager.png" width="80%">
</p>

In this repository, the selected Gradient Boosting model is exported as a serialized Python model (`gradient_boosting_model.pkl`) for future deployment into production environments such as REST APIs, Streamlit dashboards, or cloud platforms.

This demonstrates the transition from an enterprise SAS deployment workflow to an open-source Python deployment workflow.

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

# 📚 Lessons Learned

Developing this project provided several practical insights into both enterprise analytics and modern machine learning workflows.

Key lessons include:

- Customer behavioural variables consistently outperformed demographic variables for churn prediction.
- Ensemble learning methods achieved substantially better predictive performance than linear baseline models.
- Explainable AI techniques such as SHAP and LIME significantly improved model transparency and stakeholder confidence.
- Reproducing an enterprise SAS Viya workflow using open-source Python tools improved reproducibility, documentation, and flexibility.
- Business value is created not only through accurate predictions, but also through interpretable insights that support actionable retention strategies.

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

## 🚀 Future Roadmap

### Engineering

- GitHub Actions CI/CD
- Automated unit testing
- Docker containerisation

### MLOps

- Model versioning
- Model monitoring
- Automated retraining
- Drift detection

### Cloud Deployment

- AWS SageMaker deployment
- REST API with FastAPI
- Streamlit dashboard

### Explainable AI

- Counterfactual explanations
- Fairness and bias analysis
- Model cards

---

## 📦 Key Deliverables

- Enterprise SAS Viya workflow documentation
- Six end-to-end Python notebooks
- Trained Gradient Boosting model
- Explainable AI (SHAP & LIME) analyses
- Business recommendation report
- Workflow diagrams and visualisations

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

# 🔄 Reproducing Results

To reproduce the complete analytics workflow, execute the notebooks sequentially:

```text
01_data_understanding.ipynb
        ↓
02_data_preprocessing.ipynb
        ↓
03_data_preparation.ipynb
        ↓
04_model_development_and_evaluation.ipynb
        ↓
05_model_interpretation.ipynb
        ↓
06_business_recommendations_and_conclusion.ipynb
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