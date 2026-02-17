# 🐼 Pandas Comprehensive Assignment 4
### Mastering Pandas Fundamentals — Data Analysis with Python

---

## 📌 Project Overview

This project is a comprehensive hands-on assignment covering core Pandas operations for data analysis. It works across four real-world-style datasets and demonstrates skills in data loading, cleaning, filtering, aggregation, and transformation.

- **Author:** Oluwadara Olamide (Dara)
- **Course:** Data Science with Python | Week 4
- **Topic:** Comprehensive Pandas Fundamentals

---

## 📁 Project Structure

```
Oluwadara_Olamide_pandas/
│
├── Python4DataAnalysis.ipynb              # Main notebook with all solutions
├── README.md                              # This file
│
└── data/
    ├── sales_data.csv        # 1000 rows — transactions, products, regions
    ├── customer_data.csv     # 500 rows  — customer demographics & purchase history
    ├── inventory_data.csv    # 100 rows  — product inventory (contains missing values)
    └── employee_data.csv     # 200 rows  — employee info, salaries, departments
```

---

## ⚙️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install dependencies
```bash
pip install pandas numpy jupyter
```

### 3. Launch the notebook
```bash
jupyter notebook Python4DataAnalysis.ipynb
```

> **Important:** Update the file paths in the data loading cells to match your local machine before running. The current paths point to a local Windows directory.

---

## 📚 Topics Covered

| Section | Topic |
|---------|-------|
| Section 1 | DataFrame Basics — shape, dtypes, `.info()`, summary stats |
| Section 2 | Data Selection & Indexing — filtering, `.loc`, `.iloc` |
| Section 3 | Data Cleaning — missing values, duplicates, negative value checks |
| Section 4 | Sorting & Ranking — single and multi-column sorts |
| Section 5 | GroupBy & Aggregations — totals, means, insights |
| Section 6 | Data Transformation — new columns, datetime parsing |

---

## 💡 Assumptions Made

- Negative values in `quantity` or `total_amount` in `sales_data` are treated as data entry errors — **none were found** in this dataset.
- Missing values in `stock_quantity` are filled with the **median** to avoid skew from outliers.
- Missing values in `unit_cost` are filled with the **mean** value.
- Missing `supplier` values are filled with the string `'Unknown'`.
- For `spending_per_purchase`, rows where `total_purchases == 0` are set to `NaN` using `np.where` to avoid division errors.
- The `hire_date` column is converted to datetime before creating the `tenure_category` column.

---

## 🔍 Key Findings

### 📊 Sales Data (1,000 transactions, Jan–Dec 2023)

| Metric | Value |
|--------|-------|
| **Top Revenue Product** | Smartwatch — **$1,192,539.16** total revenue |
| **Highest Revenue Region** | North — **$1,850,944** total |
| **Region with Highest Avg Transaction** | North — **$5,510.78** median transaction value |
| **Best Performing Sales Rep** | David — **$1,026,429** total sales |
| **2nd Best Sales Rep** | Frank — **$1,005,982** total sales |
| **Peak Revenue Month** | August — **$699,440.87** |
| **Average Transaction Value** | ~**$6,908.75** |
| **Negative values found** | None — data is clean ✓ |

### 👥 Customer Data (500 customers)

| Metric | Value |
|--------|-------|
| **City with Most Customers** | Los Angeles — **121 customers** |
| **2nd Most Customers** | Phoenix — **101 customers** |
| **Mean Customer Age** | **46.28 years** |
| **Duplicate rows found** | None — data is clean ✓ |

### 👩‍💼 Employee Data (200 employees)

| Metric | Value |
|--------|-------|
| **Largest Department** | Sales — **53 employees** |
| **Department with Highest Mean Salary** | HR — **$97,153** |
| **Department with Highest Median Salary** | HR — **$111,641** |
| **Highest Paid Employee** | Employee_147 (IT, Junior) — **$149,712** |
| **Salary Range** | **$30,916 – $149,712** |

### 📦 Inventory Data (100 products)

| Metric | Value |
|--------|-------|
| **Missing: stock_quantity** | 10 values (10%) → filled with median |
| **Missing: supplier** | 25 values (25%) → filled with `'Unknown'` |
| **Missing: unit_cost** | 14 values (14%) → filled with mean |
| **Lowest Stock Product** | Product_45 (Toys) — only **2 units** remaining |

---

## 🛠️ Requirements

- Python 3.8+
- pandas
- numpy
- jupyter

---

## 📖 Resources

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Pandas User Guide](https://pandas.pydata.org/docs/user_guide/index.html)
- [Pandas Cheat Sheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)

---

## ⚠️ Academic Integrity

This is an individual assignment completed in accordance with course academic integrity policies. All code is original work by the author.
