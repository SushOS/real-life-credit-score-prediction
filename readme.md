# Credit Score Movement Predictor: ML-Driven Decision Intelligence

## Overview

Welcome to the **Credit Score Movement Predictor**, a high-impact machine learning project. This solution simulates realistic credit behavior and delivers actionable insights by predicting whether a customer's credit score will *increase*, *decrease*, or *remain stable* in the next 3 months. Built with business strategy in mind, this project not only demonstrates technical excellence but also provides a robust framework to inform product, risk, and growth decisions at scale.

---

## Why This Project?

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
---

## How is the Dataset created?
#### A. **Customer Profiles**

- `n_customers`: Default = 25,000
- Each customer includes:
  - A unique `customer_id`
  - Randomized **age** (18–70), **gender**, and **location**
  - **Base income** determined by age and location multiplier

#### B. **Monthly Records**

- Each customer has data for **1 to 5 months** (randomized)
- For each monthly record:
  - **Monthly income** includes seasonal variation
  - **EMI outflow** calculated from income and age-based EMI ratios
  - **Current outstanding amount** derived from EMI and a realistic repayment window
  - **Credit utilization ratio** sampled from a beta distribution
  - **Number of open loans** based on income and age
  - **Repayment history score** depends on customer age
  - **Days past due (DPD)** influenced by repayment history
  - **Number of hard inquiries** higher for younger customers
  - **Recent credit card usage** simulated from a beta distribution
  - **Recent loan disbursed amount** conditional on good repayment score
  - **Total credit limit** derived from income and repayment history
  - **Months since last default** modeled using probability from repayment behavior

#### C. **Target Variable**

- `target_credit_score_movement`: Final classification label with three possible values:
  - `"increase"`: credit score expected to rise
  - `"stable"`: credit score remains the same
  - `"decrease"`: credit score expected to fall
- Calculated using weighted factors:
  - **Payment behavior** (DPD and repayment score)
  - **Credit utilization**
  - **EMI burden**
  - **Credit-seeking behavior**
  - **Stability** (age and months since last default)
  - **Recent loan activity**
- Small random noise is added to simulate natural variation
- Thresholds are applied to categorize the final score into one of the three classes
---


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

## Business Takeaways

This project isn’t just about building a smart model—it’s about making a real difference for Jupiter’s business and customers. Here’s how these insights can drive value:

- **Spotting Risks Early:**  
  The model helps you quickly identify customers whose credit scores are likely to drop. This means you can reach out with support—like restructuring EMIs or offering financial advice—before things get worse. It’s a proactive way to reduce defaults and losses.

- **Smarter Customer Targeting:**  
  By grouping customers into high-risk, stable, and high-opportunity segments, Jupiter can personalize product offers and communication. For example, customers with improving scores can get pre-approved for higher credit limits or exclusive products, boosting both loyalty and revenue.

- **Better Lending Decisions:**  
  Moving beyond traditional scorecards, this solution uses a wide range of behavioral and financial data to make lending decisions that are both safer and more inclusive. This means fewer good customers are turned away, and risky ones are flagged before approval.

- **Staying Agile:**  
  The system adapts to changing customer behavior and market conditions, so your risk models remain sharp even as the world changes. This flexibility is crucial for handling economic shifts or new types of fraud.

- **Explainable, Trustworthy AI:**  
  With clear explainability (thanks to SHAP analysis), business leaders and regulators can see exactly why the model makes its predictions. This builds confidence, supports compliance, and makes it easier to refine policies.

- **Operational Efficiency:**  
  Automating risk assessment frees up your teams to focus on the most important cases and strategic projects. This leads to faster decisions and a better experience for customers.

- **Portfolio Health & Growth:**  
  By monitoring key indicators like DPD, utilization, and repayment history, Jupiter can balance risk and growth, optimizing the lending portfolio for long-term success.

---

## Features

- **Realistic Credit Simulation:** Synthetic data mimics actual customer credit dynamics.
- **Multi-Class Prediction:** Predicts increase, decrease, or stable credit score movement.
- **Advanced EDA & Visualization:** In-depth analysis for data-driven decisions.
- **Robust Model Training:** Multiple algorithms, hyperparameter tuning, and class balancing.
- **Explainability:** SHAP-based insights for model transparency.
- **Business Strategy:** Concrete recommendations for product and policy interventions.

