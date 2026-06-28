# 🍷 Wine Quality Prediction using Machine Learning

A machine learning project that predicts whether a wine is **Good** or **Bad** based on its physicochemical properties. This project was completed as part of my Machine Learning coursework and follows the complete ML workflow from data preprocessing to model optimization.

**🔗 GitHub Repository**

:contentReference[oaicite:0]{index=0}

---

# 📌 Project Overview

The Wine Quality dataset contains various chemical properties of red wine along with quality ratings ranging from **3 to 8**.

Instead of predicting multiple quality scores, I converted the problem into a **binary classification** task.

- Good Wine → Quality > 7
- Bad Wine → Quality ≤ 7

The objective was to compare different machine learning algorithms, identify the best-performing model, optimize it using GridSearchCV, and save the trained model for future predictions.

---

# 📂 Dataset Information

- Dataset: Wine Quality Dataset
- Number of Features: **11**
- Target Column: **quality**
- Records after removing duplicates: **1359**
- Missing Values: **0**
- Duplicate Records: Removed

### Features

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

---

# ⚙️ Project Workflow

## 1. Data Loading

- Imported required Python libraries
- Loaded dataset using Pandas
- Viewed dataset
- Checked dimensions
- Verified data types

---

## 2. Data Cleaning

Performed the following preprocessing steps:

- Checked missing values
- Removed duplicate records
- Generated descriptive statistics
- Checked feature correlations
- Created binary target variable
- Split dataset into training and testing sets
- Balanced the training data using **SMOTE**

---

## 3. Exploratory Data Analysis

The following visualizations were created during the analysis:

- Correlation Heatmap
- Class Distribution Plot
- Model Accuracy Comparison
- Model Performance Comparison
- ROC Curve
- Confusion Matrix
- Feature Importance Plot

---

# 🤖 Machine Learning Models

The following models were trained and evaluated.

### Logistic Regression

- StandardScaler applied
- Hyperparameter tuning using GridSearchCV

---

### K-Nearest Neighbors (KNN)

- Trained using scaled features
- Compared with other classifiers

---

### Decision Tree

- Trained using original features
- Used for model comparison

---

# 📊 Model Evaluation

Models were evaluated using multiple classification metrics instead of relying only on accuracy.

Evaluation Metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curve
- Confusion Matrix

After comparing all models, **Logistic Regression** achieved the best overall performance based on F1 Score and was selected as the final model.

---

# 🔍 Hyperparameter Tuning

GridSearchCV was applied to improve the Logistic Regression model.

### Parameters Tuned

- Regularization Strength (C)
- Solver
- Penalty

### Best Parameters

```text
C = 10
Penalty = L2
Solver = lbfgs
```

---

# 📈 Feature Importance

Feature importance was analyzed using the coefficients of the optimized Logistic Regression model.

The most influential features observed were:

- Chlorides
- Alcohol
- Total Sulfur Dioxide
- pH
- Citric Acid

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Joblib

---

# 📁 Project Structure

```
Wine-Quality-Prediction-using-Machine-Learning
│
├── winequality.csv
├── winequality.ipynb
├── wine_quality_model.pkl
├── scaler.pkl
├── README.md
└── requirements.txt
```

---

# 🚀 How to Run

### Clone the Repository

```bash
git clone https://github.com/Sanjayduduka45/Wine-Quality-Prediction-using-Machine-Learning.git
```

Move into the project directory

```bash
cd Wine-Quality-Prediction-using-Machine-Learning
```

Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn joblib
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
winequality.ipynb
```

and run all cells sequentially.

---

# 📚 What I Learned

Working on this project helped me understand the complete machine learning pipeline beyond simply training a model.

Some of the key concepts I practiced include:

- Data preprocessing
- Exploratory Data Analysis (EDA)
- Handling imbalanced datasets using SMOTE
- Feature scaling with StandardScaler
- Binary classification
- Comparing multiple machine learning models
- Hyperparameter tuning using GridSearchCV
- Model evaluation using Precision, Recall, F1 Score, ROC Curve and Confusion Matrix
- Saving trained models using Joblib

---

# 👨‍💻 Author

Sanjay Duduka

B.Tech Computer Science & Engineering

Machine Learning | Data Science | Python | SQL

GitHub: :contentReference[oaicite:1]{index=1}