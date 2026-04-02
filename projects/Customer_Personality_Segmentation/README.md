# Customer Personality Segmentation
Unsupervised machine learning project using K-Means clustering to 
segment retail customers into distinct personality groups.

---

## Problem Statement
A retail company wants to move away from one-size-fits-all marketing 
by identifying distinct customer segments based on demographics, 
spending behavior, and purchasing patterns. This project uses 
K-Means clustering to discover those natural groupings and provides 
targeted recommendations for each segment.

---

## Dataset
| Property | Detail |
|---|---|
| Source | [Kaggle — Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis) |
| Records | 2,240 customers |
| Features | 29 columns |
| Format | Tab-separated (.csv) |

---

## Project Workflow
Follows a structured 13-step data science workflow:

| Phase | Steps | Description |
|---|---|---|
| Foundation | 1-4 | Business problem, data understanding, preparation, feature engineering |
| Exploration | 5 | EDA — 7 business questions answered |
| Hypothesis | 6-7 | 6 hypotheses formed and statistically tested |
| Modeling | 8-10 | Preprocessing, K-Means clustering, model evaluation |
| Insights | 11-12 | Cluster profiling and model tuning |
| Communication | 13 | Business recommendations and documentation |

---

## Key Results
- **4 customer segments** identified from 2,230 customers
- **Silhouette Score: 0.1901**
- **6 statistical tests** run (correlation, t-test, ANOVA)

### Customer Segments
| Cluster | Name | Size | Profile |
|---|---|---|---|
| 0 | Deal Seekers | 581 | Moderate income, deal-driven, active web buyers |
| 1 | Budget Browsers | 1,012 | Low income, high web visits, low conversion |
| 2 | Premium Loyalists | 560 | High income, high spend, campaign responsive |
| 3 | Campaign Responsive Seniors | 77 | Oldest segment, store preference, wine buyers |

---

## How to Run

1. Clone the repository
2. Open the notebook:
```
projects/Customer_Personality_Segmentation/Customer_Personality_Segmentation.ipynb
```
3. Download the dataset from Kaggle:
   [Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)
   - Place the downloaded file in the `datasets/` folder
   - Rename the file to: `Customer_Personality_Segmentation.csv`
4. Run all cells top to bottom

---

## Tools and Libraries
- Python 3
- Pandas, NumPy — data manipulation
- Matplotlib, Seaborn — visualization
- Scikit-learn — K-Means, PCA, StandardScaler, silhouette score
- SciPy — statistical hypothesis testing

---

## Skills Demonstrated
- Exploratory data analysis
- Feature engineering
- Statistical hypothesis testing
- Unsupervised machine learning
- Customer segmentation
- Business recommendations from data insights