# Heart Disease Risk Analysis

## Overview
This project focuses on analyzing key cardiovascular health indicators to predict the presence of heart disease using the UCI Heart Disease dataset. It combines exploratory data analysis (EDA), dimensionality reduction with PCA, and classification model building. Multiple machine learning models are tested to evaluate predictive performance and identify the most effective model.

## Dataset
The dataset consists of 303 patient records with 14 attributes, including:

- `age`: Age of the patient
- `sex`: Sex (1 = male, 0 = female)
- `cp`: Chest pain type (0–3)
- `trestbps`: Resting blood pressure
- `chol`: Serum cholesterol (mg/dl)
- `fbs`: Fasting blood sugar > 120 mg/dl
- `restecg`: Resting ECG results
- `thalach`: Maximum heart rate achieved
- `exang`: Exercise-induced angina
- `oldpeak`: ST depression induced by exercise
- `slope`: Slope of the ST segment
- `ca`: Number of major vessels colored by fluoroscopy
- `thal`: Thalassemia
- `target`: Presence of heart disease (1 = yes, 0 = no)

## Exploratory Data Analysis
- Countplots and boxplots were used to examine distributions and relationships with the target variable.
- Correlation heatmaps revealed strong and weak associations between features and heart disease.
- Violin and pair plots helped visualize feature separability.
- PCA was applied to visualize data clusters in 2D and 3D.

## Data Preprocessing
- Features were scaled using `MinMaxScaler`.
- The data was split into training and test sets (80:20).
- PCA was applied for visualization and dimensionality reduction.

## Models Used
The following classification models were trained and evaluated:
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Classifier (SVC)
- Decision Tree Classifier
- Random Forest Classifier

## Results
| Model                  | Accuracy | Precision | Recall | F1-score |
|------------------------|----------|-----------|--------|----------|
| Logistic Regression    | 0.82     | 0.83      | 0.84   | 0.83     |
| K-Nearest Neighbors    | 0.79     | 0.80      | 0.81   | 0.80     |
| Support Vector Machine | 0.81     | 0.81      | 0.82   | 0.81     |
| Decision Tree          | 0.77     | 0.77      | 0.78   | 0.77     |
| Random Forest          | 0.83     | 0.84      | 0.84   | 0.84     |

## Conclusion
Random Forest emerged as the best-performing model. PCA visualizations demonstrated clear cluster separations, and feature relationships were clearly established through EDA.

## Future Work
- Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
- Addressing potential class imbalance using techniques like SMOTE
- Model ensembling or stacking for improved accuracy
- Cross-validation for robust performance evaluation
