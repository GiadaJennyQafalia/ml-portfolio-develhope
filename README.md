# Machine Learning Portfolio — Develhope Data Science Program

> **Open to work:** Data Analyst · UX Researcher · Trieste or Full Remote (Italy)  
> [LinkedIn](https://www.linkedin.com/in/giada-jenny-qafalia-778417390) · [GitHub](https://github.com/GiadaJennyQafalia)

End-to-end Machine Learning portfolio developed during the Develhope Data Science 
program (2025–2026). All models are applied to real-world datasets with full 
preprocessing pipelines, evaluation metrics, and business observations.

**What makes this portfolio different:** each notebook goes beyond the model —  
every result is translated into actionable business recommendations, reflecting  
a background in Psychology and a focus on human-centered data interpretation.

---

## About Me

I am a Data Science student with a Bachelor's degree in Psychology (University of Trieste).  
My background gives me a dual perspective: I approach data with analytical rigor  
and translate findings into insights that are meaningful for people and organizations.

**Target roles:** Data Analyst · UX Researcher · Junior Data Scientist  
**Location:** Trieste (on-site or hybrid) · Full Remote (Italy)  
**Program end:** May 2026 — available for internships and junior positions

**Core skills:**
- Full ML pipeline: EDA → preprocessing → modeling → evaluation → business insights
- Classification, regression, clustering, dimensionality reduction
- Python · pandas · scikit-learn · matplotlib · seaborn
- Statistical thinking from Psychology background (experimental design, behavioral data)
- Communication of technical results to non-technical stakeholders

---

## Repository Structure

ml-portfolio-develhope/
├── notebooks/
│   ├── 01_foundations/
│   │   ├── 01_linear_regression_advertising.ipynb
│   │   ├── 02_logistic_regression_titanic.ipynb
│   │   └── 03_logistic_regression_churn.ipynb
│   └── 02_advanced/
│       ├── 04_decision_tree_rf.ipynb
│       ├── 05_knn_lda_svm.ipynb
│       ├── 06_clustering.ipynb
│       ├── 07_pca.ipynb
│       ├── 08_adaboost_xgboost.ipynb
│       └── 09_ann.ipynb
├── data/
└── images/

---

## Notebooks Overview

| # | Topic | Dataset | Key Result |
|---|-------|---------|------------|
| 01 | Linear Regression | Advertising | R² = 0.899 — TV is the strongest sales predictor |
| 02 | Logistic Regression + Threshold Tuning | Titanic | AUC = 0.752 — optimal threshold for insurance context |
| 03 | Logistic Regression + Odds Ratio | Telco Churn | AUC = 0.842 — Fiber Optic OR = 3.09 |
| 04 | Decision Tree & Random Forest | Telco Churn | tenure top predictor (importance = 0.23) |
| 05 | KNN, LDA, SVM | Telco Churn | KNN K=27 — best Churn Recall (0.59) |
| 06 | K-Means & Hierarchical Clustering | Telco Churn | 3 segments — Cluster 2: 44% churn rate ⚠️ |
| 07 | PCA | Telco Churn | 30 → 17 components, 95.11% variance retained |
| 08 | AdaBoost & XGBoost | Telco Churn | AdaBoost AUC = 0.841, XGBoost AUC = 0.837 |
| 09 | Artificial Neural Network | Telco Churn | AUC = 0.754 — simpler models outperform on small data |

---

## Model Comparison — Telco Churn Dataset

> **Primary metric: Recall on Churn class.**  
> In a retention context, a missed churner (false negative) costs 5–7x more  
> than a wrongly flagged loyal customer (false positive).

| Model | AUC-ROC | Recall (Churn) | F1 |
|-------|---------|----------------|----|
| Logistic Regression | 0.842 | 0.56 | 0.59 |
| AdaBoost | 0.841 | 0.50 | 0.56 |
| XGBoost | 0.837 | 0.54 | 0.58 |
| Random Forest | 0.832 | 0.40 | 0.50 |
| **KNN (K=27)** | 0.828 | **0.59** | **0.60** |
| LDA | 0.828 | 0.56 | 0.59 |
| Decision Tree | 0.820 | 0.50 | 0.55 |
| SVM | 0.783 | 0.48 | 0.55 |
| ANN | 0.754 | 0.33 | 0.45 |

**Best model for retention context: KNN (K=27).**  
On this dataset (~7,000 rows, 73/27 class imbalance), simpler models  
consistently outperform complex ensembles and neural networks —  
a result with direct implications for model selection in real CRM contexts.

---

## Key Business Insights

- **Churn risk peaks in the first 16 months** — new customers on premium plans 
  are the most vulnerable segment (44% churn rate, K-Means Cluster 2)
- **Fiber Optic customers churn 3x more** than average (Odds Ratio = 3.09) — 
  pricing or service quality likely driving dissatisfaction
- **Two-year contracts reduce churn by 73%** vs month-to-month (OR = 0.27) — 
  lock-in strategies have measurable impact
- **Electronic check users show higher churn** — tech-savvy customers 
  with higher competitor awareness require proactive retention offers
- **PCA and K-Means converge on the same customer segments** — 
  two independent methods confirm the same underlying data structure

---

## Tech Stack

| Area | Tools |
|------|-------|
| Language | Python 3.x |
| Data manipulation | pandas, numpy |
| Machine Learning | scikit-learn |
| Visualization | matplotlib, seaborn |
| Environment | Jupyter Notebook, VS Code, venv |
| Version control | Git, GitHub |

---

## How to Run

```bash
git clone https://github.com/GiadaJennyQafalia/ml-portfolio-develhope.git
cd ml-portfolio-develhope
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

---

## Author

**Giada Jenny Qafalia**  
Data Science Student — Develhope (2025–2026)  
BSc Psychology — University of Trieste  

📍 Trieste, Italy · Open to Full Remote  
📩 [LinkedIn](https://www.linkedin.com/in/giada-jenny-qafalia-778417390) 
[GitHub](https://github.com/GiadaJennyQafalia)