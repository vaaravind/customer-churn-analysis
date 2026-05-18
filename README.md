# 📊 Customer Churn Analysis — Telecom

> \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*Business Analyst Portfolio Project\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\* | Python · Pandas · Seaborn · Matplotlib

\---

## 🗂️ Project Overview

A telecom company is losing customers at an alarming rate of **26.5%** — above the industry average.  
This project identifies *who* is leaving, *why* they are leaving, and *what the business should do* to fix it.

This is one of the most commonly asked BA interview projects at companies like **TCS, Infosys, Accenture, Deloitte, KPMG**, and product startups.

\---

## 📁 Repository Structure

```
customer-churn-analysis/
│
├── churn\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_analysis.ipynb               # Main analysis notebook
├── WA\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_Fn-UseC\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_-Telco-Customer-Churn.csv  # Dataset (IBM Telco)
├── high\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_risk\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_churned\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_customers.csv    # Exported at-risk segment
│
├── fig1\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_churn\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_rate.png                # Overall churn donut + bar
├── fig2\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_contract\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_churn.png            # Contract type vs churn
├── fig3\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_tenure\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_churn.png              # Tenure histogram + band chart
├── fig4\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_charges\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_churn.png             # Monthly charges boxplot + KDE
├── fig5\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_internet\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_payment.png          # Internet \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\& payment method churn
│
└── README.md
```

\---

## 📦 Dataset

* **Source:** [IBM Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
* **Rows:** 7,032 customers (after cleaning)
* **Columns:** 20 features + 1 target (`Churn`)
* **Key Features:** `tenure`, `Contract`, `MonthlyCharges`, `InternetService`, `PaymentMethod`

\---

## 🔍 Key Findings

|#|Finding|Churn Rate|
|-|-|-|
|1|Month-to-month contract customers|**\~42%**|
|2|Customers in first 12 months|**\~47%**|
|3|Fiber optic internet users|**\~41%**|
|4|Electronic check payment users|**\~45%**|
|5|Customers with no tech support|**\~41%**|

> 💡 The highest-risk segment: \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*month-to-month + fiber optic + < 12 months tenure\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\* — estimated churn probability exceeds \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*60%\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\*.

\---

## 📊 Charts Generated

|Figure|Description|
|-|-|
|Fig 1|Overall churn rate — bar + donut chart|
|Fig 2|Contract type vs churn — grouped bar + rate chart|
|Fig 3|Tenure vs churn — overlapping histogram + band analysis|
|Fig 4|Monthly charges vs churn — boxplot + KDE density|
|Fig 5|Internet service \& payment method vs churn|

\---

## 🎯 Business Recommendations

### 1\. Incentivise Long-Term Contracts 🔴 Critical

Month-to-month customers churn **14× more** than 2-year contract customers.  
→ Offer 10–15% discounts on annual plans; run "Switch \& Save" campaigns.

### 2\. Build an Early Warning \& Onboarding Programme 🟠 High

47% of churn happens in the first 12 months — customers leave before becoming loyal.  
→ 90-day onboarding journey; CRM flags for at-risk customers (< 12 mo + M2M + charges > $70).

### 3\. Review Fiber Optic Pricing \& Service Quality 🟠 High

Fiber optic customers pay the most but churn the most — a value perception problem.  
→ NPS survey, 12-month price lock for new fiber customers, value-added bundles.

\---

## 🛠️ Tools \& Libraries

```python
pandas       # Data loading, cleaning, transformation
numpy        # Numerical operations
matplotlib   # Base plotting
seaborn      # Statistical visualizations
```

\---

## 🚀 How to Run

### Option A — Google Colab 

1. Upload `churn\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_analysis.ipynb` and `WA\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_Fn-UseC\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_-Telco-Customer-Churn.csv` to Colab
2. Run all cells (`Runtime → Run all`)

### Option B — Jupyter Locally

```bash
git clone https://github.com/YOUR\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_USERNAME/customer-churn-analysis.git
cd customer-churn-analysis
pip install pandas numpy matplotlib seaborn
jupyter notebook churn\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_analysis.ipynb
```

\---

## 📈 Results Summary

```
Total customers analysed  :  7,032
Overall churn rate        :  26.5%
Charts generated          :  5
Business recommendations  :  3
High-risk records flagged :  exported to CSV
```

\---

## 👤 Author

**V A Aravind**

&#x20;
Business Analyst | Data Analytics Enthusiast

&#x20;
LinkedIn: https://www.linkedin.com/in/v-a-aravind-6a458a207?utm\_source=share\&utm\_campaign=share\_via\&utm\_content=profile\&utm\_medium=android\_app ·



GitHub: https://github.com/vaaravind



\---

*Dataset originally published by IBM on Kaggle. Used here for educational and portfolio purposes.*

