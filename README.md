# Lung Cancer Prediction Project

## Overview

This project aims to predict lung cancer diagnosis based on various patient characteristics using machine learning models. The dataset contains 3000 rows and 16 columns, each representing an individual patient's medical and demographic information.

## Dataset Description

The dataset consists of the following features:
- **Age**: The age of the patient in years.
- **Gender**: The gender of the patient (e.g., Male, Female).
- **Smoking Status**: Indicates whether the patient is a current smoker, former smoker, or has never smoked.
- **Family History of Cancer**: Indicates whether there is a family history of cancer.
- **Chronic Diseases**: Information about any chronic diseases the patient may have.
- **Exposure to Environmental Pollutants**: Data on the patient's exposure to environmental pollutants.
- **Occupational Hazards**: Information about occupational exposure to hazardous substances.
- **Medical Imaging Results**: Results from relevant medical imaging tests.
- **Previous Medical Conditions**: Any previous medical conditions that might be relevant.
- **Clinical Symptoms**: Symptoms reported by the patient.
- **Laboratory Test Results**: Results from various laboratory tests.
- **Genetic Factors**: Information on any known genetic predispositions.
- **Lifestyle Factors**: Lifestyle habits such as diet, physical activity, etc.
- **Biomarkers**: Presence and levels of specific biomarkers associated with lung cancer.
- **Treatment History**: Any previous treatments or interventions the patient has undergone.
- **Lung Cancer Diagnosis**: Indicates whether the patient has been diagnosed with lung cancer (Yes/No).

## Libraries Used

- **Pandas**: For data manipulation and analysis.
- **Numpy**: For numerical computations.
- **Matplotlib**: For creating static, animated, and interactive visualizations.
- **Seaborn**: For statistical data visualization.
- **TensorFlow & Keras**: For building and training deep learning models.
- **Scikit-learn**: For machine learning algorithms and utilities.

## Data Distribution and Patterns

- The gender distribution is balanced with a 50-50 split between males and females.
- The ages of the patients range from 30 to 80, with 21% of the patients falling in the 30-39 age group.
- The distribution of positive lung cancer cases among genders is nearly balanced, close to a 50-50 split.
- A higher percentage of patients aged 30-39 tested positive for lung cancer compared to other age groups.

## Models and Results

### Decision Tree Classifier

After ensuring the independent variables were not correlated, I scaled the age data and encoded gender as 0 and 1. The initial Decision Tree classifier showed overfitting with the training data and produced moderate performance with an F1-Score of 0.52.

Hyperparameter tuning slightly improved the performance, yielding an F1-Score of 0.53.

### Random Forest

The initial Random Forest model also overfitted and provided a normal prediction result with an F1-Score of 0.53.

After hyperparameter tuning, the performance improved with an F1-Score of 0.56.

### Deep Learning Models

Exploring deep learning models using `SimpleImputer` from Scikit-Learn, I tested different configurations with multiple parameters, `EarlyStopping`, `Dask`, and `SMOTE` for synthetic observations. The best results were achieved using `DropOut` and `RandomSearch` from Keras-Tuner for hyperparameter optimization. The final model achieved an F1-Score of 0.60.

## Conclusion

The deep learning model with 6 layers achieved an F1-Score of 0.60. With a larger dataset, performance could improve further. Feedback and constructive criticism are welcome.

## Contact

Sergio Lezama - info@sergiolezama.com
