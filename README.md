# diabetes-prediction-ml-models

This project compares the performance of five supervised machine learning models to predict diabetes status using a real-world health dataset of over 250,000 individuals from the CDC's Behavioral Risk Factor Surveillance System (BRFSS). This was conducted as part of NYU's CS-UA 473: Fundamentals of Machine Learning.

---

## Models Compared
- **Logistic Regression** (AUC = 0.82)
- **Support Vector Machine (SVM)** (AUC = 0.81)
- **Single Decision Tree** (AUC improved to 0.81 after tuning)
- **Random Forest** (AUC = 0.81)
- **AdaBoost** (AUC = 0.82 — best overall performance)

---

## Key Methods
- **Preprocessing:** One-hot encoding (for non-ordinal features), standardization (for scale-sensitive models), and ordinal encoding (for ordered variables like income and education brackets)
- **Evaluation Metric:** ROC AUC was prioritized due to dataset imbalance
- **Feature Importance:** AUC drop test — the impact of removing each feature on overall performance

---

##  Results Summary
- **BMI** was consistently identified as the most important predictor of diabetes across all models.
- **GeneralHealth** (a self-reported, subjective variable) also played a significant supporting role and was found to reflect nonlinear combinations of objective factors like BMI and HighBP.
- **AdaBoost** provided the best balance of performance and interpretability, avoiding overfitting and highlighting interpretable features.

---

## Dataset
The dataset contains 250,000+ health records collected by the CDC. It includes features such as BMI, high blood pressure, smoking status, income, education, physical and mental health, and more. The target variable is diabetes diagnosis (binary: 0 = no, 1 = yes).


- `Diabetes_Predictor.ipynb` — Main Jupyter notebook with code
- `Diabetes_Predictor.pdf` — Full write-up and analysis
