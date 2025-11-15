# Anomaly Detection Project — Combined README

This README file covers both uploaded notebooks:

* **Anaomaly_detection1.ipynb**
* **Anomaly_detection_2.ipynb**

It provides a unified, clean, pre-formatted documentation structure suitable for GitHub or project submission.

---

## 📌 Project Title

**Anomaly Detection — Statistical & Distance-Based Approaches**

---

## 📘 Overview

This project explores multiple anomaly-detection techniques across two Jupyter notebooks. It covers:

* Exploratory data analysis (EDA)
* Statistical anomaly-detection methods
* Robust iterative outlier removal strategies
* Distance-based anomaly scoring (k-NN)
* Visual analysis of flagged anomalies

Notebook 1 focuses on **introductory analysis + basic techniques**, while Notebook 2 expands into **advanced or iterative methods**.

---

## 🗂 Files Included

### **1. Anaomaly_detection1.ipynb**

Focuses on:

* Data exploration
* Preprocessing steps
* Simple statistical anomaly detection

  * z-score method
  * IQR method (1.5×IQR)
* Basic visualization

### **2. Anomaly_detection_2.ipynb**

Focuses on:

* Iterative 3-sigma outlier detection
* Robust thresholding
* k-Nearest Neighbors (k-NN) anomaly scoring
* Percentile-based cutoffs
* Detailed visualization & comparison across methods

### Optional folders you can add:

```
/ data           → datasets
/ results        → generated outputs
/ images         → stored plots
```

---

## 🔧 Environment & Dependencies

Install using pip:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

Recommended Python version: **3.8+**

---

## 📂 Notebook Structure

### **Notebook 1 — Anaomaly_detection1.ipynb**

1. Data loading
2. Cleaning & preprocessing
3. Exploratory analysis
4. Statistical anomaly detection:

   * Mean/Std (z-score)
   * IQR rule
5. Basic visualizations

---

### **Notebook 2 — Anomaly_detection_2.ipynb**

1. Refined preprocessing
2. **Iterative 3-sigma implementation**
3. **k-NN anomaly score** using scikit-learn
4. Threshold selection (99th percentile, etc.)
5. Outlier comparison table
6. Exporting flagged anomalies

---

## 📊 Implemented Methods Summary

| Method            | Description                                           | Notebook |
| ----------------- | ----------------------------------------------------- | -------- |
| Z-score           | Uses mean & std to flag extreme values                | 1        |
| IQR Rule          | Detects values outside Q1−1.5×IQR or Q3+1.5×IQR       | 1 & 2    |
| Iterative 3-sigma | Recomputes stats after removing extreme points        | 2        |
| k-NN Score        | Uses avg distance to k neighbors to measure isolation | 2        |

---

## ▶️ How to Run

Open the notebooks using Jupyter:

```bash
jupyter lab
```

Run cells from top to bottom. Editable parameters include:

* `n_sigma`
* `max_iters`
* `k` for k-NN
* percentile thresholds (e.g., 95, 99, 99.5)

---

## 📈 Visualization

Both notebooks include:

* Boxplots
* Histograms
* Scatter plots with highlighted anomalies
* Score distributions

You can export them using:

```python
plt.savefig("results/plot_name.png", dpi=300)
```

---

## ✔️ Reproducibility Checklist

* [ ] Set fixed random seeds
* [ ] Document dataset source
* [ ] Store hyperparameters
* [ ] Export anomalies as CSV
* [ ] Keep separate logs for each notebook

---

## 📌 Notes

* Use robust statistical measures when dataset contains many outliers.
* Combine multiple methods for more confidence.
* Iterative sigma rules help reduce influence of extreme outliers.

---
