# COVID-19 Data Analysis Project

This project involves analyzing a COVID-19 dataset to extract meaningful insights using Python. The dataset is sourced from (https://raw.githubusercontent.com/SR1608/Datasets/main/covid-data.csv).

---

## Dataset Description
The dataset contains COVID-19 statistics for different countries and continents, including:
- **Columns:** 
  - Continent
  - Location
  - Date
  - Total Cases
  - Total Deaths
  - GDP Per Capita
  - Human Development Index

---

## Objective
To perform the following tasks on the dataset:
1. Data Import and Cleaning
2. High-Level and Low-Level Data Understanding
3. Data Aggregation and Feature Engineering
4. Data Visualization and Insight Extraction

---

## Requirements
- Python 3.7 or above
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`

Install dependencies using:
```bash
pip install pandas numpy matplotlib seaborn
```

---

## Steps Performed
### 1. Data Import
- The dataset was loaded using the `pandas.read_csv()` function.

### 2. High-Level Data Understanding
- Number of rows and columns were identified.
- Data types of all columns were determined.
- Used `.info()` and `.describe()` to summarize the dataset.

### 3. Low-Level Data Understanding
- Unique counts of `location` were calculated.
- The continent with the maximum frequency was identified.
- Calculated statistical metrics for `total_cases` and `total_deaths`.
- Identified continents with:
  - Maximum `human_development_index`
  - Minimum `gdp_per_capita`

### 4. Data Cleaning
- Removed duplicate rows.
- Handled missing values:
  - Removed rows with missing `continent`.
  - Replaced other missing values with `0`.

### 5. Data Transformation
- Converted the `date` column to `datetime` format.
- Created a new `month` column from the `date`.

### 6. Data Aggregation
- Grouped data by `continent` and calculated maximum values for all columns.
- Saved the grouped data into a new DataFrame (`df_groupby`).

---

## Features Engineered
- Created a new column: `total_deaths_to_total_cases` as the ratio of total deaths to total cases.

---

## Data Visualization
- **Histogram:** Distribution of `gdp_per_capita`.
- **Scatter Plot:** Relationship between `total_cases` and `gdp_per_capita`.
- **Pairplot:** Visualized correlations in the aggregated dataset (`df_groupby`).
- **Bar Plot:** Displayed total cases by continent.

---

## Results
- Insights into COVID-19 statistics across continents.
- Identification of trends between economic indicators (e.g., GDP per capita) and COVID-19 impact.

---
