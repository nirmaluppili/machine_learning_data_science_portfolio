# Merchandising Customer Insights

Data-driven analysis of retail customer behavior to support merchandising decisions, churn prevention, and promotional strategy optimization.

---

## Problem Statement

Merchandising team faces three interconnected challenges:

1. **Repeat purchase rates are declining** — unclear which customer segments are at risk
2. **Promotional spend is increasing** — uncertain if promotions drive incremental revenue or cannibalize full-price sales
3. **Category-level revenue is underperforming** — lack of visibility into customer behavior by segment

The business suspects that heavy promotions are attracting price-sensitive, one-time buyers who don't return at full price — masking a structural decline in loyal customer engagement.

---

## Dataset

| Property | Detail |
|---|---|
| Source | UCI Machine Learning Repository — Online Retail II |
| Period | December 1, 2009 — December 9, 2011 (738 days) |
| Records (Raw) | 1,067,371 transactions |

---

## Project Objectives

### Objective 1: Customer Segmentation ✅
Build RFM-based behavioral segmentation to identify distinct customer types and their characteristics.

**Status:** Complete
- 7 customer segments defined (VIP, Loyal, New Customers, Potential Loyalists, At Risk, Cannot Lose, Churned)
- Segment sizes: 22% VIP, 25% Churned, 16% New Customers, others distributed
- **Key Insight:** 40% of customers are inactive or at-risk

### Objective 2: Churn & Retention Analysis 🟡
Identify high-risk segments, quantify revenue at risk, and surface behavioral signals that predict churn.

**Status:** In Progress

### Objective 3: Promotional Incrementality ⏳
Determine whether promotions drive net new revenue or cannibalize/pull forward demand, and whether they disproportionately attract low-retention customers.

**Status:** Upcoming

---

## Project Workflow

Follows the **CRISP-DM framework** (6 stages, 12 steps):

| Stage | Steps | Status |
|-------|-------|--------|
| **1. Business Understanding** | Define problem, success criteria | ✅ Complete |
| **2. Data Understanding** | Load, explore, identify quality issues | ✅ Complete |
| **3. Data Preparation** | Clean, transform, engineer features | ✅ Complete |
| **4. Modeling** | Build churn model, promo analysis | 🟡 In Progress |
| **5. Evaluation** | Assess performance, interpret results | ⏳ Upcoming |
| **6. Deployment** | Present findings, recommendations | ⏳ Upcoming |

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/nirmaluppili/machine_learning_data_science_portfolio.git
```

2. Navigate to the project:
```bash
cd projects/merchandising-customer-insights
```

3. Download the dataset:
   - Source: [UCI Online Retail II](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)
   - Place in: `../../datasets/`
   - Filename: `online_retail_2.csv`

4. Open and run the notebook: 
merchandising-customer-insights.ipynb

5. Run all cells top to bottom

---

## Tools and Libraries

- **Python 3.x**
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn (classification, clustering)
- **Statistics:** SciPy

---

## Skills Demonstrated

- Exploratory data analysis (EDA)
- Data cleaning and validation
- Feature engineering and aggregation
- RFM customer segmentation
- Customer behavior analysis
- Churn prediction modeling (in progress)
- Statistical hypothesis testing
- Business insights and recommendations
- CRISP-DM framework application

---

## Project Structure

```
machine_learning_data_science_portfolio/
├── datasets/
│   ├── online_retail_2.csv                  # Raw data
│   ├── data_clean.csv                       # Cleaned transactions
│   └── rfm_segments.csv                     # RFM table with segments
├── projects/
│   └── merchandising-customer-insights/
│       ├── merchandising-customer-insights.ipynb    # Main notebook
│       └── README.md                                 # This file
├── references/
├── .gitignore
└── README.md                                 # Portfolio README
```

---

## Key Findings (In Progress)

### Completed
✅ Customer segmentation identifies 7 distinct groups  
✅ Data quality issues documented and resolved  
✅ 40% of customer base is inactive or at-risk — major retention problem  

### Next Steps
🟡 Build churn prediction model to identify at-risk customers early  
⏳ Measure promotional incrementality and impact on customer retention  
⏳ Generate business recommendations for merchandising team  

---

## A Note on AI Assistance Transparency

An AI assistant was used as a learning tool during this project.

Its role was to:
- Explain data science concepts (RFM, quintiles, CRISP-DM framework)
- Guide the analytical process through questions rather than solutions
- Verify calculations and data quality checks
- Format markdown and code comments
- Help debug technical issues

**All analytical decisions are my own:**
- The data cleaning strategy was developed through analysis
- RFM segmentation logic and thresholds were chosen based on data insights
- Feature engineering decisions reflected business understanding
- Segment naming and profiles reflect my interpretation of the results
- All code was written and executed by me

AI was used the way a senior colleague would be used — to answer questions, provide feedback, and guide thinking — not to do the analysis.

---

## Contact & Feedback

Questions or feedback? Feel free to open an issue or reach out.

---

**Last Updated:** April 17, 2026  
**Status:** 🟡 In Progress — Modeling phase active