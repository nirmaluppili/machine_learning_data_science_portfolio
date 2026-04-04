# Lead Conversion Prediction

Identifying which leads are most likely to convert to paying customers
using classification models on an EdTech startup dataset.

---

## Business Problem

ExtraaLearn is an EdTech startup that generates leads through multiple
channels — website, mobile app, email, and marketing campaigns. Not all
leads convert to paying customers. The sales team needs to prioritize
which leads to contact first.

**Goal:** Build a classification model that predicts lead conversion
and identifies the key factors driving it.

**Primary Metric:** Recall — missing a real conversion (False Negative)
is more costly than contacting a lead that won't convert (False Positive).

---

## Dataset

- **Source:** ExtraaLearn EdTech lead dataset
- **Size:** 4,612 leads, 15 features
- **Target:** `status` (1 = Converted, 0 = Not Converted)
- **Class distribution:** 70% not converted, 30% converted (imbalanced)

**Features include:**
- Demographics: age, current occupation
- Behavioral: time spent on website, website visits, page views
- Channel: first interaction (website vs mobile app), last activity
- Marketing: print media, digital media, referral, educational channels
- Profile: profile completion level

---

## Approach

This project follows a 13-step end-to-end data science workflow:

1. **Business Problem Definition** — defined cost of each mistake,
   established recall as primary metric
2. **Data Understanding** — profiled 4,612 records across 15 features
3. **Data Preparation** — no missing values or duplicates found,
   dropped ID column
4. **Exploratory Data Analysis** — identified strong signals in
   first interaction channel, time on website, and profile completion
5/6. **Hypothesis Formation and Statistical Testing** — chi-square
   tests for categorical features, t-tests for continuous features.
   6 features showed no statistically significant relationship with
   conversion and were dropped
7. **Feature Engineering** — ordinal encoding for profile completion,
   one-hot encoding for categorical features, dropped 6 insignificant
   features identified by hypothesis testing
8. **Preprocessing for Modeling** — 70/30 stratified train/test split,
   StandardScaler applied for Logistic Regression only
9/10/11/12. **Model Building, Evaluation, Tuning and Selection** —
   three models built, tuned with GridSearchCV, and compared
13. **Feature Importance and Business Recommendations** — top drivers
    identified, actionable recommendations provided

---

## Model Results

| Model | Recall | Precision | F1 | AUC |
|---|---|---|---|---|
| Logistic Regression (Baseline) | 0.84 | 0.63 | 0.72 | 0.8793 |
| Decision Tree (Tuned) | 0.90 | 0.61 | 0.73 | 0.8845 |
| **Random Forest (Tuned)** | **0.88** | **0.64** | **0.74** | **0.9142** |

**Selected Model:** Tuned Random Forest

**Reason:** Highest AUC (0.9142) indicates strongest class separation
and best generalization to new data. Recall of 0.88 beats the baseline.
Preferred over Decision Tree for its stability and performance on
larger datasets.

---

## Key Findings

1. **First interaction channel is the strongest driver (34.8% importance)**
   — leads who first interact via the website convert at 45% vs 10%
   for mobile app leads

2. **Time spent on website is the second strongest driver (33.1%)**
   — converted leads spend significantly more time exploring the platform

3. **Profile completion strongly predicts conversion (21.1%)**
   — high completion leads convert at the highest rate

4. **Referral shows high conversion rate (65%) but low model importance**
   — referral's signal is captured by stronger correlated features
   (profile completion, website interaction)

---

## Business Recommendations

1. **Invest in mobile app experience** — close the 35-point conversion
   gap between website and mobile app leads

2. **Optimize website content quality** — reduce time-to-decision,
   consolidate key information to convert leads faster

3. **Reduce profile completion friction** — implement CV parsing or
   professional platform integration to pre-populate profiles

---

## Technologies

- Python 3.x
- pandas, numpy
- matplotlib, seaborn
- scikit-learn (LogisticRegression, DecisionTreeClassifier,
  RandomForestClassifier, GridSearchCV)
- scipy (chi2_contingency, ttest_ind)

---

## How to Run
```bash