#  Customer Churn Analysis — Telecom

> * Portfolio Project | Python · Pandas · Seaborn · Matplotlib · Scikit-learn



##  Project Overview

This project analyzes customer churn patterns in a telecom dataset with an overall churn rate of 26.5%.
It identifies key churn drivers, high-risk customer segments, and baseline predictive insights for retention strategy. 





##  Repository Structure

```
customer-churn-analysis
│
├── churn_analysis.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── high_risk_churned_customers.csv
├── fig1_churn_rate.png
├── fig2_contract_churn.png
├── fig3_tenure_churn.png
├── fig4_charges_churn.png
├── fig5_internet_payment.png
├── fig6_correlation_heatmap.png
├── fig7_logistic_regression_confusion_matrix.png
└── README.md
```



##  Dataset

* Source:  [IBM Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
* **Rows:** 7,032 customers (after cleaning)
* **Columns:** 20 features + 1 target (`Churn`)
* **Key Features:** `tenure`, `Contract`, `MonthlyCharges`, `InternetService`, `PaymentMethod`

**Key variables:**

- `tenure`
- `Contract`
- `MonthlyCharges`
- `TotalCharges`
- `InternetService`
- `PaymentMethod`
- `TechSupport`
- `Churn`

##  Key Findings

|#|Finding|Churn Rate|
|-|-|-|
|1|Month-to-month contract customers|**\~42%**|
|2|Customers in first 12 months|**\~47%**|
|3|Fiber optic internet users|**\~41%**|
|4|Electronic check payment users|**\~45%**|
|5|Customers with no tech support|**\~41%**|


## Rule-Based Risk Scoring Framework

A heuristic churn risk scoring model was created using observed churn indicators:

| Risk Factor | Score |
|------------|-------|
| **Month-to-month contract** | +40 |
| **Tenure under 12 months** | +30 |
| **Fiber optic service** | +20 |
| **Electronic check payment** | +10 |

**High-risk threshold:** Customers scoring **70+** were flagged for retention targeting.

The highest-risk segment consists of **month-to-month customers using fiber optic service with tenure under 12 months,with an observed churn rate of approximately 60%**.

##  Charts Generated

| Figure | Description |
|--------|-------------|
| Fig 1 | Overall churn rate (bar + donut chart) |
| Fig 2 | Contract type vs churn |
| Fig 3 | Tenure churn analysis |
| Fig 4 | Monthly charges vs churn |
| Fig 5 | Internet service & payment churn |
| Fig 6 | Correlation heatmap |
| Fig 7 | Logistic regression confusion matrix |


## Predictive Modeling

A baseline logistic regression model was trained to predict customer churn for a baseline classifier, although churn recall indicates that there is still much work to do in detecting potential churners.

### Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | **79%** |
| Churn Precision | **64%** |
| Churn Recall | **48%** |
| F1-Score | **55%** |

The classification performance is reasonable for a baseline model, though churn recall suggests further improvement is needed in identifying potential churners



---

## Business Recommendations

### 1. Promote Long-Term Contracts

Churn rates were considerably high for consumers using monthly subscriptions than for those having long-term customers.

**Potential actions:**
- Offer discounted annual or multi-year plans
- Run targeted retention upgrade campaigns

---

### 2. Improve Early Customer Retention

A large share of churn occurs within the first 12 months, indicating that early customer experience is critical.

**Potential actions:**
- Create structured onboarding journeys
- Introduce early warning retention interventions for at-risk customers

---

### 3.  Review Services With High Churn Rate

Fiber optics service experienced high monthly bills and high churn rate, which implies dissatisfaction with billing or pricing structure of the service

**Potential actions:**
- Review service quality metrics
- Reassess pricing strategy and bundled offerings

## Tools & Libraries

| Library | Purpose |
|---------|---------|
| pandas | Data loading, cleaning, and transformation |
| numpy | Numerical operations and array handling |
| matplotlib | Data visualization and plotting |
| seaborn | Statistical visualizations |
| scikit-learn | Predictive modeling and machine learning |


## How to Run

### Option 1: Google Colab

Upload the following files to Google Colab:

- `churn_analysis.ipynb`
- `WA_Fn-UseC_-Telco-Customer-Churn.csv`

Then run all notebook cells.

---

### Option 2: Run Locally (Jupyter Notebook)

```bash
git clone https://github.com/vaaravind/customer-churn-analysis.git
cd customer-churn-analysis
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook churn_analysis.ipynb
```



##  Results Summary

```
Total customers analysed    :  7,032
Overall churn rate          :  26.5%
Predictive model            :  Logistic Regression
Charts generated            :  7
Business recommendations    :  3
High-risk customers flagged :  exported to CSV
```



##  Author

**V A Aravind**

&#x20;


&#x20;
LinkedIn: https://www.linkedin.com/in/v-a-aravind-6a458a207



GitHub: https://github.com/vaaravind





*Dataset originally published by IBM on Kaggle. Used here for educational and portfolio purposes.*

