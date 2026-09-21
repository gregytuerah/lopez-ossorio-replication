# Lopez-Ossorio Replication

# Replication of López-Osorio et al. (IPV Risk Assessment)

This repository contains the R-based replication and analysis of López-Ossorio et al.'s study on predictors of repeat intimate partner violence (IPV). The goal is to re-analyze the original risk assessment indicators using multiple hypothesis testing procedures, visualize statistical significance, and evaluate robustness to correction techniques like Bonferroni and Benjamini–Hochberg (FDR).

---

## 🔗 Original Study Reference

You can find the original paper here:  
📄 [López-Ossorio et al. (2017), ScienceDirect](https://www.sciencedirect.com/science/article/pii/S1697260017300017#tbl0005)

The dataset (`lopez_osrio.xls`) has been **pre-cleaned** and combines **all 65 parental predictors** from the five main risk assessment tables, making it easier to analyze in a single unified format.

---

## 📁 Repository Structure
```
.
├── data/                       # Cleaned .xls dataset  
│   └── lopez_osrio.xls
├── scripts/                   # R Markdown analysis file
│   └── lopez-osorio-analysis.Rmd
├── README.md
```
---

## 📊 What This Project Does

This project walks through seven key analytical questions:

1. **Reads and formats** the original López-Osorio dataset (n = 65 predictors).
2. **Displays the cleaned dataset** using LaTeX-style tables.
3. **Computes raw p-values** based on reported chi-square statistics.
4. **Visualizes** the p-value distribution compared to a uniform null.
5. **Applies Bonferroni correction**, identifying predictors that remain significant under strict family-wise error control.
6. **Applies Benjamini–Hochberg (BH) FDR procedure**, estimating the number of expected false discoveries and generating the threshold plot.
7. **Compares** decision rules across the three approaches (single test, Bonferroni, BH), and identifies the most and least significant predictors accordingly.

---

## 📦 Key R Packages Used

- `readxl`, `dplyr`, `ggplot2` — data loading and visualization  
- `knitr`, `kableExtra` — nicely formatted output tables  
- `p.adjust()` — for multiple-testing correction  

---

## 📄 Output

If you knit the `.Rmd` file, it will generate a PDF report that includes:

- Cleaned and unified predictor table
- Histogram of raw p-values vs uniform
- Bonferroni and BH-adjusted significance results
- FDR curve and false discovery estimate
- Final classification table showing predictors flagged by each method

---

## ✅ Summary of Findings

The most robust predictors of repeat IPV offenses are not isolated violent events or demographic features, but rather the **underlying behavioral and attitudinal patterns of aggressors**—such as controlling behavior, prior criminal history, and substance abuse. These predictors remain significant even after adjusting for multiple hypothesis testing.

In contrast, many marginal predictors flagged by the raw p-values lose significance under Bonferroni or BH-FDR adjustments, underscoring the importance of controlling for false discoveries when building risk assessment tools.

---

## 🧠 Author

**Gregy Gustavo Tuerah**  
MPP student, University of Chicago   
