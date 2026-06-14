# Task 3: Heart Disease Prediction

## Objective
Build a model to predict whether a person is at risk of heart disease based on their health data using binary classification techniques.

---

## Dataset

- **Name:** Heart Disease UCI Dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/ronitf/heart-disease-uci)
- **Size:** 303 rows × 14 columns
- **Target:** 1 = Heart Disease, 0 = No Heart Disease

### Features

| Feature | Description |
|---------|-------------|
| age | Age of patient |
| sex | Gender (1=male, 0=female) |
| cp | Chest pain type (0-3) |
| trestbps | Resting blood pressure |
| chol | Cholesterol level |
| fbs | Fasting blood sugar |
| restecg | Resting ECG results |
| thalach | Maximum heart rate achieved |
| exang | Exercise induced angina |
| oldpeak | ST depression |
| slope | Slope of peak exercise |
| ca | Number of vessels colored |
| thal | Thalassemia type |
| target | 1=Heart disease, 0=No heart disease |

---

## Libraries Used

```
pandas
numpy
matplotlib
seaborn
scikit-learn
```

Install with:
```bash
pip install -r requirements.txt
```

---

## Steps Performed

### 1. Data Loading
- Loaded Heart Disease UCI dataset using pandas
- Inspected shape, column names, and first few rows

### 2. Data Cleaning
- Checked for missing values (none found)
- Verified data types for all columns
- Analyzed class distribution of target variable

### 3. Exploratory Data Analysis (EDA)
| Visualization | Purpose |
|---------------|---------|
| Count Plot | Shows class distribution of heart disease |
| Correlation Heatmap | Reveals relationships between all features |
| Box Plot | Compares age distribution across disease classes |

### 4. Feature Engineering
- Separated features (X) and target (y)
- Applied StandardScaler to normalize all features
- Split into 80% training and 20% testing sets

### 5. Model Training
Two classification models trained and compared:

| Model | Description |
|-------|-------------|
| Logistic Regression | Linear classifier, fast and interpretable |
| Decision Tree | Non-linear classifier, captures complex patterns |

### 6. Evaluation Metrics

| Metric | Description |
|--------|-------------|
| Accuracy | Overall correct predictions percentage |
| Confusion Matrix | Shows true/false positives and negatives |
| ROC Curve | Plots true positive rate vs false positive rate |
| AUC Score | Area under ROC curve (closer to 1.0 = better) |

### 7. Feature Importance
- Used Decision Tree's built-in feature importance
- Identified which health features most affect heart disease prediction

---

## Key Findings

- Logistic Regression achieved higher accuracy than Decision Tree
- Most important features: chest pain type (cp), maximum heart rate (thalach), number of vessels (ca)
- ROC-AUC score above 0.85 indicates strong model performance
- Age alone is not the strongest predictor — chest pain type matters more
- No missing values found — dataset is clean and ready for modeling

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/elleenfatima05/AI_ML_Internship.git
```

2. Navigate to this task
```bash
cd AI_ML_Internship/Task3
```

3. Download the dataset from Kaggle and place `heart.csv` in this folder

4. Install dependencies
```bash
pip install -r requirements.txt
```

5. Open the notebook in VS Code and run all cells
```
task3_heart_disease.ipynb
```

---

## Skills Demonstrated

- Binary classification using scikit-learn
- Medical data understanding and interpretation
- Model evaluation using ROC-AUC and confusion matrix
- Feature importance analysis
- Data preprocessing and feature scaling
