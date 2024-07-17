# Car Data Analysis - Nigeria

## Overview

This repository contains Python code for analyzing car data from Nigeria. The analysis explores various aspects of the dataset, including car makes, conditions, and prices, using popular data analysis and visualization libraries such as pandas, matplotlib, seaborn, and plotly.

## Features

- **Data Loading and Preprocessing**: Load the car dataset (`car_data.csv`) and preprocess it by removing unnecessary columns and handling missing values.
  
- **Exploratory Data Analysis (EDA)**: Gain insights into the dataset's structure and contents using descriptive statistics and visualizations.
  
- **Data Visualization**: Visualize key aspects of the data, including:
  - Distribution of car makes in Nigeria using pie charts and bar plots.
  - Analysis of car body types using count plots.
  - Exploration of car conditions and engine fuel types with pie charts.
  - Scatter plots depicting relationships between car price, mileage, body type, and condition.
  - 3D scatter plots to visualize relationships among car make, model, and condition.

- **Insights and Findings**: Derive insights such as the most expensive car in the dataset, distribution of cars across price ranges, and top/bottom car makes by condition.

## Description

This Python script analyzes a dataset of cars from Nigeria, aiming to provide actionable insights for automotive businesses and enthusiasts. By leveraging data visualization techniques and statistical analysis, the script uncovers patterns in car ownership, preferences, and market dynamics within the Nigerian automotive sector. This analysis helps stakeholders understand consumer behavior, pricing trends, and the popularity of different car models and conditions in the market.

## Code Explanation

### Loading and Preprocessing Data

```python
import pandas as pd

# Load dataset
df = pd.read_csv('car_data.csv')

# Drop unnecessary columns
df.drop(columns=['bought_condition'], inplace=True)
```

### Data Visualization

The script uses various plotting libraries to visualize different aspects of the car data:

```python
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px

# Example visualization: Pie chart of top car makes in Nigeria
fig = plt.figure(figsize=(10, 10))
ax = fig.subplots()
df['make'].value_counts().plot(ax=ax, kind='pie', autopct='%1.1f%%')
ax.set_ylabel("")
ax.set_title("Top Car Makes in Nigeria")
plt.show()
```

### Dependencies

Ensure you have the following Python libraries installed:

- pandas
- matplotlib
- seaborn
- plotly

Install them using pip if necessary:

```bash
pip install pandas matplotlib seaborn plotly
```

## Data

The dataset (`car_data.csv`) contains detailed information about cars in Nigeria, including make, model, condition, price, mileage, body type, and more.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
