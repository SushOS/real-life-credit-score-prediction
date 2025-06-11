# Credit Score Movement Predictor: ML-Driven Decision Intelligence

## Overview

Welcome to the **Credit Score Movement Predictor**, a high-impact machine learning project designed for Jupiter’s President’s Office. This solution simulates realistic credit behavior and delivers actionable insights by predicting whether a customer's credit score will *increase*, *decrease*, or *remain stable* in the next 3 months. Built with business strategy in mind, this project not only demonstrates technical excellence but also provides a robust framework to inform product, risk, and growth decisions at scale.

---

## Why This Project?

- **Strategic Impact:** Directly aligns with Jupiter’s mission to drive AI-powered product innovation, risk optimization, and business intelligence.
- **Real-World Simulation:** Uses a synthetic dataset mirroring actual customer behavior, ensuring relevance to real banking scenarios.
- **Explainability & Insights:** Goes beyond prediction—delivers clear drivers of credit score movement and actionable business recommendations.
- **End-to-End Excellence:** Covers the full ML pipeline: data generation, EDA, feature engineering, model training, explainability, and business strategy.

---

## Project Logic & Implementation

### 1. **Synthetic Dataset Generation**
- **Size:** 25,000+ customer-month records.
- **Features:** Demographics (age, gender, location), financials (income, EMI, outstanding), credit behavior (utilization, repayment score, DPD, inquiries), and more.
- **Target Logic:** 
  - *Decrease:* High DPD, high utilization, many new inquiries.
  - *Increase:* Low EMI/income ratio, strong repayment history.
  - *Stable:* Balanced behavior.
- **Method:** Logical heuristics and controlled noise for realism.

### 2. **Exploratory Data Analysis (EDA)**
- Comprehensive visualizations: target distribution, risk segmentation, outlier detection, and feature correlations.
- Business-friendly plots highlight risk zones and opportunity segments.

### 3. **Feature Engineering**
- Domain-driven features: debt-to-income ratio, credit limit utilization, income brackets, age groups, risk indicators, and recent activity score.
- Enhanced model signal and business interpretability.

### 4. **Preprocessing & Class Imbalance Handling**
- Advanced pipeline: scaling, encoding, and robust handling of missing values.
- Imbalance tackled using SMOTE-Tomek and other resampling strategies for fair, unbiased learning.

### 5. **Model Training & Optimization**
- **Algorithms:** Random Forest, HistGradientBoosting, Logistic Regression.
- **Hyperparameter Tuning:** RandomizedSearchCV with Stratified K-Fold.
- **Metrics:** Accuracy, F1-score (macro/weighted), class-wise recall, AUC.
- **Time Analysis:** Detailed logging for performance vs. efficiency benchmarking.

### 6. **Model Explainability**
- **SHAP Analysis:** Feature importance and summary plots for transparency.
- **Business Insights:** Top drivers identified for each risk segment.

### 7. **Business Recommendations**
- Actionable interventions for high-risk and high-opportunity segments.
- Strategic playbook for risk mitigation, growth, monitoring, and portfolio optimization.

---

## Features

- **Realistic Credit Simulation:** Synthetic data mimics actual customer credit dynamics.
- **Multi-Class Prediction:** Predicts increase, decrease, or stable credit score movement.
- **Advanced EDA & Visualization:** In-depth analysis for data-driven decisions.
- **Robust Model Training:** Multiple algorithms, hyperparameter tuning, and class balancing.
- **Explainability:** SHAP-based insights for model transparency.
- **Business Strategy:** Concrete recommendations for product and policy interventions.

