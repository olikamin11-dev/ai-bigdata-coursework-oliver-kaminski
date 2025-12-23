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
**Order characteristics**
- Order ID
- Number of items
- Total purchase cost
- Product category
- Product ID

**Context**
- Day, date, time
- Season
- Special event
- Home vs. work
- Neighborhood / zone
- Population density

**User characteristics**
- User ID
- Address
- Address type
- Age
- Gender
- Payment methods
- Socioeconomic level (NSE)
- Digital adoption

**Purchase drivers**
- Promotion applied
- Store reputation

the dataset is included in this repository.

---

## Methodology
The project follows an unsupervised learning workflow:

- Data preprocessing and feature engineering
- Feature scaling and normalization
- Application of clustering algorithms:
  - **K-Means**
  - **K-Medoids**
- Model selection using internal validation metrics
- Dimensionality reduction for visualization
- Qualitative interpretation of resulting clusters

---

## Model Evaluation
Since no ground truth labels are available, models were evaluated using
**internal clustering metrics**:

- **Inertia**
- **Silhouette score**

Additionally, dimensionality reduction techniques were used to visualize
cluster separation:
- PCA
- t-SNE
- UMAP

---

## Cluster Interpretation and Results

### Cluster 0 – Replenishment Orders
**Description:** Small, low-cost orders.

**Key characteristics**
- Moderate number of items
- Low total amount
- Moderate user order frequency
- Low quantities of dairy, beverages, and meat products

**Interpretation**
These orders likely represent **replenishment purchases**, where users place
small and frequent orders to restock essential products.

---

### Cluster 1 – Large Purchase Orders
**Description:** Large and high-value orders.

**Key characteristics**
- High number of items
- High total amount
- High quantities of dairy, beverages, and meat products

**Interpretation**
These orders are consistent with **large grocery purchases**, such as weekly
or bi-weekly shopping, covering a wide range of products.

---

### Cluster 2 – Frequent Habitual Orders
**Description:** Orders placed by highly frequent users.

**Key characteristics**
- Moderate number of items
- Moderate total amount
- Very high order frequency per user

**Interpretation**
This cluster represents **habitual purchasing behavior**, where users place
regular orders with moderate size and value.

---

### Summary of Clusters
| Cluster | Order Type | Description |
|-------|-----------|-------------|
| 0 | Replenishment | Small, frequent restocking orders |
| 1 | Large purchase | High-volume, high-cost grocery orders |
| 2 | Habitual | Regular orders from highly active users |

---

## Business Insights
The clustering results reveal **distinct order archetypes** that can support:
- Personalized promotions
- User segmentation strategies
- Optimization of delivery and inventory planning
- Identification of high-value and high-frequency user segments

---

## How to Run
1. Install dependencies:
   pip install -r requirements.txt
   
2. Open and run:
    notebooks/unsupervised_ml_final.ipynb

## Notes

This project demonstrates:

- Application of unsupervised learning to real-world business data
- Use of internal metrics for model evaluation
- Interpretation of clusters beyond purely mathematical criteria
- Translation of data-driven insights into business-relevant concepts


