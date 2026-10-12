# Heart Disease Prediction Using Logistic Regression and XGBoost

## Project Overview
Heart disease remains one of the leading causes of death worldwide, making early detection and risk prediction critically important. This project applies and compares two supervised machine learning algorithms, Logistic Regression and XGBoost, to predict whether an individual is at risk of heart disease based on a set of clinical and demographic attributes. The project also includes a thorough exploratory data analysis (EDA) to understand which health indicators are most strongly associated with heart disease.

## Objectives
- Implement Logistic Regression and XGBoost on the Heart Disease dataset to predict disease risk.
- Compare the predictive performance of both algorithms using standard classification metrics.
- Identify the key risk factors most strongly associated with heart disease based on model results and exploratory analysis.

## Dataset
- **Source:** UCI Machine Learning Repository (Heart Disease dataset)
- **Attributes:** 14 variables, including age, sex, chest pain type, resting blood pressure, cholesterol level, fasting blood sugar, resting electrocardiographic results, maximum heart rate, exercise-induced angina, ST depression, slope of the ST segment, number of major vessels, and thallium test results
- **Target variable:** Presence (1) or absence (0) of heart disease

## Methodology
1. Data loading, cleaning, and validation of attribute types and value ranges.
2. Exploratory Data Analysis (EDA) using violin plots and mosaic plots to examine the relationship between each predictor and the target variable (e.g., age, maximum heart rate, cholesterol, blood pressure, chest pain type, fasting blood sugar, thallium test result, ST segment slope).
3. Model building using Logistic Regression as a baseline, interpretable model.
4. Model building using XGBoost, followed by hyperparameter tuning to optimize performance.
5. Model evaluation using confusion matrices, precision, recall, and F1-score.

## Key Results
- Logistic Regression achieved an F1-score of 0.833, with strong recall (0.91) for detecting positive heart disease cases but relatively lower recall (0.68) for negative cases.
- XGBoost achieved an F1-score of 0.837 before tuning, improving to **0.891 after hyperparameter tuning**, a performance gain of 6.3%.
- Exploratory analysis found that older age, higher resting blood pressure, reversible defect on the thallium test, downsloping ST segment, and ST-T wave abnormality on ECG were associated with a higher likelihood of heart disease, while several commonly assumed risk indicators (such as high fasting blood sugar or presence of angina) were not always consistent predictors in this dataset.

## Tools and Technologies
- Python (pandas, NumPy, matplotlib/seaborn for EDA, scikit-learn for Logistic Regression, XGBoost library)
- Jupyter Notebook

## Repository Contents
- `classification_dataset.csv` — Heart Disease dataset (14 attributes)
- `Classification.ipynb` — full analysis workflow, including EDA, model training, and evaluation
- `README.md` — this documentation

## Conclusion
This project demonstrates a complete supervised classification workflow, from data validation and exploratory analysis to model building, tuning, and evaluation. The results show that XGBoost, after hyperparameter tuning, outperforms Logistic Regression in predicting heart disease risk, while the exploratory analysis provides valuable, interpretable insight into the clinical factors most associated with the condition.
