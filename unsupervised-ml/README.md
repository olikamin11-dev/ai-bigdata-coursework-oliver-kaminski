# Unsupervised Machine Learning – Order Segmentation (Delivery Hero - PedidosYa )

## Problem
The objective of this project is to identify **different types of purchase orders**
using **unsupervised learning techniques**, in order to detect **business
development opportunities** for supermarkets managed through **PedidosYa**.

By grouping orders based on behavioral, contextual, and transactional features,
the project aims to uncover latent patterns that can support decision-making
in areas such as promotions, user targeting, and operational optimization.

This project was developed as the final assignment for the
**Unsupervised Machine Learning** course of the MSc in Big Data & Artificial Intelligence.

---

## Dataset
The analysis is based on **real-world, anonymized tabular data** from
PedidosYa, describing purchase orders and user behavior.

### Feature groups
- **Order characteristics:** quantity of items, total cost, product categories
- **Context:** time, location, seasonality, special events
- **User characteristics:** demographics, socioeconomic level, digital adoption
- **Purchase drivers:** promotions and store reputation

Due to confidentiality constraints, the dataset is not included in this repository.

---

## Methodology
- Data preprocessing and feature engineering
- Feature scaling and normalization
- Clustering using **K-Means** and **K-Medoids**
- Model selection using internal metrics
- Dimensionality reduction for visualization
- Qualitative interpretation of clusters

---

## Model Evaluation
Models were evaluated using **internal clustering metrics**:

- **Inertia**
- **Silhouette score**

The following figure shows the evaluation of different numbers of clusters:

![Silhouette and inertia](assets/silhouette_inertia.png)

---

## Cluster Visualization
Dimensionality reduction techniques were used to visualize cluster separation:

![Cluster visualization](assets/clustering_visualization.png)

These projections confirm meaningful separation between different order types.

---

## Cluster Interpretation and Results

### Cluster Profiles
The following figure summarizes the main characteristics of each cluster:

![Cluster profiles](assets/cluster_profiles.png)

### Identified Order Types
- **Cluster 0 – Replenishment orders:** small, low-cost, frequent purchases
- **Cluster 1 – Large purchases:** high-volume, high-cost grocery orders
- **Cluster 2 – Habitual orders:** regular orders from highly active users

---

## Business Insights
The identified order archetypes can support:
- Targeted promotions
- User segmentation strategies
- Inventory and delivery optimization
- Identification of high-value and high-frequency users

---

## How to Run
1. Install dependencies:
   pip install -r requirements.txt
   
2. Open and run:
    notebooks/unsupervised_ml_final.ipynb

-----

## Notes

This project demonstrates:

- Application of unsupervised learning to real-world business data
- Use of internal metrics for model evaluation
- Interpretation of clusters beyond purely mathematical criteria
- Translation of data-driven insights into business-relevant concepts


