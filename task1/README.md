# Task 1: Exploring and Visualizing the Iris Dataset 🌸

## Task Objective
The goal of this task is to load, inspect, and visualize the Iris dataset to understand data trends and distributions using Python libraries like Pandas, Matplotlib, and Seaborn.

---

## Dataset Used
- **Name:** Iris Dataset
- **Source:** CSV file / Seaborn built-in dataset
- **Total Rows:** 150
- **Total Columns:** 5

### Columns:
| Column Name | Description |
|-------------|-------------|
| sepal_length | Length of the sepal (cm) |
| sepal_width | Width of the sepal (cm) |
| petal_length | Length of the petal (cm) |
| petal_width | Width of the petal (cm) |
| species | Type of flower (setosa, versicolor, virginica) |

---

## Libraries Used
- `pandas` — Data loading and inspection
- `matplotlib` — Data visualization
- `seaborn` — Advanced data visualization

---

## Steps Performed

### Step 1 — Data Loading
- Loaded the Iris CSV file using `pandas`
- Checked the shape, column names, and first few rows using `.head()`

### Step 2 — Data Inspection
- Used `.info()` to check data types and null values
- Used `.describe()` to get summary statistics like mean, min, max

### Step 3 — Data Visualization
- **Scatter Plot** — Shows relationship between sepal length and petal length
- **Histogram** — Shows distribution of sepal length values
- **Box Plot** — Shows outliers in sepal length across different species

---

## Key Results and Findings

- The dataset has **150 rows** and **5 columns** with **no missing values**
- There are **3 species** of flowers: Setosa, Versicolor, and Virginica
- **Setosa** flowers have the smallest petal length and width
- **Virginica** flowers have the largest petal length and width
- The scatter plot clearly shows that the **3 species are well separated**
- Box plots show that **Virginica has some outliers** in sepal length

---

## How to Run

1. Open Google Colab or Jupyter Notebook
2. Upload the `iris.csv` file
3. Run the notebook `Task1_Iris_Dataset.ipynb`

---

## Code Summary

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load Data
df = pd.read_csv('iris.csv')

# Inspect Data
print(df.shape)
print(df.head())
print(df.info())
print(df.describe())

# Scatter Plot
sns.scatterplot(data=df, x='sepal_length', y='petal_length', hue='species')
plt.show()

# Histogram
df['sepal_length'].hist(bins=20, color='blue', edgecolor='black')
plt.show()

# Box Plot
sns.boxplot(data=df, x='species', y='sepal_length')
plt.show()
```

---

## Author
- **Internship:** AI/ML Engineering Internship
- **Company:** DevelopersHub Corporation
- **Task:** Task 1 out of 6
