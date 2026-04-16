# 📊 Week 1 – Salary Distribution Analysis

## DeepTech_Ready Upskilling Program (3MTT)

This repository documents my progress and  hands-on practice for **Week 1** of the **Advanced Data Analysis and Visualization** track under the **3MTT DeepTech Ready Upskilling Program**.

---

## Overview
This project demonstrates foundational yet powerful data analysis techniques applied to a small dataset to extract meaningful insights. Despite the dataset being minimal, the analysis clearly shows how statistical and visualization methods can uncover patterns and anomalies when correctly applied.

---

## Problem Statement

A dataset representing employee salaries was provided:

```
1000, 500, 800, 700, 700, 800, 700, 900, 750, 850
```

## Objectives:

* Understand salary distribution patterns
* Identify data variability and spread
* Calculate and interpret a **box plot**
* Visualize distributions using box plots
* Compute and analyze **Z-scores**
* Identify **outliers** using statistical methods

---

## Step 1: Data Preparation

Sorted dataset:

```
500, 700, 700, 700, 750, 800, 800, 850, 900, 1000
```

---

## Step 2: Box Plot Analysis

### Key Metrics:

* **Minimum:** 500
* **Q1 (25th percentile):** 700
* **Median (Q2):** 775
* **Q3 (75th percentile):** 850
* **Maximum:** 1000

### Interquartile Range (IQR):

```
IQR = Q3 - Q1 = 850 - 700 = 150
```

### Outlier Boundaries:

* Lower Bound = 475
* Upper Bound = 1075

---

### Box Plot Interpretation

* The **middle 50%** of salaries fall between **700 and 850**
* The **median (775)** indicates a fairly balanced distribution
* Slight **right skew** due to higher maximum value (1000)
* Salary distribution is **consistent with moderate variation**

---

### Box Plot Visualization

```
plt.boxplot(salary)
plt.title('Salary Distribution Box Plot')
plt.show()
```
<img width="614" height="437" alt="Screenshot 2026-04-16 102049" src="https://github.com/user-attachments/assets/a2687f5b-5a2b-4ec2-8c17-81b256979f9b" />


## Step 3: Z-Score Analysis

Using:

[
z = \frac{x - \mu}{\sigma}
]

Where:

* Mean (μ) = 770
* Standard Deviation (σ) ≈ 128.84

---

### Z-Score Table

| Salary (x) | Z-Score | Interpretation                            |
| ---------- | ------- | ----------------------------------------- |
| 1000       | 1.79    | 1.79 standard deviations above the mean   |
| 900        | 1.01    | About 1 standard deviation above the mean |
| 800        | 0.23    | Very close to the average salary          |
| 750        | -0.16   | Slightly below the average                |
| 700        | -0.54   | Moderately below the average              |
| 500        | -2.10   | 2.10 standard deviations below the mean   |

---

### Z-Score Interpretation

* Most values fall within **-1 to +1**, showing low variability
* The lowest value (500) is the most extreme but still within range
* No value exceeds **±3 standard deviations**

**👉 Rule of thumb:**

- Values beyond ±3 are considered extreme
- since dataset stays within ±2.1, this implies that it's well-behaved

---

## Step 4: Outlier Detection

### Using IQR Method:

* Acceptable range: **475 to 1075**
* All values fall within this range

### Using Z-Score Rule:

* Threshold: **|z| > 3**
* No values exceed this threshold

---

## Final Conclusion

* 🚫 No outliers detected
* 📊 Salary distribution is well-structured
* 📉 Variation is moderate and controlled
* 🧠 Indicates a consistent and fair compensation system

This project reinforces an important data analytics principle:

> Even small datasets can reveal strong insights when properly analyzed.

It also demonstrates how combining statistical methods with visualization leads to better interpretation and decision-making. 

---

## Key Learnings

* Box plots provide a quick summary of data distribution
* Z-scores quantify how far values deviate from the mean
* Combining IQR and Z-score improves outlier detection
* Even simple datasets can reveal meaningful insights

---

## Tools & Concepts Applied

* Descriptive Statistics
* Box Plot (IQR Method)
* Z-Score Analysis
* Outlier Detection
* Python (NumPy, Matplotlib)

---

## Acknowledgment

This practice work is part of my learning journey in the **3MTT DeepTech Ready Upskilling Program**, supported by:

* 3MTT Nigeria
* Data Science Nigeria (DSN)
* Google
