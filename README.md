# Machine Learning and Predictive Analytics in Insurance Pricing  
*Balancing Accuracy and Risk in Premium Predictions*  

**Course Project:** DBA3803 – Predictive Analytics in Business  
**Institution:** National University of Singapore (Exchange Semester)  
**Authors:** Group 19 (incl. Michaïl Maréchal)  
**Date:** November 2023
**Achievement:** Awarded *Highest Mark in Class*  

---

## 📌 Project Overview  
This project, which received the *highest mark in class*, applies **machine learning techniques** to predict **health insurance charges**, focusing on the business challenge of **limiting underestimation** of premiums. Underestimating risky individuals can expose insurers to significant financial losses, while overpricing risks losing clients to competitors.  

Using a structured dataset of 1,338 insurance policyholders with demographic, lifestyle, and regional variables, we built predictive models designed to achieve a balance between **accuracy, interpretability, and business applicability**.  

---

## ⚙️ Methodology  
- **Dataset:** 1,338 observations with 7 features (age, sex, BMI, children, smoker, region, charges).  
- **Models Implemented:**  
  - Linear: Lasso, Ridge, Quantile Regression  
  - Tree-based: Random Forest, Extra Trees, Gradient Boosting  
- **Loss Functions:**  
  - L2 loss (linear and tree-based models) with 102% adjustment to penalise underestimation  
  - Pinball loss (τ = 0.75) for Gradient Boosting and Quantile Regression  
- **Interpretability:** Local Interpretable Model-Agnostic Explanations (**LIME**) used to analyze variable-level impact for individual cases.  

---

## 📊 Key Findings  
- **Smoker status** was the most influential predictor across all models, followed by **age, BMI, and number of children**.  
- **Gradient Boosting** delivered the best performance on **Pinball loss**, making it ideal for aggregate underestimation control.  
- **Random Forest** excelled in **worst-case analysis**, making it better suited for turbulent conditions with high-risk individuals.  
- **Quantile Regression** consistently underperformed, confirming the non-linear nature of the dataset.  
- Recommendation:  
  - Use **Gradient Boosting** in stable markets.  
  - Use **Random Forest** in turbulent environments to better capture tail risks.  

---

## 🛠 Tech Stack  
- **Languages & Libraries:** Python, scikit-learn, pandas, NumPy, LIME, matplotlib  
- **Techniques:** Hyperparameter tuning (random search grid), asymmetric loss adjustments, interpretability with LIME  

---

## 📈 Results Visualization  
- Radar charts comparing model performance across multiple error metrics  
- LIME interpretability plots for selected individuals  
- Error distribution analysis (validation vs. test set)  

---

## 📜 Citation  
If referencing this work, please cite as:  

*Michaïl Maréchal et al. (2023). Machine Learning and Predictive Analytics in the Context of Insurance Pricing. DBA3803 Predictive Analytics in Business, National University of Singapore (Exchange Semester).*  
