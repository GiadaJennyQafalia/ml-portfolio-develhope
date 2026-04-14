# 🤖 ML Portfolio — Develhope Data Science Program

> Machine Learning projects developed during the Develhope 
> Data Science & Behavioral Analysis Program (2024-2025).
> Focus on supervised learning, unsupervised learning,
> and business-oriented data analysis.

---

## 👩‍💻 About

Hi! I'm **Giada**, a Data Science student with a background
in **Psychological Sciences** (University of Trieste).

My approach combines technical ML skills with behavioral
analysis and business insight — bridging the gap between
data and human decision-making.

**Career targets:** Data Analyst · UX Researcher

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.12-blue)
![sklearn](https://img.shields.io/badge/scikit--learn-latest-orange)
![pandas](https://img.shields.io/badge/pandas-latest-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)

---

## 📁 Repository Structure

---

## 🗂️ Projects

---

### 📈 Project 1 — Advertising Sales Prediction
`notebooks/01_foundations/01_linear_regression_advertising.ipynb`

**Objective:** identify which advertising channel (TV, Radio, Newspaper)
has the highest impact on sales and build a predictive model.

| Detail | Value |
|---|---|
| Dataset | Advertising.csv — 200 observations |
| Algorithm | Linear Regression |
| Best predictor | TV (r = 0.78) |
| R² | 0.899 |
| RMSE | 1.782 |

**Key insight:** TV advertising generates the highest return on investment.
Newspaper shows minimal impact and could be deprioritized in budget allocation.

---

### 🚢 Project 2 — Titanic Survival Prediction
`notebooks/01_foundations/02_logistic_regression_titanic.ipynb`

**Objective:** predict passenger survival using age, sex, class and fare.
Explore the precision/recall tradeoff and select the optimal threshold
for an insurance business context.

| Detail | Value |
|---|---|
| Dataset | Titanic — 1,309 observations |
| Algorithm | Logistic Regression |
| Accuracy | ~82% |
| Key finding | Threshold 0.3 maximizes recall for high-risk passengers |

**Key insight:** in an insurance context, missing a high-risk passenger
(false negative) costs more than a false alarm — threshold 0.3 chosen
to maximize recall.

---

### 📱 Project 3 — Telco Customer Churn — Logistic Regression + Odds Ratio
`notebooks/01_foundations/03_logistic_regression_churn.ipynb`

**Objective:** predict customer churn and interpret the drivers
using Odds Ratio analysis.

| Detail | Value |
|---|---|
| Dataset | Telco Customer Churn — 7,043 observations |
| Algorithm | Logistic Regression |
| AUC-ROC | 0.842 |
| Recall (Churn) | 56% |

**Top churn drivers:**
| Feature | Odds Ratio | Effect |
|---|---|---|
| InternetService — Fiber Optic | 3.09 | +209% churn probability |
| Contract — Two Year | 0.27 | -73% churn probability |
| Electronic Check Payment | 1.47 | +47% churn probability |

**Key insight:** fiber optic customers are 3x more likely to churn —
likely due to pricing or service quality issues vs competitors.

---

### 🌳 Project 4 — Telco Churn — Decision Tree & Random Forest
`notebooks/02_advanced/04_decision_tree_rf.ipynb`

**Objective:** compare Decision Tree and Random Forest on the churn
prediction task. Extract feature importance and business insights.

| Model | AUC-ROC | Churn Recall | Churn F1 |
|---|---|---|---|
| Decision Tree | 0.820 | 0.50 | 0.55 |
| Random Forest | 0.832 | 0.40 | 0.50 |

**Key insight:** Decision Tree selected over Random Forest despite
lower AUC-ROC — higher recall (0.50 vs 0.40) is critical in a
retention context where missing at-risk customers is more costly.

**Top feature:** `tenure` (importance: 0.23) — new customers are
at significantly higher churn risk.

---

### 🔍 Project 5 — Telco Churn — KNN, LDA, SVM Comparison
`notebooks/02_advanced/05_knn_lda_svm.ipynb`

**Objective:** compare three classification algorithms on churn
prediction. Select the best model for a business retention context.

| Model | AUC-ROC | Churn Recall | Churn F1 |
|---|---|---|---|
| KNN (K=27) | 0.828 | **0.59** | **0.60** |
| LDA | 0.828 | 0.56 | 0.59 |
| SVM (rbf) | 0.783 | 0.48 | 0.55 |

**Key insight:** KNN selected as best model — highest recall (0.59)
identifies 59 out of 100 at-risk customers in advance.
SVM underperforms due to class overlap (46% of samples are support vectors).

---

### 🔵 Project 6 — Telco Churn — K-Means & Hierarchical Clustering
`notebooks/02_advanced/06_clustering.ipynb`

**Objective:** segment customers into meaningful groups without using
churn labels. Identify high-risk segments for targeted retention strategies.

**K-Means (K=3):**
| Cluster | Tenure | Monthly Charges | Churn Rate | Size |
|---|---|---|---|---|
| 0 — Premium Stable 🟡 | 55 months | €89 | 15.4% | 2,360 |
| 1 — Loyal Customers 🟢 | 31 months | €21 | 7.4% | 1,520 |
| 2 — High Risk 🔴 | 16 months | €67 | **44.2%** | 3,152 |

**Key insight:** Cluster 2 is the critical segment — 3,152 customers
(the largest group) with 44% churn rate. New customers spending
€67/month have high expectations but low loyalty.

**Hierarchical vs K-Means:**
| Metric | K-Means | Hierarchical |
|---|---|---|
| Silhouette Score | 0.219 | **0.289** |
| Separation variable | Tenure | Monthly Charges |

---

### 📐 Project 7 — Telco Churn — PCA Dimensionality Reduction
`notebooks/02_advanced/07_pca.ipynb`

**Objective:** reduce 30 features to fewer uncorrelated components
while preserving 95% of information. Evaluate impact on model performance.

| Metric | Value |
|---|---|
| Original features | 30 |
| Components (95% variance) | 17 |
| Dimensionality reduction | -43% |
| Variance retained | 95.11% |
| AUC-ROC without PCA | 0.816 |
| AUC-ROC with PCA | 0.799 |
| Performance loss | 0.017 ✅ acceptable |

**Key insight:** 43% feature reduction with only 1.7% AUC loss.
PCA resolved the multicollinearity between `tenure` and `TotalCharges`
identified in earlier projects.

---

## 📊 Models Comparison — Final Summary

| Model | Type | AUC-ROC | Churn Recall | Interpretable | Scaling |
|---|---|---|---|---|---|
| Linear Regression | Supervised Reg. | — | — | ✅ | No |
| Logistic Regression | Supervised Clf. | 0.842 | 0.56 | ✅ | Yes |
| Decision Tree | Supervised Clf. | 0.820 | 0.50 | ✅ | No |
| Random Forest | Supervised Clf. | 0.832 | 0.40 | Partial | No |
| **KNN** | **Supervised Clf.** | **0.828** | **0.59** | ❌ | Yes |
| LDA | Supervised Clf. | 0.828 | 0.56 | ✅ | No |
| SVM | Supervised Clf. | 0.783 | 0.48 | ❌ | Yes |
| K-Means | Unsupervised | — | — | Partial | Yes |
| Hierarchical | Unsupervised | — | — | ✅ | Yes |
| PCA | Dim. Reduction | — | — | ❌ | Yes |

> **Best model for churn retention:** KNN (K=27)
> Highest recall (0.59) — identifies the most at-risk customers.

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/ml-portfolio-develhope.git

# Navigate to folder
cd ml-portfolio-develhope

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows

# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn scipy xgboost jupyter

# Launch Jupyter
jupyter notebook
```

---

## 📬 Contacts

| | |
|---|---|
| 💼 LinkedIn | [linkedin.com/in/YOUR_PROFILE](https://linkedin.com/in/) |
| 📧 Email | your.email@gmail.com |
| 📍 Location | Trieste, Italy |

---

*Currently completing the Develhope Data Science Program (ending May 2026).
Open to Data Analyst and UX Researcher roles — local (Trieste) and remote.*