# Cirrhosis Stage Prediction: Healthcare ML Project

![Python](https://img.shields.io/badge/language-Python-blue)
![Jupyter Notebook](https://img.shields.io/badge/output-Jupyter%20Notebook-orange)

## Overview
This repository contains a machine learning project for predicting **stages of cirrhosis** using patient clinical data.  
The project is developed as a **final project for the Machine Learning course**.  

Dataset contains 418 patient records with 18 columns. After removing irrelevant or highly incomplete features (e.g., ID, Registration Date, Birth Date, Cholesterol), the dataset is cleaned and ready for model training.  

---

## Repository Structure

- `1A.tsv` → raw dataset for cirrhosis stage prediction
- `Cirrhosis_Stage_Prediction.ipynb` → main notebook containing EDA, preprocessing, model training, evaluation, and feature importance analysis

---

## Methodology
1. **Data Preprocessing**
   - Dropped irrelevant columns
   - Handled missing values (median for numerical, mode for categorical)
   - Encoded categorical variables (LabelEncoder & OneHotEncoder)
2. **Model Training**
   - Random Forest and XGBoost models were trained
   - Hyperparameters tuned via GridSearchCV
3. **Evaluation**
   - Performance assessed using precision, recall, and F1-score
   - XGBoost slightly outperformed Random Forest on minority classes
4. **Feature Importance**
   - Key predictors identified: Ascites, Hepatomegaly, Prothrombin, Bilirubin, Albumin, Platelets, Triglycerides

---

## Key Insights

- XGBoost performs slightly better than Random Forest, particularly for Stage 3 and Stage 4, but both models struggle to correctly classify Stage 1 and Stage 2.
- Overall model performance is limited due to class imbalance and a relatively small dataset. Weighted precision, recall, and F1-scores remain modest.
- Preprocessing and encoding steps ensure that the input data is clean and structured, supporting the model’s predictions.
- Feature importance analysis identifies **Ascites**, **Hepatomegaly**, and **Prothrombin** as the top predictors for cirrhosis stage.
- While the pipeline provides a clear workflow, the current predictions **should not be considered fully reliable for clinical decision-making**, and there is room for improvement with additional data, better handling of class imbalance, and alternative modeling strategies.

---

## Presentation Video
[Cirhosis Prediction Analysis – Video Presentation](https://your-onedrive-link-here)

---

## References
- Python libraries: pandas, scikit-learn, XGBoost, matplotlib, seaborn

---

## Author

Syalista Galuh Nadira
