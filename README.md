# Pokémon Data Analysis Dashboard

A data analysis project focused on exploring Pokémon statistics, battle performance, and trends across generations using Python and visualization libraries.

## Project Overview

This project analyzes Pokémon datasets to uncover insights related to:

* Pokémon types and distributions
* Average battle statistics
* Legendary vs non-Legendary comparisons
* Efficiency ratios and battle strength metrics
* Trends across generations

The project was developed using Python, Jupyter Notebook, Pandas, Matplotlib, and Seaborn.

---

## Features

* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Statistical comparisons
* Heatmaps and visual analytics
* Type-based performance analysis
* Custom battle efficiency metrics

---

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn

---

# Data Cleaning Process

The dataset was cleaned and standardized before analysis.

### Cleaning Steps

1. Handled missing values in `Type 2`
2. Standardized column names
3. Removed duplicate entries
4. Converted numeric columns into proper data types
5. Created additional derived metrics and rarity classifications

Example:

```python
df['Type 2'] = df['Type 2'].fillna('None')
```

```python
df.columns = df.columns.str.replace(' ', '_')
```

---

# Sample Analysis

## Pokémon Distribution by Type

```python
type_counts = df['Type 1'].value_counts()
type_counts.plot.bar()
```

## Average Stats Heatmap

```python
average_stats = df.groupby('Type 1').mean()
sns.heatmap(average_stats, annot=True, cmap='coolwarm')
```

---

# Key Insights

* Water-type Pokémon appeared most frequently in the dataset
* Legendary Pokémon generally showed higher total base stats
* Some types demonstrated stronger offensive capabilities than others
* Efficiency ratios helped compare overall battle effectiveness

---

# Future Improvements

* Build an interactive dashboard using Streamlit
* Add filtering by generation and type
* Include predictive analysis using machine learning
* Deploy as a web application

---

# Author

Daksh Patel

*Enhanced and customized Pokémon data analysis project using Python and data visualization techniques.*
