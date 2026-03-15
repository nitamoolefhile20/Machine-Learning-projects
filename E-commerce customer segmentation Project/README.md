# 🛒 Shopping Center Customer Segmentation
 
Unsupervised machine learning project to segment customers of an online grocery store using K-Means clustering. Built on the [Ulabox Orders Dataset](https://www.kaggle.com/datasets/ulabox/ulabox-orders-with-categories-partials-2017/data) from Kaggle.
 
---
 
## 📌 Problem Statement
 
Understanding customer behavior is critical for any retail business. This project segments customers into distinct groups based on their purchasing patterns, discount usage and product preferences which enables targeted marketing and personalized retention strategies.
 
---
 
## 📂 Dataset
 
- **Source:** [Kaggle - Ulabox Orders with Categories 2017](https://www.kaggle.com/datasets/ulabox/ulabox-orders-with-categories-partials-2017/data)
- The dataset constituted of 30,000 orders from 10,000 customers, with 14 features.
- **Features:** Numeric - spending across product categories, discount usage, order frequency and more
- **Challenge:** Duplicate Customer IDs required aggregation before modeling
 
---
 
## 🛠️ Methodology
 
1. **Data Cleaning**: Ensured data quality by making sure that the dataset does not have any missing values, structural errors, duplicates and any other inconsistencies.
2. **Exploratory Data Analysis (EDA)**: bar plots and pie charts to understand spending distribution, discount usage and category preferences
3. **Feature Engineering**: aggregated duplicate Customer IDs to get one row per customer (total items, mean discount, category spending etc.)
4. **Preprocessing**: applied Quantile Transformer and Standard Scaler on the numeric dataset
5. **Optimal Clusters**: determined number of clusters using Elbow Method and Silhouette Scores
6. **Clustering**: applied K-Means clustering with 4 clusters
7. **Dimensionality Reduction**: used PCA and t-SNE to visualize clusters 
8. **Cluster Profiling**: analyzed each cluster by grouped means to extract business insights
 
---
 
## 📊 Results
 
### Cluster Profiles
 
| Cluster | Avg Total Items | Avg Discount | Profile |
|---------|----------------|--------------|---------|
| 0 | 14.4 | 7.4 | Low-engagement bargain buyers |
| 1 | 196.9 | 6.5 | High-value premium customers |
| 2 | 38.8 | 19.2 | Price-sensitive moderate shoppers |
| 3 | 155.0 | 7.2 | High-frequency reliable customers |
 
### Cluster Visualisation
![Customer Segments](Distribution of Categories.png)
 
---
 
## 🔍 Key Insights
 
- **Cluster 0 # Bargain Buyers:** Low engagement customers who shop infrequently and primarily seek discounts. Minimal spending across all categories.
 
- **Cluster 1 # Premium Customers:** The most valuable segment. Highest item purchases, invest heavily in food, fresh items, beverages and beauty products. Rarely rely on discounts and willingly pay full price.
 
- **Cluster 2 # Discount Shoppers:** Price-sensitive moderate shoppers who take advantage of significant discounts and shop within a limited category selection.
 
- **Cluster 3 # Loyal Regulars:** High-frequency shoppers with diverse category interests. Do not heavily rely on discounts yet consistently purchase in significant quantities. Customers in this cluster typically shop on **Tuesdays, between 12:00–15:00**.
 
---
 
## 🗂️ Project Structure
 
```
├── ulabox_orders.csv
├── customer_segmentation.ipynb
├── customer_segments.png
└── README.md
```
 
---
 
## ▶️ How to Run
 
1. Clone the repository
2. Install dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```
3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/ulabox/ulabox-orders-with-categories-partials-2017/data) and place it in the root folder
4. Run `customer_segmentation.ipynb` end to end
 
---
 
## 👤 Author
 
**Nitamo Olefhile** 
[Kaggle Profile](https://www.kaggle.com/nitamoolefhile)
 
---
