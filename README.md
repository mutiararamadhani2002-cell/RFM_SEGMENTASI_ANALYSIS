# 🛒 AI² Mart Customer Behavior Analysis (2016)
### RFM Segmentation & CV-Based Purchasing Behavior

---

## 📌 Overview

This project analyzes customer transaction data from **AI² Mart**, a retail company in Jakarta, to better understand customer purchasing behavior and design more targeted marketing strategies. The analysis combines **RFM Segmentation** with **Coefficient of Variance (CV)-Based Behavioral Profiling** to uncover customer personality patterns and recommend actionable campaigns per segment.

This project was completed as part of the **Purwadhika Data Science & Machine Learning Bootcamp**.

---

## 🎯 Problem Statement

AI² Mart faces two key challenges:
1. Difficulty in understanding **customer purchasing behavior patterns**
2. Difficulty in identifying **the most effective marketing campaign** for different customer segments

---

## 🎯 Goals

- Segment customers based on transaction behavior using **RFM Analysis**
- Understand purchasing consistency using the **Coefficient of Variance (CV)**
- Combine both approaches to reveal **customer personality patterns**
- Provide **actionable, segment-specific marketing strategies**

---

## 👥 Stakeholders

| Stakeholder | Role |
|---|---|
| Management Team | Strategic decision-making |
| Business & Marketing Team | Designing retention and campaign strategies |

---

## 📊 Dataset

**Source:** AI² Mart Transaction Records (Jakarta, 2016)

| Column | Description |
|---|---|
| `Customer_ID` | Unique identifier for each customer |
| `Date` | Transaction date |
| `Transaction_ID` | Unique identifier per transaction |
| `SKU_Category` | Product category based on SKU system |
| `SKU` | Unique product code |
| `Quantity` | Number of units purchased |
| `Sales_Amount` | Total monetary value of the transaction |

---

## 🧠 Analytical Framework

```
RFM Analysis → Customer Segmentation → Behavior Variability (CV) → Customer Personality → Marketing Campaign Strategy
```

### 1. RFM Analysis
Each customer is scored across three dimensions:
- **Recency** — How recently they made a purchase
- **Frequency** — How often they purchase
- **Monetary** — How much they spend

Scores are assigned from 1–5 using quantile-based scoring (`pd.qcut`), then combined into an RFM score to classify customers into **11 segments**:

| Segment | Description |
|---|---|
| Champion | High R, F, and M — best customers |
| Loyal Customer | Frequent buyers with high spend |
| Potential Loyalist | Almost loyal — needs nurturing |
| New Customer | Recently acquired, still exploring |
| Promising | New with growth potential |
| Need Attention | Moderate engagement needing re-activation |
| Cannot Lose Them | High value but at risk of churning |
| About to Sleep | Declining engagement |
| At Risk | Previously active, now drifting |
| Hibernating | Long inactive, low engagement |
| Lost | Disengaged, low value |

### 2. Coefficient of Variance (CV)
Customers within each RFM segment are further categorized by purchasing consistency:
- **Stable** — Consistent, predictable purchasing patterns
- **Normal** — Moderate variability in purchasing behavior
- **Impulsive / Uncertain** — Highly irregular or limited purchase history

### 3. Merging RFM + CV
The two frameworks are combined to create **detailed customer personality profiles**, enabling more precise and cost-effective campaign targeting.

---

## 💡 Key Insights

1. **Dominance of "Blind" Data** — Critical segments (Lost 98.9%, About to Sleep 89.9%, Cannot Lose Them 87.2%) are dominated by the Uncertain category, indicating insufficient customer data capture at the point of sale.

2. **High-Value Customer Leakage** — The *Cannot Lose Them* segment (429 customers) represents the largest monetary asset at risk. Failing to re-engage them directly impacts profitability.

3. **Sleeping Giant in the Lost Segment** — With 5,560 customers, reactivating even 5–10% of the Lost segment could significantly grow revenue without new customer acquisition costs.

---

## 📋 Strategic Recommendations

| Priority | Focus Segment | Action |
|---|---|---|
| 🔴 High | Cannot Lose Them | VIP Rescue — personalized outreach, exclusive loyalty rewards |
| 🟡 Medium | About to Sleep | Data Validation — interactive surveys with voucher incentives |
| 🟢 Efficiency | Lost | A/B Testing — low-cost retargeting before full budget allocation |

**Long-term recommendation:** Build a Customer Data Infrastructure (CDP) to reduce Uncertain customer profiles — link every transaction to a validated contact, offer profiling incentives, and automate 30-day check-in messages.

---

## 📎 Presentation

📊 (https://www.canva.com/design/DAHDV49E1fw/ntrX9ZL1-_uSJ4bw4o4i6g/edit)

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-001E1A?style=for-the-badge&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-2E97A1?style=for-the-badge&logoColor=white)

**Additional libraries:** `squarify` (treemap visualization)

---

## 👤 Authors

This project was completed as a group assignment at Purwadhika Digital Technology School.

**Indira Faisa Afgani**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mutiara-ayu-1a343528).

---

## 📄 License

This project is for educational purposes as part of the Purwadhika Digital Technology School Data Science & Machine Learning program.
