<div align="center">

![Banner](banner.svg)

# ðŸ¦ Bank Loan Repayment Analysis
### Predicting Loan Defaults with Machine Learning to Reduce Lending Risk

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)

![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)
![Model](https://img.shields.io/badge/Model-Logistic%20Regression-blue?style=flat-square)
![ROC--AUC](https://img.shields.io/badge/ROC--AUC-0.915-brightgreen?style=flat-square)
![Records](https://img.shields.io/badge/Dataset-37K%20Loans-orange?style=flat-square)

</div>

---

## ðŸ“Œ Project at a Glance

| | |
|---|---|
| **ðŸŽ¯ Goal** | Predict whether a borrower will **repay** or **default** on a loan |
| **ðŸ§  Model** | Logistic Regression (balanced class weights) |
| **ðŸ“Š Dataset** | 37,138 real loan applications |
| **ðŸ† Result** | **ROC-AUC of 0.915** â€” strong predictive power |
| **ðŸ’¡ Impact** | Enables lenders to flag high-risk borrowers *before* approval |

---

## ðŸ§© Business Problem

Every loan a bank approves carries risk: some borrowers repay in full, others **default (charge off)** â€” and each default is a direct financial loss.

The core business question:

> **Can we predict, at the point of application, which borrowers are likely to default â€” so the bank can price risk correctly and reduce losses?**

An accurate model lets lending teams **approve good borrowers faster** and **flag risky ones for review**, protecting the loan portfolio without turning away profitable customers.

---

## ðŸ—‚ï¸ Dataset

| Attribute | Detail |
|---|---|
| **Source** | `financial_loan.csv` (internal lending dataset) |
| **Size** | **37,138** loan applications |
| **Target** | `loan_status` â†’ *Fully Paid* vs. *Charged Off* |
| **Class Balance** | 84% repaid Â· 14% charged off Â· 3% current |

**Key features analyzed:**
- ðŸ’° Interest Rate
- ðŸ¢ Annual Income
- âš–ï¸ Debt-to-Income (DTI) Ratio
- ðŸ“… Employment Length (encoded 0â€“10)

> âš ï¸ **Challenge:** The dataset is *imbalanced* â€” far more repaid loans than defaults. This was handled with **balanced class weights** so the model doesn't ignore the minority (default) class.

---

## ðŸ”¬ Methodology

```
1. Data Cleaning      â†’  Handle missing values, remove noise
2. Feature Encoding   â†’  Convert categorical fields to numeric
3. Feature Scaling    â†’  Standardize continuous variables
4. Train/Test Split   â†’  80% training Â· 20% testing
5. Model Training     â†’  Logistic Regression (class_weight='balanced')
6. Evaluation         â†’  ROC-AUC, Confusion Matrix, Coefficients
```

**Why Logistic Regression?** It's interpretable â€” the bank can see *exactly which factors* drive default risk, which matters for regulatory and lending decisions.

---

## ðŸ“Š Model Performance Dashboard

<div align="center">

![Dashboard](dashboard.svg)

*ROC curve, confusion matrix, feature influence, and loan-outcome distribution â€” all from the model's actual results.*

</div>

---

## ðŸ“ˆ Key Insights

### Model Performance
| Metric | Score |
|---|---|
| **ROC-AUC** | **0.9154** âœ… |
| True Positives | 3,922 |
| True Negatives | 768 |
| False Positives | 477 |
| False Negatives | 2,261 |

### What Drives Default? ðŸ”
- ðŸ”´ **Interest Rate** â€” the *strongest* signal. Higher rates strongly correlate with defaults.
- ðŸŸ  **DTI Ratio** â€” higher debt burden â†’ higher default likelihood.
- ðŸŸ¡ **Employment Length** â€” instability increases risk.
- ðŸŸ¢ **Annual Income** â€” only a mild protective effect.

> **Takeaway:** A borrower's *interest rate and debt load* predict default far better than income alone.

---

## ðŸ’¼ Business Impact

| Benefit | How the Model Delivers |
|---|---|
| **ðŸ“‰ Lower Losses** | Flags high-risk loans before approval, cutting charge-offs |
| **âš¡ Faster Decisions** | Automates initial risk scoring for loan officers |
| **ðŸŽ¯ Smarter Pricing** | Aligns interest rates with true borrower risk |
| **ðŸ“‹ Explainable** | Transparent coefficients support audit & compliance |

With **91.5% discriminative accuracy**, this model gives lending teams a data-driven safety net that scales across thousands of applications.

---

## ðŸ› ï¸ Technologies Used

| Category | Tools |
|---|---|
| **Language** | Python |
| **ML** | scikit-learn (Logistic Regression) |
| **Data** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Jupyter Notebook |

---

## ðŸ“ Repository Contents

```
Bank-Loan-Repayment-Analysis/
â”œâ”€â”€ ðŸ“„ Final Report.docx          # Full written analysis
â”œâ”€â”€ ðŸ“Š Final Presentation.pdf     # Stakeholder slide deck
â”œâ”€â”€ ðŸ“ˆ financial_loan.csv         # Primary dataset
â”œâ”€â”€ ðŸ“ˆ supplier datasets (2)      # Supporting data
â””â”€â”€ ðŸ“ README.md                  # You are here
```

---

<div align="center">

### ðŸ‘©â€ðŸ’» Author

**Heta Chavda** â€” Data Analytics | Machine Learning | Business Intelligence

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hetachavda)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/hetachavda)

â­ *If you found this project insightful, consider giving it a star!*

</div>

