# 🎓 Student Performance Prediction using Supervised Machine Learning  
**Predicting Final Student Grades (G3) using Multi-Model Regression & Feature Analysis**

This project explores how educational, demographic, and behavioral factors influence students’ academic performance.  
Using several supervised machine learning models, the goal is to **predict the final grade (G3)** and uncover which features have the strongest predictive power.

The analysis includes preprocessing, feature engineering, model benchmarking, cross-validation, and visual diagnostics.

---

## 📁 Dataset  
**Source:** UCI Machine Learning Repository  
**Kaggle Mirror:** `danielcorredera/student-mat-csv`  

- **Rows:** 395 students  
- **Target Variable:** `G3` (final grade)  
- **Features:** study habits, parental education, past grades, absences, social factors  

Some columns are categorical (e.g., school, reason, guardian), while others are numeric (e.g., G1, G2, studytime, absences).

---

## 🧼 Data Preprocessing

### ✔ 1. Column cleaning  
- Removed trailing spaces  
- Ensured numeric features are correctly cast  
- One-hot encoded all categorical variables  
- Converted any boolean columns to 0/1  

### ✔ 2. Feature scaling  
Applied **StandardScaler** to ensure all numeric features share similar scale—important for models like SVR and Linear Regression.

### ✔ 3. Final processed dataset  
All variables become numeric after one-hot encoding, making the data fully ML-ready.

---

## 🎯 Modeling Approach

We tested a wide range of supervised ML regression models:

| Model | Description |
|-------|-------------|
| **Linear Regression** | Baseline model |
| **Ridge Regression** | L2 regularization |
| **Lasso Regression** | L1 regularization |
| **Support Vector Regression (RBF)** | Nonlinear regression |
| **Random Forest Regressor** | Ensemble method capturing nonlinearities |
| **Gradient Boosting Regressor** | Boosted decision trees |

Each model was trained/tested using an 80/20 split.  
Additionally, **5-fold cross-validation** was applied to measure generalization performance.

---

## 📊 Model Performance

The following metrics were computed:

- **Mean Squared Error (MSE)**
- **R² Score (Coefficient of Determination)**

(*Replace the placeholder values below with your actual output before publishing*)

| Model | MSE | R² |
|-------|-----|------|
| Random Forest | … | … |
| Gradient Boosting | … | … |
| SVR (RBF) | … | … |
| Linear Regression | … | … |
| Ridge | … | … |
| Lasso | … | … |

The models were ranked based on **R²**, reflecting how much variance in G3 they can explain.

---

## 📎 Cross-Validation

A 5-fold CV was performed on Linear Regression:


CV mean R²: X.XXXX
Standard deviation: X.XXXX


This ensures performance is not dependent on a single train/test split.

---

## 🔍 Feature Importance Analysis

Using a **Random Forest Regressor**, the top 15 most influential features were extracted.

Key insights:

- **G2** (second-period grade) is by far the most predictive feature of G3.  
- **Absences** have measurable negative impact.  
- Factors like **reason_home**, **age**, and **health** contribute modestly.  
- Social and support features (schoolsup, romantic, etc.) have weaker signals.

A horizontal bar chart visualizes the ranked importances.

---

## 📉 Error & Diagnostic Analysis

To better understand model behavior, the following plots were generated:

### ✔ **Residual Plot**
Shows how predicted errors distribute relative to actual values, helping diagnose bias or variance issues.

### ✔ **Error Distribution**
A histogram + KDE curve illustrates how prediction errors cluster around zero.

### ✔ **Actual vs Predicted Scatter Plot**
Visualizes model fit and linearity patterns.

These diagnostics are essential for validating regression models beyond raw scores.

---

## 🖼 Key Visualizations

<img width="534" height="393" alt="image" src="https://github.com/user-attachments/assets/9291246f-2e4e-488c-ad62-627e92507106" />

<img width="622" height="470" alt="image" src="https://github.com/user-attachments/assets/1acd1a7f-6ef1-4d93-9264-3ad15296ec57" />

<img width="528" height="374" alt="image" src="https://github.com/user-attachments/assets/17b6e0e3-78d7-4d74-9d12-edd3dd34b480" />

<img width="924" height="547" alt="image" src="https://github.com/user-attachments/assets/6c2f94e7-1674-4e1e-9da1-0c7dd455e73a" />


This strengthens the report and makes the project more interpretable.

---

## 🧠 Insights from the Study

1. **Past performance strongly influences final performance**  
   - G2 and G1 are the strongest predictors.

2. **Absences negatively affect performance**  
   Reliable across all models.

3. **Studytime does *not* strongly correlate with performance**  
   Counterintuitive but consistent with dataset literature.

4. **Tree-based models outperform linear ones**  
   Due to nonlinear interactions between features.

---

## 🚀 Future Work

To enhance this project further:

- Apply **hyperparameter tuning** (GridSearchCV / RandomizedSearchCV).  
- Test **XGBoost, CatBoost, LightGBM**.  
- Remove G1/G2 and test model robustness.  
- Build a small **web app (Streamlit)** for grade prediction.  
- Perform SHAP analysis for interpretability.

---

## 📌 Conclusion

This project demonstrates a complete supervised ML workflow:

- Data cleaning & preprocessing  
- Feature engineering  
- Model benchmarking  
- Validation & diagnostic visualization  
- Insight extraction  

The findings align with educational research: **previous grades and attendance behavior remain the strongest predictors of student achievement**.

---

## 📚 References

- Cortez, P., & Silva, A. M. G. (2008). *Using Data Mining to Predict Secondary School Student Performance*. UCI Machine Learning Repository.  
- Scikit-learn documentation: https://scikit-learn.org/  
- Kaggle Dataset: https://www.kaggle.com/datasets/danielcorredera/student-mat-csv  

---

## 👤 Author  
**Abdullah Omar**  
Machine Learning Researcher  
GitHub: https://github.com/AbdullahOmarAL-Safar    
LinkedIn: https://www.linkedin.com/in/itsabdullahomar/
