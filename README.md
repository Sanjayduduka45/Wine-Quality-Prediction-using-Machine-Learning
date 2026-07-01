# 🍷 Wine Quality Prediction using Machine Learning

Predicting whether a wine is **Good** or **Bad** using physicochemical properties and classical Machine Learning algorithms.

---

## Project Overview

This project builds a binary classification model to predict wine quality using laboratory measurements. The original **quality** score was transformed into a binary target:

- **Good (1)** → Quality ≥ 7
- **Bad (0)** → Quality < 7

The project follows a complete machine learning workflow, including exploratory data analysis, preprocessing, model comparison, hyperparameter tuning, feature importance analysis, and model persistence.

---

## Repository

**GitHub Repository**

:contentReference[oaicite:0]{index=0}

---

## Problem Statement

Wine quality is generally determined through sensory evaluation performed by experts, making the process subjective and time-consuming.

The objective of this project is to develop a machine learning model that predicts wine quality directly from measurable chemical properties, enabling faster and more consistent quality assessment.

---

## Dataset Information

The dataset contains **11 physicochemical features** collected from red wine samples.

### Input Features

- Fixed Acidity
- Volatile Acidity
- Citric Acid
- Residual Sugar
- Chlorides
- Free Sulfur Dioxide
- Total Sulfur Dioxide
- Density
- pH
- Sulphates
- Alcohol

### Target Variable

Original Target

```
quality
```

Binary Target

```
quality_label

0 → Bad Wine
1 → Good Wine
```

---

## Machine Learning Workflow

- Dataset Loading
- Exploratory Data Analysis
- Missing Value Analysis
- Duplicate Record Removal
- Correlation Analysis
- Binary Target Creation
- Feature & Target Separation
- Train-Test Split
- Feature Scaling using StandardScaler
- Model Training
- Model Comparison
- Hyperparameter Tuning using GridSearchCV
- Model Evaluation
- Learning Curve Analysis
- Permutation Feature Importance
- Model Serialization

---

## Data Preprocessing

The following preprocessing steps were performed:

- Removed duplicate records
- Created binary target labels
- Stratified train-test split
- Standardized numerical features using StandardScaler
- Compared models on identical train-test partitions

---

## Models Evaluated

Three supervised machine learning algorithms were trained and compared.

| Model | Purpose |
|-------|----------|
| Logistic Regression | Baseline linear classifier |
| K-Nearest Neighbors (KNN) | Distance-based classification |
| Decision Tree | Rule-based classification |

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## Hyperparameter Tuning

The highest-performing baseline model (**K-Nearest Neighbors**) was optimized using **GridSearchCV**.

Parameters tuned include:

- Number of Neighbors
- Weight Strategy
- Distance Metric
- Minkowski Distance Parameter (p)

---

## Model Evaluation

The optimized model was evaluated using:

- Classification Report
- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1-Score
- Learning Curve

Learning curve analysis was additionally used to study the model's generalization behaviour after hyperparameter tuning.

---

## Feature Importance

Since K-Nearest Neighbors does not provide native feature importance scores, **Permutation Importance** was used to estimate the contribution of each feature.

The analysis identified the following features as having the strongest influence on prediction:

- Alcohol
- Sulphates
- Volatile Acidity
- Total Sulfur Dioxide
- Residual Sugar

---

## Project Structure

```
Wine-Quality-Prediction-using-Machine-Learning
│
├── Wine_Quality_Pred.ipynb
├── winequality.csv
├── wine_quality_model.pkl
├── scaler.pkl
├── README.md
└── requirements.txt
```

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

---

## Key Outcomes

- Converted the original quality scores into a binary classification problem.
- Compared three classical machine learning algorithms.
- Optimized the best-performing model using GridSearchCV.
- Evaluated model performance using multiple classification metrics.
- Analysed feature influence using permutation importance.
- Saved the trained model and preprocessing scaler for deployment or future inference.

---

## Future Improvements

- Evaluate ensemble models such as Random Forest, Gradient Boosting, and XGBoost.
- Improve minority-class prediction using advanced resampling techniques.
- Build a Streamlit web application for real-time wine quality prediction.
- Extend the solution to predict the original multi-class wine quality score.

---

## Author

**Sanjay Duduka**

Machine Learning • Data Science • Python • Scikit-learn

GitHub: :contentReference[oaicite:1]{index=1}