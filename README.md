# 🔍 ChurnLens
### *Turning Customer Loss into Business Strategy*

> A business intelligence tool that predicts customer churn risk and translates raw data into decisions a non-technical team can actually act on.

![Status](https://img.shields.io/badge/Status-In_Development-f59e0b?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.10+-3b82f6?style=flat-square&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-f2c811?style=flat-square&logo=powerbi&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-10b981?style=flat-square)

---

## 🧩 The Business Problem

Every company loses customers. Most don't know *which* customers are about to leave — until it's too late.

Customer acquisition costs **5x more** than retention. Yet most analytics tools built for churn prediction require a data science team to interpret them. Business managers end up with a black-box model and no clear next step.

**ChurnLens bridges that gap.**

It identifies at-risk customers *before* they leave, explains *why* in plain business language, and recommends *what to do about it* — all through a dashboard a non-technical manager can open on Monday morning.

---

## ✨ What It Does

| Feature | Description |
|---|---|
| 📥 **Data Ingestion** | Accepts customer datasets (CSV/Excel) with usage, billing, and support data |
| 🧹 **Auto Cleaning** | Handles missing values, outliers, and inconsistent formats automatically |
| 🤖 **Churn Prediction** | ML model flags customers by risk level — High / Medium / Low |
| 📊 **BI Dashboard** | Interactive Power BI dashboard with filters by segment, region, and plan |
| 💡 **Action Cards** | Each high-risk customer gets a plain-English reason + recommended retention action |
| 📤 **Export Ready** | Download filtered churn reports as CSV for CRM or ops team handoff |

---

## 📊 Key Findings

Exploratory analysis on 7,043 customers revealed clear churn drivers:

| Driver | Finding |
|---|---|
| **Contract type** | Month-to-month customers churn at **42.7%** vs just **2.8%** for two-year contracts |
| **Tenure** | New customers (0–12 months) churn at **47.7%** — the first year is the highest-risk window |
| **Pricing** | Churned customers pay **₹13 more per month** on average than retained customers |
| **Top model signal** | Contract type and tenure are the two strongest predictors — far more than demographics |

**The business takeaway:** churn is driven almost entirely by contract structure and pricing, not who the customer is. Retention strategy should focus on converting month-to-month customers to longer contracts, especially within the first year.

---

## 🧠 Model Performance

- **Algorithm:** Random Forest Classifier (balanced for class imbalance)
- **ROC-AUC:** 0.838
- **Recall on churned customers:** 68% — correctly catches most at-risk customers
- **Precision on churned customers:** 55% — acceptable tradeoff, since the cost of a false alarm is low compared to losing a real customer

---

## 🗂️ Project Structure

```
ChurnLens/
│
├── data/
│   └── raw/                       # Original dataset (Telco Customer Churn)
│
├── notebooks/
│   └── churn_analysis.ipynb       # Full EDA, cleaning, and model training
│
├── churn_model.pkl                # Trained ML model
├── label_encoders.pkl             # Encoders for categorical features
├── telco_churn_cleaned.csv        # Cleaned dataset, ready for Power BI
│
├── dashboard/
│   └── ChurnLens.pbix             # Power BI dashboard file
│
├── reports/
│   └── ChurnLens_BusinessReport.pdf   # Summary for non-tech stakeholders
│
├── requirements.txt
└── README.md
```

---

## 📊 Dataset

**Source:** [Telco Customer Churn — IBM Sample Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

- 7,043 customer records
- 21 features: contract type, tenure, monthly charges, support tickets, and more
- Real-world churn rate of **26.5%** — highly representative of business scenarios

---

## 🧠 ML Approach

| Step | Method |
|---|---|
| Data Cleaning | Handled missing `TotalCharges` values (new customers with 0 tenure) |
| Feature Engineering | Tenure buckets, categorical encoding for all customer attributes |
| Model | Random Forest Classifier, balanced for the 26.5% churn class imbalance |
| Evaluation | Precision, recall, F1-score, ROC-AUC |
| Feature Importance | Identified contract type and tenure as the dominant churn drivers |

---

## 📈 Dashboard Preview

> *Power BI dashboard in progress — screenshots coming soon*

The dashboard will include:
- 🔴 High / 🟡 Medium / 🟢 Low churn risk segments
- Churn drivers ranked by impact (contract type, tenure, support calls)
- Month-over-month at-risk customer trend
- One-click export of high-risk customer list for retention teams

---

## 💼 Business Impact

This project simulates a real-world BA deliverable — not just a model, but a **decision support system**:

- Retention teams get a prioritized call list every week
- Product teams see which features correlate with long-term loyalty
- Finance teams can model revenue saved from proactive retention campaigns
- All without needing to open a single Jupyter notebook

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/yourusername/ChurnLens.git
cd ChurnLens

# Install dependencies
pip install -r requirements.txt

# Open the notebook to see the full analysis
jupyter notebook notebooks/churn_analysis.ipynb
```

Open `dashboard/ChurnLens.pbix` in Power BI Desktop to explore the dashboard once built.

---

## 🛣️ Roadmap

- [x] Project structure & documentation
- [x] Dataset sourced and cleaned
- [x] EDA — identified key churn drivers
- [x] Model training & evaluation (ROC-AUC: 0.838)
- [ ] Power BI dashboard (v1)
- [ ] Business report PDF
- [ ] SHAP explainability layer
- [ ] Deploy model as REST API

---

## 🛠️ Tech Stack

**Analysis:** Python, pandas, scikit-learn
**Modeling:** Random Forest Classifier
**Visualization:** Power BI
**Dev environment:** Google Colab

---

## 👩‍💻 About the Author

**Anu** — B.Tech Computer Science & Data Science, Presidency University Bengaluru
CSI Chapter President | IEEE Student Coordinator | BEL Process Automation Intern

Passionate about translating data into decisions that non-technical teams can actually use.

[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/anupriya-tv)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/anupriya-t-v/)

---

*Built with Python · Power BI · scikit-learn · Pandas*
