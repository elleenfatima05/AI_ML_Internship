# Task 2: Predict Future Stock Prices (Short-Term)

## Objective
Use historical stock market data to predict the next day's closing price using regression models.

---

## Dataset

- **Source:** Yahoo Finance via the `yfinance` Python library
- **Stock Used:** Apple Inc. (AAPL) — or Tesla (TSLA)
- **Date Range:** 2022-01-01 to present
- **Features:** Open, High, Low, Close, Volume

---

## Libraries Used

```
pandas
numpy
matplotlib
scikit-learn
yfinance
```

Install with:
```bash
pip install -r requirements.txt
```

---

## Steps Performed

### 1. Data Collection
- Downloaded historical stock data using `yfinance.download()`
- Inspected shape, columns, and checked for missing values

### 2. Feature Engineering
- Used Open, High, Low, Volume as input features (X)
- Used next day's Close price as the target variable (y)
- Shifted the Close column by 1 day to predict tomorrow from today's data

### 3. Data Splitting
- Split data into 80% training and 20% testing using `train_test_split`

### 4. Model Training
Two models trained and compared:

| Model | Description |
|-------|-------------|
| Linear Regression | Baseline model, fast and interpretable |
| Random Forest Regressor | Ensemble model, captures non-linear patterns |

### 5. Evaluation

| Metric | Description |
|--------|-------------|
| MAE (Mean Absolute Error) | Average prediction error in dollars |
| R² Score | How well the model explains variance (closer to 1.0 = better) |

### 6. Visualization
- Plotted actual vs predicted closing prices on the same chart
- Used distinct colors with legend, title, and axis labels

---

## Key Findings

- Random Forest outperformed Linear Regression in both MAE and R² score
- Short-term price prediction is feasible but sensitive to market volatility
- Volume alone is a weak predictor; price-based features (Open, High, Low) carry more signal

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/yourusername/AI_ML_Internship.git
```

2. Navigate to this task
```bash
cd AI_ML_Internship/Task2_Stock_Prediction
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Open the notebook in VS Code and run all cells
```
task2_stocks.ipynb
```

> Note: An active internet connection is required to fetch stock data via yfinance.

---

## Skills Demonstrated

- Data fetching using financial APIs (yfinance)
- Time series data handling and feature engineering
- Regression modeling with scikit-learn
- Model evaluation using MAE and R² metrics
- Plotting predictions vs real data using matplotlib
