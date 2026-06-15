# 📊 Sales Data Analysis — Project 2

An end-to-end exploratory data analysis (EDA) of sales/e-commerce transaction data, covering descriptive statistics, distribution analysis, trend detection, and correlation modelling.

---

## 📁 Project Structure

```
├── Code_File_Project2.ipynb   # Main analysis notebook
├── cleaned_data_project1.csv  # Pre-cleaned input dataset (from Project 1)
└── README.md
```

---

## 🔍 Analysis Overview

### 1. Descriptive Statistics
- Summary statistics (mean, median, std, min, max) for all numerical columns
- Skewness detection — columns flagged as `(skewed)` when |skew| > 1

### 2. Distribution Analysis
- **Histograms with KDE** — visualise the shape of each numeric variable with mean vs. median overlaid
- **Boxplots (IQR method)** — visualise spread and identify outliers per column
- **IQR Outlier Detection** — programmatic report of Q1, Q3, IQR, fences, and outlier counts per column

### 3. Trend & Pattern Analysis
- Date feature extraction (Month, Year, Day of Week)
- **Monthly Revenue Trend** — line chart with area fill across the full time range
- **Product Performance** — revenue and order-count bar charts by product
- **Referral Source Performance** — total revenue, order count, and average order value per acquisition channel

### 4. Correlation Analysis
- **Pearson Correlation Heatmap** — lower-triangle heatmap of all numeric variables
- **Product × Order Status Pivot Heatmap** — average order value broken down by product and order status

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| `pandas` | Data loading, wrangling, aggregation |
| `numpy` | Numerical operations |
| `matplotlib` | Core plotting and formatting |
| `seaborn` | Statistical visualisations |
| `scipy.stats` | Statistical utilities |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scipy
```

### Run the Notebook
```bash
jupyter notebook Code_File_Project2.ipynb
```

> **Note:** Update the CSV path in cell 2 to match your local file location before running:
> ```python
> df = pd.read_csv('path/to/cleaned_data_project1.csv')
> ```

---

## 📌 Key Features

- Automated skewness flagging on all numeric columns
- Dynamic plot grid — adapts to however many numeric columns exist in the dataset
- Formatted axis labels (comma-separated revenue values)
- Clean seaborn `darkgrid` theme throughout

---

## 📄 Dataset

The input dataset (`cleaned_data_project1.csv`) is the cleaned output from **Project 1** and contains transaction-level sales records with the following expected columns:

| Column | Description |
|---|---|
| `Date` | Transaction date |
| `Product` | Product name |
| `TotalPrice` | Revenue for the order |
| `OrderStatus` | Status of the order (e.g. Completed, Cancelled) |
| `ReferralSource` | Marketing channel that drove the order |

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 📝 License

This project is for educational and internship purposes.
