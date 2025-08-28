# Fraud Detection using Machine Learning  

This repository contains my Accredian Assessment Project on **Fraud Detection in Online Transactions**.  
The goal is to build an intelligent fraud detection system that not only identifies suspicious transactions but also provides meaningful insights for businesses to strengthen fraud prevention strategies.  

---

## 🚀 Project Workflow  

1. **Data Cleaning & Preprocessing**  
   - Removed duplicates & missing values  
   - Outlier detection using boxplots and log-transform on skewed features  
   - Multi-collinearity check using correlation heatmap + VIF  

2. **Class Imbalance Handling**  
   - Used **SMOTE** and undersampling to balance fraud vs. non-fraud classes  

3. **Modeling**  
   - Built and compared multiple models:  
     - Logistic Regression  
     - Random Forest  
     - XGBoost  
     - LightGBM  
   - Performed **hyperparameter tuning** with `RandomizedSearchCV`  

4. **Evaluation Metrics**  
   - Precision, Recall, F1-score  
   - ROC-AUC, PR-AUC  
   - Classification reports and comparison heatmaps  

5. **Model Explainability**  
   - SHAP summary plots  
   - Feature importance plots (XGBoost & LightGBM)  

6. **Key Insights**  
   - High transaction amounts are strongly linked to fraud  
   - Fraud concentrated in **CASH_OUT** and **TRANSFER** transactions  
   - Fraudulent accounts often start with zero balance or show sudden spikes in activity  
   - Sequence pattern: **TRANSFER → CASH_OUT** is highly suspicious  

7. **Business Takeaways**  
   - Enable real-time alerts for large risky transactions  
   - Profile customer transaction behavior to detect anomalies  
   - Monitor destination accounts receiving sudden large inflows  
   - Apply stronger authentication (OTP/2FA) for high-value transfers  
   - Merchant accounts need tighter fraud monitoring  

---

## 📊 Results  
- **XGBoost** and **LightGBM** achieved the best balance of fraud detection (high recall) and low false positives.  
- Transaction **amount, balances, and type** emerged as the most important fraud indicators.  

---

## 🔑 Tech Stack  
- Python, Pandas, NumPy, Seaborn, Matplotlib  
- Scikit-learn, imbalanced-learn  
- XGBoost, LightGBM  
- SHAP for interpretability  

