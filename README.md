# 🛒 Superstore Sales Analysis — Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project performs a full Exploratory Data Analysis (EDA) on the **Tableau Superstore Sales Dataset** — a real-world retail dataset containing 9,994 orders across the United States (2014–2017).

The goal is to extract actionable business insights by analyzing sales performance, profitability, discount patterns, and shipping behavior across different product categories, regions, and customer segments.

---

## 📂 Dataset

- **Source:** [Kaggle — Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- **Rows:** 9,994 orders
- **Columns:** 21 features (Order Date, Category, Region, Sales, Profit, Discount, etc.)
- **Time Period:** 2014 – 2017
- **No missing values | No duplicates**

---

## 🛠️ Tools & Libraries

| Tool | Purpose |
|------|---------|
| Python 3.13 | Core language |
| Pandas | Data manipulation & analysis |
| NumPy | Numerical operations |
| Matplotlib | Plotting |
| Seaborn | Statistical visualizations |
| Jupyter Notebook | Development environment |

---

## 📊 Analysis Performed

### 1. Data Cleaning & Preprocessing
- Loaded CSV with latin1 encoding (handles special characters)
- Converted `Order Date` and `Ship Date` to datetime format
- Verified zero null values and zero duplicate rows

### 2. Feature Engineering
- `Order Year` — extracted from Order Date
- `Order Month` — extracted for time trend analysis
- `Shipping Days` — calculated as `Ship Date - Order Date`
- `Profit Margin` — calculated as `Profit / Sales` (efficiency metric)

### 3. Business Questions Answered
- Category-wise and Sub-Category-wise Sales & Profit analysis
- Region-wise and State-wise Sales performance
- Top 10 best-selling products
- Year-wise Sales trend (2014–2017)
- Discount vs Profit relationship (loss analysis)
- Profit Margin comparison across categories
- Shipping Days analysis by Ship Mode
- Multi-level groupby: Region × Category profitability

### 4. Correlation Analysis
- Heatmap of Sales, Profit, Discount, Quantity, Margin
- Key finding: Discount has strong negative correlation with Margin (-0.86)

---

## 🔍 Key Insights

1. **Technology dominates profitability** — Highest sales ($836K) and best profit margin (~15.6%) among all categories.

2. **Furniture is inefficient** — Despite high sales ($742K), profit margin is only ~3.8% due to heavy discounting.

3. **Tables & Bookcases are loss-makers** — Only sub-categories with negative total profit (-$17,725 and -$3,472 respectively).

4. **High discounts cause losses** — Loss orders had an average discount of **48%** vs only **8%** for profitable orders.

5. **West Region leads in sales** (~$725K), while South Region has the lowest (~$390K).

6. **California is the top state** by sales ($457K) — nearly 1.5x higher than #2 New York ($311K).

7. **Standard Class shipping takes ~5 days** on average vs Same Day (~0 days) — 5x difference in delivery time.

---

## 📁 Project Structure

```
superstore-sales-eda/
│
├── superstore_sale_analysis.ipynb   # Main notebook
├── sale.csv                         # Dataset (download from Kaggle)
└── README.md                        # Project documentation
```

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/hassanqurashi007/superstore-sales-eda.git

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn

# 3. Open Jupyter Notebook
jupyter notebook superstore_sale_analysis.ipynb
```

> **Note:** Download `sale.csv` from [Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) and place it in the project folder.

---

## 👨‍💻 Author

**Hassan Qureshi**
- GitHub: [github.com/hassanqurashi007](https://github.com/hassanqurashi007)
- University of Gujrat — BS Information Technology (AI/ML)
