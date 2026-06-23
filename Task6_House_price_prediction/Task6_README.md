# Task 6: House Price Prediction

## Objective
Predict house sale prices using property features such as size, number of bedrooms, and overall quality through regression modeling.

---

## Dataset

- **Name:** House Prices — Advanced Regression Techniques
- **Source:** [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
- **File Used:** train.csv
- **Target:** SalePrice

### Selected Features

| Feature | Description |
|---------|-------------|
| GrLivArea | Above ground living area (sq ft) |
| BedroomAbvGr | Number of bedrooms above ground |
| FullBath | Number of full bathrooms |
| YearBuilt | Year the house was built |
| OverallQual | Overall material and finish quality (1-10) |
| GarageCars | Garage capacity in cars |
| TotalBsmtSF | Total basement area (sq ft) |

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
- Loaded `train.csv` using pandas
- Inspected key columns including LotArea, BedroomAbvGr, Neighborhood, and SalePrice

### 2. Data Preprocessing
- Selected 7 key numerical features most relevant to price prediction
- Filled missing values using median imputation
- Verified no missing values remained after cleaning

### 3. Exploratory Data Analysis (EDA)
| Visualization | Purpose |
|---------------|---------|
| Histogram | Shows distribution of house sale prices |
| Scatter Plot | Living area vs sale price relationship |
| Correlation Heatmap | Reveals relationships between all selected features |

### 4. Model Training
- Split data into 80% training and 20% testing sets
- Trained a **Gradient Boosting Regressor** with 200 estimators, learning rate 0.1, max depth 4

### 5. Model Evaluation

| Metric | Description |
|--------|-------------|
| MAE | Mean Absolute Error in USD |
| RMSE | Root Mean Squared Error in USD |
| R² Score | Proportion of variance explained (closer to 1.0 = better) |

### 6. Visualization
- Plotted actual vs predicted prices with a perfect prediction reference line
- Visualized feature importance to identify top price-driving factors

---

## Key Findings

- Gradient Boosting significantly outperforms simple Linear Regression for house price prediction
- **OverallQual** (overall quality rating) and **GrLivArea** (living area) are the strongest predictors
- R² score above 0.85 indicates strong model performance
- House prices are right-skewed — most homes are moderately priced with a few luxury outliers
- Median imputation works well for handling missing values in numerical real estate features

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/elleenfatima05/AI_ML_Internship.git
```

2. Navigate to this task
```bash
cd AI_ML_Internship/Task6_House_Price
```

3. Download `train.csv` from [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data) and place it in this folder

4. Install dependencies
```bash
pip install -r requirements.txt
```

5. Open the notebook in VS Code and run all cells
```
task6_house_price.ipynb
```

---

## Skills Demonstrated

- Regression modeling with Gradient Boosting
- Data cleaning and missing value imputation
- Exploratory data analysis and correlation analysis
- Feature importance interpretation
- Model evaluation using MAE, RMSE, and R² metrics
