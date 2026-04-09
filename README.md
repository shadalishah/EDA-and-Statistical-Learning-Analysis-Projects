# 📊 Exploratory Data Analysis & Statistical Insights — College, Auto & Boston Datasets

> **Skills Demonstrated:** Exploratory Data Analysis (EDA) · Data Cleaning · Statistical Summarization · Data Visualization · Feature Engineering · Correlation Analysis · Outlier Detection · Python · Pandas · Matplotlib · NumPy

[![Author](https://img.shields.io/badge/Author-Shad%20Ali%20Shah-blue)](https://github.com/shadalishah)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin)](https://www.linkedin.com/in/shad-ali-shah-6439ab339/)
[![Language](https://img.shields.io/badge/Language-Python-3776AB?logo=python)](https://www.python.org/)
[![Topic](https://img.shields.io/badge/Topic-EDA%20%26%20Statistical%20Analysis-green)]()

---

## 🎯 Project Overview

This project demonstrates a **complete Exploratory Data Analysis (EDA) pipeline** applied to three real-world datasets — uncovering patterns in higher education, automotive engineering, and urban economics before any modeling begins.

> *"Every ML project starts with EDA. Understanding your data — its distributions, correlations, outliers, and missing values — determines the quality of every downstream model. This project demonstrates exactly that foundational workflow."*

Three datasets analyzed across four applied exercises:

| Exercise | Dataset | Business Question |
|----------|---------|-----------------|
| Ex. 8 | College (777 universities) | Which universities stand out academically and financially? |
| Ex. 9 | Auto (392 vehicles) | What factors drive fuel efficiency? |
| Ex. 10 | Boston Housing (506 suburbs) | What shapes crime rates and housing values? |
| Ex. 11 | Mixed | Custom dataset creation and analysis |

---

## 📁 Datasets Used

| Dataset | Source | Size | Domain |
|---------|--------|------|--------|
| **College** | U.S. News & World Report 1995 (Real) | 777 universities, 18 features | Higher Education |
| **Auto** | Carnegie Mellon StatLib (Real) | 392 vehicles, 9 features | Automotive |
| **Boston** | U.S. Census Bureau (Real) | 506 suburbs, 13 features | Urban Economics |

---

## 🔧 Techniques & Tools Applied

| Technique | Library | Purpose |
|-----------|---------|---------|
| Descriptive Statistics | `pandas.describe()` | Mean, std, range, quartiles per feature |
| Missing Value Analysis | `pandas.isnull()` | Identifying and handling incomplete data |
| Correlation Matrix | `pandas.corr()` | Feature relationship quantification |
| Scatter Plot Matrix | `pandas.plotting.scatter_matrix()` | Visual pairwise relationships |
| Boxplots | `matplotlib` | Distribution comparison across groups |
| Histograms | `matplotlib` | Feature distribution shape analysis |
| Feature Engineering | `numpy.where()` | Creating Elite university binary flag |
| Outlier Detection | Visual + IQR | Identifying extreme observations |
| Data Indexing Fix | `pandas.read_csv()` | Correcting column header misalignment |

**Libraries:** `numpy` · `pandas` · `matplotlib` · `ISLP`

---

## 📊 Key Results

### Exercise 8 — College Dataset (777 US Universities)

**Feature Overview:**

| Feature | Range | Mean |
|---------|-------|------|
| Apps (applications) | 81 – 48,094 | 3,002 |
| Accept | 72 – 26,330 | 2,019 |
| Outstate tuition | $2,340 – $21,700 | $10,441 |
| Grad.Rate | 10% – 118% | 65.5% |
| PhD faculty | 8% – 103% | 72.7% |

**Elite University Analysis:**
- **Elite definition:** >50% of students from top 10% of high school class
- **Elite count:** 78 universities out of 777 (**10.0%**)
- **Non-Elite count:** 699 universities

| Group | Avg Out-of-State Tuition | Avg Grad Rate |
|-------|--------------------------|---------------|
| **Elite** | **Significantly higher** | **Higher** |
| Non-Elite | Lower | Lower |

> **Finding:** Elite universities charge significantly higher out-of-state tuition and have higher graduation rates. Private universities also charge considerably more than public ones — actionable insight for college access policy and financial aid strategy.

**Correlation Highlights:**
- `Apps` ↔ `Accept`: Strong positive (r ≈ 0.94) — high-application schools accept more students in absolute terms
- `Top10perc` ↔ `Outstate`: Moderate positive — selective schools charge more
- `Grad.Rate` outlier: One university reported **118%** graduation rate — data quality flag requiring investigation

---

### Exercise 9 — Auto Dataset (392 Vehicles)

**Quantitative Feature Ranges:**

| Feature | Min | Max | Mean |
|---------|-----|-----|------|
| mpg | 9.0 | 46.6 | 23.4 |
| cylinders | 3 | 8 | 5.47 |
| displacement | 68 | 455 | 194 |
| horsepower | 46 | 230 | 104 |
| weight | 1,613 | 5,140 | 2,978 |
| acceleration | 8.0 | 24.8 | 15.5 |
| year | 70 | 82 | 75.9 |

**Top Predictors of Fuel Efficiency (MPG):**

| Feature | Correlation with MPG | Direction |
|---------|---------------------|-----------|
| **Weight** | **Strongest negative** | Heavier → lower MPG |
| **Horsepower** | Strong negative | More power → lower MPG |
| **Displacement** | Strong negative | Larger engine → lower MPG |
| Cylinders | Strong negative | More cylinders → lower MPG |
| Year | Positive | Newer cars → higher MPG |
| Acceleration | Weak positive | — |

> **Key Finding:** Weight, horsepower, and displacement are the **three strongest predictors** of fuel inefficiency — these three features alone form the basis of a strong predictive model. Newer model years show significantly better MPG, confirming systematic efficiency improvements in automotive manufacturing over time.

**Subset Analysis (removing cylinders 3 & 5):**
- Range after subset: mpg [10.4, 46.6], cylinders [4, 8]
- Removing low-frequency cylinder counts reduces noise in subsequent modeling

---

### Exercise 10 — Boston Housing Dataset (506 Suburbs)

**Crime Rate Analysis:**

| Variable | Correlation with Crime | Interpretation |
|----------|----------------------|----------------|
| **rad** (highway access) | **Strongest positive** | Urban density → higher crime |
| tax | Strong positive | High tax areas → higher crime |
| lstat (lower status %) | Positive | Poverty → higher crime |
| medv (home value) | Negative | Wealthy areas → lower crime |
| dis (job distance) | Negative | Suburban areas → lower crime |

**High Crime Suburbs (above median):**

| Metric | High-Crime Suburbs | All Suburbs |
|--------|-------------------|-------------|
| Crime rate range | Up to **88.97** per capita | 0.006 – 88.97 |
| Tax rates | Higher | Mixed |
| Pupil-teacher ratio | Higher | Mixed |

**Charles River Suburbs:**
- **35 suburbs** border the Charles River (`chas = 1`)
- These suburbs have distinct property characteristics vs non-river suburbs

**High Room Count Analysis (rm > 7 or rm > 8):**

| Category | Count | Avg Crime | Avg Home Value |
|----------|-------|-----------|----------------|
| rm > 7 | 64 suburbs | Lower | Higher |
| **rm > 8** | **13 suburbs** | **Lowest** | **Highest** |

> **Key Finding:** The 13 suburbs with >8 rooms per dwelling have the **lowest crime rates and highest home values** — confirming a clear socioeconomic divide in Boston neighborhoods. Suburb 398 stands out with the lowest median home values, highest crime, and maximum building age — a priority candidate for urban renewal analysis.

---

## 💡 Business Insights

1. **Higher Education Strategy:** Elite universities (top 10% high school representation >50%) command premium tuition and deliver better graduation outcomes. A binary Elite flag is a strong feature for any college ranking or financial aid prediction model.

2. **Automotive Engineering:** Weight is the single strongest negative predictor of fuel efficiency — stronger than horsepower or displacement. This guides lightweight materials investment decisions and regulatory compliance modeling for automotive manufacturers.

3. **Urban Crime Policy:** Highway accessibility (`rad`) shows the strongest positive correlation with crime — suggesting that transit infrastructure investment without complementary social programs may inadvertently increase crime exposure. This finding is directly relevant to urban planning and public safety resource allocation.

4. **Real Estate Valuation:** The 13 Boston suburbs with >8 rooms per dwelling show both lowest crime and highest home values — confirming that dwelling size is a reliable proxy for neighborhood quality in hedonic pricing models.

5. **Data Quality Matters First:** The 118% graduation rate outlier in the College dataset would corrupt any downstream model if unchecked. EDA before modeling is not optional — it is the foundational step that determines model validity.

---

## 🗂️ File Structure

```
Chapter_2_Applied_Exercise_Solution/
│
├── Chapter_2.ipynb          ← Main analysis notebook (all exercises)
├── chapter_2.html           ← Rendered HTML version (easy browser viewing)
├── chapter_2.qmd            ← Quarto source file
├── College.csv              ← College dataset (Exercise 8)
└── README.md                ← This file
```

---

## ▶️ How to Run

```bash
# Install dependencies
pip install ISLP pandas numpy matplotlib jupyter

# Launch notebook
jupyter notebook Chapter_2.ipynb
```

---

## 📚 Reference

James, G., Witten, D., Hastie, T., Tibshirani, R., & Taylor, J. (2023).
*An Introduction to Statistical Learning with Applications in Python.* Springer.
Chapter 2: Statistical Learning — Applied Exercises 8–11.

---

## 🙏 Acknowledgements

Special thanks to **Karim Aboussel Ham** whose repository
[ISLP-applied-solutions](https://github.com/KarimABOUSSELHAM/ISLP-applied-solutions)
provided useful guidance and reference during the completion of this project.

---

## 👤 About the Author

**Shad Ali Shah**
🎓 MPhil Economics Student — School of Economics, Quaid-i-Azam University, Islamabad
💡 Passionate about the intersection of **Economics**, **Data Science**, and **Machine Learning**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/shad-ali-shah-6439ab339/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/shadalishah)

---

*Part of the [ML Portfolio](../README.md) by Shad Ali Shah*
