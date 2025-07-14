# Data Cleaning and Pre-processing Tools

This repository contains a Jupyter Notebook that demonstrates basic data cleaning and pre-processing techniques using the pandas and numpy libraries in Python.

---

## Description

The `cleaning.ipynb` notebook walks through a series of common data cleaning tasks on a sample dataset. The purpose is to show how to identify and handle issues like missing values, duplicate entries, and outliers to prepare data for analysis.

---

## Dataset

The notebook uses a small, synthetically generated dataset created as a pandas DataFrame. The dataset includes the following columns:

* `age`: The age of an individual (contains a missing value).
* `salary`: The salary of an individual (contains an outlier).
* `city`: The city where the individual resides.

---

## Data Cleaning and Pre-processing Steps

The following techniques are demonstrated in the notebook:

### 1. Handling Missing Values

Missing data, represented as `NaN`, can cause problems in data analysis. The notebook demonstrates how to handle these by:
* Identifying missing values in the `age` column.
* **Imputing** the missing value with the **median** of the column. This is a common strategy to fill in missing numerical data without significantly skewing the distribution.

### 2. Handling Duplicate Data

Duplicate rows can lead to incorrect analysis and biased results. The notebook shows how to:
* Add duplicate rows to the DataFrame to simulate a real-world scenario.
* Identify and remove these duplicate entries to ensure each data point is unique.

### 3. Outlier Detection and Removal

Outliers are data points that differ significantly from other observations and can skew statistical measures. The notebook demonstrates the **Interquartile Range (IQR)** method for outlier detection:
* The first quartile (Q1) and third quartile (Q3) of the `salary` column are calculated.
* The IQR is computed as `Q3 - Q1`.
* Upper and lower bounds are defined based on the IQR (`Q1 - 1.5 * IQR` and `Q3 + 1.5 * IQR`).
* Any data points in the `salary` column that fall outside these bounds are considered outliers and are removed from the dataset.
