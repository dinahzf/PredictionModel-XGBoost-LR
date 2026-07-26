# Prediksi Penyakit Jantung Menggunakan Logistic Regression dan XGBoost

## Gambaran Umum Proyek
Penyakit jantung masih menjadi salah satu penyebab utama kematian di seluruh dunia, sehingga deteksi dini dan prediksi risiko menjadi sangat penting. Proyek ini menerapkan dan membandingkan dua algoritma machine learning terawasi (supervised), yaitu Logistic Regression dan XGBoost, untuk memprediksi apakah seseorang berisiko mengalami penyakit jantung berdasarkan sejumlah atribut klinis dan demografis. Proyek ini juga mencakup exploratory data analysis (EDA) secara menyeluruh untuk memahami indikator kesehatan mana yang paling berkaitan dengan penyakit jantung.

## Tujuan
- Menerapkan algoritma Logistic Regression dan XGBoost pada dataset penyakit jantung untuk memprediksi risiko penyakit.
- Membandingkan performa prediktif kedua algoritma menggunakan metrik evaluasi klasifikasi standar.
- Mengidentifikasi faktor risiko utama yang paling berkaitan dengan penyakit jantung berdasarkan hasil model dan analisis eksploratif.

## Sumber Data
- **Sumber:** UCI Machine Learning Repository (dataset Heart Disease)
- **Atribut:** 14 variabel, meliputi usia, jenis kelamin, tipe nyeri dada, tekanan darah istirahat, kadar kolesterol, gula darah puasa, hasil elektrokardiografi istirahat, detak jantung maksimum, gejala angina akibat olahraga, depresi segmen ST, kemiringan segmen ST, jumlah pembuluh darah utama, dan hasil tes thallium
- **Variabel target:** Ada (1) atau tidak adanya (0) penyakit jantung

## Metodologi
1. Pemuatan, pembersihan, dan validasi data terkait tipe atribut serta rentang nilai.
2. Exploratory Data Analysis (EDA) menggunakan violin plot dan mosaic plot untuk menelaah hubungan antara setiap variabel prediktor dan variabel target (misalnya usia, detak jantung maksimum, kolesterol, tekanan darah, tipe nyeri dada, gula darah puasa, hasil tes thallium, dan kemiringan segmen ST).
3. Pembangunan model menggunakan Logistic Regression sebagai model dasar (baseline) yang mudah diinterpretasikan.
4. Pembangunan model menggunakan XGBoost, dilanjutkan dengan hyperparameter tuning untuk mengoptimalkan performa.
5. Evaluasi model menggunakan confusion matrix, precision, recall, dan F1-score.

## Hasil Utama
- Logistic Regression mencapai F1-score sebesar 0,833, dengan recall yang cukup tinggi (0,91) dalam mendeteksi kasus positif penyakit jantung, namun recall yang relatif lebih rendah (0,68) untuk kasus negatif.
- XGBoost mencapai F1-score sebesar 0,837 sebelum tuning, meningkat menjadi **0,891 setelah hyperparameter tuning**, atau peningkatan performa sebesar 6,3%.
- Analisis eksploratif menemukan bahwa usia yang lebih tua, tekanan darah istirahat yang lebih tinggi, hasil reversible defect pada tes thallium, kemiringan segmen ST yang menurun (downsloping), serta kelainan gelombang ST-T pada elektrokardiografi berkaitan dengan risiko penyakit jantung yang lebih tinggi. Sebaliknya, beberapa indikator risiko yang umum diasumsikan (seperti gula darah puasa tinggi atau adanya gejala angina) tidak selalu menjadi prediktor yang konsisten pada dataset ini.

## Alat dan Teknologi
- Python (pandas, NumPy, matplotlib/seaborn untuk EDA, scikit-learn untuk Logistic Regression, library XGBoost)
- Jupyter Notebook

## Isi Repository
- `classification_dataset.csv` — dataset penyakit jantung (14 atribut)
- `Classification.ipynb` — alur kerja analisis lengkap, termasuk EDA, pelatihan model, dan evaluasi
- `README.md` — dokumentasi ini

## Kesimpulan
Proyek ini menunjukkan alur kerja klasifikasi terawasi secara menyeluruh, mulai dari validasi data dan analisis eksploratif hingga pembangunan model, tuning, dan evaluasi. Hasil menunjukkan bahwa XGBoost, setelah melalui hyperparameter tuning, memberikan performa yang lebih baik dibandingkan Logistic Regression dalam memprediksi risiko penyakit jantung, sementara analisis eksploratif memberikan insight yang berharga dan mudah diinterpretasikan mengenai faktor-faktor klinis yang paling berkaitan dengan kondisi tersebut.

---------------------------------------------------------------------------------

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
