# Diabetes Risk Prediction with Machine Learning

## Project Overview

This project demonstrates a complete machine learning workflow for predicting diabetes risk using patient-level clinical data.

The goal is to build interpretable predictive models and explore clinically meaningful features that contribute to diabetes risk.

The project includes:

- Exploratory Data Analysis (EDA)
- Clinically informed Feature Engineering
- Logistic Regression baseline model
- Random Forest model comparison
- Model evaluation using ROC-AUC
- Feature importance analysis
- Clinical risk stratification

---

## Dataset

This project uses the **Pima Indians Diabetes Dataset**, a widely used dataset for healthcare machine learning research.

The dataset contains clinical variables such as:

- Glucose level
- BMI
- Age
- Blood pressure
- Insulin level
- Diabetes pedigree function
- Pregnancy history

Target variable:
Outcome

Where:
1 = Diabetes
0 = No Diabetes

---

## Feature Engineering

To enhance model interpretability and incorporate clinical intuition, several engineered features were created:

| Feature | Description |
|------|------|
| is_elderly | Indicator for patients aged ≥60 |
| high_bmi | BMI ≥30 (obesity indicator) |
| high_glucose | Glucose ≥140 indicator |
| metabolic_risk | Combined metabolic stress score |
| pregnancy_age_interaction | Interaction between pregnancy count and age |

These features reflect known clinical risk factors for metabolic disease.

---

## Machine Learning Models

Two models were trained and compared.

### Logistic Regression

Used as a baseline interpretable model.

Evaluation metric:
ROC-AUC

Result:
ROC-AUC = 0.84

---

### Random Forest

A nonlinear ensemble model used for comparison.

Result:
ROC-AUC = 0.81

---

## Key Predictors

The most important predictors identified by the models include:

- Glucose
- Metabolic risk score
- BMI
- Diabetes pedigree function
- Age

These predictors are consistent with established clinical risk factors for diabetes.

---

## Model Evaluation

Performance was evaluated using:

- ROC-AUC
- Confusion Matrix
- Classification Report

Example ROC curve:
ROC-AUC ≈ 0.84

This indicates good discrimination between patients with and without diabetes.

---

## Clinical Risk Stratification

Predicted probabilities were used to stratify patients into risk groups:

| Risk Group | Predicted Probability |
|------|------|
| Low Risk | < 0.30 |
| Medium Risk | 0.30 – 0.60 |
| High Risk | > 0.60 |

Patients in the high-risk group showed substantially higher observed diabetes prevalence, suggesting the model may support clinical risk stratification.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Project Structure
diabetes-ml-project
│
├── diabetes_ml_project.ipynb
├── README.md

---

## Key Takeaways

This project demonstrates an end-to-end healthcare machine learning workflow:

- data exploration
- feature engineering based on clinical knowledge
- interpretable baseline modeling
- nonlinear model comparison
- model interpretation and risk stratification

The results highlight how clinically informed feature engineering can improve model interpretability and predictive performance in healthcare datasets.

---
