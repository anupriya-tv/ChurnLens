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

## 🗂️ Project Structure

```
ChurnLens/
│
├── data/
│   ├── raw/                  # Original dataset (Telco Customer Churn)
│   └── processed/            # Cleaned, feature-engineered data
│
├── notebooks/
│   ├── 01_eda.ipynb          # Exploratory Data Analysis
│   ├── 02_preprocessing.ipynb
│   └── 03_model_training.ipynb
│
├── model/
│   └── churn_model.pkl       # Trained ML model
│
├── dashboard/
│   └── ChurnLens.pbix        # Power BI dashboard file
│
├── src/
│   ├── preprocess.py
│   ├── predict.py
│   └── utils.py
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
- Real-world churn rate of ~26.5% — making it highly representative of business scenarios

---

## 🧠 ML Approach

| Step | Method |
|---|---|
| Feature Engineering | Tenure buckets, charge-per-month ratios, support interaction scores |
| Model | Random Forest Classifier (baseline) + XGBoost (optimized) |
| Evaluation | F1-Score, ROC-AUC, Precision-Recall curve |
| Explainability | SHAP values — so the model explains *why* a customer is high-risk |

---

## 📈 Dashboard Preview

> *Screenshots coming soon — dashboard in progress*

The Power BI dashboard includes:
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

# Run preprocessing
python src/preprocess.py

# Run prediction
python src/predict.py
```

Open `dashboard/ChurnLens.pbix` in Power BI Desktop to explore the dashboard.

---

## 🛣️ Roadmap

- [x] Project structure & documentation
- [x] Dataset sourced and documented
- [ ] EDA notebook
- [ ] Preprocessing pipeline
- [ ] Model training & evaluation
- [ ] SHAP explainability layer
- [ ] Power BI dashboard (v1)
- [ ] Business report PDF
- [ ] Deploy model as REST API

---

## 👩‍💻 About the Author

**Anupriya T.V** — B.Tech Computer Science & Data Science, Presidency University Bengaluru  
CSI Chapter President | IEEE Student Coordinator | BEL Process Automation Intern

Passionate about translating data into decisions that non-technical teams can actually use.

[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github)](https://github.com/yourusername)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=flat-square&logo=linkedin)](https://linkedin.com/in/yourprofile)

---

*Built with Python · Power BI · scikit-learn · SHAP · Pandas*
