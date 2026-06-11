# Task 1: Exploring and Visualizing the Iris Dataset

## Objective
Load, inspect, and visualize the Iris dataset to understand data trends, distributions, and relationships between features.

---

## Dataset

- **Name:** Iris Dataset
- **Format:** CSV / loaded directly via seaborn
- **Size:** 150 rows × 5 columns
- **Features:** Sepal Length, Sepal Width, Petal Length, Petal Width, Species
- **Classes:** Setosa, Versicolor, Virginica

---

## Libraries Used

```
pandas
numpy
matplotlib
seaborn
```

Install with:
```bash
pip install -r requirements.txt
```

---

## Steps Performed

### 1. Data Loading
- Loaded the Iris dataset using seaborn's built-in `load_dataset()` function
- Stored it as a pandas DataFrame

### 2. Data Inspection
- Checked dataset shape using `.shape`
- Viewed column names and first 5 rows using `.head()`
- Reviewed data types and null counts using `.info()`
- Generated summary statistics (mean, std, min, max) using `.describe()`

### 3. Visualizations

| Plot | Purpose |
|------|---------|
| Scatter Plot (Pairplot) | Shows relationships between all feature pairs, colored by species |
| Histogram | Shows value distribution for each feature |
| Box Plot | Reveals outliers and spread per feature grouped by species |

---

## Key Findings

- Petal Length and Petal Width are the most discriminating features between species
- Setosa is clearly separable from the other two classes
- Versicolor and Virginica show some overlap in sepal dimensions
- No missing values found in the dataset

---

## How to Run

1. Clone the repository
```bash
git clone https://github.com/yourusername/AI_ML_Internship.git
```

2. Navigate to this task
```bash
cd AI_ML_Internship/Task1_Iris_EDA
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Open the notebook in VS Code and run all cells
```
task1_iris.ipynb
```

---

## Skills Demonstrated

- Data loading and inspection using pandas
- Descriptive statistics and exploratory data analysis (EDA)
- Data visualization using seaborn and matplotlib
- Identifying patterns and distributions in structured data
