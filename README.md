
# 🏦 Bank Loan Repayment Analysis

**Course:** DAMO-611-2 Data Analytics Case Study 3 (Spring 2025)  
**Instructor:** Omid Isfahanialamdari  
**Submitted by:**  
- Heta Chavda (NF1014555)  
- Yash Patel (NF1009944)  
- Devarsh Oza (NF1003776)  
- Joy Ajayi (NF1002698)  

---

## 📌 Project Overview  
Banks face increasing challenges with **loan defaults (non-performing loans)**, which affect profitability, compliance, and investor confidence.  
This project leverages **Logistic Regression** to predict loan repayment outcomes (“Fully Paid” vs. “Charged Off”) using borrower and loan-specific features.  

**Key Goals:**  
- Reduce **default risk** via predictive analytics.  
- Provide **actionable recommendations** for financial institutions.  
- Build a **transparent, interpretable model** suitable for deployment.  

---

## 🎯 Objectives  
- Classify loans as **“Fully Paid” or “Charged Off”** using borrower attributes.  
- Quantify the impact of key variables:  
  - Interest Rate  
  - Annual Income  
  - Debt-to-Income (DTI) ratio  
  - Employment Length  
- Support **business decision-making** with risk segmentation.  
- Provide a framework for **deployment & monitoring**:contentReference[oaicite:0]{index=0}:contentReference[oaicite:1]{index=1}.  

---

## 📂 Dataset & Preprocessing  

- **Source:** Internal lending dataset (`financial_loan.csv`)  
- **Rows:** ~37,138 loan applications  
- **Target Variable:** `loan_status` → Binarized into *Paid (0)* and *Charged Off (1)*  

### Preprocessing Steps  
- Removed missing records in critical fields.  
- Encoded `emp_length` → Numeric scale (0–10).  
- Scaled continuous variables (`int_rate`, `dti`, `income`).  
- Created binary classification target.  

---

## 🔎 Exploratory Data Analysis  

### Loan Status Distribution  
![Loan Status Distribution](images/loan_status_distribution.png)  
- **84%** fully repaid  
- **14%** charged off  
- **3%** current loans:contentReference[oaicite:2]{index=2}  

---

### Loan Status by Employment Length  
![Employment vs Loan Status]  
- Longer tenure (10+ years) = highest repayment likelihood.  
- Defaults remain consistent (~12–15%) across groups:contentReference[oaicite:3]{index=3}.  

---

### DTI vs Loan Status  
![DTI vs Loan Status]  
- Median DTI:  
  - **Charged Off:** ~14.5%  
  - **Fully Paid:** ~13%  
- Higher DTI correlates with repayment challenges:contentReference[oaicite:4]{index=4}.  

---

### Interest Rate vs Loan Status  
![Interest Rate vs Loan Status]  
- Higher interest rates → higher default probability.  
- Fully repaid loans cluster at lower interest brackets:contentReference[oaicite:5]{index=5}.  

---

## 🤖 Modeling Approach  

### Algorithm  
- **Logistic Regression** (chosen for interpretability & statistical rigor).  

### Workflow  
1. Train/Test Split: 80/20  
2. Class Imbalance: `class_weight='balanced'`  
3. Metrics: ROC-AUC, Precision, Recall, F1, Confusion Matrix:contentReference[oaicite:6]{index=6}  

---

## 📊 Model Performance  

- **ROC-AUC Score:** 0.9154 → Strong predictive performance:contentReference[oaicite:7]{index=7}  
- **Confusion Matrix Results:**  
  - TP = 3922  
  - TN = 768  
  - FP = 477  
  - FN = 2261  

### Interpretation  
- **Interest Rate (–16.45):** Strong negative driver (higher rates → higher defaults).  
- **DTI (–1.06):** Higher ratios → more defaults.  
- **Employment Length (–0.03):** Longer tenure slightly reduces default risk.  
- **Annual Income (+0.000003):** Minimal positive effect:contentReference[oaicite:8]{index=8}.  

---

## ✅ Business Impact  

- **Risk Mitigation:** Early identification of high-risk borrowers.  
- **Portfolio Optimization:** Shift focus toward safer borrowers.  
- **Automation:** Integration with digital workflows enables real-time credit scoring.  
- **Customer Targeting:** Personalized lending terms by borrower risk segment:contentReference[oaicite:9]{index=9}.  

---

## 📌 Recommendations  

1. **Deploy Model in Pre-Loan Screening**  
   - Integrate logistic regression scoring into loan origination platforms.  
   - Flag risky applicants with >70% default probability.  

2. **Retrain Quarterly**  
   - Capture market shifts and borrower behavior changes.  

3. **Expand Feature Set**  
   - Add credit bureau data, loan purpose, payment history.  

4. **Test Ensemble Models**  
   - Random Forest, Gradient Boosting (XGBoost) for higher accuracy.  

5. **Governance & Compliance**  
   - Ensure transparency, fairness checks, explainability (e.g., SHAP values).  
   - Align with **Basel III/IV & Fair Lending** regulations:contentReference[oaicite:10]{index=10}:contentReference[oaicite:11]{index=11}.  



## 📌 Conclusion  
The **Logistic Regression model** demonstrated strong predictive power with ROC-AUC of **0.91**, making it a reliable solution for **loan risk prediction**.  
With ongoing retraining, feature expansion, and compliance oversight, the model can:  
- Reduce defaults  
- Improve profitability  
- Strengthen trust with regulators and investors  

---

## 📚 References  
1. Chris Ekai (2023). *Credit Risk Assessment: A Comprehensive Guide for Lenders and Financial Institutions*. Risk Publishing.  
2. Atul K. Gupta (2024). *Credit Risk Predictive Modeling*.
---
