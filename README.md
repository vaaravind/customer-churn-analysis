#  Customer Churn Analysis — Telecom

> * Portfolio Project* | Python · Pandas · Seaborn · Matplotlib



##  Project Overview

A telecom company is losing customers at an alarming rate of **26.5%** — above the industry average.  
This project identifies *who* is leaving, *why* they are leaving, and *what the business should do* to fix it.




##  Repository Structure

```
customer-churn-analysis/
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

* **Source:** [IBM Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
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

>  The highest-risk segment consists of month-to-month customers using fiber optic service with tenure under 12 months, identified through a rule-based churn risk scoring framework as the most at-risk customer group. **60%**.

## Rule-Based Risk Scoring Framework

A heuristic churn risk scoring model was created using observed churn indicators:

| Risk Factor | Score |
|------------|-------|
| **Month-to-month contract** | +40 |
| **Tenure under 12 months** | +30 |
| **Fiber optic service** | +20 |
| **Electronic check payment** | +10 |

**High-risk threshold:** Customers scoring **70+** were flagged for retention targeting.

The highest-risk segment consists of **month-to-month customers using fiber optic service with tenure under 12 months**.

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

A baseline **logistic regression model** was trained to predict customer churn.

### Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | **79%** |
| Churn Precision | **64%** |
| Churn Recall | **48%** |
| F1-Score | **55%** |

This serves as a baseline predictive model for churn classification.

## Predictive Modeling

To complement the exploratory analysis, a baseline **logistic regression model** was built to predict customer churn.

### Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | **79%** |
| Churn Precision | **64%** |
| Churn Recall | **48%** |
| F1-Score | **55%** |

The model performs reasonably well as a baseline classifier, though churn recall suggests there is room for improvement in identifying customers likely to leave.

The model performs reasonably well as a baseline classifier, though churn recall suggests there is room for improvement in identifying customers likely to leave.

---

## Business Recommendations

### 1. Encourage Long-Term Contracts

Customers on month-to-month plans showed significantly higher churn compared with long-term contract customers.

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

### 3. Review High-Churn Service Segments

Fiber optic customers showed both higher monthly charges and higher churn, suggesting possible dissatisfaction with pricing, service experience, or perceived value.

**Potential actions:**
- Review service quality metrics
- Reassess pricing strategy and bundled offerings


##  Tools \& Libraries

```python
| Library | Purpose |
|--------|---------|
| `pandas` | Data loading, cleaning, and transformation |
| `numpy` | Numerical operations and array handling |
| `matplotlib` | Data visualisation and plotting |
| `seaborn` | Statistical visualisations |
| `scikit-learn` | Predictive modeling and machine learning |
```



##  How to Run

### Option A — Google Colab 

1. Upload `churn_analysis.ipynb` and `WA_Fn-UseC_-Telco-Customer-Churn.csv` to Colab
2. Run all cells (`Runtime → Run all`)

### Option B — Jupyter Locally

```bash
git clone https://github.com/YOUR_USERNAME/customer-churn-analysis.git
cd customer-churn-analysis
pip install pandas numpy matplotlib seaborn
jupyter notebook churn_analysis.ipynb
```



##  Results Summary

```
Total customers analysed  :  7,032
Overall churn rate        :  26.5%
Charts generated          :  5
Business recommendations  :  3
High-risk records flagged :  exported to CSV
```



##  Author

**V A Aravind**

&#x20;


&#x20;
LinkedIn: https://www.linkedin.com/in/v-a-aravind-6a458a207



GitHub: https://github.com/vaaravind





*Dataset originally published by IBM on Kaggle. Used here for educational and portfolio purposes.*

