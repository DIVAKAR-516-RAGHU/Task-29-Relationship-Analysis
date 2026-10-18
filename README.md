# Task 29: Relationship Analysis 📊

## 📌 Project Overview

This project focuses on analyzing the relationship between two numerical variables using data visualization techniques. A scatter plot is created using Python, Pandas, and Matplotlib to identify patterns, trends, and correlations in the Iris dataset.

This task is part of my **AI & ML Internship – Task 29**.

## 🎯 Objective

To create a scatter plot that analyzes the relationship between two numerical variables and describes the observed pattern.

## 🛠️ Tools and Technologies

- Python
- Pandas
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- Git and GitHub

## 📂 Dataset

**Dataset Name:** Iris Dataset

The Iris dataset is a commonly used dataset in machine learning. It contains measurements of iris flowers belonging to three species:

- Setosa
- Versicolor
- Virginica

### Features Used

| Feature | Description |
|---|---|
| Petal Length (cm) | Length of the flower petal |
| Petal Width (cm) | Width of the flower petal |
| Species | Species of the iris flower |

## 📈 Project Workflow

1. Imported the required Python libraries.
2. Loaded the Iris dataset using Scikit-learn.
3. Converted the dataset into a Pandas DataFrame.
4. Inspected the dataset structure, columns, missing values, and duplicate rows.
5. Selected petal length and petal width as the numerical variables.
6. Created a scatter plot using Matplotlib.
7. Created an additional scatter plot with different colors for each species.
8. Calculated the Pearson correlation coefficient.
9. Identified patterns and documented observations.
10. Prepared the final analysis and conclusion.

## 💻 Python Code

```python
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris

# Load the Iris dataset
iris = load_iris(as_frame=True)
df = iris.frame

# Add species names
df["species"] = df["target"].map(
    dict(enumerate(iris.target_names))
)

# Remove the numerical target column
df = df.drop(columns=["target"])

# Select numerical variables
x = df["petal length (cm)"]
y = df["petal width (cm)"]

# Create scatter plot
plt.figure(figsize=(8, 6))
plt.scatter(
    x,
    y,
    color="blue",
    alpha=0.7,
    edgecolors="black"
)

plt.title("Relationship Between Petal Length and Petal Width")
plt.xlabel("Petal Length (cm)")
plt.ylabel("Petal Width (cm)")
plt.grid(True, linestyle="--", alpha=0.4)
plt.tight_layout()
plt.show()

# Calculate correlation
correlation = x.corr(y)
print("Correlation Coefficient:", round(correlation, 3))
```

## 🔍 Observations

1. **Positive Relationship:** Petal length and petal width generally increase together.
2. **Strong Correlation:** The Pearson correlation coefficient is approximately 0.963 for the complete dataset, indicating a strong positive linear association.
3. **Species Clustering:** The scatter plot reveals distinguishable groups corresponding to different Iris species.
4. **Differences in Measurements:** Setosa generally has smaller petals, while Virginica generally has larger petals.
5. **Visualization Benefits:** Scatter plots help identify trends, clusters, and relationships between numerical variables.

## 📊 Results

The scatter plot shows a strong positive association between petal length and petal width in the Iris dataset. The correlation coefficient supports the visual observation.

The species-colored plot further demonstrates how visualization can reveal patterns and groupings in data.

**Note:** Correlation does not necessarily imply causation.

## 🎓 Interview Questions and Answers

### 1. What is a scatter plot?

A scatter plot is a data visualization technique that represents the relationship between two numerical variables using individual points.

### 2. What does a positive relationship mean?

A positive relationship means that as one variable increases, the other variable generally tends to increase.

### 3. Does correlation always mean causation?

No. Correlation indicates an association between variables but does not prove that one variable causes changes in another.

### 4. What is the purpose of a scatter plot?

A scatter plot helps identify relationships, trends, clusters, and possible outliers between two numerical variables.

### 5. What does a correlation coefficient of 0.963 indicate?

It indicates a strong positive linear association between petal length and petal width across the complete Iris dataset.

## 📁 Project Structure

```text
Task-29-Relationship-Analysis/
│
├── Task_29_Relationship_Analysis.ipynb
└── README.md
```

## 🏁 Conclusion

This project demonstrates how Python, Pandas, and Matplotlib can be used to analyze relationships between numerical variables.

By visualizing petal length against petal width, a strong positive relationship was identified. The task improved my understanding of scatter plots, correlation, and exploratory data analysis.

## 👨‍💻 Author

**Divakar R**

AI & ML Internship — Task 29

## ⭐ Key Learning Outcomes

- Understanding scatter plots
- Selecting numerical variables
- Visualizing relationships using Matplotlib
- Calculating Pearson correlation
- Identifying positive relationships and clusters
- Interpreting visualization results

---

**Task:** 29 — Relationship Analysis  
**Status:** Completed
