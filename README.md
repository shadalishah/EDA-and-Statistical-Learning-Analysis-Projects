# Data Exploration & Statistical Analysis in Python
### Chapter 2 Applied Exercises — *An Introduction to Statistical Learning (ISLR2)*

[![Author](https://img.shields.io/badge/Author-Shad%20Ali%20Shah-blue)](https://github.com/shadalishah)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin)](https://www.linkedin.com/in/shad-ali-shah-6439ab339/)
[![Language](https://img.shields.io/badge/Language-Python-3776AB?logo=python)](https://www.python.org/)
[![Topic](https://img.shields.io/badge/Topic-Statistical%20Learning-green)]()

---

## 🔍 What This Project Is About

This project demonstrates **hands-on data analysis skills** applied to three real-world datasets. Using Python, I explore, clean, visualize, and draw insights from data — skills that are directly relevant to roles in **data analysis, business intelligence, and economic research**.

The work is based on Chapter 2 of a leading academic textbook used in universities worldwide: *An Introduction to Statistical Learning with Applications in Python* by James, Witten, Hastie, and Tibshirani.

> **In simple terms:** I took raw datasets, asked meaningful questions about them, and used Python to find and communicate the answers — just like a data analyst would do on the job.

---

## 💼 Skills Demonstrated

| Skill | What I Did |
|---|---|
| **Data Cleaning** | Handled missing values, fixed column indexing, removed inconsistencies |
| **Exploratory Data Analysis (EDA)** | Summarized datasets using statistics and identified patterns |
| **Data Visualization** | Created scatter plots, boxplots, histograms, and correlation matrices |
| **Feature Engineering** | Created new variables (e.g., categorizing universities as "Elite" or not) |
| **Statistical Thinking** | Interpreted relationships between variables and drew evidence-based conclusions |
| **Python & Libraries** | `pandas`, `numpy`, `matplotlib`, `ISLP` |

---

## 📂 Datasets Analyzed

### 🎓 1. College Dataset — *Which universities stand out?*
Analyzed data from **777 US universities** covering tuition, enrollment, faculty qualifications, and graduation rates.

**Key findings:**
- Universities where more than 50% of students came from the top 10% of their high school class were classified as "Elite" — and they charge significantly higher out-of-state tuition.
- Private universities charge considerably more than public ones on average.
- Application volume, acceptance numbers, and enrollment are strongly correlated, which has implications for admissions strategy.

---

### 🚗 2. Auto Dataset — *What drives fuel efficiency?*
Examined a dataset of **automobiles** to understand what factors predict gas mileage (MPG).

**Key findings:**
- Vehicle weight, horsepower, and engine displacement are the strongest predictors of fuel efficiency.
- Heavier and more powerful cars consistently show lower MPG — a clear, actionable insight for automotive or environmental policy analysis.
- These three variables alone could form the basis of a strong predictive model for MPG.

---

### 🏙️ 3. Boston Housing Dataset — *What shapes crime and housing values?*
Explored data on **506 Boston-area suburbs** to understand crime, housing values, and neighborhood characteristics.

**Key findings:**
- High accessibility to radial highways (a proxy for urban density) is strongly associated with higher crime rates.
- The 13 suburbs with the most rooms per dwelling have **lower crime rates** and **higher home values** — suggesting a clear socioeconomic divide.
- 35 suburbs border the Charles River, and these tend to have distinct property characteristics.
- One suburb (no. 398) stands out with the lowest median home values, highest crime, and maximum age of buildings — a candidate for urban renewal priority.

---

## 📁 Repository Structure

```
📦 ISLR2-Chapter2-StatisticalLearning/
│
├── 📓 Chapter_2.ipynb     # Full Python notebook with code + explanations
├── 🌐 chapter_2.html      # Web-viewable version of the notebook
├── 📄 chapter_2.qmd       # Source file (Quarto format)
├── 📊 College.csv         # Dataset used in Exercise 8
└── 📋 README.md           # This file
```

---

## ▶️ How to Run This Project

**Step 1 — Install Python dependencies:**
```bash
pip install numpy pandas matplotlib islp jupyter
```

**Step 2 — Clone the repository:**
```bash
git clone https://github.com/shadalishah/ISLR2-Chapter2-StatisticalLearning.git
cd ISLR2-Chapter2-StatisticalLearning
```

**Step 3 — Open the notebook:**
```bash
jupyter notebook Chapter_2.ipynb
```

---

## 🙏 Acknowledgements

Special thanks to **[Karim Aboussel Ham](https://github.com/KarimABOUSSELHAM)** whose repository [ISLP-applied-solutions](https://github.com/KarimABOUSSELHAM/ISLP-applied-solutions) provided helpful code examples and guidance during the completion of these exercises.

---

## 👤 About the Author

**Shad Ali Shah**
MPhil Economics Student — School of Economics, Quaid-i-Azam University, Islamabad
Passionate about the intersection of **Economics, Data Science, and Machine Learning**

🔗 [LinkedIn](https://www.linkedin.com/in/shad-ali-shah-6439ab339/) &nbsp;|&nbsp; 🐙 [GitHub](https://github.com/shadalishah)

---

## 📚 Reference

> James, G., Witten, D., Hastie, T., Tibshirani, R., & Taylor, J. (2023).
> *An Introduction to Statistical Learning with Applications in Python*. Springer.
> [https://www.statlearning.com](https://www.statlearning.com)

---

*This project is for academic and portfolio purposes.*
