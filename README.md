<div align="center">

# 🛒 Retail Sales — Exploratory Data Analysis & BI Dashboard

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Completed-22c55e?style=for-the-badge)]()

<br/>

> **Uncovering hidden patterns in retail transactions through rigorous EDA and an interactive Power BI dashboard — turning raw sales data into business intelligence.**

<br/>

<img src="https://img.shields.io/badge/Level-1%20Project-gold?style=flat-square"/> &nbsp;
<img src="https://img.shields.io/badge/Domain-Retail%20Analytics-blue?style=flat-square"/> &nbsp;
<img src="https://img.shields.io/badge/Records-367K%20Sales-purple?style=flat-square"/> &nbsp;
<img src="https://img.shields.io/badge/Customers-813%20Unique-red?style=flat-square"/>

</div>

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Dashboard Preview](#-dashboard-preview)
- [Key Metrics](#-key-metrics)
- [Dataset](#-dataset)
- [Project Architecture](#-project-architecture)
- [Methodology](#-methodology)
- [Key Findings & Insights](#-key-findings--insights)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Results & Recommendations](#-results--recommendations)
- [Learning Outcomes](#-learning-outcomes)
- [Contributing](#-contributing)

---

## 🎯 Project Overview

This project conducts a full **Exploratory Data Analysis (EDA)** pipeline on a real-world retail sales dataset, followed by building an interactive **Power BI dashboard** for stakeholder-ready business intelligence.

The goal is to answer critical retail business questions:

| Business Question | Analysis Technique |
|---|---|
| Which age segments drive the most revenue? | Customer segmentation analysis |
| What are the peak sales periods? | Time series analysis |
| Which product categories perform best? | Category performance comparison |
| How does gender influence purchasing behavior? | Demographic breakdown |
| What is the average customer transaction value? | Descriptive statistics |

---

## 📊 Dashboard Preview

<div align="center">

### Retail Performance & Consumer Insights Dashboard

![image alt](https://github.com/Abhi-Git44u/OIBSIP_Data_Analytics_prop1_Level1/blob/4dfdcfbeba360b5580b88859bf081af291558683/Visuals/Retail_Dashboard.png)


---

## 📈 Key Metrics

<div align="center">

| Metric | Value | Insight |
|:---:|:---:|:---|
| 💰 **Total Sales** | ₹3,67,000 | Full period revenue |
| 📦 **Units Sold** | 2,054 | Across all categories |
| 🧾 **Avg Transaction** | ₹451.85 | Per customer per visit |
| 👤 **Total Customers** | 813 | Unique customer base |
| 🏆 **Top Age Group** | 25–35 | ₹88K in sales |
| 🛍️ **Top Category** | Clothing | Highest revenue segment |

</div>

---

## 🗂️ Dataset

| # | Dataset | Description | Link |
|---|---|---|---|
| 1 | Retail Sales Dataset 1 | Primary transaction records | [Download](https://github.com/Abhi-Git44u/OIBSIP_Data_Analytics_prop1_Level1/blob/70b8a9c477ef261b9f9e3c90ec51bee342a7c9dc/Data/Clean_Retails_salesData.csv) |

**Data Coverage:** January 2023 — October 2023

**Key Columns:**
```
├── Transaction ID      → Unique identifier per sale
├── Date                → Transaction date
├── Customer ID         → Unique customer reference
├── Gender              → Customer gender
├── Age                 → Customer age
├── Product Category    → Clothing / Electronics / Beauty
├── Quantity            → Units purchased per transaction
├── Price per Unit      → Unit selling price
└── Total Amount        → Final transaction value
```

---

## 🏗️ Project Architecture

```
Raw Data (CSV)
      │
      ▼
┌─────────────────────┐
│   Data Ingestion    │  ← pandas.read_csv()
│   & Initial Audit   │
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│   Data Cleaning     │  ← Handle nulls, duplicates,
│   & Preprocessing   │    type casting, outlier check
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│  Descriptive Stats  │  ← mean, median, std dev,
│                     │    distribution, skewness
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│  Segmentation &     │  ← Age group, gender,
│  Category Analysis  │    product category breakdown
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│  Time Series        │  ← Daily/monthly trend,
│  Analysis           │    seasonality detection
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│  Visualization &    │  ← Matplotlib, Seaborn plots
│  Python EDA Output  │    + exported CSVs for BI
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│  Power BI Dashboard │  ← Interactive slicers,
│  (Final Deliverable)│    KPI cards, charts
└─────────────────────┘
```

---

## 🔬 Methodology

### Phase 1 — Data Loading & Cleaning
- Imported datasets using `pandas`
- Audited shape, dtypes, null counts, and duplicates
- Standardized date formats and categorical labels
- Verified data consistency across both datasets

### Phase 2 — Descriptive Statistics
- Computed central tendency measures: **mean, median, mode**
- Measured spread: **standard deviation, IQR, variance**
- Generated correlation matrix for numeric features
- Identified outliers using IQR and Z-score methods

### Phase 3 — Time Series Analysis
- Resampled data to daily and monthly frequency
- Plotted rolling averages to smooth noise
- Detected potential seasonality across the Jan–Oct 2023 window
- Analyzed day-of-week effects on transaction volume

### Phase 4 — Customer & Product Segmentation
- Grouped customers into 5 age bands: `<25`, `25-35`, `36-45`, `46-55`, `55+`
- Cross-tabulated gender × category × revenue
- Ranked product categories by units sold and total revenue
- Computed customer-level spend metrics

### Phase 5 — Visualization & Dashboard
- Built Python visualizations: bar charts, line plots, heatmaps, pie charts
- Exported cleaned, aggregated tables to Power BI
- Designed interactive dashboard with slicers for **Date**, **Category**, and **Gender**
- Added KPI cards for at-a-glance executive summary

---

## 💡 Key Findings & Insights

### 1. 👥 Age Group Revenue Distribution
```
25–35   ████████████████████  88K  ← Primary revenue driver
46–55   ████████████████      79K
55+     ██████████████        72K
36–45   █████████████         70K
< 25    ████████████          58K  ← Lowest — potential growth opportunity
```
> The 25–35 cohort outspends all other groups by a **11%+ margin**, making them the core revenue driver.

### 2. 🛍️ Category Performance
- **Clothing** leads across both units and revenue
- **Electronics** trails closely — higher margin potential per unit
- **Beauty** shows steady performance — likely driven by repeat purchases

### 3. 📅 Sales Trend Observation
- Daily sales exhibit **high volatility**, indicating possible promotional spikes or event-driven demand
- No strong linear upward trend — suggests a stable but plateauing market over the period

### 4. ⚧ Gender Insights
- Gender split is nearly balanced with a **slight female majority** in purchase volume
- Category preferences likely vary by gender — cross-tab analysis recommended for deeper targeting

---

## 🧰 Tech Stack

| Layer | Tool | Purpose |
|---|---|---|
| Language | Python 3.10+ | Core analysis |
| Data Manipulation | Pandas, NumPy | Cleaning & aggregation |
| Visualization | Matplotlib, Seaborn | EDA charts |
| Statistical Analysis | SciPy | Outlier detection, correlation |
| Notebooks | Jupyter | Interactive analysis environment |
| BI Dashboard | Power BI Desktop | Final interactive deliverable |
| Version Control | Git + GitHub | Source control |

---

## 📁 Project Structure

```
retail-sales-eda/
│
├── 📂 data/
│   ├── raw/
│   │   ├── dataset1.csv              # Original dataset 1
│   │   └── dataset2.csv              # Original dataset 2
│   └── processed/
│       └── cleaned_retail_data.csv   # Post-cleaning output
│
├── 📂 notebooks/
│   ├── 01_data_cleaning.ipynb        # Ingestion & cleaning
│   ├── 02_descriptive_stats.ipynb    # Statistical analysis
│   ├── 03_time_series.ipynb          # Trend analysis
│   ├── 04_segmentation.ipynb         # Customer & product analysis
│   └── 05_visualizations.ipynb       # Final plots & charts
│
├── 📂 dashboard/
│   └── retail_dashboard.pbix         # Power BI file
│
├── 📂 visuals/
│   ├── sales_trend.png
│   ├── age_group_chart.png
│   ├── category_performance.png
│   └── gender_split.png
│
├── 📂 reports/
│   └── eda_summary.pdf               # Final written report
│
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
```bash
Python >= 3.10
pip >= 23.0
```

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/retail-sales-eda.git
cd retail-sales-eda

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Jupyter
jupyter notebook notebooks/
```

### `requirements.txt`
```
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
jupyter>=1.0.0
openpyxl>=3.1.0
scipy>=1.10.0
```

### Viewing the Power BI Dashboard
1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Open `dashboard/retail_dashboard.pbix`
3. Use the **Slicers panel** on the right to filter by Date, Product Category, and Gender

---

## 📌 Results & Recommendations

| # | Recommendation | Based On |
|---|---|---|
| 1 | **Double down on 25–35 marketing budget** | Top revenue segment at ₹88K |
| 2 | **Investigate <25 segment drop-off** | Lowest spend — pricing or awareness gap? |
| 3 | **Bundle Electronics with Clothing promotions** | Close revenue gap, increase basket size |
| 4 | **Run targeted promotions during sales dip periods** | High volatility in daily trend |
| 5 | **Personalize campaigns by gender for Beauty category** | Distinct gender-linked purchasing behavior |

---

## 📚 Learning Outcomes

- ✅ End-to-end EDA pipeline from raw data to business insights
- ✅ Hands-on data cleaning: null handling, type casting, deduplication
- ✅ Descriptive statistics interpretation for non-technical stakeholders
- ✅ Time series trend analysis and visualization
- ✅ Customer segmentation across demographic dimensions
- ✅ Power BI dashboard design with slicers, KPI cards, and chart selection

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

```bash
# Fork → Create your branch → Commit → Push → Open PR
git checkout -b feature/your-feature-name
git commit -m "Add: your feature description"
git push origin feature/your-feature-name
```

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

---

<div align="center">

**⭐ If this project helped you, consider giving it a star!**

Made with 🐍 Python + 📊 Power BI

</div>
