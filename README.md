# Diabetes Prediction Model

## Purpose
Develop a machine learning model to predict diabetes based on patient demographics and symptoms for early diagnosis and treatment planning.

## Project Overview
This repository contains a comprehensive analysis and model development pipeline for diabetes prediction. It covers exploratory data analysis (EDA), data preprocessing, hyperparameter tuning with `RandomizedSearchCV`, and model deployment using a Flask API.

## Dataset Overview
- **Total Samples:** 520 patients
- **Features:** 17 columns
- **Numerical:** Age (range: 16–90 years; mean ~48, std ~12, IQR = 18)
- **Categorical:** Gender, Polyuria, Polydipsia, sudden weight loss, weakness, Polyphagia, Genital thrush, visual blurring, Itching, Irritability, delayed healing, partial paresis, muscle stiffness, Alopecia, Obesity
- **Target Variable:** `class` (diabetes diagnosis)

## Key Analyses Performed

### Exploratory Data Analysis (EDA)
- **Univariate Analysis:** Distribution and summary statistics of Age.
- **Bivariate Analysis:** Examination of correlations, e.g. strong positive correlation between Polyuria and Polydipsia.
- **Observations:** Majority of patients fall between 30–60 years, with symmetric distribution; a few outliers exist in the older age group.

### Data Preprocessing
- **Categorical Encoding:** Conversion of categorical features using One-Hot or Label Encoding.
- **Data Cleaning:** Verifying and handling any missing values or anomalies.

### Predictive Modeling
- **Model Selection:** RandomForestClassifier is chosen for its robustness and ability to handle non-linear interactions.
- **Hyperparameter Tuning:** Utilizing `RandomizedSearchCV` (20 iterations over 3-fold cross-validation, totalling 60 fits) to find optimal parameters.
- **Evaluation Metrics:** Accuracy, precision, recall, f1-score, and confusion matrix.
- **Performance:** Initial experiments yielded an accuracy of ~97%.

### Model Deployment
- **Flask API:** A lightweight API is created in `app.py` to serve real-time predictions.
- **Usage:** The API accepts JSON input and returns the predicted class.



