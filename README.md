# 🏦 Bank Marketing Campaign Analysis & Customer Segmentation

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=flat"/>
</p>

---

## 🔍 What This Project Does

A bank ran a phone-based marketing campaign targeting ~45,000 customers to sell term deposit subscriptions — but only **~11% converted**. This project answers three business questions:

1. **Who is likely to subscribe?** → Feature selection to find the top predictors
2. **What customer types exist?** → Unsupervised segmentation to find high-potential groups
3. **What patterns drive conversion?** → Association rule mining for actionable campaign rules

The full pipeline follows the **CRISP-DM methodology** and ends with an interactive **Power BI dashboard** built for non-technical stakeholders.

---

## 📊 Power BI Dashboard

### Preview

<p align="center">
  <img src="assets/dashboard.png" alt="Power BI Dashboard Preview" width="900"/>
</p>

### Dashboard Pages

The dashboard is structured into **4 pages**, each addressing a different business question:

#### Page 1 — Campaign Overview
A high-level summary of the marketing campaign performance:
- **KPI Cards**: Total customers contacted, total subscriptions, overall conversion rate (~11%)
- **Subscriptions by Month**: Bar chart revealing which months had the highest success rates
- **Contact Method Breakdown**: Pie chart comparing cellular vs. telephone effectiveness
- **Call Duration vs. Outcome**: Visual showing that longer calls strongly correlate with subscriptions

#### Page 2 — Customer Demographics
Who are the customers, and which profiles convert?
- **Age Distribution**: Histogram segmented by subscription outcome (yes/no)
- **Job Category**: Conversion rates broken down by occupation (admin, blue-collar, retired, etc.)
- **Education & Marital Status**: Stacked bar charts showing subscription behavior across groups
- **Financial Profile**: Housing loan and personal loan status impact on subscription likelihood

#### Page 3 — Customer Segmentation
Results of K-Means clustering (K=4) to identify high-potential customer groups:
- **Cluster Profiles Table**: Average age, balance, call duration, and campaign contacts per cluster
- **Subscription Rate by Cluster**: Which segments convert the most?
- **Balance vs. Duration Scatter Plot**: Clusters plotted to show separation and overlap
- **Cluster Size Distribution**: How many customers fall into each segment

#### Page 4 — Pattern Mining Insights
Actionable rules discovered through association rule mining:
- **Top Rules by Lift**: The strongest behavioral patterns linked to subscription
- **Support vs. Confidence Chart**: All mined rules visualized for business filtering
- **Key Insight Callouts**: Plain-language summaries of the most actionable rules (e.g., customers contacted ≤ 3 times with a prior success → high conversion)

### 🔗 Links
| | |
|---|---|
| **Live Dashboard** | [View on Power BI Service](https://app.powerbi.com/links/t1IOABFPjN?ctid=2dff09ac-2b3b-4182-9953-2b548e0d0b39&pbi_source=linkShare) |
| **Download .pbix** | [Download from SharePoint](https://uithcm-my.sharepoint.com/:u:/g/personal/23521562_ms_uit_edu_vn/IQDGxOhayuSFR7Di9KsFMCQsAfJBeHdNDqCjCOIbkzKKpnY?e=WqhSQs) |

---

## 💡 Key Results

| Finding | Detail |
|---|---|
| **Top predictor** | `duration` (call length) — longest calls convert at 3× the average rate |
| **#2 predictor** | `balance` — customers with higher savings are more receptive |
| **Best segment** | Cluster of older, higher-balance customers with prior successful contact |
| **Actionable rule** | Customers contacted ≤ 3 times + prior success → significantly higher conversion |
| **Feature agreement** | Random Forest and Mutual Information both rank the same top 5 features |

---

## 🔄 Analysis Pipeline

```
1. Business Understanding    Define the problem as a segmentation + conversion task
         ↓
2. Exploratory Data Analysis  Distribution, correlation, class imbalance (89% / 11%)
         ↓
3. Data Preprocessing         Encoding · Log Transformation · Feature Discretization
         ↓
4. Feature Selection          Random Forest Importance + Mutual Information → Top 5 features
         ↓
5. Customer Segmentation      K-Means Clustering (K=4, validated via Elbow Method)
         ↓
6. Pattern Mining             Association Rules: Support · Confidence · Lift
         ↓
7. Visualization              Interactive Power BI Dashboard for business stakeholders
```

---

## 🛠️ Skills Demonstrated

| Area | What I Did |
|---|---|
| **Data Analysis** | EDA on 45K+ records — distributions, outliers, correlations, class imbalance |
| **Feature Engineering** | Log transformation to fix skewness, discretization for rule mining |
| **Machine Learning** | Random Forest for feature importance; K-Means for unsupervised segmentation |
| **Statistical Methods** | Mutual Information, Elbow Method, Association Rule Mining |
| **Data Visualization** | Power BI dashboard with DAX measures, slicers, segment-level breakdowns |
| **Business Thinking** | Translated model outputs into campaign strategy recommendations |

---

## 📁 Project Structure

```
Bank-Marketing-Customer-Analysis/
│
├── Final Project/
│   ├── EDA.ipynb                   # Exploratory Data Analysis
│   ├── Preprocessing.ipynb         # Cleaning, encoding, transformation
│   ├── Feature_Selection.ipynb     # Random Forest + Mutual Information
│   ├── Clustering.ipynb            # K-Means + Elbow Method
│   ├── Pattern_Mining.ipynb        # Association rule extraction
│   └── Dashboard.pbix              # Power BI dashboard
│
├── assignment/                     # Coursework supporting materials
├── assets/                         # Screenshots and images for README
└── README.md
```

> ⚠️ Update notebook filenames above to match your actual files.

---

## 📂 Dataset

**[Banking Dataset – Marketing Targets](https://www.kaggle.com/datasets/prakharrathi25/banking-dataset-marketing-targets)** — Kaggle

| | |
|---|---|
| Records | ~45,000 customer interactions |
| Features | 17 (demographic, financial, campaign history) |
| Target | `y` — did the customer subscribe? (`yes` / `no`) |
| Class balance | ~89% No · ~11% Yes |

---

## ⚙️ How to Run

```bash
# 1. Clone the repo
git clone https://github.com/thybui1903/Bank-Marketing-Customer-Analysis.git
cd Bank-Marketing-Customer-Analysis

# 2. Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn mlxtend jupyter

# 3. Add dataset
# Download from Kaggle and place CSV files inside Final Project/

# 4. Run notebooks in order
# EDA → Preprocessing → Feature_Selection → Clustering → Pattern_Mining

# 5. Open Dashboard.pbix in Power BI Desktop
```

---

## 👤 About the Author

**Bui Tran Thy Thy** — Data Science student at UIT VNU-HCM (GPA: 8.69/10)

Seeking a **Data Analyst / Data Scientist internship** where I can apply end-to-end analytical skills to real business problems.

[![GitHub](https://img.shields.io/badge/GitHub-thybui1903-181717?style=flat&logo=github)](https://github.com/thybui1903)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-thybui1903-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/thybui1903)
[![Email](https://img.shields.io/badge/Email-thybui1903qn@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:thybui1903qn@gmail.com)
