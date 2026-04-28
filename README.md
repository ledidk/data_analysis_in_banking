# 🏦 Bank Marketing Analysis - Who Actually Says Yes?

> *A bank called 4,119 clients trying to sell a term deposit. Only 10.9% said yes. I dug into the data to find out why.*

A visual data analysis project built on a real-world bank marketing dataset - exploring what client characteristics and campaign behaviors predict a positive response.

Started as a guided IBM Skills Network lab. Extended with independent analysis and custom visualizations.

📂 Full notebook → [`VDA_Banking_L2.ipynb`](VDA_Banking_L2.ipynb)

---

## 📌 Project Overview

This project uses Python's core visualization libraries to analyze 4,119 bank marketing records across 21 features. The central question - *who actually subscribes to a term deposit after a phone call?* - led to findings that go beyond the guided lab.

---

## 📊 Key Findings

| Finding | Detail |
|---|---|
| Overall conversion rate | 10.9% of clients said yes |
| Best call duration | 10 min+ → 49.1% conversion |
| Worst call duration | Under 1 min → 0% conversion |
| Highest converting job | Students (23.2%) and Retired (22.9%) |
| Lowest converting job | Management (9.3%) |
| Best month | March → 58.3% conversion (48 calls) |
| Worst month | May → 6.5% conversion (1,378 calls) |
| Contact drop-off point | After 5 contacts conversion falls below 6% |
| Contact 7+ | Near-zero returns (1.7%) |

**The pattern the data reveals:**

Nobody says yes in under a minute. Almost 1 in 2 say yes after 10 minutes. The conversation itself is the product - not the volume of calls.

---

## 📈 Visualization

### Call Duration vs Conversion Rate
![Call Duration vs Conversion](outputs/charts/call_duration_vs_conversion.png)

---

## 🗂️ Project Structure

```
bank_marketing_analysis/
├── VDA_Banking_L2.ipynb              # Main analysis notebook
├── bank-additional/
│   ├── bank-additional-full.csv      # Full dataset (41,188 records)
│   └── bank-additional.csv           # Sample dataset (4,119 records)
├── outputs/
│   └── charts/
│       └── call_duration_vs_conversion.png
└── README.md
```

---

## 🛠️ Tools & Methodology

**Tools:** Python · Pandas · Matplotlib · Seaborn · Plotly · Jupyter Notebook

**What the guided lab covered:**
- Single feature analysis - histograms, box plots, count plots
- Feature interaction - pair plots, heatmaps, violin plots
- Categorical analysis - cross-tabulation, grouped bar charts
- Interactive visualization - Plotly line charts, bar charts, box plots
- Comprehensive EDA - correlation matrix, distribution by target variable

**What I added independently:**
- Converted `duration` (seconds) to minutes and bucketed into 6 ranges
- Calculated conversion rate per duration bucket using `groupby` + `mean`
- Built a standalone dark-theme Matplotlib chart with color-coded bars and annotations
- Identified the contact drop-off point at 5 calls using campaign groupby analysis
- Compared month volume vs conversion rate to surface the May paradox

---

## 📂 Data Sources

| Dataset | Source |
|---|---|
| UCI Bank Marketing Dataset | [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing) |
| Guided lab curriculum | [IBM Skills Network · Cognitive Class](https://cognitiveclass.ai) |

> Moro, S., Cortez, P., & Rita, P. (2014). *A Data-Driven Approach to Predict the Success of Bank Telemarketing.* Decision Support Systems, Elsevier, 62:22–31.

---

## ⚙️ Getting Started

```bash
# Download dataset
wget https://archive.ics.uci.edu/ml/machine-learning-databases/00222/bank-additional.zip
unzip bank-additional.zip

# Install dependencies
pip install pandas matplotlib seaborn plotly

# Open notebook
jupyter notebook VDA_Banking_L2.ipynb
```

---

## 💡 What I Learned

- How to bucket continuous variables into meaningful ranges using `pd.cut`
- How to calculate conversion rates per group with `groupby` + `mean` on a binary column
- How to build a standalone dark-theme chart with color-coded bars and annotations in Matplotlib
- Why call volume and call quality are completely different metrics - May had the most calls and the worst results
- That the most interesting findings in a dataset are rarely the obvious ones - they come from asking the next question after the first answer

---

## 🔗 Connect

[dieudonne.ca](https://www.dieudonne.ca) ·
[LinkedIn](https://www.linkedin.com/in/dieudonnentakirutimana/)
