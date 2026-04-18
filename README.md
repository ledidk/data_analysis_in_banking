# Visual Data Analysis in Banking 📊

A guided Jupyter notebook lab exploring visual data analysis techniques applied to a real-world bank marketing dataset. Built as part of the IBM Skills Network curriculum.

## Overview

This lab covers how to use Python's core visualization libraries — **Matplotlib**, **Seaborn**, and **Plotly** — to analyze banking client data and support data-driven decisions for marketing campaigns.

The central question: *What client characteristics predict whether someone will subscribe to a term deposit after a phone call?*

## Dataset

**UCI Bank Marketing Dataset** — a subset of the open-source dataset from the UCI ML Repository.

- **41,188 records** × **21 features**
- Mix of demographic, behavioral, and macroeconomic indicators
- Target variable: `y` — did the client subscribe to a term deposit? (yes/no)

> Source: Moro, S., Cortez, P., & Rita, P. (2014). *A Data-Driven Approach to Predict the Success of Bank Telemarketing.* Decision Support Systems, Elsevier, 62:22–31.

## What's Covered

| Section | Techniques |
|---|---|
| Single feature analysis | Histograms, box plots, count plots |
| Feature interaction | Pair plots, heatmaps, violin plots, scatter plots |
| Categorical analysis | Cross-tabulation, grouped bar charts |
| Interactive visualization | Plotly line charts, bar charts, box plots |
| Comprehensive EDA | Correlation matrix, distribution by target variable |

## Key Libraries

- `pandas` — data loading and manipulation
- `matplotlib` — base plotting
- `seaborn` — statistical graphics
- `plotly` — interactive charts

## Key Findings

- Clients aged 25–50 make up the bulk of the dataset
- `euribor3m` and `nr.employed` are strongly correlated with `emp.var.rate`
- `housing`, `loan`, and `day_of_week` show little predictive signal
- Campaigns during high interest rate periods yield better results
- The target variable is imbalanced — positive outcomes are significantly fewer

## Getting Started

```bash
# Download and unzip the dataset
wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/VDA_Banking_L2/bank-additional.zip
unzip -o -q bank-additional.zip

# Install dependencies
pip install pandas matplotlib seaborn plotly
```

Then open `VDA_Banking_L2.ipynb` in Jupyter and run the cells in order.

## Project Structure