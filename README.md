# Credit Card Fraud Detection – Portfolio Project

Project Overview
This project builds a machine learning model to detect fraudulent credit card transactions. It involves data preprocessing, exploratory analysis, and training models such as logistic regression and random forest. The model is evaluated using precision, recall, and F1-score to effectively identify fraud while minimizing false alarms.
  

The workflow includes:
- Exploratory Data Analysis (EDA)  
- Feature Engineering  
- Machine Learning Modeling (Logistic Regression & Random Forest)  
- Hyperparameter Tuning  
- Precision–Recall and Cost-Based Optimization  

**Objective:** Minimize financial losses due to fraud while balancing operational efficiency and customer experience.

---

## Tools Used

- **Python:** pandas, numpy, scikit-learn, matplotlib, seaborn  
- **Jupyter Notebook:** Interactive coding and visualization  
- Initial exploration and export  
- **Git & GitHub:** Version control and portfolio presentation  
- **Advanced Tools:** GridSearchCV/RandomizedSearchCV, cost-based threshold optimization

---

## Visualization Insights

### 1. Fraud vs Non-Fraud Transaction History
<img width="600" height="400" alt="anaconda_projects_252f3fdb-6ab8-4742-a60d-511fa335ecf2_fraudvsnon-fraudcount" src="https://github.com/user-attachments/assets/e2dfc6fe-7caa-475f-bf73-59f8a1236dbe" />


**Insight:** Legitimate transactions dominate, fraud is rare and irregular. Spikes indicate targeted attacks.

### 2. Fraud by Transaction Hour
<img width="1000" height="500" alt="anaconda_projects_252f3fdb-6ab8-4742-a60d-511fa335ecf2_FraudbyTransaction" src="https://github.com/user-attachments/assets/fde8cb7d-fa2b-415d-a9b8-4e4f062d3446" />


**Insight:** Fraud peaks during late-night/early-morning hours; legitimate transactions peak during business hours.

### 3. Transaction Amount Distribution
<img width="800" height="500" alt="anaconda_projects_252f3fdb-6ab8-4742-a60d-511fa335ecf2_TransactionAmount" src="https://github.com/user-attachments/assets/e9ca6d4c-77cf-4465-a632-348a7449e912" />


**Insight:** Fraud often involves high or unusual amounts; legitimate transactions cluster at moderate amounts.


### 4. Transaction Amount vs Fraud
<img width="600" height="500" alt="anaconda-projects-252f3fdb-6ab8-4742-a60d-511fa335ecf2-Transaction-Amountby-Fraud" src="https://github.com/user-attachments/assets/8de80f07-f8ef-4692-8bcc-8fe33eaf0e46" />

**Insight:** Fraud occurs at extreme amounts; transaction amount alone cannot fully separate fraud from non-fraud.

### 5. Correlation Heatmap
<img width="1280" height="1157" alt="download" src="https://github.com/user-attachments/assets/041b13ec-b746-4103-b8dd-60189f8fb92a" />


**Insight:** Features are mostly independent, providing unique predictive information. Identifies redundant features for feature selection.

---

## Logistic Regression Results

| Metric | Value |
|--------|-------|
| Precision (Fraud) | 1.0 |
| Recall (Fraud) | 0.19 |
| F1-Score (Fraud) | 0.32 |
| Accuracy | 0.93 |
| R² Score | 0.102 |

<img width="800" height="600" alt="anaconda_projects_252f3fdb-6ab8-4742-a60d-511fa335ecf2_LogisticRegressionFeatures" src="https://github.com/user-attachments/assets/0426fb95-1673-4d22-ad9b-6a14dee4d073" />


**Interpretation:**  
- High precision but low recall → model misses most fraud cases.  
- Features like Transaction Amount and Hour are important predictors.  
- Accuracy is misleading due to class imbalance.

---

## Random Forest Results (Hyperparameter Tuned)

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0 (Non-Fraud) | 1.00 | 0.92 | 0.96 | 2948 |
| 1 (Fraud)     | 0.18 | 1.00 | 0.31 | 52 |

- **ROC-AUC:** 0.993

  <img width="1000" height="600" alt="anaconda_projects_252f3fdb-6ab8-4742-a60d-511fa335ecf2_FeaturesImportance" src="https://github.com/user-attachments/assets/55868023-26d5-4197-bccf-a382b75a93a2" />


**Interpretation:**  
- Perfect recall ensures no fraud is missed.  
- Precision drops → many legitimate transactions flagged.  
- Hyperparameter tuning balances fraud detection and operational cost.

---

## Precision–Recall Curve

<img width="567" height="455" alt="__results___25_0" src="https://github.com/user-attachments/assets/d7887914-de0d-4348-9b79-bf0d4d22d4ea" />

**Insight:**  
- Trade-off between detecting fraud (recall) and false alerts (precision).  
- Optimal threshold prioritizes high recall to ensure fraud is captured.

---


## Cost-Based Optimization

- **Best Threshold:** 0.85  
- **Minimum Cost:** 16,500,000  

**Insight:**  
- Threshold minimizes total financial loss while balancing false positives and missed fraud.  
- Demonstrates **business-driven decision-making** beyond model metrics.

---

## Business Insights & Recommendations

**Insights:**
- Fraud is rare but critical; occurs at unusual hours and high amounts.  
- Transaction Amount, Hour, and Location Score are strong predictors.  
- High recall is essential for minimizing losses.  

**Recommendations:**
1. Deploy **time-aware and amount-based monitoring**.  
2. Use **Random Forest with tuned thresholds** for production.  
3. Apply **cost-based thresholds** to minimize losses.  
4. Retrain models periodically with new data.  
5. Monitor metrics continuously to ensure sustained performance.

**Business Impact:**
- Reduces financial losses by detecting all fraud.  
- Improves operational efficiency and customer trust.  
- Supports data-driven fraud prevention policies and resource allocation.

---

## Conclusion

The project demonstrates **end-to-end fraud detection**, combining:  
- Exploratory analysis  
- Machine learning modeling  
- Hyperparameter and threshold optimization  
- Business-driven decision-making  

Random Forest captures all fraud cases (high recall), while logistic regression provides interpretability. Cost-based optimization ensures **financially optimal deployment**, balancing risk, operational cost, and customer experience.

This portfolio piece shows **technical skills and business impact**, making it a strong example of a data-driven solution to a real-world problem.

---

