# Online Retail Customer Segmentation — RFM Analysis

## Overview
Segmented customers of a UK online retailer using RFM Analysis and K-Means Clustering on 1M+ raw transactions. RFM features were engineered from scratch — no pre-built feature columns were used.

## Dataset
[UCI Online Retail II — Kaggle](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci) — ~1M transactions from a UK retailer (2009–2011)

## What I Did
- Cleaned raw data — removed cancellations, negative quantities, and missing CustomerIDs
- Engineered RFM features (Recency, Frequency, Monetary) from scratch
- Applied log transformation to fix skewed distributions
- Scaled features using StandardScaler before clustering
- Used Elbow Method + Silhouette Score to find optimal K=4
- Applied K-Means Clustering and visualized segments with PCA (95.1% variance explained)
- Validated results using Hierarchical Clustering (dendrogram confirmed K=4)

## Results — 4 Customer Segments

| Segment | Recency | Frequency | Monetary | Count |
|---|---|---|---|---|
| 🏆 Champions | 27 days | 19 orders | £11,007 | 1,189 |
| 🌱 Loyal Customers | 28 days | 3 orders | £867 | 1,251 |
| ⚠️ At Risk | 228 days | 5 orders | £2,000 | 1,465 |
| 💀 Lost | 396 days | 1 order | £325 | 1,976 |

## Conclusion
K-Means with K=4 produced well-separated, business-meaningful customer segments confirmed by a 95.1% PCA variance explained score and Hierarchical Clustering. Champions should be rewarded, At Risk customers targeted with win-back campaigns, and Lost customers deprioritized.

## Tools Used
`pandas` `numpy` `scikit-learn` `matplotlib` `seaborn` `scipy`