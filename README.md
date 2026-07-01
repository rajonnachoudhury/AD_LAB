# MiniProjects
 
A collection of small, self-contained data science projects. Each one is a step up in complexity from the last — this repo is where I practice end-to-end analysis, build intuition for working with real datasets, and get comfortable questioning results instead of accepting them at face value.
 
Every project lives in its own folder with its own notebook(s), data (or data source), and findings.
 
---
 
## Projects
 
### 1. [Walmart Weekly Sales — Descriptive Analysis](./walmart-weekly-sales)
**Status:** ✅ Complete
 
A descriptive/exploratory analysis of Walmart's weekly sales data (2010–2012, 45 stores), combining SQL and Python to dig into sales trends, seasonality, and store-level performance.
 
**Tools:** PostgreSQL / SQL (DBeaver), Python (pandas, numpy, matplotlib, seaborn), Jupyter Notebook
 
**Dataset:** 6,435 rows × 8 columns — `Store`, `Date`, `Weekly_Sales`, `Holiday_Flag`, `Temperature`, `Fuel_Price`, `CPI`, `Unemployment`. No missing values. Weekly (Friday) records across 2010–2012 (2012 data runs through October).
 
**Key findings:**
- Highest weekly sales: **$3,818,686.45** on Dec 24, 2010 (Christmas Eve). Lowest: **$209,986.25** on Dec 3, 2010.
- December was the top-selling month in 2010 and 2011 (holiday effect); January was consistently the weakest month.
- **Store 33** had the lowest total sales of any store in every year studied; **Store 4** had the highest for 2 consecutive years — Store 4 operates at roughly 8x Store 33's sales scale.
- Store 4's sales showed moderate correlation with CPI (+0.43) and Unemployment (−0.46), while Store 33 showed near-zero correlation with either.
- Deeper investigation showed this wasn't causal: CPI is a shared regional trend that rose steadily through 2011, and it simply coincided with a period when Store 4's sales happened to trend higher and grow more volatile. Store 33's sales stayed flat regardless of CPI or season.
- **Takeaway:** a solid reminder that correlation ≠ causation, especially with time-based data where unrelated series can drift together.
**Skills practiced:** SQL aggregation/filtering/date functions; pandas (`groupby`, `pivot`, `sort_values`, boolean indexing, datetime handling, categorical ordering); matplotlib/seaborn (line plots, scatter plots, subplots, heatmaps); hypothesis-driven analysis.
 
---
 
### 2. Fraud Detection
**Status:** 🚧 In progress
 
A step up in complexity — moving from descriptive analysis into predictive modeling. This project will focus on identifying fraudulent transactions, likely involving classification models, handling class imbalance, and evaluating models with metrics beyond plain accuracy (precision, recall, ROC-AUC).
 
*Details, dataset, and findings to be added as the project develops.*
 
---
 
## Roadmap
 
As this repo grows, each project is intended to build on the skills of the last — moving from descriptive analysis → predictive modeling → more advanced techniques (e.g., feature engineering, model tuning, deployment). Rough progression:
 
1. ✅ Descriptive analysis / EDA
2. 🚧 Classification & predictive modeling (Fraud Detection)
3. ⬜ More advanced modeling / additional domains (TBD)
---
 
## Structure
 
```
MiniProjects/
├── walmart-weekly-sales/
│   └── ...
├── fraud-detection/
│   └── ...
└── README.md
```
 
---
 
*This repo is a personal learning log as much as a portfolio — expect notes on what worked, what didn't, and what I'd do differently.*
