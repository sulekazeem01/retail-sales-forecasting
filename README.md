# Retail Sales Analysis and Prediction Using Python

## Project Overview

This project analyzes retail customer transactions to understand spending patterns and demonstrate predictive modeling using Linear Regression.

The analysis explores how purchase quantity, unit price, customer demographics, and product categories relate to total customer spending.

The project combines exploratory data analysis, feature engineering, data visualization, and machine learning to generate business insights.

## Business Objectives

- Analyze customer spending patterns across product categories.
- Identify variables associated with higher transaction spending.
- Examine the relationships between quantity, unit price, and total spending.
- Build and evaluate a baseline Linear Regression model.
- Translate analytical findings into practical business recommendations.

## Dataset

The dataset contains **1,000 retail transaction records** with the following variables:

| Column | Description |
|---|---|
| CustomerID | Unique customer identifier |
| Age | Customer age |
| Gender | Customer gender |
| ProductCategory | Purchased product category |
| Quantity | Number of units purchased |
| UnitPrice | Price per unit |
| TotalSpending | Total transaction spending |

**Dataset file:** `retail_sales_prediction_1000.csv`

## Tools and Technologies

- **Python** — Data analysis and predictive modeling
- **Pandas** — Data manipulation and feature engineering
- **NumPy** — Numerical calculations
- **Matplotlib and Seaborn** — Data visualization
- **Scikit-learn** — Linear Regression, train-test splitting, and model evaluation
- **Jupyter Notebook** — Analysis development and documentation
- **GitHub** — Project version control and portfolio presentation

## Exploratory Data Analysis

The analysis includes:

1. Customer spending distribution using a histogram.
2. Spending comparisons across product categories using boxplots.
3. Correlation analysis using a heatmap.
4. Descriptive statistics to summarize transaction characteristics.

### Key Findings

- Average transaction spending was approximately **$1,456.69**.
- Median transaction spending was approximately **$1,169.49**.
- Electronics had the highest average spending at approximately **$1,501.53**.
- Home & Kitchen recorded the highest number of transactions, with **269**.
- Unit price and quantity showed strong positive correlations with total spending.

These findings describe patterns in the analyzed dataset and should not be interpreted as causal relationships.

## Feature Engineering

An interaction feature was created:

`Quantity_UnitPrice = Quantity × UnitPrice`

The analysis confirmed that total spending is calculated from quantity and unit price across all 1,000 records.

Because the interaction feature reproduces the target variable, it was excluded from the regression model to avoid direct target leakage.

## Machine Learning Model

A baseline **Linear Regression** model was developed to estimate transaction spending.

### Model Configuration

- Target variable: `TotalSpending`
- Predictors: `Age`, `Gender`, `ProductCategory`, `Quantity`, `UnitPrice`
- Training data: 70%
- Testing data: 30%
- Random state: 70
- Categorical variables encoded using one-hot encoding

### Model Evaluation

| Metric | Result |
|---|---:|
| R² Score | 0.8755 |
| Root Mean Squared Error (RMSE) | $419.49 |
| Mean Absolute Error (MAE) | $321.61 |

The model explains approximately **87.55% of the variation** in transaction spending within the test dataset.

These metrics demonstrate baseline regression performance on the available data rather than validated future-sales forecasting capability.

## Business Insights and Recommendations

- Monitor quantity and unit price because they are strongly associated with transaction spending.
- Examine product-category spending patterns to inform merchandising and promotional decisions.
- Explore customer segmentation to identify differences in purchasing behavior.
- Collect historical transaction dates, prior purchasing behavior, discounts, and promotional information for more meaningful forecasting.

## Project Limitations

Total spending is mechanically calculated as quantity multiplied by unit price. Consequently, the regression model primarily approximates a known mathematical relationship rather than predicting genuinely unknown future sales.

The dataset does not include transaction dates or sufficient pre-purchase information for reliable future-sales forecasting.

Future improvements should focus on predicting outcomes using information available before purchases occur.

## Repository Files

- `Retail_Sales_Prediction.ipynb` — Complete Python analysis and visualizations
- `retail_sales_prediction_1000.csv` — Dataset used in the analysis

- `README.md` — Project documentation

## Conclusion

This project demonstrates practical skills in Python data analysis, exploratory data analysis, data visualization, feature engineering, Linear Regression, model evaluation, and communicating analytical findings.

It also demonstrates the importance of recognizing target leakage and understanding the limitations of predictive models before making business recommendations.

## Author

**Sule Kazeem**

Data Analytics Portfolio Project
