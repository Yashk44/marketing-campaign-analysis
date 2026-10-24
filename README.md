# Marketing Campaign Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/Type-Unsupervised%20Learning-brown)


<img width="1286" height="644" alt="aui" src="https://github.com/user-attachments/assets/ed0ae1d5-bdcf-44a6-8e64-27c785ff934c" />



**Customer segmentation using clustering (K-Means elbow + Agglomerative Clustering + PCA) to build targeted marketing strategies.**

---

## Overview

Sending the same offer to every customer wastes marketing money. This project groups **2,212 customers** into **4 clusters** based on who they are (age, income, family) and how they spend, then recommends a different marketing strategy for each group.

| Key numbers | |
|---|---|
| Customers analysed | 2,212 (from 2,240 raw records) |
| Features used for clustering | 23 |
| PCA components | 3 |
| Customer clusters | 4 |

---

## Project Workflow

1. Load the data and handle missing values
2. Convert dates and engineer new features (Age, Spent, Children, Family_Size, Is_Parent, Customer_For)
3. Detect and remove outliers (Age above 90, Income above 600,000)
4. Encode categorical columns and scale features (StandardScaler)
5. Reduce dimensions with PCA (23 features to 3 components)
6. Choose the number of clusters with the elbow method (k = 4)
7. Form the clusters with Agglomerative Clustering
8. Profile each cluster and recommend marketing actions

---

## Customer Clusters

| Cluster | Who they are | Spending | Strategy |
|---|---|---|---|
| 0 | Older parents, mostly with a teenager | Medium to high | Family value packs, multi-buy offers |
| 1 | Younger parents, usually one young child | Lowest | Child-focused products, app coupons, social media |
| 2 | No children, high income, all ages | Highest | Premium and specialty products, quality over discounts |
| 3 | Older parents with teenagers, larger families, lower income | Low | Bulk discounts, private-label products, loyalty rewards |

**Key insight:** the biggest spenders are high-income customers without children. Parents, especially those with teenagers, spend less and look for deals.

---

## Tech Stack

- **Python** (Jupyter Notebook)
- **pandas, NumPy** for data handling
- **Matplotlib, Seaborn** for visualisation
- **scikit-learn** for encoding, scaling, PCA and clustering
- **Yellowbrick** for the elbow plot

---

## Repository Structure

```
Marketing-Campaign-Analysis/
├── marketing_campaign_analysis.ipynb      # Full code and outputs
├── marketing_campaign.csv                 # Dataset (tab-separated)
├── Marketing_Campaign_Analysis_Project-Report.pdf   # Detailed project report
└── README.md
```

---

## How to Run

```bash
pip install numpy pandas matplotlib seaborn scikit-learn yellowbrick
jupyter notebook marketing_campaign_analysis.ipynb
```

> The dataset is tab-separated, so it is loaded with `pd.read_csv(..., sep="\t")`.

---

## Full Report

See [`Marketing_Campaign_Analysis_Project-Report.pdf`](Marketing_Campaign_Analysis_Project-Report.pdf) for the complete methodology, graphs, cluster profiles and business recommendations.
